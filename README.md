# SilverStripe live templates
Some useful live templates for IntelliJ PHP/WebStorm. 

# Installation
Download and place the template files inside your IDE's templates folder. Where the folder is located depends on the version and type of IDE you are using. 

See [this IntelliJ article](https://intellij-support.jetbrains.com/hc/en-us/articles/206544519-Directories-used-by-the-IDE-to-store-settings-caches-plugins-and-logs) on where your settings are stored.


If you're lazy and you have PhpStorm2016.1 and wget installed, you can copy and paste the following:
### Mac OSX
````
cd ~/Library/Preferences/PhpStorm2016.1/templates/
wget https://raw.githubusercontent.com/janneklouman/silverstripe-phpstorm-live-templates/master/SilverStripe%20PHP%20Fields.xml
wget https://raw.githubusercontent.com/janneklouman/silverstripe-phpstorm-live-templates/master/SilverStripe%20PHP%20Functions.xml
wget https://raw.githubusercontent.com/janneklouman/silverstripe-phpstorm-live-templates/master/SilverStripe%20PHP%20Skeletons.xml
wget https://raw.githubusercontent.com/janneklouman/silverstripe-phpstorm-live-templates/master/SilverStripe%20PHP%20Static%20Fields.xml
````

### Windows
````
cd c:\Users\USER_NAME\.PhpStorm2016.1\templates\
wget https://raw.githubusercontent.com/janneklouman/silverstripe-phpstorm-live-templates/master/SilverStripe%20PHP%20Fields.xml
wget https://raw.githubusercontent.com/janneklouman/silverstripe-phpstorm-live-templates/master/SilverStripe%20PHP%20Functions.xml
wget https://raw.githubusercontent.com/janneklouman/silverstripe-phpstorm-live-templates/master/SilverStripe%20PHP%20Skeletons.xml
wget https://raw.githubusercontent.com/janneklouman/silverstripe-phpstorm-live-templates/master/SilverStripe%20PHP%20Static%20Fields.xml
````

### Linux
````
cd ~/.PhpStorm2016.1/templates/
wget https://raw.githubusercontent.com/janneklouman/silverstripe-phpstorm-live-templates/master/SilverStripe%20PHP%20Fields.xml
wget https://raw.githubusercontent.com/janneklouman/silverstripe-phpstorm-live-templates/master/SilverStripe%20PHP%20Functions.xml
wget https://raw.githubusercontent.com/janneklouman/silverstripe-phpstorm-live-templates/master/SilverStripe%20PHP%20Skeletons.xml
wget https://raw.githubusercontent.com/janneklouman/silverstripe-phpstorm-live-templates/master/SilverStripe%20PHP%20Static%20Fields.xml
````

# List of available templates
## Static variables
### aa (allowed actions)
````PHP
/**
 * @var array
 */
private static $allowed_actions = [
    '$END$'
];
````
### bmm (belongs many-many)
````PHP
/**
 * @var array
 */
private static $belongs_many_many = [
    '$VAR$'  => '$END$'
];
````
### db (database)
````PHP
/**
 * @var array
 */
private static $db = [
    '$VAR$' => '$END$'
];
````
### hm (has many)
````PHP
/**
 * @var array
 */
private static $has_many = [
    '$VAR$'  => '$END$'
];
````
### ho (has one)
````PHP
/**
 * @var array
 */
private static $has_one = [
    '$VAR$'  => '$END$'
];
````
### mm (many many)
````PHP
/**
 * @var array
 */
private static $many_many = [
    '$VAR$'  => '$END$'
];
````
### mmef (many many extra fields)
````PHP
/**
 * @var array
 */
private static $many_many_extraFields = [
    '$RELATION$' => [
        '$NAME$' => '$TYPE$'
    ]
];

````
### sef (searchable fields)
````PHP
/**
 * @var array
 */
private static $searchable_fields = [
    $END$
];
````
### suf (summary fields)
````PHP
/**
 * @var array
 */
private static $summary_fields = [
    $END$
];
````
## Fields
### gf (grid field)
````PHP
$config = GridFieldConfig_$TYPE$::create();
$$$FIELDNAME$ = GridField::create(
    '$RELATIONNAME$',
    _t('$CLASSNAME$.PLURALNAME', '$RELATIONNAME$'),
    $this->$DATALIST$(),
    $config
);
````
## Functions
### gcms (get cms fields)
````PHP
/**
 * @return FieldList
 */
public function getCMSFields() {

    $fields = parent::getCMSFields();
    
    $END$

    return $fields;

}
````
### log
````PHP
SS_Log::log( print_r ( $END$, true ), SS_Log::WARN );
````
### t (translate)
````PHP
_t('$STRING$', '$END$')
````
### ucms (update cms fields)
````PHP
/**
 * @param FieldList $fields
 */
public function updateCMSFields(FieldList $fields) 
{
    $END$
}
````
## Skeletons
### dofs (data object file start)
````PHP
/**
 * $DESCRIPTION$
 * @author $AUTHOR$
 * @package $PACKAGE$
 * @subpackage $SUBPACKAGE$
 */
class $CLASS$ extends DataObject
{
    $END$
}
````
### pfs (page file start)
````PHP
/**
 * $DESCRIPTION$
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
````
