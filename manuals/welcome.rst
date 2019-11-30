========
欢迎使用
========

FizeSession 是一个易于扩展的 Session 底层管理类库。

FizeSession 允许您将会话数据存放在任意的位置，无论是数据库、文件、Memcached 还是 Redis。

FizeSession 可以进行处理器选择，因此您可以根据系统环境自行选择 Session 处理器。

FizeSession 有非常完善的参考文档，且其功能追求简洁明了，相信您会喜欢上这样的 Session 管理类库。


处理器支持
==========

目前 FizeSession 已支持的处理器如下：

-  :doc:`Database </configs/database>` : 数据库，具体可以参考 `FizeDb <https://fizedb.readthedocs.io/zh_CN/latest/configs/index.html>`_ 。
-  :doc:`File </configs/file>` : 文件形式 。
-  :doc:`Memcache </configs/memcache>` : Memcache 形式 (暂未实现)。
-  :doc:`Memcached </configs/memcached>` : Memcached 形式 (暂未实现)。
-  :doc:`Redis </configs/redis>` : Redis 形式 (暂未实现)。


入门三部曲
==========

1.配置参数
----------

根据 :doc:`参数配置 </configs/index>` 进行FizeSession 配置。

2.设置默认会话或者设置新会话
----------------------------

使用 `new Session(array $config = []);`进行默认会话设置，或者 `Session` 提供的各类方法设置新会话并手动启动会话。

3.进行 session 会话操作
----------------

FizeSession 作为 session 底层管理类库，并不直接对全局变量 `$_SESSION` 进行操作。
FizeSession 的作用是设置 session 环境，满足系统对会话数据、方式的要求。


入门示例
========

.. code-block:: php

	use fize\session\Session;

	$config = [
		'save_handler'      => [
			'type'              => 'Database',
			'config'            => [
				'db' => [
					'type' => 'mysql',
					'config' => [
						'host'     => 'localhost',
						'user'     => 'root',
						'password' => '123456',
						'dbname'   => 'gm_test'
					]
				],
				'table' => 'sys_session'
			],
			'register_shutdown' => true
		]
	];
	new Session($config);

	$_SESSION['admin'] = [
		'name' => '中华人民共和国2',
		'age'  => 30,
		'time' => date('Y-m-d H:i:s')
	];

	echo '写入 session';
		

