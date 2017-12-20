# NBT Docs

This repo is basically JSON Schema but for NBT. the format is as following  

Node:  

```
type: STRING. An NBT tag type or `root`.
ref: STRING. A URI to another file. in the form of *file path*#*node path in file*. The `#` and anything after is optional  
child_ref: LIST. A List of refrences to add to the child if `type` is "compound"  
    *: STRING. A URI like *ref*  
children: OBJECT. The sub nodes in `type` is "compound"  
    **a node**: OBJECT. A child node. See *Node*  
item: OBJECT. The object type if `type` is "list". See *Node*  
use-context: BOOLEAN. If the parser should use context to see what ref to use next.
context: OBJECT. A object containing references to pass to the context manager
	entity_id: STRING. A ref to the string that specifies what entity to use
```
