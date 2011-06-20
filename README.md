mongoose-closures - Plugin support for *transactional closures* in Mongoose
=================

### Overview

Mongoose-Closures is an extension for Mongoose that implements a concept of a *transactional closure* using the
Mongoose ORM.  

Although Mongoose (and MongoDB) do not support transactions at a semantic or operational level a *pseudo transaction*
can be managed at the ORM level that allows multiple operations to be performed within a *closure*, around which 
transactional semantics can be applied.

### Contributors
- [Stuart Hudson](https://github.com/goulash1971)

### License
MIT License

### Acknowledgements
- [Brian Noguchi](https://github.com/bnoguchi) for the 'mongoose-types' extension that was used as a template for this extension

---
### Author
Stuart Hudson		 
