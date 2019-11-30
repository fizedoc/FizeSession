=========
Memcached
=========


::

    Memcached 方式 Session 处理器


+-------------+------------------------+
|属性         |值                      |
+=============+========================+
|命名空间     |fize\\session\\handler  |
+-------------+------------------------+
|类名         |Memcached               |
+-------------+------------------------+
|实现接口     |SessionHandlerInterface |
+-------------+------------------------+


:方法:


+-----------------+--------------------+
|方法名           |说明                |
+=================+====================+
|`__construct()`_ |构造                |
+-----------------+--------------------+
|`open()`_        |打开session         |
+-----------------+--------------------+
|`close()`_       |关闭session         |
+-----------------+--------------------+
|`read()`_        |读取Session         |
+-----------------+--------------------+
|`write()`_       |写入Session         |
+-----------------+--------------------+
|`destroy()`_     |删除Session         |
+-----------------+--------------------+
|`gc()`_          |垃圾回收Session     |
+-----------------+--------------------+


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
  |config |       |
  +-------+-------+
  
  


open()
------
打开session

.. code-block:: php

  public function open (
      string $save_path,
      string $session_name
  ) : bool


:参数:
  +-------------+-------+
  |名称         |说明   |
  +=============+=======+
  |save_path    |       |
  +-------------+-------+
  |session_name |       |
  +-------------+-------+
  
  


close()
-------
关闭session

.. code-block:: php

  public function close () : bool



read()
------
读取Session

.. code-block:: php

  public function read (
      string $session_id
  ) : string


:参数:
  +-----------+-------+
  |名称       |说明   |
  +===========+=======+
  |session_id |       |
  +-----------+-------+
  
  


write()
-------
写入Session

.. code-block:: php

  public function write (
      string $session_id,
      string $session_data
  ) : bool


:参数:
  +-------------+-------+
  |名称         |说明   |
  +=============+=======+
  |session_id   |       |
  +-------------+-------+
  |session_data |       |
  +-------------+-------+
  
  


destroy()
---------
删除Session

.. code-block:: php

  public function destroy (
      string $session_id
  ) : bool


:参数:
  +-----------+-------+
  |名称       |说明   |
  +===========+=======+
  |session_id |       |
  +-----------+-------+
  
  


gc()
----
垃圾回收Session

.. code-block:: php

  public function gc (
      int $maxlifetime
  ) : bool


:参数:
  +------------+-------+
  |名称        |说明   |
  +============+=======+
  |maxlifetime |       |
  +------------+-------+
  
  


