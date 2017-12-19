Sysl
====

.. image:: https://img.shields.io/travis/anz-bank/sysl/master.svg?label=Linux%20build%20%40%20Travis%20CI
   :target: http://travis-ci.org/anz-bank/sysl

Sysl (pronounced "sizzle") is a system specification language. Using Sysl, you
can specify systems, endpoints, endpoint behaviour, data models and data
transformations. The Sysl compiler automatically generates sequence diagrams,
integrations, and other views and also offers a range of code generation
options, all from a common Sysl spec. The set of outputs is open-ended and will
grow to support other representations in future.

Cross-platform strategy
-----------------------
To make it easy to reuse Sysl across systems, the compiler translates Sysl files
into an intermediate representation expressed as protocol buffer messages. Using
the protoc compiler, users can easily consume Sysl models in their programming
language of choice in a typesafe way without having to write a ton of mapping
boilerplate.

Installation
------------
If you are interested in trying out Sysl, you will need to build it yourself from source::

  > python setup.py install
  > python setup.py test

Run from command line:

  > python -m sysl.core  --root demo/petshop textpb -o out/petshop.txt /petshop
  > python -m sysl.reljam  --root demo/petshop model /petshop PetShopModel

Create distribution

  > python setup.py bdist_wheel --universal

Status
------
Sysl is currently targeted at early adopters. It is usable in alpha, but has a
ways to go in terms of usability, especially on the documentation front (as can
be seen above).