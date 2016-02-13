# README #
This repository is provided to work on the product features and tasks listed below.
It is mostly based in [the example proposed for MVC5 in the ASP.NET page](http://www.asp.net/mvc/tutorials/getting-started-with-ef-using-mvc/creating-an-entity-framework-data-model-for-an-asp-net-mvc-application). The app manages a database of students, courses to apply to and the corresponding enrollments.
 
Agile terminology is used throuought this document.

## Product Backlog Item ##
*Page Survey*: a survey will be offered to the students to fulfill when creating a new Student. 

### Tasks ###

* *\#1*: Adapt Model for Students survey
>Each student will fill a survey, with 20 questions and answers.
>Questions are always the same for all the students, but each student will be able to edit his answers.
>Answers will be always strings, edited in Text Areas.
 
* *\#2*: Modify View Student>Edit accordingly to new Model
>Model created in Task 1

* *\#3*: Set Pagination in View Student>Edit
>Similar to the pagination in View Students>Index (use the pagination system explained in [this ASP.NET page](http://www.asp.net/mvc/tutorials/getting-started-with-ef-using-mvc/sorting-filtering-and-paging-with-the-entity-framework-in-an-asp-net-mvc-application)).
>Number of pages: 6. The first page will show all fields not corresponding to the survey (see Task #1). The resting 5 pages will show the fields corresponding to the >survey, split in groups of 4, to complete 20.

* *\#4*: Convert Students Edit Page in Students Index Page
>When clicking Students option in the Nav Menu, we want the current Edit View instead of the Index (we may use the current Create View when no Student is selected).
>Previous Index will be renamed to List and it will be accesible from a link in the new Index page.

* *\#5*: Add List Group in the left
>We will place a List Group on the left which will work exactly the same as the Paginator: same number of items as pages.
>Use [Bootstrap List Group with Linked Items](http://getbootstrap.com/components/#list-group).

* *\#6*: Choose type of Answer
>Now we will introduce a new type of answer, for the Students survey.
>So far, answers always were strings. From now on we want to be able to select which of the answers will be numeric and which will be text. As before, once selected, all answer types will be the same for all the Students.
>For this, we will insert in the Nav Menu a new option "Select Answers", where we may choose the type of answer for all answers in the Model. As a result, when showing the Index page, the edit options for each answer will depende on this selection.