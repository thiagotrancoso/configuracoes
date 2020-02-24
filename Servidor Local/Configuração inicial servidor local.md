## Configuração inicial servidor local
Está configuração é feita apenas uma vez após instalar o servidor web local.

## Configurando arquivo do php "php.ini"
~~~php
memory_limit=128M
max_execution_time=60
date.timezone=America/Sao_Paulo
post_max_size=20M
~~~

~~~php
// Development Value: E_ALL
// Production Value:  E_ALL & ~E_DEPRECATED & ~E_STRICT
error_reporting=E_ALL
~~~

~~~php
// Development Value: On
// Production Value:  Off
display_errors=On
~~~

~~~php
// Descomente essa linha
extension=php_openssl.dll
~~~

~~~php
// Habilitar extensão do PostgreSql. Descomente a linha abaixo.
extension=pdo_pgsql
~~~

## Configurando arquivo do apache "httpd.conf"
~~~php
// Descomente a linha abaixo
LoadModule rewrite_module modules/mod_rewrite.so
~~~
