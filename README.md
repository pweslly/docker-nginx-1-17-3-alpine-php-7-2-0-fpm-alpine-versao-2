<h1> Versão 2 - Mais simples e organizada </h2>

<h3> Configuração parte 1 </h3>

O arquivo <strong>Dockerfile-app-php-fpm</strong>  ele instala composer caso tenha alguam aplicação que precise, caso queira
baixar depedências só adicionar

* RUN  composer install 

e também libera a porta 9000, porta padrão do PHP-FPM

<h3> Configuração parte 2 </h3>

O arquivo <strong>Dockerfile-nginx</strong> onde fica configurações do nginx, ele remove as configurações padrão de lá
e adiciona o arquivo <strong>nginx.conf</strong> que estão com as minhas configurações, tipo:
* Pasta onde vai ficar minha aplicação
* Configuração com PHP-FPM
* Configurações em geral do uso .htacess 
* Configurações das páginas de erros e entre outros.


<h3> Observação </h3>

Só vai fazer provisionamento pelo <strong>docker-compose </strong> aplicação com php-fpm e o nginx, não tem banco dados, phpmyadmin, jenkis e não o redis.
E também não esta configurado para pegar aplicação com Laravel. 

<h2> Objetivo </h2>
É mais para criar ambiente de desenvolvimento com PHP para fazer testes com PHP, HTML e CSS