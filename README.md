Silex Kraftwagen Drupal 7
=========================

A [Drupal](https://drupal.org/) application built using the [Kraftwagen](http://kraftwagen.org/) profile and development framework.

## Development Setup

Kraftwagen provides a unique system for defining application environments and building the Drupal application accordingly.

These steps will prepare the code for development; although these steps are common to all builds:

1. Clone repo to `src`

    ```bash
    git clone git@github.com:SilexConsulting/silex_kraftwagen_d7.git silex/src
    ```

2. Navigate into `src` to install `drush` and the Kraftwagen plugin with [Composer](http://getcomposer.org/)

    ```bash
    cd silex/src
    composer install
    ```

3. Run Kraftwagen setup

    ```bash
    bin/drush kw-s
    ```

4. Run Kraftwagen build

    ```bash
    bin/drush kw-b
    ```

    The build process will copy the contents of `src` into `build/profiles/silex` and will include the `.git` directory, making it a full copy of the workspace.

5. Update local settings and application environment

    ```bash
    cd ..
    ```

    Update MySQL settings in `cnf/settings.local.php`

    Set environment in `cnf/environment` (optional)

    The build process will copy the contents of `src` into `build/profiles/silex` and will include the `.git` directory, making it a full copy of the workspace.

    Navigate to `build/profiles/silex` to work and you can refresh your code as necessary.

6. Initialize the database:

    ```bash
    cd build
    profiles/silex/bin/drush kw-id
    ```
