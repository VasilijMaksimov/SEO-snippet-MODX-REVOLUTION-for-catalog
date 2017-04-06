# SEO-snippet-MODX-REVOLUTION-for-catalog
SEO snippet MODX REVOLUTION for catalog

RU/
Вызов сниппета
EN/
The snippet call
<title>[[seoTitleCatalog]]</title>


RU/
Cниппет
EN/
The snippet
<?php
$nameCategoryPagetitle = $modx->resource->get("pagetitle");
$nameCategoryLongtitle = $modx->resource->get("longtitle");
$nameCategory = $modx->resource->getTVValue("nameCategory");


$v = '';
if($nameCategory != ''){
 $v = $nameCategory;
}
else if ($nameCategoryLongtitle != "") {
 $v = $nameCategoryLongtitle;
}
else{
    $v = $nameCategoryPagetitle;
}

return $v;
