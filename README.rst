===================
kotti_content_proxy
===================

This is an extension to the Kotti CMS that allows you to add *content proxies* to your Kotti site.

A *content proxy* is very similar to a *symbolic link* on UNIX systems.
It allows you to refer to a single content node from multiple places in your content tree without having to duplicate the content itself.
In other words: it will show up in the navigation in multiple places, but still only exist once.

For the moment only the ``view`` view is proxied.
This means when you request the "view" of the ContentProxy object it will return the rendered view of the proxied object instead (respecting its permissions).

For future versions it is planned to also proxy all attribute objects.

`Find out more about Kotti`_

Setup
=====

To activate the kotti_content_proxy add-on in your Kotti site, you need to add an entry to the ``kotti.configurators`` setting in your Paste
Deploy config.
If you don't have a ``kotti.configurators`` option, add one.
The line in your ``[app:main]`` section could then look like this::

  kotti.configurators = kotti_content_proxy.kotti_configure

With this, you'll be able to add content proxy items in your site.


.. _Find out more about Kotti: http://pypi.python.org/pypi/Kotti
