=========
数据库
=========


::

    数据库方式 Session 处理器


+-------------+------------------------+
|属性         |值                      |
+=============+========================+
|命名空间     |fize\\session\\handler  |
+-------------+------------------------+
|类名         |Database                |
+-------------+------------------------+
|实现接口     |SessionHandlerInterface |
+-------------+------------------------+


:方法:


+-----------------+---------------------+
|方法名           |说明                 |
+=================+=====================+
|`__construct()`_ |构造                 |
+-----------------+---------------------+
|`open()`_        |打开 session         |
+-----------------+---------------------+
|`close()`_       |关闭 session         |
+-----------------+---------------------+
|`read()`_        |读取 Session         |
+-----------------+---------------------+
|`write()`_       |写入 Session         |
+-----------------+---------------------+
|`destroy()`_     |删除 Session         |
+-----------------+---------------------+
|`gc()`_          |垃圾回收 Session     |
+-----------------+---------------------+
|`initMysql()`_   |针对MySQL初始化      |
+-----------------+---------------------+


方法
======
__construct()
-------------
构造

.. code-block:: php

  public function __construct (
      array $config = []
  )


:参数:
  +-------+-------+
  |名称   |说明   |
  +=======+=======+
  |config |配置   |
  +-------+-------+
  
  


open()
------
打开 session

.. code-block:: php

  public function open (
      string $save_path,
      string $session_name
  ) : bool


:参数:
  +-------------+----------------------+
  |名称         |说明                  |
  +=============+======================+
  |save_path    |存储会话的路径        |
  +-------------+----------------------+
  |session_name |会话名称              |
  +-------------+----------------------+
  
  


close()
-------
关闭 session

.. code-block:: php

  public function close () : bool



read()
------
读取 Session

.. code-block:: php

  public function read (
      string $session_id
  ) : string


:参数:
  +-----------+----------+
  |名称       |说明      |
  +===========+==========+
  |session_id |会话 ID   |
  +-----------+----------+
  
  


write()
-------
写入 Session

.. code-block:: php

  public function write (
      string $session_id,
      string $session_data
  ) : bool


:参数:
  +-------------+-------------+
  |名称         |说明         |
  +=============+=============+
  |session_id   |会话 ID      |
  +-------------+-------------+
  |session_data |会话数据     |
  +-------------+-------------+
  
  


destroy()
---------
删除 Session

.. code-block:: php

  public function destroy (
      string $session_id
  ) : bool


:参数:
  +-----------+----------+
  |名称       |说明      |
  +===========+==========+
  |session_id |会话 ID   |
  +-----------+----------+
  
  


gc()
----
垃圾回收 Session

.. code-block:: php

  public function gc (
      int $maxlifetime
  ) : bool


:参数:
  +------------+-------------------+
  |名称        |说明               |
  +============+===================+
  |maxlifetime |最长有效时间       |
  +------------+-------------------+
  
  


initMysql()
-----------
针对MySQL初始化

.. code-block:: php

  public static function initMysql (
      array $config
  )


:参数:
  +-------+-------+
  |名称   |说明   |
  +=======+=======+
  |config |       |
  +-------+-------+
  
  


::

    如果尚未建立 session 表，可以运行该方法来建立表


