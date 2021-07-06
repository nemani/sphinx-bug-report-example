
### Example Repo to showcase bug in sphinx autodoc

While working on some related project we noticed that autodoc does not generate valid xml output
when we use params in docstrings. This repo serves as an example for the same.

Steps to reproduce:
1. Install sphinx
2. cd docs
3. make xml
4. `xmllint --noout docs/build/xml/index.xml`


xmllint errors:
```
docs/build/xml/index.xml:19: namespace error : Namespace prefix py for class on literal_strong is not defined
ph><literal_strong py:class="True" py:module="myproject.main" refspecific="True"
                                                                               ^
docs/build/xml/index.xml:19: namespace error : Namespace prefix py for module on literal_strong is not defined
ph><literal_strong py:class="True" py:module="myproject.main" refspecific="True"
                                                                               ^
docs/build/xml/index.xml:22: namespace error : Namespace prefix py for class on literal_strong is not defined
ph><literal_strong py:class="True" py:module="myproject.main" refspecific="True"
                                                                               ^
docs/build/xml/index.xml:22: namespace error : Namespace prefix py for module on literal_strong is not defined
ph><literal_strong py:class="True" py:module="myproject.main" refspecific="True"
                                                                               ^
docs/build/xml/index.xml:25: namespace error : Namespace prefix py for class on literal_strong is not defined
ph><literal_strong py:class="True" py:module="myproject.main" refspecific="True"
                                                                               ^
docs/build/xml/index.xml:25: namespace error : Namespace prefix py for module on literal_strong is not defined
ph><literal_strong py:class="True" py:module="myproject.main" refspecific="True"
                                                                               ^
```
