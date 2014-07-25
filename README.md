ESON
====

Extensible JSON

What is it?
-----------

ESON is just a JSON with hashtags. You can hashtag any value writing hashtag
before it. Each hashtag has associated function that transforms tagged
value to something new during parsing time. You can chain more hashtags.
More you can read in [formal specification](specification.txt).

What is it good for?
--------------------

You can store types. For example, function associated to `#datetime` can
transform ISO time format string to proper Date type in the language.
So `#datetime "2014-07-24T16:47:47Z"` will be parsed naturally.

Hashtag namespace convention
-------------------------

It is possible to organize hashtags in namespaces using `/` (slash) separator.
This allow you to create whole namespace tree. Implementations should support
this convention.

&nbsp;

-------------------------------------------------------------------------------

ESON is really young project. More information will be provided in future.
