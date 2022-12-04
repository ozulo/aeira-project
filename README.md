# AEira 

## O proxecto

A Eira é un proxecto tecnolóxico que ten como principal obxectivo o desenvolvemento dun sistema de xestión contidos homoxéneo libre e gratuito, baseado en Drupal, para publicación de catálogos de elementos patrimoniais. 

A día hoxe publicamos catro proxectos:

* [A Cultura da Auga](https://www.aculturadaauga.org)
* [Abeancos](https://www.abeancos.gal)
* [Palleira](https://www.palleira.gal)
* [obaixoulla](https://www.obaixoulla.gal)

Despois da publicación do proxecto **obaixoulla** en Novembro de 2019, xurde a necesidade de desenvolver unha única peza de software que axilice a publicación de novos sitios.

## O código

O repositorio que estás a visitar contén un único arquivo **composer.json** desde o que podes iniciar a instalación completa(hoxe aínda en versión **alpha**), seguindo os pasos descritos a continuación.

### Requirimentos

* PHP - Versión 8.0 ou máis recente.
* Base de datos - Nun contexto Drupal, a xestión da base de datos está incluida dentro dunha capa de abstración que fai, en certo modo, indiferente o emprego de MySQL, SQLite ou PostgreSQL.
* Servidor web - AEira funciona ben con [Nginx](https://www.nginx.org), debería tamén facelo con Apache2 ou Hiawatha.
* Sistema operativo. AEira funciona ben en **Linux**, tamén en **OSX**.  :kissing:

## Instalación

Clona o respositorio no teu equipo.

```bash
git clone https://github.com/apermuy/aeira-project.git
```

Copia o arquivo composer.json ó directorio de instalación do sitio, por exemplo: /var/www/aeira e executa composer install.

```php
cp composer.json /var/www/aeira && cd /var/www/aeira
composer install --prefer-dist --no-dev --no-interaction
```

Executa drush para iniciar a instalación. Exemplo para instalación con MySQL como backend de base de datos.

```php
cd /var/www/aeira/web
drush -y site-install aeira --db-url=mysql://usuaria:contrasinal@localhost:porto/aeira --account-name=admin --account-pass=admin
```

Podes servir o directorio **/var/www/aeira/web** para publicar elementos patrimoniais co teu novo sitio AEira.

## Financiamento e licenza

Este proxecto forma parte das actividades que a asociación [MeLiSA](https://www.melisa.gal) realiza ao abeiro do convenio de colaboración asinado coa [Axencia para a Modernización Tecnolóxica](https://amtega.xunta.gal) (AMTEGA), e está incluída no Plan de Acción de Software Libre 2020 da [Xunta de Galicia](https://www.xunta.gal).

Os traballos realizados están dispoñibles baixo unha licenza [GNU GENERAL PUBLIC LICENSE v3](https://www.gnu.org/licenses/gpl-3.0.html), tal e como se recolle no ficheiro COPYING.

![image](/img/bottom.png)
