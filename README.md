# Skills matrix package

Provides a form and template for users to add skills to their user pages and a special aggregation
template to display a skills matrix with all users' data.

# Requirements

* SemanticMediaWiki
* PageForms
* ParserFunctions
* PageExchange or PagePort
* Bootstrap (optional) - Without it, the styling will be very plain

# Setup

## via PagePort 

* download the repository
* run `php extensions/PagePort/maintenance/importPages.php --source ~/mediawiki-pages-Skillsmatrix`

## via PageExchange

* add the following to the bottom of your `LocalSettings.php`: `$wgPageExchangePackageFiles[] = 'https://raw.githubusercontent.com/WikiTeq/mediawiki-pages-SkillsMatrix/master/page-exchange.json';`
* navigate to `Special:Packages` and install the package
* (optional) run `php maintenance/runJobs.php`

# Usage
* Create the page `Property:Skill/Values` on your wiki. Customize it by adding one skill per line.
* Add the `{{EditSkills}}` template to user pages. This will display a form button which allows adding this user's skills.
* Include the `{{Skills matrix}}` template on any page to display the skills matrix.
