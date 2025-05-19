<!-- markdownlint-enable require-heading-annex -->
<style>
body { counter-set: section 4; }
</style>

# Examples for Material for MkDocs {.annex}

## Call-out Blocks {.annex}

### Code blocks with syntax highlighting {.annex}

Code blocks allow a user to define a block of text that is called out to appear as computer code in a specified language. Material for MkDocs includes [an extension](https://squidfunk.github.io/mkdocs-material/setup/extensions/python-markdown-extensions/?h=highligh#highlight) to support a wide range of syntax highlighters (i.e., to colorize keywords) and also allows custom-defined syntax highlighters for user-defined languages. Code blocks start with three tick marks followed by a space and then an indication of the syntax highlter to be used. The block of code is indented with four spaces and the block ends with another three tick mark code.

=== "C++ Example"
    ``` c++
        for(i = 0; i < max; i++) {
            // sample loop code
        }
    ```

=== "C++ Example Code"
    ```
        ``` c++
            for(i = 0; i < max; i++) {
                // sample loop code
            }
        ```
    ```

=== "ASN.1 Example"
    ``` asn1
        SEQUENCE OF {
            item1 INTEGER (0..255),
            item2 OCTET STRING
        }
    ```

=== "ASN.1 Example Code"
    ```
        ``` asn1
            SEQUENCE OF {
                item1 INTEGER (0..255),
                item2 OCTET STRING
            }
        ```
    ```

### Admonitions {.annex}

Material for MkDocs supports creating call-out boxes for notes, examples, questions, information, etc. It calls these boxes "admonitions". They are represented in a similar way to code blocks but start with three exclamation points (!) followed by a space and then the type of admonition.

=== "Note Example"
    !!! note
        Material for MkDocs allows users to define their own admonition types as well.

=== "Code for Note"
    ```
        !!! note
            Material for MkDocs allows users to define their own admonition types as well.
    ```

=== "Warning Example"
    !!! warning
        The type of admonition defines the color and icon used in the banner of the box.

=== "Code for Warning"
    ```
        !!! warning
            The type of admonition defines the color and icon used in the banner of the box.
    ```

### Collapsable {.annex}

Material for MkDocs also allows call-out boxes to be collapsible by using question marks instead of the exclamation points.

=== "Note Example"
    ??? note
        Material for MkDocs allows users to define their own admonition types as well.

=== "Code for Note"
    ```
        ??? note
            Material for MkDocs allows users to define their own admonition types as well.
    ```

=== "Warning Example"
    ??? warning
        The type of admonition defines the color and icon used in the banner of the box.

=== "Code for Warning"
    ```
        ??? warning
            The type of admonition defines the color and icon used in the banner of the box.
    ```

### Content Tabs {.annex}

As shown in these examples, boxes can also have multiple tabs. This is achieved by using three equal signs (=).

!!! example
    === "Tab 1"
        !!! example
            This is an example using tabs.

    === "Tab 2"
        !!! note
            The code tab only shows the first two tabs to avoid recursive code.

    === "Code"
        ```
        === "Tab 1"
            !!! example
                This is an example using tabs.

        === "Tab 2"
            !!! note
                The code tab only shows the first two tabs to avoid recursive code.
        ```

## Annotations {.annex}

If there is a preference to have comments appear by the user clicking and seeing a tooltip, Material for MkDocs also supports annotations

=== "Sample annotation"
    Clicking on this (1) icon will show more text
    { .annotate }

    1. More text

=== "Code for annotation"
    ``` md
        Clicking on this (1) icon will show more text
        { .annotate }

        1. More text
    ```

## Footnotes {.annex}

Footnotes are similar to annotations but place the additional information at the bottom of the page rather than as a tooltip that appears.

=== "Sample footnote"
    Clicking on the superscripts[^1] will jump to the footnote[^2]

    [^1]: Short note on one line
    [^2]:
        Long footnotes must start on the following line and be indented by four 
        spaces. Clicking on the icon at the end of the footnote will cause the 
        display to jump back to the location of the footnote in the text.

=== "Code for annotation"
    ``` md
        Clicking on this[^1] icon will show more text[^2]

        [^1]: Short note on one line
        [^2]:
            Long footnotes must start on the following line and be indented by four 
            spaces. Clicking on the icon at the end of the footnote will cause the 
            display to jump back to the location of the footnote in the text.
    ```

## Abbreviations / Glossary {.annex}

Tooltips can also be used to display term definitions or meanings of abbreviations (abbr). For one-off usage, the file simply includes a line (typically at the end) the indicates the term in square brackets preceded by an asterisk and followed by a colon space and the definition. The line defining the term is not rendered, but the term being defined (e.g., abbr) will be underlined whereever it occurs in the document and hovering over any instance of the term will reveal its definition in a tooltip. By using the auto_append feature, all term definitions can be moved to a separate file and applied to all pages within the project.

*[abbr]: abbreviation

=== "Code for defining abbr"
    ``` md
        *[abbr]: abbreviation
    ```

=== ":octicons-file-code-16: mkdocs.yml"
    ``` yaml
        markdown_extensions:
          - pymdownx.snippets:
              auto_append:
                - includes/abbreviations.md
    ```

## Paragraph attributes {.annex}

The [Attribute Lists](https://python-markdown.github.io/extensions/attr_list/) extension allows to add HTML attributes and CSS classes to [almost every](https://python-markdown.github.io/extensions/attr_list/#limitations) Markdown inline- and block-level element with a special syntax.

For example, this document marks all headings with the .annex class. This applies the annex style from the extra.css file so that the heading is preceded with a section number that starts with a letter.

!!! example
    === "Example heading"
        ### My heading {.annex}

    === "Code for example"
        ```
            ### My heading {.annex}
        ```

## Fields for information from GitHub {.annex}

Users can also obtain information from the GitHub repository per the following examples

!!! example
    === "GitHub information"
        Version {{ release_number }}

        Stars {{ stars }}

        Forks {{ forks }}

        !!! note
            The fields are only populated when rendered on the GitHub account. When rendering on your local 
            machine using a working directory, the field names are displayed in their brackets since the local
            working directory does not contain the GitHub information.

    === "Code for GitHub information"
        ```
            Version {{ release_number }}

            Stars {{ stars }}

            Forks {{ forks }}

            !!! note
                The fields are only populated when rendered on the GitHub account. When rendering on your local 
                machine using a working directory, the field names are displayed in their brackets since the local
                working directory does not contain the GitHub information.
        ```    

## Sortable tables {.annex}

Standard markdown supports tables; Material for MkDocs allows for extending this feature to allow for sortable tables with some edits to the mkdocs.yml file and a javascript.

=== "Sortable table"
    |Group | Title                 |
    |:----:|:----------------------|
    |WG 1  | Architecture          |
    |WG 3  | ITS geographic data   |
    |WG 5  | Fee and toll collection |
    |WG 7  | General fleet management and commercial/freight|
    |WG 8  | Public transport/emergency |
    |WG 9|Integrated transport information, management and control|
    |WG 10|Traveller information systems|
    |WG 14 | Driving automation and active safety systems|
    |WG 16 | Communications |
    |WG 17 | Nomadic Devices in ITS Systems |
    |WG 18 | Cooperative systems |
    |WG 19 | Mobility integration |
    |WG 20 | Big Data and Artificial Intelligence supporting ITS |

=== ":octicons-file-code-16: mkdocs.yml"
    ``` yaml
        extra_javascript:
          - <https://unpkg.com/tablesort@5.3.0/dist/tablesort.min.js>
          - javascripts/tablesort.js
    ```

=== ":octicons-file-code-16: docs/javascripts/tablesort.js"
    ``` js
        document$.subscribe(function() {
          var tables = document.querySelectorAll("article table:not([class])")
          tables.forEach(function(table) {
            new Tablesort(table)
          })
        })
    ```

=== "Sortable table code"
    ```
        |Group | Title                 |
        |:----:|:----------------------|
        |WG 1  | Architecture          |
        |WG 3  | ITS geographic data   |
        |WG 5  | Fee and toll collection |
        |WG 7  | General fleet management and commercial/freight|
        |WG 8  | Public transport/emergency |
        |WG 9|Integrated transport information, management and control|
        |WG 10|Traveller information systems|
        |WG 14 | Driving automation and active safety systems|
        |WG 16 | Communications |
        |WG 17 | Nomadic Devices in ITS Systems |
        |WG 18 | Cooperative systems |
        |WG 19 | Mobility integration |
        |WG 20 | Big Data and Artificial Intelligence supporting ITS |
    ```

## Mermaid diagrams {.annex}

Material for MkDocs supports Mermaid diagrams. Mermaid allows for relatively simple text-based statements to define diagrams that follow well-defined rules, such as UML diagrams, block diagrams, etc.

!!! example
    === "Sequence diagram"
        ```mermaid
        %%{init: { 'sequence': { 'mirrorActors': false } }}%%
        sequenceDiagram
          participant Proposer
          participant Committee
          participant WG as Working Group
          participant Maintainer
          participant Repo as Open-Source Project Repository

          Proposer ->> Committee: Propose project
          Committee ->> WG: Establish WG
          Committee ->> Maintainer: Assign maintainer
          Maintainer ->> Repo: Establish public repository
          Maintainer ->> Repo: Upload initial baseline
          Maintainer ->> WG: Suggest project plan
          WG -->> Maintainer: feedback
          Maintainer ->> Repo: Post project plan
          Maintainer ->> Repo: Create appropriate branches for work
        ```

    === "Sequence diagram code"
        ```
            ```mermaid
            %%{init: { 'sequence': { 'mirrorActors': false } }}%%
            sequenceDiagram
              participant Proposer
              participant Committee
              participant WG as Working Group
              participant Maintainer
              participant Repo as Open-Source Project Repository

              Proposer ->> Committee: Propose project
              Committee ->> WG: Establish WG
              Committee ->> Maintainer: Assign maintainer
              Maintainer ->> Repo: Establish public repository
              Maintainer ->> Repo: Upload initial baseline
              Maintainer ->> WG: Suggest project plan
              WG -->> Maintainer: feedback
              Maintainer ->> Repo: Post project plan
              Maintainer ->> Repo: Create appropriate branches for work
            ```
        ```

## Additional features {.annex}

## Search {.annex}

The search feature adds a search field into the page header. Include by including the following in your mkdocs.yml file.

``` yaml
    plugins:
      - search
```

## Comment System {.annex}

Material for MkDocs allows to easily [add the third-party comment system](https://squidfunk.github.io/mkdocs-material/setup/adding-a-comment-system/?h=comment) of your choice to the footer of any page by using theme extension.

### Version history {.annex}

Material for MkDocs has a powerful [versioning system](https://squidfunk.github.io/mkdocs-material/setup/setting-up-versioning/) that allows a site to maintain a history of all released versions of a document.

### Last edit date for each page {.annex}

The `mkdocs-git-revision-date-localized-plugin` for Material for MkDocs. An example of this appears at the bottom of this page and is enabled by ensuring the git-revision-date-localized feature is listed in the plugins section of your mkdocs.yml file.
