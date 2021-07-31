
# apertium-olo-fin: Finnish–Karelian rules for rule-based machine translation

This is a visualisation of some rules in apertium transfer.


## Categories (parts of chunks)
   
These are the categories Apertium is using in order to chunk, re-order and
transfer lexemes.
    
| Category | Items |
|:---------|:------|
| SN |  `<SN>`  `<SN.*>`  |
| PR_PO | pr_po `<*>`  |
| SENT |  `<SENT>`  |

    
## Attributes

These are the morphological analysis value (tag) sets that can be processed in
the transfer.

| Attribute set name | Tags |
|:-------------------|:-----|
| a_nbr | `<sg>` `<pl>` `<sp>` `<ND>`  |
| a_cas | `<nom>` `<acc>` `<ill>` `<par>` `<ess>` `<gen>` `<loc>` `<com>` `<abe>`  |

    
## Macros

Macros are helper functions in apertium transfer files.



### test1

Parametres: 1

1. **let** `$POST` ≔ ""

## Rules
    
The actual rules concerning stuff.



### REGLA: SN
    
#### Matching pattern:
    

1. SN

#### Action:
    

1. Output: 
  1. ``
    

### REGLA: SN
    
#### Matching pattern:
    

1. PR_PO
1. SN

#### Action:
    

1. Output: 
  1. ``
    1. `blank`1
    1. ``
    

- - -

Documentation for [apertium-olo-fin](//github.com/apertium/apertium-olo-fin/).
Generated with [Flammie’s apevis-xslt](https://github.com/flammie/apevis-xslt).
  