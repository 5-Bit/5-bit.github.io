---
layout: post
title: "Coding Standards"
author: "Michael MacCallum"
date: 2015-10-05 19:09:00
excerpt: "This document outlines the coding standards that we will follow while working on Eagleslist. It includes some info on things like, how we will be testing our code, code organization and conventions, code reviews and other policies that we will attempt to follow."
---
This document outlines the coding standards that we will follow while working on {{ site.project.title }}. It includes some info on things like, how we will be testing our code, code organization and conventions, code reviews and other policies that we will attempt to follow.

##### Coding Conventions
In terms of coding conventions, our team will strive to follow existing conventions for things like variable names, indentation and general code formatting. For Go, we will be following the conventions listed in [golang.org][0]'s [Effective Go][1], and for C#, we will be following Microsoft's [C# Coding Conventions][2] programming guide.

##### Code Organization
All files in our project, and methods within classes should be grouped logically by their functionality. This means that we will always attempt to have methods that are related to each other in groups, and related files stored together in folders. We will attempt to follow these rules, even if doing so requires refactoring the project because we believe this will make the project easier to maintain long term.

##### Test Coverage
We will strive to have high test coverage in our entire project, both in the WinForms application, and for our web service. All unit tests should make sure that every method is capable of behaving in an expected way for both correct and incorrect input. Updates to the code base that include fixes for any previously observed bugs should always include at least 1 unit test demonstrating the problematic behavior, and showing that the code no longer malfunctions.

##### Code Reviews
Even though we will all have write access to our collective [GitHub][3] repositories, and could just commit changes to their master branches directly, all changes to the master branches should be made in the form of [pull requests][4]. Doing so will allow other members of the group to review differences in the code before they are merged into the master branch. We believe that working like this will help us catch potential problems with updated code before it causes problems with the project.

##### KISS (Keep it Simple Stupid)
When writing code for our project, all team members will try to write code with readability in mind and try to refrain from "cool tricks" that may sacrifice clarity, even if they produce slight performance gains or less total code.

##### DRY (Don't Repeat Yourself)
Repeated code will not be tolerated. If ever in a situation where the same code is required more than once, our team members will refactor the duplicated code into a method, function or similar so that the code only exists once within the project.

[0]: https://www.golang.org
[1]: https://golang.org/doc/effective_go.html
[2]: https://msdn.microsoft.com/en-us/library/ff926074.aspx
[3]: https://www.github.com
[4]: https://help.github.com/articles/using-pull-requests/
