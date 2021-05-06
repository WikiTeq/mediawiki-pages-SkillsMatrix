# Skills matrix package

Provides template for users to add skills to their user-pages and a special aggregation
template to display skills matrix with all users data.

# Requirements

* SemanticMediaWiki
* PageForms
* ParserFunctions
* PageExchange or PagePort

# Setup

## via PagePort 

* download the repository
* run `php extensions/PagePort/maintenance/importPages.php --source ~/mediawiki-pages-Skillsmatrix`

## via PageExchange

* add the following to the bottom of your `LocalSettings.php`: `#$wgPageExchangePackageFiles[] = 'https://raw.githubusercontent.com/WikiTeq/mediawiki-pages-Skillsmatrix/master/page-exchange.json';`
* navigate to `Special:Packages` and install the package
* run `php maintenance/runJobs.php`

# Usage

* Add the `{{EditSkills}}` template to user pages, this will display a form button and so let users to input their skills
* Include the `{{Skills matrix}}` template on any page to display the skills matrix
