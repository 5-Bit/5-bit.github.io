---
layout: post
title: "Classes Needed"
permalink: "/classesNeeded.html"
---

Class names should start with capital letters and use CamelCase. Fields and instance methods should follow the same convention. All fields (unless otherwise specified) should have a public getter and a private setter. All classes should be declared as public, and should be added to the Eagleslist namespace.

For example, a new class called MyClass that inherits from MySuperClass, and has one field called MyField, could be declared as follows.

~~~{c#}
namespace Eagleslist
{
    public class MyClass : MySuperClass
    {
        public string MyField { get; private set; }
    }
}
~~~

If an explicit superclass is not required, simply omit the ": MySuperClass" component of the declaration, and the class will have the default superclass "Object."


##### Classes Needed With Fields

- Book
    - BookID (int)
    - ISBN10 (string)
    - ISBN13 (string)
    - Title (string)
    - ImageURL (string)
    - Description (string)
- BookCreationResponse
    - Error (string)
    - BookID (int)
- Course
    - CourseID (int)
    - CRN (string)
    - Books (List<Book>)
    - Professor (string)
    - StartTime (int)
    - EndTime (int)
    - Dates (List<string>)
- CourseCreationResponse
    - Error (string)
    - CourseID (int)
- Flag
    - Raiser (User)
    - PostID (int)
    - Content (string)
    - Type (FlagType)
- FlagHandlerRequest
    - Marking (FlagResolution)
    - Message (string)
    - PostID (int)  
- FlagRaisedResponse
    - Error (string)
    - Message (string)


----------------------------------

##### Enum Example:

~~~{c#}
namespace Eagleslist
{
    public enum Test : int
    {
        Case1 = 1,
        Case2 = 2,
        Case3 = 4
    }
}
~~~

##### Enums Needed With Enumerators

- FlagResolution (int)
    - Helpful = 1
    - Declined = 2
    - AgedAway = 4
    - Other = 8
- FlagType (int)
    - Spam = 1
    - Inappropriate = 2
    - Other = 4
