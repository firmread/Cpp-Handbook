
A Soso Tour of Modern C++
=========================

Compilable source files explaining common modern C++ techniques. Heavily commented source files explain the techniques and show them in a practical format. Running the programs may show “proof” of their stated behavior.

These programs are not meant to exhaustively document what you can do with C++. Instead, they aim to show a subset of the language that is simple, productive, and--yes--even fun to work with.

Have a read through the source files. Build and run the sample applications. Try changing some pieces to see how it changes the program behavior.

## Building
```bash
$ make all
```

## Running
```bash
$ ./SampleName.sample
```

## The Samples:

The samples are loosely ordered. The sequence laid out below will hopefully make the most sense if you don't know where to start.

- Object Creation: creating C++ objects dynamically and on the stack.
- Namespaces and Aliases: organizing code into modules and writing readable names.
- Templates: creating functions that can operate on many types.
- Functional: creating function objects (lambdas).
- Collections: sequential and key-based containers, with "CRUD" operations on their contents.
- Async and Future: load and parse a file asynchronously and read the results back in the main thread.

### Early Samples
- Resource (Memory) Management: smart pointer types and managing resources (e.g. memory) with objects. Object Creation is probably a better sample for these concepts.

### Forthcoming? Samples:
- Threads and atomics (for continuously-running objects that process tasks without returning a value)

## Code Style

This being a Sosolimited project, we follow the company code conventions throughout. We use 2-space tabs, so you might need to adjust your editor settings for everything to line up nicely.

## Further Reading

The techniques shown here are largely influenced by Scott Meyer’s [Effective Cpp](http://www.aristeia.com/books.html) books as well as Herb Sutter’s [Guru of the Week](http://herbsutter.com/gotw/) column. Additionally, Bjarne Stroustrup’s recent [A Tour of C++](http://www.stroustrup.com/Tour.html) was influential in setting the tone of the samples. If you are interested in learning more in breadth and/or depth, have a look at those sources.

If you want to learn more, start here:
- [A Tour of C++](http://www.stroustrup.com/Tour.html)
- [Guru of the Week](http://herbsutter.com/gotw/)
- [Effective Modern C++](http://shop.oreilly.com/product/0636920033707.do)

If you just want function references, see:
- [MSDN C++ Reference](http://msdn.microsoft.com/en-us/library/3bstk3k5.aspx)
- [MSDN C++ Standard Library Reference](http://msdn.microsoft.com/en-us/library/cscc687y.aspx)
- [cplusplus.com](http://www.cplusplus.com/reference/)
- [cppreference.com](http://en.cppreference.com/w/)

## C++ Versions and Compatibility

This is only tested with clang on OSX. All code should work in VS2013, as well.

We tell the compiler to use C++14 so we can use std::make_unique, which (like many C++14 features) really just completes and adds consistency to things in C++11. Other than that, everything should compile fine with just C++11 (and much will with C++98).

Currently, C++14 is called C++1y by the command-line version of Clang on OSX. In Xcode, you can set your "C++ Language Dialect" to C++14. In your build settings, it will look like the following:
![C++ Language Dialect Screenshot](https://cloud.githubusercontent.com/assets/81553/5036817/f7f51060-6b50-11e4-8f81-9f41fbabc23c.png)
