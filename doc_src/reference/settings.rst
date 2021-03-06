========
Settings
========

ELRTE_DEBUG
===========

**Default:** ``False``

Use the full version of the elrte code instead of the minified version. Makes debugging much easier.

ELRTE_JS_BASE_URL
=================

**Default:** ``MEDIA_URL + 'elrte/js/'``

Where to find the various javascript files for loading. It is assumed that the CSS files will be found at ``../css/``

ELRTE_LOAD_JQUERY
=================

**Default:** ``True``

If you already load jQuery in your templates, you can avoid the additional loading of jQuery by setting this to ``False``\ .

ELRTE_LOAD_JQUERYUI
===================

**Default:** ``True``

If you already load jQuery UI in your templates, you can avoid the additional loading of jQuery UI by setting this to ``False``\ .

ELRTE_ADMIN_FIELDS
==================

**Default:** ``{}``

This allows you to specify the application models and fields that should automatically have elrte applied to them as a text widget. Elrte must load after the application(s) you are applying this to as it subclasses their ``ModelAdmin`` class.

The format is::

	ELRTE_ADMIN_FIELDS = {
	    'app_name.model': ['field_name', 'field_name'],
	    'app_name.model': ['field_name'],
	    'app_name.model': ['field_name', 'field_name'],
	}

For example, to apply elrte to the Flat Pages application::

	ELRTE_ADMIN_FIELDS = {
	    'flatpages.flatpage': ['content']
	}
