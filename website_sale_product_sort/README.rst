=========================
Website Sale Product Sort
=========================

.. 
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
   !! This file is generated by oca-gen-addon-readme !!
   !! changes will be overwritten.                   !!
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
   !! source digest: sha256:355197e200bbdae78e1136147447c3e381fa62dc793f95fb04a91cc1fffab085
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

.. |badge1| image:: https://img.shields.io/badge/maturity-Production%2FStable-green.png
    :target: https://odoo-community.org/page/development-status
    :alt: Production/Stable
.. |badge2| image:: https://img.shields.io/badge/licence-AGPL--3-blue.png
    :target: http://www.gnu.org/licenses/agpl-3.0-standalone.html
    :alt: License: AGPL-3
.. |badge3| image:: https://img.shields.io/badge/github-OCA%2Fe--commerce-lightgray.png?logo=github
    :target: https://github.com/OCA/e-commerce/tree/15.0/website_sale_product_sort
    :alt: OCA/e-commerce
.. |badge4| image:: https://img.shields.io/badge/weblate-Translate%20me-F47D42.png
    :target: https://translation.odoo-community.org/projects/e-commerce-15-0/e-commerce-15-0-website_sale_product_sort
    :alt: Translate me on Weblate
.. |badge5| image:: https://img.shields.io/badge/runboat-Try%20me-875A7B.png
    :target: https://runboat.odoo-community.org/builds?repo=OCA/e-commerce&target_branch=15.0
    :alt: Try me on Runboat

|badge1| |badge2| |badge3| |badge4| |badge5|

This module allows to set a default sorting criteria for the e-commerce product
list.

It provides the standard criterias, but allows to extend the options via third
modules.

**Table of contents**

.. contents::
   :local:

Configuration
=============

To configure this module, you need to:

#. Go to *Website > Configuration > Settings*
#. Select the website you want to configure.
#. In the *Product* section there's a *Sort Criteria* option that you
   can set as the default one for the website selected.

To extend the module you can override the method providing sorting options like
this:

  .. code-block:: python

    @api.model
    def _get_product_sort_criterias(self):
      res = super()._get_product_sort_criterias()
      return res.append(("default_code asc", _("Reference - A to Z")))

Usage
=====

After you've configured the default website settings:

#. Go to the configured website shop url.
#. The products will be sorted by default by the chosen option.

Known issues / Roadmap
======================

* Could be nice to have a related model to configure the sorting options without
  the need of third modules.

Bug Tracker
===========

Bugs are tracked on `GitHub Issues <https://github.com/OCA/e-commerce/issues>`_.
In case of trouble, please check there if your issue has already been reported.
If you spotted it first, help us to smash it by providing a detailed and welcomed
`feedback <https://github.com/OCA/e-commerce/issues/new?body=module:%20website_sale_product_sort%0Aversion:%2015.0%0A%0A**Steps%20to%20reproduce**%0A-%20...%0A%0A**Current%20behavior**%0A%0A**Expected%20behavior**>`_.

Do not contact contributors directly about support or help with technical issues.

Credits
=======

Authors
~~~~~~~

* Tecnativa

Contributors
~~~~~~~~~~~~

* `Tecnativa <https://www.tecnativa.com>`_:

    * David Vidal
    * Carlos Roca

Maintainers
~~~~~~~~~~~

This module is maintained by the OCA.

.. image:: https://odoo-community.org/logo.png
   :alt: Odoo Community Association
   :target: https://odoo-community.org

OCA, or the Odoo Community Association, is a nonprofit organization whose
mission is to support the collaborative development of Odoo features and
promote its widespread use.

This module is part of the `OCA/e-commerce <https://github.com/OCA/e-commerce/tree/15.0/website_sale_product_sort>`_ project on GitHub.

You are welcome to contribute. To learn how please visit https://odoo-community.org/page/Contribute.
