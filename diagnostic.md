# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components.

    ```md
    Any UI elements that are nested are a good answer. Siblings do not count.

    For example: There is a visual hierarchy in the navbar in many applications.
    The navbar represents a block and buttons or links within that block are
    elements of the navigation structure. Another example might be a sidebar for
    a blog, which is a visual block containing navigation elements or even
    comments.
    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
    ember generate component my-map
    ```

1.  What files are edited to produce a component, and what are their
    responsibilities?

    ```md
    Template files (`template.hbs`) are responsible for containing markup
    (defining structure), binding data, and binding and dispatching actions.

    Components objects (`component.js`) are responsible for defining actions,
    declaring HTML attributes, and other presentation or behavior.

    In general, templates are responsible for markup, while components are
    responsible for presentation and behavior.
    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` path. What is
    the syntax for loading this component inside that template?

    ```html
    {{#each model as |contact|}}
    {{my-contact contact=contact}} <!-- most important part of response -->
    {{/each}}
    ```

    Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    ```html
    <!-- iteration necessary in response -->
    {{#each contact.phones as |phone|}} <!-- correct object property access -->
    {{my-phone phone=phone}} <!-- sub-component included, binding necessary -->
    {{/each}}
    ```
