# Structural Notes

## Framework Class Simplicity

Framework classes are restricted to a single reference. It reduces the need for possible property overrides, selector specificity, and class redunancy in markup.

Examples:

- b-media\_left vs. b-media b-media-a b-media_left
- b-media_left vs. b-media b-media-left
- b-media_left vs. b-media s-left

OOCSS - ".media .imgExt{float:right; /\*margin-left: 10px;*/}" | Two classes needed where one consolidated class could be used through placeholder selectors and constructors. Value of 20 specificity.

## Generate Code Only When Needed

The framework, imported without modification or premade theme, will only generate base browser styles (located in /base/). Each Block does not generate any styles until instanced on the project level, per case basis.

## Project Blueprint

The idea of implementing project level styles through instanced Blocks builds a logical, consistent system of structuring for your front-end styles on one or more projects. Every style is encapsulated within its single responsibility, therefore, styles can be mapped out by section for easy reference and maintainability.

*[SHOW BLUEPRINT EXAMPLE HERE]*

There are no stray styles that are ambigous. Projects with two or more developers will benefit by working from a common foundation.

## Variable Cohesion

There exist three types of variables: theme (color), global box-model, and component variables.Theme and global variables are stored within each core theme file (aspire/theme/theme\_name/\_t-themeName\_vars). These control default values. If needed, the theme variable file can be instanced on the project level (project/_vars-project\_name) and any overrides can be done at that point. Component varialbes are housed within its parent component file; these variables are typically set up with a relation to global variables. Keeping component variables within the component file itself helps increase cohesion.

E.g. - In the old version of Curse Blocks, we placed all variables into one master variable file which became large and cumbersome; each new feature that was added that required variable support bloated the file even farther. Finding and referencing variables became tedious due to the need of having to check two or more different files.

## Naming Conventions

Block components utilize dashes, camel case, and underscores. Each of the previous three elements have specific meaning behind their uses; following the established naming convention is essential to keep the framework organized.

**Example Block name: b-box_inverse**

Breakdown:

**"b-"** - Scope of the element; Defines that this particular element is a Block. Scope descriptions are always a single letter followed by a dash (-). Prefixing the scope of the element prevents conflicts with other class names or 3rd party plugins.

**"box"** - Identifies what type of element it is, in this example this Block (b-) is a box Block. Identifiers always follow the scole of the element, and if two or more words are used to identify the Block, camel case is used:

**"\_inverse"** - Variation of element; this example is the inverse (_inverse) variation of the box (box) Block (b-). Variations are always preceded by an underscore (_), no other element uses the underscore. Variations are optional and may not be present. If two or more words are used to describe the variation, use camel case in the same manner as the identifier.

Variables utilize the same naming conventions as the Block components except dashes: camel case and underscores.

**Example variable name: $boxModel_margin**

Breakdown:

**"$boxModel"** - Description of the variable, typically describes the component it is used within. Camel case is used if two or more words are needed to describe the variable. "$" is unique to Sass and identifies the element as a variable.

**"\_margin"** - Property identifier; typically matches up with a standard CSS property.