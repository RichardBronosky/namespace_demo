# namespace_demo
a simple Python namespace demonstration

## WARNING: this is not currently functioning.

More to come.

-----

## Structure

    mbp:namespace_demo bruno$ find * -ls
    4733807        8 -rw-r--r--    1 bruno            staff                1082 Mar 11 15:53 LICENSE
    4733940        8 -rw-r--r--    1 bruno            staff                 969 Mar 11 15:57 README.md
    4732064        0 drwxr-xr-x    5 bruno            staff                 170 Mar 11 15:50 namespace_demo
    4733477        8 -rw-r--r--    1 bruno            staff                  57 Mar 11 15:49 namespace_demo/__init__.py
    4718105        0 drwxr-xr-x    5 bruno            staff                 170 Mar 11 15:50 namespace_demo/example_namespace
    4727985        8 -rw-r--r--    1 bruno            staff                  57 Mar 11 15:17 namespace_demo/example_namespace/__init__.py
    4718106        0 drwxr-xr-x    4 bruno            staff                 136 Mar 11 15:49 namespace_demo/example_namespace/module1
    4733479        8 -rw-r--r--    1 bruno            staff                  57 Mar 11 15:49 namespace_demo/example_namespace/module1/__init__.py
    4730512        8 -rw-r--r--    1 bruno            staff                  61 Mar 11 15:21 namespace_demo/example_namespace/module1/tools.py
    4733499        8 lrwxr-xr-x    1 bruno            staff                  11 Mar 11 15:50 namespace_demo/example_namespace/setup.py -> ../setup.py
    4733497        8 lrwxr-xr-x    1 bruno            staff                  11 Mar 11 15:50 namespace_demo/setup.py -> ../setup.py
    4732327        8 -rw-r--r--    1 bruno            staff                1821 Mar 11 15:33 setup.py

## Errors!

I've tried copying the setup.py to multiple depths and running `python setup.py egg_info` from each but keep getting the same error.

    mbp:namespace_demo bruno$ python setup.py egg_info
    error in namespace_demo setup command: Distribution contains no modules or packages for namespace package 'example_namespace'

    mbp:namespace_demo bruno$ cd namespace_demo/
    mbp:namespace_demo bruno$ ln -s ../setup.py
    mbp:namespace_demo bruno$ python setup.py egg_info
    error in namespace_demo setup command: Distribution contains no modules or packages for namespace package 'example_namespace'

    mbp:namespace_demo bruno$ cd example_namespace/
    mbp:example_namespace bruno$ ln -s ../setup.py
    mbp:example_namespace bruno$ python setup.py egg_info
    error in namespace_demo setup command: Distribution contains no modules or packages for namespace package 'example_namespace'
