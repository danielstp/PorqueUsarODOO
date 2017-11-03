:title: Porque ODOO
:author: Daniel Saguez Tezanos Pinto
:description: Ventajas de Usar ODOO
:keywords: presentación, restructuredtext, impress.js, ODOO
:data-transition-duration: 1500
:auto-console: true
:css: Presenta.css

################
Porque usar ODOO
################


----

Qué es ODOO
###########

Odoo (conocido anteriormente como OpenERP y anteriormente como TinyERP) es un
sistema de ERP integrado de código abierto actualmente producido por la empresa
belga Odoo S.A. El fabricante declara su producto como una alternativa de código
abierto a SAP ERP y Microsoft Dynamics.

----

Qué es ERP
##########

Sistema de planificación de recursos empresariales ('ERP', por sus siglas en
inglés, enterprise resource planning) son los sistemas de información
gerenciales que integran y manejan muchos de los negocios asociados con las
operaciones de producción y de los aspectos de distribución de una compañía en la
producción de bienes o servicios.

----

Módulos base de ODOO
####################

Odoo viene provisto de módulos estándar tales como:

-    Gestión de compraventa.
-    CRM. (Manejo de la Relación con el Cliente)
-    Gestión de proyectos.
-    Sistema de gestión de almacenes.
-    Manufactura. Producción.
-    Contabilidad analítica y financiera.
-    Puntos de venta.
-    Gestión de activos.
-    Gestión de recursos humanos.
-    Gestión de inventario.
-    Ayuda técnica.
-    Campañas de marketing.
-    Flujos de trabajo.

----

Ventajas de ODOO
################

- Python (un lenguaje fácil de aprender y mantener)
- Desarrollo muy activo
- Versiones muy probadas
- Responsivo
- Aplicaciones moviles y API para crear nuevas apps
- Usabilidad

----

:data-x: r+1600
:data-z: r+1600


Más Ventajas
############

- Reutilizar (no desarrollar de 0)

  - Trae funciones de generación de reportes, exportación a csv y otros
  - Pruebas de Seguridad
  - Validaciones de datos

- Integración
- Independencia (Soberanía)
- Actualización Continua
- Mantenibilidad

----

Seguridad
#########

La seguridad de las computadoras está incluida dentro del ERP, para proteger a la
organización en contra de crímenes externos, tal como el espionaje industrial y
**crimen interno, tal como malversación**.

----

Módulos Adicionales
###################

- `APPS <https://www.odoo.com/apps>`_

  - `Gestión de activos fijos para España <https://apps.openerp.com/apps/modules/8.0/l10n_es_account_asset/>`_

----


Propuesta de valor
##################

El modelo de código abierto de Odoo nos ha permitido aprovechar los
conocimientos de miles de desarrolladores y expertos en el mundo empresarial
para construir cientos de aplicaciones en solo unos años.

Con bases tecnológicas potentes. Ofrece usabilidad de la más alta calidad en
todas las aplicaciones.

Las mejoras en usabilidad realizadas en Odoo se implementarán directamente en
todas nuestras aplicaciones totalmente integradas.

----

De esa manera, Odoo evoluciona mucho más rápido que cualquier otra solución.

- 5400+ desarrolladores
- 312 nuevas aplicaciones al mes
- 23 idiomas
- Fácil de usar y alcance empresarial frente a Oracle, SAP, Microsoft Dynamics,
  NetSuite etc.
- 2 millones de usuarios

----

Expanden su negocio gracias a Odoo
##################################

- `Toyota utiliza Odoo <https://www.odoo.com/blog/customer-reviews-6/post/312>`_

  Con complejas necesidades funcionales en su división de manipulación de
  materiales, descubra cómo Toyota utiliza Odoo para resolver sus desafíos
  operacionales y simplificar sus flujos de trabajo.

- `"Chez Felix" usa Odoo <https://www.odoo.com/blog/customer-reviews-6/post/325>`_

  Una vinoteca implementó Odoo Online hace dos años. Desde el inventario hasta
  el punto de venta, descubra cómo Chez Felix aplicó un enfoque totalmente
  nuevo a su negocio de venta de vinos.

----

Argentina
#########

- `Caso de éxito: Odoo Argentina para editoriales de libros y revistas <http://www.eynes.com.ar/2013/08/13/caso-de-exito-openerp-para-editoriales-libros-revistas/>`_

----

Bolivia
#######

- Pollos Kingdom

  - 9 Sucursales en 2 departamentos

Se esta comercializando odoo con otros nombres. Como Servico en la nuve, entre
otros JalaSoft.

----

Fácil instalación con Docker
############################

- `Repo Docker <https://github.com/odoo/docker>`_


  .. code::

    They depends on postgresql images, usage is pretty simple:

    $ docker run -d -e POSTGRES_USER=odoo -e POSTGRES_PASSWORD=odoo --name db postgres
    $ docker run -p 127.0.0.1:8069:8069 --name odoo --link db:db -t odoo

    We will update the install/deploy documentation to mention them.


  `Instalación <https://www.odoo.com/documentation/8.0/setup/install.html>`_

----

Desarrollo Rápido
#################


.. code:: xml

  <?xml version="1.0" encoding="UTF-8"?>
  <openerp>
    <data>
        <!-- This file should contain only menuitem elements -->
        <!-- Ejemplo: -->
        <menuitem action="action_order_report_all"
                  id="menu_report_product_all"
                  parent="base.next_id_64"
                  sequence="10"/>
    </data>
  </openerp>

----

Módelo
######

.. code:: python

  import logging

  from openerp.osv import orm, fields
  from openerp.tools.translate import _

  _logger = logging.getLogger(__name__)


  class mymodel(orm.Model):

     _name = '{{name}}.mymodel'
     _inherit = "res.company"

     _columns = {
         'res_model': fields.char('Model'),
         'file': fields.binary(i
             'File', help="File to check"),
         'partner_id': fields.many2one(
             'res.partner',
             string="Attached Partner",
             domain="[('type', '=', 'other')]",),
     }

----

Buenas Practicas de Desarrollo
##############################


- `Aplica los principios de la programación funcional <http://97cosas.com/programador/aplica-programacion-funcional.html>`_
- `No te repitas <http://97cosas.com/programador/no-te-repitas.html>`_
- `Cumple tus ambiciones con Software Libre <http://97cosas.com/programador/cumple-ambiciones-con-software-libre.html>`_

----

Fin
###

¡¡¡ Gracias !!!
^^^^^^^^^^^^^^^
