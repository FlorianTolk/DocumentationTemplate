# DocumentationTemplate
A small repository that can be used as a template for good public use documentation

##Example Project
This folder is a sample of a project currently under development 

## Orginal Drop
This folder contains a template for a properly documented initial repository README templates.
This README template can also be used for all non-SCE updates to a repository.

## Version Drop
This folder contains a template for a properly documented version update README templates.

#Pull Requests
## Update Documentation
Every time a new update needs to be pushed to the ADL GitHub, the vendor will push to their branch initially, including all below information.
After pushing to their branch, the vendor is to generate a pull request that must be approved by ADL. 
### New version number in the push title
Version format is #.#.#
Version updating #.#.X is minor, non-breaking changes
Version updating #.X.# is major, potentially breaking changes
Version updating X.#.# is a new SCM that ADL will draft as a new release
### Detailed Summary
What Software Trouble Reports (STR) or GitHub Issues are being addressed
What additional functionality are being made
What services are being changed (if multiple services are being used, GitHub automatically tracks what files are being changed)

# Coding Best Practices
## Code Documentation
The first line(s) of each file should be a comment clearly stating the purpose of the file
Each function should include a comment clearly stating its purpose within the file
License headers and copywrite statements must be included (where applicable)
Variable, operation, and arguments names should be intuitive, if not they must include comments that explain their purpose
Use Camel Case when naming variables
Use white spaces consistently
Use overloaded functions conservatively
