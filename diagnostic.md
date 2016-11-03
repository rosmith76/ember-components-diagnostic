# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components. Explain why each piece might be it's own component.

    ```md
    You can have mulitple lists in an app. Each list will be made up of multiple items.
    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
    ember g component my-map
    ```

1.  What files are created and/or edited to produce a component, and what are their responsibilities?

    ```md
    A component has a component.js and template.hbs file.
    The component.js has properties of the component and the actions associated with that component.
    The template.hbs file has the the handlebars code associated with that items view state.
    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` route. What is
    the syntax (code that is written) to render this component inside that template?

    ```html
    <h3 class="list-header" {{action 'toggleListDetail'}}>{{list.title}}</h3>
      <ul>
        {{#each list.contacts as |my-contact|}}
        {{contacts/my-contact my-contact=my-contact toggleDone='toggleItemDone'}}
        {{/each}}
      </ul>
    ```

1.  Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    ```html
    <span class="list-contact" {{action 'toggleDone'}}>{{my-phone.text}}</span>
    ```
