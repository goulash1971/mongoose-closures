mongoose-closures - Plugin support for *transactional closures* in Mongoose
=================

### Overview

Mongoose-Closures is an extension for Mongoose that implements a concept of a *transactional closure* using the
Mongoose ORM.  

Although Mongoose (and MongoDB) do not support transactions at a semantic or operational level a *pseudo transaction*
can be managed at the ORM level that allows multiple operations to be performed within a *closure*, around which 
transactional semantics can be applied.

### Installation
	npm install mongoose-closures

### Setup
To install all of the types, plugins, patches and utilities provided by the extension into a Mongoose 
instance:

	var mongoose = require("mongoose");
	   
	// Create a connection to your database
	var db = mongoose.createConnection("mongodb://localhost/sampledb");
	
	// Access the mongoose-closures module and install everything
	var closures = require("mongoose-closures");
	var utils = closures.utils
	
	// Install the types, plugins and monkey patches
	var loaded = closures.install(mongoose);

The `loaded` value returned contains 2 properties:

- `loaded.types` : the join types that were loaded
- `loaded.plugins` : the extension plugins that were loaded

To just install the types provided by the extension (either all types or a list of named types):

	var mongoose = require("mongoose");
   
	// Create a connection to your database
	var db = mongoose.createConnection("mongodb://localhost/sampledb");

	// Access the mongoose-closures module
	var closures = require("mongoose-closures");
	var utils = closures.utils
	
	// Install the plugins
	var loaded = closures.loadTypes(mongoose);

The `loaded` value returned contains the types that were loaded, keyed by the name of each type 
loaded.

To just install the plugins provided by the extension (either all plugins or list of named plugins):

	var mongoose = require("mongoose");
	   
	// Create a connection to your database
	var db = mongoose.createConnection("mongodb://localhost/sampledb");
	
	// Access the mongoose-closures module
	var closures = require("mongoose-closures");
	var utils = closures.utils
	
	// Install the plugins
	var loaded = closures.installPlugins(mongoose);

The `loaded` value returned contains the plugins that were loaded, keyed by the name of each plugin 
loaded.

To just install the patches provided by the extension (either all patches or list of named patches):

	var mongoose = require("mongoose");
	   
	// Create a connection to your database
	var db = mongoose.createConnection("mongodb://localhost/sampledb");
	
	// Access the mongoose-closures module and the utilities
	var closures = require("mongoose-closures");
	var utils = closures.utils;
	
	// Install the monkey patches
	closures.installPatches(mongoose);

### Contributors
- [Stuart Hudson](https://github.com/goulash1971)

### License
MIT License

### Acknowledgements
- [Brian Noguchi](https://github.com/bnoguchi) for the 'mongoose-types' extension that was used as a template for this extension

---
### Author
Stuart Hudson		 
