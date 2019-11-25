!!! Warning "This site is very new, and thus does not have a lot of documentation. Contributions are greatly appreciated!"

# Roblox humanoid bugs

This website serves as a central knowledgebase to document known bugs with humanoids and how to work around them. This list is updated often.

## Contributing

If you know of a humanoid bug and it is not documented here on this site, or you see outdated/missing information, please submit a [pull request](https://github.com/RobloxHumanoids/RobloxHumanoids.github.io/pulls). When submitting pull requests for undocumented humanoid bugs, please be sure to have clear and detailed information about the bug, with a solid reproduction. Please make sure to also link any relevant bug report threads from the devforums. When submitting a new bug, make sure to also create new symptoms in the symptoms list as well.

### Bug format

When adding a bug to this list, please use the following format:
```markdown
## Name of bug

Bug description goes here. It should be clear and concise, explaining what causes the bug, symptoms, etc.

** Workarounds **

Describe the various workarounds to the bug here. As with the description of the bug, they should be clear and concise.

??? bug "Reproduction"
    ```lua
    print("Code reproduction goes here.")
    ```

    ** Bug report thead ** : [link to bug report on devforums](https://devforum.roblox.com/Blahblah)

<hr/>
```

### Symptom format

When adding a symptom to the symptoms list, please use the following format:
```markdown
## Name of symptom

Symptom description goes here. It should be clear and concise, explaining the effects of the symptom.

** Possible causes **

Possible causes should be explained here. Any relevant humanoid bugs should be linked to here.

<hr/>
```

### Extra stuff
This site uses [markdown material extensions](https://squidfunk.github.io/mkdocs-material/extensions/admonition/) for extra capabability. For example, you can make use of [admonition](https://squidfunk.github.io/mkdocs-material/extensions/admonition/) blocks when writing documentation, like so:

!!! Warning
    If the humanoid does a barrel roll, then the server will flip upside down.
    In order to avoid this, please avoid making humanoids do a barrel roll.