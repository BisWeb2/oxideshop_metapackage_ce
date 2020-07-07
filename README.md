OXID eShop metapackage
======================

This repository contains OXID eShop dependencies.

More information how to setup Shop:

  - https://docs.oxid-esales.com/developer/en/6.2/getting_started/installation/eshop_installation.html
  
## Install your own OXID eShop compilation

1. Fork https://github.com/OXID-eSales/oxideshop_metapackage_ce Repository on GitHub
2. Create your own Branch e.g. "bisweb" and push it to GitHub
3. Change composer.json e.g. remove Demodata from Community Edition and Demodata Installer with

```bash
composer remove --update-no-dev oxid-esales/oxideshop-demodata-ce
composer remove --update-no-dev oxid-esales/oxideshop-demodata-installer
composer update --no-dev
```

4. Commit and push your Changes to your forked Repository without source, vendor and composer.lock Directories or else File
5. Open your own Shop Project and loading OXID eShop compilation from your forked Repository https://getcomposer.org/doc/05-repositories.md#vcs

```bash
composer config repositories.repo-name vcs https://github.com/BisWeb2/oxideshop_metapackage_ce.git
```

6. Change oxid-esales/oxideshop-metapackage-ce: "v6.2.1" to oxid-esales/oxideshop-metapackage-ce: "dev-bisweb" in your composer.json
7. Update your Shop Project with Composer

```bash
composer update --no-dev
```

## Bugs and Issues

If you experience any bugs or issues, please report them in the section **OXID eShop (all versions)** of https://bugs.oxid-esales.com.
