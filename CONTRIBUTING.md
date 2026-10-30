# Contributing guidelines

Thank you for considering contributing to Glip Glops! As the creators and maintainers of this project, we want to ensure that the project lives and continues to grow. Not blocked by any singular person's computer time. One of the simplest ways of doing this is by encouraging a larger set of shallow contributors. Through this, we hope to mitigate the problems of a project that needs updates, but there is no-one who has the power to do so.

### Development Process

We adhere to a [trunk-based development](https://trunkbaseddevelopment.com/) approach, maintaining a single protected branch:

- **`main`**: This is our primary branch where all development occurs, including new themes, colour fixes, and updates. It's vital that `main` remains stable and always ready to install.

Contributors are encouraged to create a new branch for each set of related changes. These branches are merged back into `main` through a pull request once they're ready. When it comes to commit messages, We follow the [conventional commits](https://www.conventionalcommits.org/) specification, and while not mandatory, using [gitmoji](https://gitmoji.dev/) for commit types is encouraged.

By contributing to this project, you agree to abide by [its terms](CODE_OF_CONDUCT.md).

### Making changes

There's no build step or toolchain: every theme is a plain file in [`themes/`](themes), one folder per app. A few rules keep them consistent:

- **The palette comes first.** All colours come from the Glip Glops palette ([`assets/colors.csv`](assets/colors.csv), pictured in [`assets/palette.png`](assets/palette.png)). If a change needs a colour that isn't there, propose it as a palette change rather than adding a one-off hex value to a single theme.
- **Keep the variants in sync.** Every theme ships as **Glip Glops** (dark) and **Glip Glops Light**. A change to one usually needs the same change in the other.
- **Keep the apps in sync.** The same role should look the same everywhere: keywords, strings, comments, the terminal colours and so on. If you change how a role is coloured in one app, update the others too.
- **Keep the Xcode sizes in sync.** The regular, Presentation and Presentation Large Xcode themes differ only in font size.
- **Show it.** Include before and after screenshots in your pull request, ideally of both variants.

To try your changes:

| App | How to test |
| --- | --- |
| **Xcode** | Copy the files into `~/Library/Developer/Xcode/UserData/FontAndColorThemes/` and restart Xcode. |
| **Terminal** | Double-click the `.terminal` profile. |
| **VS Code** | Open [`themes/VSCode/glip-glops`](themes/VSCode/glip-glops) in VS Code and press `F5`. |
| **Ghostty** | Point `theme` at the file's absolute path, run `ghostty +validate-config`, then reload with `⌘⇧,`. |
| **Zed** | Run `zed: install dev extension` and pick [`themes/Zed`](themes/Zed). |

Adding support for a new app is very welcome, and it should follow the same palette and role mapping as the existing themes.

### Release Process

Our release process is manual, ensuring each version aligns with our high standards for stability and completeness. Discussions about when to cut a release and what it should include are encouraged among all participants.

Releases are prepared on branches named `release/x.y.z`—reflecting [Semantic Versioning (SemVer)](https://semver.org). Rigorous testing and community feedback are sought to finalize each release. Once the version is stable, and every theme is verified in its app, the release is tagged (`x.y.z`) and published to appropriate distribution channels.

### Ownership

If you get a merged Pull Request, regardless of content (typos, colours, doc fixes), then you are eligible for push access to this repository.

Offhand, it is easy to imagine that this would make quality suffer, but in reality it offers fresh perspectives to the project and encourages ownership from people who are depending on it. If you use these themes every day, then you probably have the eye to improve them and offer valuable feedback.

Everyone comes in with their own perspective on what a project could/should look like, and encouraging discussion can help expose good ideas sooner.

#### Why do we give out push access?

It can be overwhelming to be offered the chance to wipe the source code for a project. Do not worry, we do not let you push to `main`. All changes are peer-reviewed, and we have the convention that someone other than the submitter should merge non-trivial pull requests.

As a contributor, you can merge other people's pull requests, or other contributors can merge yours. You will not be assigned a pull request, but you are welcome to jump in and take a review on topics that interest you.

This project is not continuously deployed, there is space for debate after review too. Offering everyone the chance to revert, or make an amending pull request. If it feels right, merge.

#### How can we help you get comfortable contributing?

It is normal for a first pull request to be a potential fix for a problem, and moving on from there to helping the project's direction can be difficult. We try to help contributors cross that barrier by offering [good first step issues](https://github.com/afonsograca/Glip-Glops/labels/good%20first%20issue). These issues can be fixed without feeling like you are stepping on toes. Ideally, these are non-critical issues that are well-defined. They will be purposely avoided by mature contributors to the project, to make space for others.

We aim to keep all project discussion inside GitHub issues. This is to make sure valuable discussion is accessible via search. If you have questions about how to use the themes, or how the project is running - GitHub issues are the go-to tool for this project.

#### Our expectations on you as a contributor

To quote [@alloy](https://github.com/alloy) from [this issue](https://github.com/Moya/Moya/issues/135):

> Do not ever feel bad for not contributing to open source.

We want contributors to provide ideas, keep the ship shipping and to take some of the load from others. It is non-mandatory; we’re here to get things done in an enjoyable way. :trophy:

The fact that you will have push access will allow you to:

- Avoid having to fork the project if you want to submit other pull requests as you will be able to create branches directly on the project.
- Help triage issues and merge pull requests.
- Pick up the project if other maintainers move their focus elsewhere.

It is up to you to use those superpowers or not though :wink:

If someone submits a pull request that is not perfect, and you are reviewing, it is better to think about the PR's motivation rather than the specific implementation. A colour that's slightly off should not be a blocker. Though we do want every theme to stay in sync across apps and variants, we will work with you to figure that out together.

### What about if you have problems that cannot be discussed in a public issue?

[Afonso](https://github.com/afonsograca) has contacts on their GitHub profile, and are happy to talk about any problems.

### Where can I get more info about this document?

The original source of this document can be found at https://github.com/moya/contributors.

### [M&M's (ABSOLUTELY NO BROWN ONES)](https://en.wikipedia.org/wiki/Van_Halen#Contract_riders)
If you made it all the way to the end, bravo, you are awesome. You can include the :skateboard: emoji in the top of your ticket to signal to us that you did in fact read this file and are trying to conform to it as best as possible: `:skateboard:`.
