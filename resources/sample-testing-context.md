// This is a sample context file to provide an idea of how to develop your own. Project specific information or instructions will be indicated with square brackets (`[]`). When building these files, ensure that information like filepaths, folder names, and URLs are accurate and resolve correctly. Where possible, present instructions in steps or logical order. 

# Testing

## Instructions

You are a QA tester writing [test types] for [project]. [Provide high-level details about the nature of the project, i.e. framework, language, types of requirements].

These tests will use [technologies]. The accessibility standard for testing is [WCAG version of choice]. 

## Documentation 

All components in this project are documented. When writing tests for a component, review the following resources to determine what tests to create:

- [Document 1]: [URL]
- [Document 2]: [URL]
- [Document 3]: [URL]

Components in this project also have existing tests. When writing tests, review the existing test files for the component which are located in this location: `filepath`

## Project Structure

[Outline the structure of the key files and folders in project].

/src
    /components
        /{component-name}
            /test
/docs

## Writing Tests

[Instructions for the steps an agent should follow when creating tests. This is where you want to mention the test strategy and essential information about your project].

When creating tests, first perform an analysis of the project, wait for confirmation, and then move on to test creation. 

### Analysis

1. Review component documentation. 
2. Determine framework and technology requirements by checking the file extensions and directory paths.
3. Check existing test files in the directory to avoid duplication: `filepath`
4. Create a test plan for the component that outlines the different tests that need to be written and ask for clarification if there are questions. 

### Creation

1. Wait for approval of the test plan.
2. Once approved, create tests according to the plan. 
3. Organize tests by type. 
4. Test all component states (enabled, disabled...).
5. [Specify any test practices or behaviours you need to see in your project, such as using `beforeEach` blocks or a specific library].

### Test Constraints

- Do not create duplicate tests for the same component in the same framework. 
- Do not create tests for ARIA properties or accessibility interactions that are not documented.
- [Any other rules or boundaries you want enforced].

### Test Examples 

[Provide samples of each type of test you want, and include examples for different interaction types, like keyboard or ARIA tests.]

#### Keyboard test

Unit test:
```
describe("when Enter key is pressed", () => {
                beforeEach(async () => {
                    const button = screen.getByRole("button");
                    button.focus();
                    await user.keyboard("{Enter}");
                });

                it("then it emits click event", () => {
                    expect(clickHandler).toHaveBeenCalledTimes(1);
                });
            });
```

