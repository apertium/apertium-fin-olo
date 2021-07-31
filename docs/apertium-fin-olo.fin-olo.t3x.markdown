
# apertium-olo-fin: Finnish–Karelian rules for rule-based machine translation

This is a visualisation of some rules in apertium transfer.


## Categories (parts of chunks)
   
These are the categories Apertium is using in order to chunk, re-order and
transfer lexemes.
    
| Category | Items |
|:---------|:------|
| sent |  `<>`  |

    
## Attributes

These are the morphological analysis value (tag) sets that can be processed in
the transfer.

| Attribute set name | Tags |
|:-------------------|:-----|
| nbr | `<sg>` `<pl>` `<sp>` `<ND>`  |


## Rules
    
The actual rules concerning stuff.



### CHUNK:
    
#### Matching pattern:
    

1. sent

#### Action:
    

1. Output: 
  1. `[1]['whole']` 
    

- - -

Documentation for [apertium-olo-fin](//github.com/apertium/apertium-olo-fin/).
Generated with [Flammie’s apevis-xslt](https://github.com/flammie/apevis-xslt).
  