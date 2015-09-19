# Introduction #
This is a quick PHP script to count how many lines of code there are. You can configure it to ignore certain files and folders, and whether to ignore comments and blank lines. Read the usage.txt to see how to use this script.

# Example #
```
$options = array(
    'ignoreFolders' => explode(', ', '.svn, nbproject'),
    'ignoreFiles' => explode(', ', 'jquery-1.5.js, jquery-1.5.min.js'),
    'extensions' => explode(', ', 'php, js'),
    'whitespace' => false,
    'comments' => false,
);

//Scan user defined directory
$folder = new Folder('path/to/project', new Option($options));
$folder->init();

$lines = $folder->getLines();
$whitespace = $folder->getWhitespace();
$comments = $folder->getComments();
```