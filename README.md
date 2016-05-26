# TemplatesChildPages

A module for ProcessWire CMS/CMF. For any page, allows the restricting of templates that may be used for child pages. Requires the [Template ASM Select](https://github.com/Hani79/Processwire_FieldType_Templates) module.

## Usage

Install Template ASM Select and TemplatesChildPages modules. A field "templates_child_pages" is created on install. Add this field to any templates of your choosing - the field is hidden in the Content tab of Page Edit and is instead rendered on the Children tab, for superusers only. Pages with the field can select from existing templates using an ASM Select inputfield, and any child pages added subsequently will be limited to those selected templates. 

Note that any template restrictions added via this module are *in addition to* any "Family" restrictions set for the child and parent templates. In other words, if template Family restrictions prevent a template being selected for a given page you can't override this simply by including the template in the parent's "templates_child_pages" field.

## Reasons for the module's existence 

The module allows you to add child page template restrictions without having to create new or duplicate templates for the parent page. [This forum post](https://processwire.com/talk/topic/13374-allowed-templates-on-a-page-basis/#entry120845) explains the situation well.

Similarly, it makes it possible to use the "Add New" page feature without an unnecessary proliferation of templates. If you specify a single template as restriction for child pages you can add a [Page Add Bookmark](https://processwire.com/blog/posts/processwire-2.6.17-expands-admin-navigation-with-bookmarks/#page-add-bookmarks) for that parent page that allows site editors to easily add a new page using the right template for the location.