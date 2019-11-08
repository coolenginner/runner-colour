# colour-runner

Colour formatting for `unittest` test output.

## Installation

    pip install colour-runner

### Django

Mix the `ColourRunnerMixin` into your `unittest` test runner (eg: in `project/runner.py`):

    from django.test.runner import DiscoverRunner  # Django 1.6's default
    from colour_runner.django_runner import ColourRunnerMixin

    class MyTestRunner(ColourRunnerMixin, DiscoverRunner):
        pass

Point django at it in `settings.py`:

    TEST_RUNNER = 'project.runner.MyTestRunner'

### Other Python

Where you would normally use:

* `unittest.TextTestRunner`, use `colour_runner.runner.ColourTextTestRunner`.
* `unittest.TextTestResult`, use `colour_runner.result.ColourTextTestResult`.
