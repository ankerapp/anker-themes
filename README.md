# Anker Themes
This repo is only for themes.

# How to Use a Theme?
This applies to all the themes in `anker-themes` repository. To use a theme you
can either download the theme file manually which is `_<theme-name>.scss` and
move it to `themes/` directory and add in `_index.scss` inside `themes/`
directory to be compiled.

The other solution is to navigate to `themes/` directory and use cURL to export
it directly from this repository like following:

```bash
curl https://raw.githubusercontent.com/ankerapp/anker-themes/master/<theme-name>/_<theme-name>.scss >_<theme-name>.scss
```

### Where do I Get the Link for cURL from?
1. Select the theme folder you want to use.

2. Next click on the SCSS theme file

3. Now click on raw to show the raw code you will see the URL changes to
   `https://raw.githubusercontent.com/...`

4. Copy the URL and run the following command e.g theme name is
   `_midnight-dark.scss`
```bash
curl <raw-code-link> >_midnight-dark.scss
```

### Put your Theme in the Right Directory
1. Navigate to `themes/` directory
```bash
cd src/sass/themes
```

2. Copy your theme manually or download it using cURL.

3. Open `_index.scss` file and add your theme there
```scss
@forward "<theme-name>";
```

4. Build the project and you now have your own landing page.

5. Push the your `dist` to a live server, Netlify etc.

# Contributing to Anker
If you want to contribute to Anker and want to make your own themes and
publish them here then please follow [these](https://github.com/0xkhan/anker-demo/blob/master/guides/CONTRIBUTING.md) guidelines.

# How do I Make a Theme?

To develop a theme for Anker please follow the guidelines following:

1. First thing first fork the [Anker](https://github.com/ankerapp/anker-app) repository

2. Clone the forked repository
```bash
git clone https://github.com/<your-username>/anker-app.git
```

3. Navigate to the project directory
```bash
cd anker-app
```

4. Create a new branch kindly give your branch a more descriptive name like `theme-add-<your-theme-name>` instead of `patch-1`.

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

7. After you finish with the theme and you're happy with it fork the [Anker
   themes](https://github.com/ankerapp/anker-themes) repository and clone it
```bash
git clone https://github.com/<your-username>/anker-themes.git
```

8. Create a branch as mentioned in point 4.

9. Navigate to `anker-themes` directory and inside that to `thtmes/`
```bash
cd anker-themes
cd themes
```

10. Put everything together and get your PR ready
    * inside `themes` directory create a directory for your theme with the same
        name as your theme e.g your theme name is `_example.scss` your directory
        will become `example/`
    * Inside put your `_<your-theme-name>.scss`
    * Take screenshots for different devices
    * Create a `README.md` file
    * Put your screenshots in `README.md` file also your instructions if needed
    * Best practice add a demo maybe a Netlify demo which is done in minutes

11. Create a new [Pull Request](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request) from `<your-branch-name>`

12. Congratulations! You've made your first pull request! Now, you should just wait until the maintainers review your pull request.
