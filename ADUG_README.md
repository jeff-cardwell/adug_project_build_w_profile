1. Initialize Project
    ```shell
    $ composer create-project drupal-composer/drupal-project:8.x-dev adug_project_w_profile --stability dev --no-interaction --profile
    ```

2. Initialize Git
    ```shell
    $ git init
    $ git add .
    $ git commit -m "initial commit"
   ```

3. Config Composer Drupal Repo
    ```shell
    $ composer config repositories.drupal composer https://packages.drupal.org/8
    ```

4. Remove the following code from `composer.json`
    ```json
    "0": {
        "type": "composer",
        "url": "https://packagist.drupal-composer.org"
    },
    ```

5. Add custom profile repo
    ```shell
    $ composer config repositories.adug_profile vcs https://github.com/jeff-cardwell/adug_profile.git
    ```

6. Require custom profile
    ```shell
    $ composer require jeff-cardwell/adug_profile
    ```

    Note that `jeff-cardwell/adug_profile` matches the package name in its `composer.json` file

