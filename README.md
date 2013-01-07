# Klarna PHP API (mirror)

This is a (very slightly altered) mirror of Klarna's PHP API. Feel free to use it as you wish.

# Very slight alterations

We've done a couple of (very slight) alterations. First off, we're not distributing the "examples" directory, because the license isn't explicitly defined.

We're also including a composer.json file. There are however a major caveat. The required XML-RPC library is not part of the autoloading definition. Klarna's code requires both ```xmlrpc.inc``` and ```xmlrpc_wrappers.inc``` to be loaded. Both these files pollutes the global namespace with a *lot* of variables, and the latter doesn't define any class, just functions.

Because of this (and the fact that we're just a mirror) we won't be submitting this repository to Packagist, so if you want to install it through Composer, you'll need to add this as an inline repository (or to an internal Satis server).