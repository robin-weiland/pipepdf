# pipepdf

---

## Installation

### PyPI

The package can be directly installed with any package manager that supports PyPI guidelines.

```bash
pip install pipepdf
```

### Github / Build it yourself

```bash
git clone git@github.com:robin-weiland/pipepdf.git

... ToDo
```

## Usage

### CLI / Terminal

ToDo

### Library

You can also use the modules in your own application by importing the modules.

ToDo

> You may also want to take a look into the examples directory for both use cases.

## Known Issues / Caveats

## Versioning

I intend to implement at least two channels, where one will be slightly ahead of the other one. See it as a beta or nightly version, that will at some point be available in the mainline release

## Contribution

> This project uses [*uv*](https://github.com/astral-sh/uv) (and other astral tooling), but you can use any other system as long as it or you update the `pyproject.toml` file appropriatly.

In terms of philosopy, I intended this tool to be as minimally invasive as possible.
This means concretly that (so far) I designed it in a way that does not create any temp wor working files on the system.
I am aware that this closes a lot of opurtunities for possibilites of this tool. 
In theory, I am not entirely opposed to this idea, but I did not come up with a convincing approach to this problem yet.
If you feel like you have an idea that uses temprary or staged files, please feel free to create an issue and/or merge request.

### ToDos

#### Test Suite

This feels like the most important problem, currently.

So far, there is no real testing (or coverage) for this tool. I am not sure how to fully do this yet. Either I ship this with a number of test files. Sources and targets, then apply tests on the sources and compare the result with the targets. Another option could be to create pdfs with something like reportlab, but then I would need to generate the sources and targets as well.

Another challenge, I see would be meaningful messages: How can the tests see that the document should be rotated by 90 degrees to the left but was rotated 180 degrees. This sounds like a lot of manual verification.

#### More modules

Any ideas for useful functionality is welcome. Please see the `modules/base.py` file. You need to create a subclass of this class, you can look into any other module for guidance.
Additionally, you need to register your module in `modules/__init__.py`.

#### Addon system

Currently, the modules are loaded from this projects code base. There might be a need for people to create and possibly publish their own modules without necessarily contributing here. Like with other projects like flask or django, whille their "plugins" are still required to be activated by the programmer, not the user like in this case.
I could imagine it being something like `pip install pipepdf-mymodule`.
But this would be considered low-priority for the time being.
Obviously I am aware of possible security concerns in this case, but in my opponion, this would be a case of your own responsibility.

#### Take a look into the issues

## Changelog
