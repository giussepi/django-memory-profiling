# django-memory-profiling

Measure memory taken by requested view and response using pympler.muppy

Works with Debug = True or False (If True results can be shown on loggin panel of django debug toolbar)

### INSTALLATION

1. Run
`pip install git+git://github.com/giussepi/django-memory-profiling`

2. On settings.py
  * Add your preffered middleware(s) to MIDDLEWARE_CLASSES
  ```
      'memory_profiling.pympler_middleware.MemoryMiddleware2',
      'memory_profiling.pympler_middleware.MemoryMiddleware1',
  ```
  * Add `memory_profiling` to INSTALLED_APPS
  * Configurate as desired. Example:
  ```
  SHOW_REQUEST_SUMMARY = True
  SHOW_RESPONSE_SUMMARY = True
  SHOW_COMPARED_REQUEST_RESPONSE_SUMMARIES = True
  IGNORE_URLS_CONTAINING = [
      'site_media', 'static', '__debug__', 'undefined', 'pulse'
  ]
  SHOW_ON_DJANGO_DEBUG_TOOLBAR_LOGGIN_PANEL = True
  SHOW_TOP_X_MEMORY_DELTAS = 15
  ```
