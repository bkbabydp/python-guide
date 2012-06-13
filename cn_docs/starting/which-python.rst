选择一种解释器
================

使用哪种Python？

2.x vs 3.x
~~~~~~~~~~~~

**tl;dr**: 普遍采用Python 2.x，Python 3.x是将闪亮登场的新事物。

`延伸阅读 <http://wiki.python.org/moin/Python2orPython3>`_

目前
-----

如果你正在选择Python解释器，那么我强烈推荐你使用Python 2.7.x，除非你有足够充分的理由不选择。

未来
-----

随着越来越多的模块移植到Python3，它使用起来将更加方便。

应该如果支持哪种Python？
~~~~~~~~~~~~~~~~~~~~~

如果你正着手开发一个新的Python模块，我推荐你以Python 2.5或Python 2.6为准进行编写，并在以后的迭代中添加Python3支持。

Python语言实现
~~~~~~~~~~~~~~~

目前，基于不同的后端，Python程序设计语言有多种流行的实现。

CPython
--------

`CPython <http://www.python.org>`_ 是使用C语言编写的参考实现。它将Python代码编译成中间字节码，然后由一个虚拟机来解释。当人们谈及 *Python* ，一般不仅指代语言自身，也指代这种实现。CPython提供了最高规格的Python程序包以及C扩展模块兼容性。

如果你正在编写开源Python代码，并且希望得到尽可能广泛的使用，那么使用CPython是你最佳的选择。如果你需要使用任何在功能上依赖于C扩展的程序包(比如：numpy)，那么CPython是你唯一选择。

作为参考实现，Python语言的所有版本都有CPython实现。Python 3则只有CPython实现可供使用。

PyPy
-----

`PyPy <http://pypy.org/>`_ 是使用Python语言静态类型子集RPython实现的Python解释器。这种解释器的特点是即时编译(动态翻译)以及支持多种后端(C, CLI, JVM)。

PyPy的目标是在与CPython参考实现保持最大的兼容的同时提高性能。

如果你正在想法子提交你的Python代码的性能，那么值得尝试一下PyPy。在一套基准测试中，它 `快于CPython 5倍有余 <http://speed.pypy.org/>` 。

目前PyPy支持Python 2.7。[#pypy_ver]_

Jython
-------
