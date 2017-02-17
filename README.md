# What is that?

## New startup

We're organizing a new company and would like you to join us. Therefore
we're asking you to do a technical exercise.

If you prefer to see some information about our new startup prior to solving
technical exercises, no problem ;) I'll explain what the startup does in
a few days.

However, if you can blindly trust me and just do the exercise in the absence
of any information about what it is we're doing, you're welcome to read the
rest of the exercise :)

## Why do I think it is a good idea to ask people to do work without explaining why?

I know I have a few thousand followers on Twitter and other social networks,
many of them know me personally, and others kind of understand where I am
coming from.

My aim for the next few days is to see if there are some motivated engineers
that would like to join us as one of the very first engineers of our
new Silicon Valley startup. Startups are risky, but may be rewarding.
Doing the technical exercise without full information is one of the smallest
risks you can take in your life.

If you aren't convinced now, no problem. There will be another chance later.
With less risk.


# Programming exercise for C/C++ engineers

Ben, I need help!

We're seeking strong C/C++ engineers with strong C/C++ skills who know C and/or C++ and can program by writing C or C++ code.

 * Do the exercise in your spare time. Do not use your current employer's equipment.
 * Leave your code on GitHub, BitBucket, or package it up in a `.tar.gz`.
 * Send a short note to [vlm@lionet.info](mailto:vlm@lionet.info) with a subject "C programmer assignment". Attach your resume, if you have it.
 * I expect your code to be self-contained and buildable on a reasonable recent unix system (such as Ubuntu 12+, CentOS 6+, FreeBSD 6+ or macOS X). If you're building on Windows OK too, just package it up neat in a way that doesn't require firing up Visual Studio.

# Exercise

You're asked to create a helper function that _normalizes_ strings containing
filesystem paths. The file system is assumed to be unix, with slash-separated
components.

This function is going to be somewhat specialized for the webserver, so `domain.com/../foo` is expected to be equivalent to `domain.com/foo`.

Examples of path normalization:

| Path              | Normalized        |
|-------------------|-------------------|
| `../bar`          | `/bar`            |
| `/foo/bar`        | `/foo/bar`        |
| `/foo/bar/../baz` | `/foo/baz`        |
| `/foo/bar/./baz/` | `/foo/bar/baz/`   |
| `/foo/../../baz`  | `/baz`            |

The solution that you are asked to write as part of this exercise should not touch the actual filesystem.
The processing is done purely lexically on a string of bytes.
Assume ASCII character encoding.

The expected interface for the function is

```C
char *normalize(const char *path);  // Allocates memory.
```

or

```C++
std::string normalize(const std::string &path);
```

# Evaluation

How will we assess your code:

 * We require bug-free code
 * We also very much enjoy reasonably fast code
 * Tests should be there

Kudos if you can:
 * Avoid dependencies (such as boost-filesystem)
 * Explain cyclomatic complexity of the solution
 * Quantify the speed of the solution (for example, in Gbps per CPU core)
 * Assess the CPU cache effects

The next steps will likely be for us to chat (in English or Russian) to see if there's a mutual fit.
