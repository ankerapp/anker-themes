# Anker Default Themes

![Anker default theme screenshot](screenshot.png)

### Live Demo
[Click Here](https://ankerdemo.netlify.app/) to see the live demo!

### How to use this theme

1. First thing first fork the [Anker](https://github.com/ankerapp/anker-app) repository

2. Clone the forked repository
    ```bash
    git clone https://github.com/<your-username>/anker-app.git
    ```

3. Navigate to the themes directory
    ```bash
    cd anker-app/themes
    ```

4. Download the theme files with SVN. You can either export one of them of both.
    Run the following command/s. 
    ```bash
    svn export https://github.com/ankerapp/anker-themes/trunk/themes/anker-default-themes/default-theme-basic
    svn export https://github.com/ankerapp/anker-themes/trunk/themes/anker-default-themes/default-theme-pro
    ```

5. Navigate back to anker-app and build the project
    ```bash
    cd ..
    make build
    ```
