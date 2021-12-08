# ![] Application Resource Bundle (ARB)

---

##### Fork notes:

In order to be able to build the arb_extractor I had to modify the gradle file `arb_extractor/build.gradle` because half of it is deprecated by now. I googled myself through the error messages until it finally worked.

The compiled `arb_extractor-0.1.jar` file sits in `arb_extractor/build/libs` and seems to actually work!

To build it I did the following:

```sh
brew install gradle
gradle compileJava
gradle test
gradle jar
```

I also left all temp files and other artefacts in here because who knows, right?

---

##### Original README:

Application Resource Bundle (abbr. ARB) is a localization resource format that is simple
(based on JSON), extensible (vocabulary can be added without affecting existing tools and
usage), and directly usable (applications can access the resource directly from this format
without converting to another form).

In ARB, localizable resources are encoded as a JSON object. Each resource will have a
resource entry identified by resource key, and an optional resource attribute entry with
resource attribute key.

## lib

This is the ARB supporting library in Javascript. ARB is not restricted to any specific
platform/languager. Issues in web application has been addressed carefully, as this is
where localization practice lacked behind.

## arb_editor

This is actually a sample app for use with our Javascript supporting library.

## arb_extractor

A tool written in Java to automate resource extraction. It uses a generic parser (Antlr),
which allow it to deal with many kinds of languages.

## doc

The specification for ARB design.

## third_party

Thirdparty code used in ARB.
