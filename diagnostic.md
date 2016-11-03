# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components. Explain why each piece might be it's own component.

    ```md
    A review website. One component could be the restaurant/business page with
    a picture and name. Then under that, specific information and reviews could
    each be their own component. Reviews will always be changing so it would be
    good to separate them so the entire view doesn't need to be updated when
    reviews are added or deleted. Business info might change a bit but not often
    and the name won't change.
    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
    ember generate component my-map
    ```

1.  What files are created and/or edited to produce a component, and what are their responsibilities?

    ```md
    When you generate a component it makes a file with the name you decide in the
    components directory that contains a component.js file and template.hbs file.
    It will also make a integration test for it. You also want to edit include
    the name of the component in the template of one of your page view files.
    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` route. What is
    the syntax (code that is written) to render this component inside that template?

    ```html
    {{my-contact contacts=model}}
    ```

1.  Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    ```html
    {{#each contact.phone-numbers as |phone-number|}}
      {{my-contact/my-phone phone-number=phone-number}}
    {{/each}}
    ```
