# University of Adelaide Site Manager Scaffold

This composer plugin provides the tools required to make a Drupal project
deployable on the Site Manager Docker system, and keeps them up to date whenever
`composer update` is run.

## Requirements

You must be running Drupal 8, and implement the [Drupal composer workflow](https://www.drupal.org/docs/develop/using-composer/using-composer-with-drupal).

## Setup

In your Drupal project, require this repository using composer.

```
composer require universityofadelaide/sm-scaffold dev-master
```

Add the following items to your project's `composer.json`:

```
"scripts": {
  "sm-scaffold": "UniversityOfAdelaide\\SiteManagerScaffold\\Plugin::scaffold",
  "post-update-cmd": [
    "@sm-scaffold",
  ]
```

## Usage

Once setup, running `composer update` will fetch the latest version of the
Site Manager utility files (i.e. `RoboFileBase.php`, `dsh`, etc).

You will need to add and commit these files to your own project repository.
