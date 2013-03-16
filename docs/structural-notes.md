// * ------------------------------------------------------------
// * Structural Notes
// * ------------------------------------------------------------


// -------------------------------------
// 3/13/13
// -------------------------------------

- VARIABLE COHESION
  
  There exist three types of variables: theme (color), global box-model, and component variables. Theme and global variables are stored within each core theme file (aspire/theme/theme_name/_vars-theme_name). These control default settings. If needed, the theme variable file can be instanced on the project level (project/_vars-project_name) and any overrides can be done at that point. Component varialbes are housed within its parent component file; these variables are typically set up with a relation to global variables.

  E.g. - In the old version of Curse Blocks, we placed all variables into one master variable file which became large and cumbersome; each new feature added that requiree variable support bloated the file even farther. Finding and referencing variables became tedious due to the need of having to check two or more different files.

- NAMING CONVENTION

  Block components utilize dashes, camel case, and underscores. Each of the previous three elements have specific meaning behind their uses; following the established naming convention is essential to keep the framework organized.

  Example Block name: b-box_inverse

  Breakdown:

  "b-" - Scope of the element; Defines that this particular element is a Block. Scope descriptions are always a single letter followed by a dash (-).

  "box" - Identifies what type of element it is, in this example this Block (b-) is a box Block. Identifiers always follow the scole of the element, and if two or more words are used to identify the Block, camel case is used:

  "b-dropDown_left"

  "_left" - Variation of element; this example is the left (_left) variation of the box (box) Block (b-). Variations are always preceded by an underscore (_), no other element uses the underscore. Variations are optional and may not be present. If two or more words are used to describe the variation, use camel case in the same manner as the identifier.

  Variables utilize the same naming conventions as the Block components except dashes: camel case and underscores.

  Example variable name: $boxModel_margin

  Breakdown:

  "$boxModel" - Description of the variable, typically describes the component it is used within. Camel case is used if two or more words are needed to describe the variable. "$" is unique to Sass and identifies the element as a variable.

  "_margin" - Property identifier; typically matches up with a standard CSS property.