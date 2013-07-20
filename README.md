# LPTUpload extension for Yii Framework
The code is based on XUpload for Yii, but it runs a more up to date version of Blue Imp jQuery File Upload


## Configuration

Add an application alias in you application configuration that points to the extracted folder

// protected/config/main.php
...
`'import'=>array(
    'application.models.*',
    'application.components.*',
),
'aliases' => array(
    //If you used composer your path should be
    'xupload' => 'ext.vendor.asgaroth.xupload'
    //If you manually installed it
    'xupload' => 'ext.xupload'
),`

Create a model, declare an attribute to store the uploaded file data, and declare the attribute to be validated by the 'file' validator. Or use XUploadForm
    Create a controller to handle form based file uploads. Or use XUploadAction
    Add the Widget to you view

<?php
$this->widget('xupload.XUpload', array(
                    'url' => Yii::app()->createUrl("site/upload"),
                    'model' => $model,
                    'attribute' => 'file',
                    'multiple' => true,
));
?>


## Yii extension page
[Extension page](http://www.yiiframework.com/extension/xupload/)

## Demo
[jQuery file upload](http://blueimp.github.com/jQuery-File-Upload/ "jQuery File Upload") extension for Yii, 
allows your users to easily upload files to the server.


* [XUpload Workflow example](http://www.yiiframework.com/wiki/348/xupload-workflow/)
* [Additional form data with XUpload](http://www.yiiframework.com/wiki/395/additional-form-data-with-xupload/)


