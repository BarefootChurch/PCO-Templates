## Customizing the reports

Some of the fields in this template are specific to the way we do things, and  will need to be slightly modified to work in your environment.

For example, on lines 119, 120, and 121 in the script document I am pulling 3 specific notes from items in our plan. ("Side Screens", "Center Screen", and "Other") If you don’t use the same note names we do, these line will cause an error. 

Let’s say you want to change the first column to show your “ProPresenter” notes. You would need to make the following changes:

  - Production Script - line 94
    ```html
    <th style="width=15%">ProPresenter</th>
    ```
  - Production Script - line 119 (partial)
    ```liquid
    ...{% if note.category_name == “ProPresenter" %}...
    ```
## Plan versioning

Another feature of these templates is the support for plan versioning.

The template will display `** PLAN IS UNFINALIZED **` by default. To have a version displayed, you will need to add a plan note titled `Information` with your version name in it (We name our versions acording to the [NATO phonetic alphabet](https://en.wikipedia.org/wiki/NATO_phonetic_alphabet), but any name will work)

## Useful links
- [Generating reports in PCO](https://pcoservices.zendesk.com/hc/en-us/articles/204262214-Plan-Reports)
- [Creating custom reports](https://pcoservices.zendesk.com/hc/en-us/articles/204461100-Custom-Reports-Wiki)
- [Adding item and plan notes](https://pcoservices.zendesk.com/hc/en-us/articles/204262134-Notes-in-Plans)
