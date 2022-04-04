# Soft Delete
## Installation
```python
pip install django-generic-delete==1.1
```

## Configuration

```python
INSTALLED_APPS = [
  ....
'softdelete',
]
```


### in urls
```python
urlpatterns = [
    ....
    path('delete/', include('softdelete.urls', namespace='softdelete'))
]
```


## Usage

### In models
* Extend 
```python

# import this
from softdelete.models import SoftDeletionModel


class YourModel(SoftDeletionModel):
    # your fields
    pass

```

## Override templates

* in your ``templates``

add the following directory

```
templates/
    softdelete/
      delete.configuration.html
```