# SilverStripe live templates
[![Mentioned in Awesome Silverstripe CMS](https://awesome.re/mentioned-badge-flat.svg)](https://github.com/wernerkrauss/awesome-silverstripe)

My collection of live templates for WebStorm and PhpStorm, following PSR-2, using PHPDoc, and utilizing PHP 5.4 array shorthand syntax. These templates do not attempt cover every field, variable, nor function, but are a collection of snippets that I frequently use in my daily work. Feel free to [open issues](https://github.com/jjjjjjjjjjjjjjjjjjjj/silverstripe-phpstorm-live-templates/issues) to suggest additional templates.

# Installation
Download and place the template files inside your IDE's `templates/` folder. Where the folder is located depends on the version and type of IDE you are using. Consult [this IntelliJ article](https://intellij-support.jetbrains.com/hc/en-us/articles/206544519-Directories-used-by-the-IDE-to-store-settings-caches-plugins-and-logs) on where you'll find yours if below table does not work. Restart your IDE after placing the files in the templates folder.

|OS| Path
|---|---|
|Windows|`<your home directory>\.<product name><version number>\config\templates`|
|Linux|`~\.<product name><version number>\config\templates`|
|OS X|`~/Library/Preferences/<product name><version number>/templates`|

Direct links to specific template files: 
* [`SilverStripe PHP Fields.xml`](https://raw.githubusercontent.com/janneklouman/silverstripe-phpstorm-live-templates/master/SilverStripe%20PHP%20Fields.xml)
* [`SilverStripe PHP Functions.xml`](https://raw.githubusercontent.com/janneklouman/silverstripe-phpstorm-live-templates/master/SilverStripe%20PHP%20Functions.xml)
* [`SilverStripe PHP Skeletons.xml`](https://raw.githubusercontent.com/janneklouman/silverstripe-phpstorm-live-templates/master/SilverStripe%20PHP%20Skeletons.xml)
* [`SilverStripe PHP Static Variables.xml`](https://raw.githubusercontent.com/janneklouman/silverstripe-phpstorm-live-templates/master/SilverStripe%20PHP%20Static%20Variables.xml)

Or you can `cd` to `templates/` directory and run:

`git clone https://github.com/jjjjjjjjjjjjjjjjjjjj/silverstripe-php-web-storm-live-templates.git .`

Then optionally remove the unused files by doing something like `rm -rf .git` and `rm README.md` if you don't want them in there.

# Usage
When editing a PHP file you can simply type in the short code for the live template and then hit the "Choose lookup Item Replace" keymap binding (`tab` by default). For example, typing in `aa` then hitting `tab`, would expand `aa` into the following and leaving your cursor in between the single quotes:
```PHP
/**
 * @var array
 */
private static $allowed_actions = [
    ''
];
```

# List of available templates and their contents
  - [Fields](#fields)
    - [cbf (check box field)](#cbf-check-box-field)
    - [ddf (drop down field)](#drop-down-field)
    - [df (date field)](#df-date-field)
    - [fg (field group)](#fg-field-group)
    - [gf (grid field)](#gf-grid-field)
    - [lf (literal field)](#lf-literal-field)
    - [nf (numeric field)](#nf-numeric-field)
    - [tf (text field)](#tf-text-field)
  - [Functions](#functions)
    - [gcms (get cms fields)](#gcms-get-cms-fields)
    - [log](#log)
    - [t (translate)](#t-translate)
    - [ucms (update cms fields)](#ucms-update-cms-fields)
  - ["Skeletons"](#skeletons)
    - [dofs (data object file start)](#dofs-data-object-file-start)
    - [defs (data extension file start)](#defs-data-extension-file-start)
    - [efs (extension file start)](#efs-extension-file-start)
    - [pfs (page file start)](#pfs-page-file-start)
  - [Static variables](#static-variables)
    - [aa (allowed actions)](#aa-allowed-actions)
    - [bmm (belongs many-many)](#bmm-belongs-many-many)
    - [db (database)](#db-database)
    - [d (defaults)](#defaults)
    - [ds (default sort)](#default-sort)
    - [hm (has many)](#hm-has-many)
    - [ho (has one)](#ho-has-one)
    - [mm (many many)](#mm-many-many)
    - [mmef (many many extra fields)](#mmef-many-many-extra-fields)
    - [sef (searchable fields)](#sef-searchable-fields)
    - [suf (summary fields)](#suf-summary-fields)

## Fields
Direct link to the live template file: https://raw.githubusercontent.com/janneklouman/silverstripe-phpstorm-live-templates/master/SilverStripe%20PHP%20Fields.xml
### cbf (check box field)
```PHP
CheckboxField::create('$NAME$', $LABEL$)$END$
```
### ddf (drop down field)
```PHP
DropdownField::create(
    '$NAME$',
    $LABEL$,
    $DATALIST$
)$END$
```
### df (date field)
```PHP
DateField::create('$NAME$', $LABEL$)$END$
```
### fg (field group)
```PHP
FieldGroup::create(
    $LABEL$,
    [
        $FIELDS$
    ]
)$END$
```
### gf (grid field)
```PHP
GridField::create(
    '$NAME$',
    $LABEL$,
    $this->$DATALIST$(),
    GridFieldConfig_$TYPE$::create()
)$END$
```
### lf (literal field)
```PHP
LiteralField::create('$NAME$', $LABEL$)$END$
```
### nf (numeric field)
```PHP
NumericField::create('$NAME$', $LABEL$)$END$
```
### tf (text field)
```PHP
TextField::create('$NAME$', $LABEL$)$END$
```
## Functions
Direct link to the live template file: https://raw.githubusercontent.com/janneklouman/silverstripe-phpstorm-live-templates/master/SilverStripe%20PHP%20Functions.xml
### gcms (get cms fields)
```PHP
/**
 * @return FieldList
 */
public function getCMSFields() {

    $fields = parent::getCMSFields();
    
    $END$

    return $fields;

}
```
### log
```PHP
SS_Log::log( print_r ( $END$, true ), SS_Log::WARN );
```
### t (translate)
```PHP
_t('$STRING$', '$DEFAULT$')$END$
```
### ucms (update cms fields)
```PHP
/**
 * @param FieldList $fields
 */
public function updateCMSFields(FieldList $fields) 
{
    $END$
}
```
## "Skeletons"
Direct link to the live template file: https://raw.githubusercontent.com/janneklouman/silverstripe-phpstorm-live-templates/master/SilverStripe%20PHP%20Skeletons.xml
### dofs (data object file start)
```PHP
/**
 * $DESCRIPTION$
 *
 * @author $AUTHOR$
 * @package $PACKAGE$
 * @subpackage $SUBPACKAGE$
 */
class $CLASS$ extends DataObject
{
    $END$
}
```
### defs (data extension file start)
```PHP
/**
 * $DESCRIPTION$
 *
 * @author $AUTHOR$
 * @package $PACKAGE$
 * @subpackage $SUBPACKAGE$
 */
class $CLASS$Extension extends DataExtension
{
    $END$
}
```
### efs (extension file start)
```PHP
/**
 * $DESCRIPTION$
 *
 * @author $AUTHOR$
 * @package $PACKAGE$
 * @subpackage $SUBPACKAGE$
 */
class $CLASS$ extends Extension
{
    $END$
}
```
### pfs (page file start)
```PHP
/**
 * $DESCRIPTION$
 *
 * @author $AUTHOR$
 * @package $PACKAGE$
 * @subpackage $SUBPACKAGE$
 */
class $CLASS$ extends Page
{
    $END$
}

class $CLASS$_Controller extends Page_Controller 
{
}
```
## Static variables
Direct link to the live template file: https://raw.githubusercontent.com/janneklouman/silverstripe-phpstorm-live-templates/master/SilverStripe%20PHP%20Static%20Variables.xml
### aa (allowed actions)
```PHP
/**
 * @var array
 */
private static $allowed_actions = [
    '$END$'
];
```
### bmm (belongs many-many)
```PHP
/**
 * @var array
 */
private static $belongs_many_many = [
    '$VAR$'  => '$END$'
];
```
### d (defaults)
```PHP
/**
 * @var array
 */
private static $defaults = [
    $END$
];
```
### db (database)
```PHP
/**
 * @var array
 */
private static $db = [
    '$VAR$' => '$END$'
];
```
### df (default sort)
```PHP
/**
 * @var string
 */
private static $default_sort '$END$';
```
### hm (has many)
```PHP
/**
 * @var array
 */
private static $has_many = [
    '$VAR$'  => '$END$'
];
```
### ho (has one)
```PHP
/**
 * @var array
 */
private static $has_one = [
    '$VAR$'  => '$END$'
];
```
### mm (many many)
```PHP
/**
 * @var array
 */
private static $many_many = [
    '$VAR$'  => '$END$'
];
```
### mmef (many many extra fields)
```PHP
/**
 * @var array
 */
private static $many_many_extraFields = [
    '$RELATION$' => [
        '$NAME$' => '$TYPE$'
    ]
];

```
### sef (searchable fields)
```PHP
/**
 * @var array
 */
private static $searchable_fields = [
    $END$
];
```
### suf (summary fields)
```PHP
/**
 * @var array
 */
private static $summary_fields = [
    $END$
];
```
