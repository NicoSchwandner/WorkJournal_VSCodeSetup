# DevJournal

You can use the scripts as described below to generate a daily template. There will be appended different reflection templates depending on which day the script runs for.

There are templates for:

- End of the year
- End of the quarter
- End of the month
- End of the week
- Weekday

## Scripts to generate template

### Generate template for today

```bash
bash ./Scripts/generateDay
```

### Generate template for tomorrow

```bash
bash ./Scripts/generateDay --dayOffset 1
```

## Example Journal entry

```markdown
    # June 13, 2024 - Implementing User Authentication

    ## Daily Overview

    - **Tasks Completed:** Implemented login and registration forms using React and TypeScript.
    - **Challenges Faced:** Struggled with handling async validation for username uniqueness.
    - **Solutions and Workarounds:** Used debounce to handle API calls for username validation to improve performance.

    ## Detailed Notes

    ### Code Snippets

    ```typescript
    const validateUsername = debounce(async (username: string) => {
    const response = await fetch(`/api/validate-username?username=${username}`);
    return response.json();
    }, 300);
    ```

    ### Learnings

    Learned about debouncing to improve the performance of API calls during form validation.

    ### References and Resources

    - [React Debounce Hook](https://usehooks.com/useDebounce/)

    ## Reflection

    - **What Went Well:** Successfully implemented and tested the forms; the debounce solution significantly improved performance.
    - **What Could Be Improved:** Need to refactor validation logic to make it more reusable.
    - **Next Steps:** Tomorrow, focus on integrating JWT authentication on the backend.

    ## Miscellaneous

    - **Ideas and Insights:** Consider adding a loading spinner during async validations.
    - **Questions:** How to securely handle JWT storage on the client side?

    ```
    Some overall insight
    ```
```
