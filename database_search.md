### Notes
- The model has been created with the name Author with the minimum fields ```id, full_name, and email```.
- The model author already has several data samples.
### Steps
- views.py
```
def author_search(request):
    keyword = request.POST.get('keyword')
    author_list = Author.objects.all()
    if keyword:
        author_list = Author.objects.filter(full_name__icontains=keyword)
    return render(request, 'author_search.html', {'author_list' : author_list})
```
- urls.py
```
path('author_search/', author_search, name='author_search'),
```
- templates/author_search.html
```
    <form action="{% url 'sources_author_search' %}" method="get">
        <input type="text" name="keyword" placeholder="Search by name">
        <button type="input">Search</button>
    </form>
```
### with Q object
---
Object Q is the logic of the query operator (OR, AND & NOT).
- Import Q object :
  ```
  from django.db.models import Q
  ```
- Use Q Object :
  ```
  def sources_author_search(request):
    keyword = request.GET.get('keyword')
    author_list = Author.objects.all()
    if keyword:
         author_list = Author.objects.filter(
            Q(full_name__icontains=keyword) | Q(email__icontains=keyword)
        )
    return render(request, 'author_search.html', {'author_list' : author_list})
  ```
