Yii-dynamic-active-record
=========================

CActiveRecord implementation that allows specifying
DB table name instead of creating a class for each table.

#Usage 
(assuming table 'user' with columns 'id' and 'name'):
```PHP
$userModel = DynamicActiveRecord::forTable('user');
//list existing users
foreach ($userModel->findAll() as $user)
	echo $user->id . ': ' . $user->name . '<br>';
//add new user
$userModel->name = 'Pavle Predic';
$userModel->save();
```