# xunsearch
 simple xunsearch package for any Framework.

 请看原作者的包：https://github.com/ShaoZeMing/xunsearch-laravel

 重复造这个轮子，只是因为我真的不喜欢demo.ini这种配置文件，根本没法和框架的配置灵活组合，还是数组操作方便。所以我改了改，以方便和我的HunterPHP框架无缝整合！具体参看此模块：

 https://github.com/hunteryun/xunsearch_api

 ### Usage

 ```php

 <?php

 $config = array(
   'project.name' => 'story',
   'project.default_charset' => 'utf-8',
   'server.index' => '192.168.1.250:8383',
   'server.search' => '192.168.1.250:8384',
   'sid' => array(
     'type' => 'id'
   ),
   'story_name' => array(
     'type' => 'title'
   ),
   'story_content' => array(
     'type' => 'body'
   ),
   'image' => array(
     'type' => 'string'
   ),
   'type' => array(
     'type' => 'string'
   ),
   'created' => array(
     'type' => 'data'
   ),
   'sid' => array(
     'type' => 'id'
   ),
 );

  use Hunter\Xunsearch\Search;

  $xs = new Search($configs); //$configs is array , not file, I hate file.

  $xs->addIndex($data); // $data is your index data array.
  $xs->updateIndexOne($data);
  $xs->delIndex($ids);
  $xs->cleanIndex();

 ```
