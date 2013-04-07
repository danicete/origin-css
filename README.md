# Origin CSS

Origin's primary objective is not to be another component library—there are many great options already available—but instead it is a holistic framework that serves as the structural foundation for your CSS. It aims to keep the CSS portion of a front-end framework as abstracted and decoupled as possible for easier management and greater scalability.

1. [Overview](#overview)
2. [Installation](#installation)
3. [Getting Started](#getting-started)
4. [Digging Deeper](#digging-deeper)
5. [Demos](#demos)

## 1. <a name="overview"></a>Overview

### Project Structuring

Origin tackles the task of defining how the structure of the project should be setup to handle the growing needs of CSS management in complex projects. Out of the box, Origin has the following structure:

    /origin-css
        --/assets
            --/css
            --/images
        --/helpers
        --/layouts
        --/partials
    /themes
        --/origin-css
    /vendors

**/origin-css -** The core files of the framework reside here; no code is generated at this level until invoked by a project.

- /assets - Core level images and custom CSS
- /helpers - Utility elements such as mixins
- /layouts - Styles for views and templates
- /partials - Styles for the component library

### Minimal Code Output

Origin outputs code only when you specifically extend an element from the core codebase. This method ensures the only code being outputted is intentional, being utilized, and at the bare minimum so file size is low and speed is optimal. There is greater control and informed reasoning about where—and more importantly why—your code is being generated.

### Meaningful Division Within Naming Conventions

Origin using a naming convention that utilize dashes, camel case, and underscores. Each of the previous three elements have specific meaning behind their uses; following the established naming convention is essential to keep the framework organized, human readable, and non-conflictual.

*Example - p-box_inverse*

**"p-"** - Scope of the element; Defines that this particular element is a partial. Scope descriptions are always a single letter followed by a dash (-). Prefixing the scope of the element prevents conflicts with other class names or 3rd party plugins.

**"box"** - Identifies what type of element it is, in this example this partial (p-) is a box partial. Identifiers always follow the scope of the element, and if two or more words are used to identify the element, camel case is used:

**"\_inverse"** - Variation of element; this example is the inverse (_inverse) variation of the box (box) partial (p-). Variations are always preceded by an underscore (_), no other element uses the underscore. Variations are optional and may not be present. If two or more words are used to describe the variation, use camel case in the same manner as the identifier.

### Simplified HTML Class & CSS Relationship

*In progress...*

### Easily Extendable with Clear Dependencies

*Up next...*

## 2. <a name="installation"></a>Installation

*In queue...*

## 3. <a name="getting-started"></a>Getting Started

*In queue...*

## 4. <a name="digging-deeper"></a>Digging Deeper

*In queue...*

## 5. <a name="demos"></a>Demos

*In queue...*