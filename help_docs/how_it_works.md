[<img src="https://cdn2.hubspot.net/hubfs/100006/images/super_logo_sb4.png" title="SeleniumBase" height="48">](https://github.com/seleniumbase/SeleniumBase/blob/master/README.md)

<a id="how_seleniumbase_works"></a>
## <img src="https://cdn2.hubspot.net/hubfs/100006/images/super_square_logo_3.png" title="SeleniumBase" height="32"> **How it works:**

At the core, SeleniumBase works by extending [pytest](https://docs.pytest.org/en/latest/) as a direct plugin. SeleniumBase automatically spins up web browsers for tests, and then gives those tests access to the SeleniumBase libraries through the [BaseCase class](https://github.com/seleniumbase/SeleniumBase/blob/master/seleniumbase/fixtures/base_case.py). Tests are also given access to [SeleniumBase command-line arguments](https://github.com/seleniumbase/SeleniumBase/blob/master/seleniumbase/plugins/pytest_plugin.py) and [SeleniumBase methods](https://github.com/seleniumbase/SeleniumBase/blob/master/help_docs/method_summary.md), which provide additional functionality.

(NOTE: pytest uses a feature called test discovery to automatically find and run Python methods that start with "``test_``" from the file that you specified on the command line.)

To use SeleniumBase calls you need the following:
```python
from seleniumbase import BaseCase
```
And then have your test classes inherit BaseCase:
```python
class MyTestClass(BaseCase):
```
(*See the example test, [my_first_test.py](https://github.com/seleniumbase/SeleniumBase/blob/master/examples/my_first_test.py), for reference.*)
