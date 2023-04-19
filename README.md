# Anker Themes
This repository is only for themes.

# How to Use a Theme?
Every theme comes with a JS file and a SCSS file. Although there might be cases
that a `data.json` file is included for reference just to show you how to
structure your data for that specific theme. To use a theme you need those files
in your project's `themes` directory.

### How to Get a Specific Theme?
To get a specific theme navigate to `themes` directory in this Repo. For example
you want one of the Anker default themes, the `anker-theme-basic`. You want to
navigate there and copy the link. The link will look as follows:

```bash
https://github.com/ankerapp/anker-themes/tree/master/themes/anker-theme-basic/
```

Next you want to use SVN to export the whole directory from this repo into your
local themes directory. To use SVN we've to change the URL a little. Replace
`tree/master` with `trunk`. Navigate to `themes` directory and run the following
command.

```bash
svn export https://github.com/ankerapp/anker-themes/trunk/themes/<theme-name>
```

After your themes files are imported run the build command to build the project.
It's a Makefile command. If you don't have it installed you can get it from [here](https://www.gnu.org/software/make/).
On windows you can install with [Chocolatey](https://chocolatey.org/install).

```bash
make build
```

# Contributing to Anker
If you want to contribute to Anker and want to make your own themes and
publish them here then please follow [these](https://github.com/ankerapp/anker-app/blob/master/CONTRIBUTING.md)
guidelines.

# How do I Make a Theme?

To develop a theme for Anker please follow the guidelines below:

1. First thing first fork the [Anker](https://github.com/ankerapp/anker-app) repository

2. Clone the forked repository
    ```bash
    git clone https://github.com/<your-username>/anker-app.git
    ```

3. Navigate to the project directory
    ```bash
    cd anker-app
    ```

4. Create a new branch kindly give your branch a more descriptive name like
    `theme-add-<your-theme-name>` instead of `patch-1`.

    You could follow this convention. Some ideas to get you started:

    * Feature Updates: `feat-<2-3-Words-Description>-<ISSUE_NO>`
    * Bug Fixes: `fix-<2-3-Words-Description>-<ISSUE_NO>`
    * Documentation: `docs-<2-3-Words-Description>-<ISSUE_NO>`
    * And so on...

    ```bash
    git checkout -b your-branch-name
    ```

5. Go to `themes/` directory
    ```bash
    cd src/sass/themes
    ```

6. There you'll find default themes
    * Copy a theme and change it's name to your theme
        ```bash
        cp _modern-light.scss _<your-theme-name>.scss
        ```
    * Make your changes following the instructions [here](https://github.com/ankerapp/anker-app#how)

7. After you finish and you're happy with the result fork the [Anker
   themes](https://github.com/ankerapp/anker-themes) repository and clone it
    ```bash
    git clone https://github.com/<your-username>/anker-themes.git
    ```

8. Create a branch as mentioned in point 4.

9. Navigate to `anker-themes` directory and inside that to `themes/`
    ```bash
    cd anker-themes
    cd themes
    ```

10. Put everything together and get your PR ready
    * Inside `themes` directory create a directory for your theme with the same
        name as your theme e.g your theme name is `_example.scss` your directory
        will become `example/`.
    * Inside your theme directory you should have a `js` and `sass` directory.
        Your theme JS file goes in `example/js` and the SCSS file in
        `example/sass`.
    * If your theme don't have a specific JS file and used the default theme you
        still have to rename it to your theme name and include it in theme
        files.
    * Inside put your `_<your-theme-name>.scss` also `<your-theme-name>.js` file
        and `data.json` if necessary.
    * Take a screenshot!
    * Create a `README.md` file
    * Put your screenshot in `README.md` file also your instructions if needed
    * Best practice add a demo maybe a Netlify demo which is done in minutes

11. Create a new [Pull Request](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request) from `<your-branch-name>`

12. Congratulations! You've made your first pull request! Now, you should just wait until the maintainers review your pull request.
