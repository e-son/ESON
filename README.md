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

You can store types. For example, function associated to `#core/datetime`
can transform ISO time format string to proper Date type in the language.
So `#core/datetime "2014-07-24T16:47:47Z"` will be parsed naturally.

Hashtag namespace convention
-------------------------

It is possible to organize hashtags in namespaces using `/` (slash) separator.
This allow you to create whole namespace tree. Implementations should support
this convention.

Built-in tags
-------------

Some of the common tags are built in ESON and every implementation should
support their parsing as well as their serialization from built-in language
structures. These tags are:

### #core/datetime ###

Tag labels a string containing time in one of the following formats:

  * `YYYY-MM-DDTHH:MM:SS[.s*]` is the datetime of any second
    precession without information about timezone.
  * `YYYY-MM-DDTHH:MM:SS[.s*]<TZO>` is the datetime, where `<TZO>`
    is an timezone offset from GMT in one of the forms:
      * `+HH:MM` positive offset
      * `-HH:MM` negative offset
      * `Z` no offset

Examples:

    [
      #core/datetime "2014-07-24T16:47:47",
      #core/datetime "2014-07-24T16:47:47.00001",
      #core/datetime "2014-07-24T16:47:47+08:30",
      #core/datetime "2014-07-24T16:47:47.4242Z",
      #core/datetime "2014-07-24T16:47:47.0-03:00",
    ]

&nbsp;

-------------------------------------------------------------------------------

ESON is really young project. More information will be provided in future.
