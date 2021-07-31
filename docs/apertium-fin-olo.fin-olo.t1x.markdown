
# apertium-olo-fin: Finnish–Karelian rules for rule-based machine translation

This is a visualisation of some rules in apertium transfer.


## Categories (parts of chunks)
   
These are the categories Apertium is using in order to chunk, re-order and
transfer lexemes.
    
| Category | Items |
|:---------|:------|
| pron |  `<prn.*>`  |
| cond |  `<vblex.*.cond.*>`  |
| conneg |  `<vblex.*.conneg.*>`  |
| adv |  `<adv.*>`  |
| nom |  `<n.*>`  |
| verb |  `<vblex.*>`  `<vaux.*>`  |
| sent |  `<sent>`  |
| kanssa | kanssa `<post>`  |
| qst |  `<qst>`  |
| inf |  `<vblex.*.infa.*>`  `<vblex.*.infe.*>`  `<vblex.*.infma.*>`  |
| default |  `<*>`  |

    
## Attributes

These are the morphological analysis value (tag) sets that can be processed in
the transfer.

| Attribute set name | Tags |
|:-------------------|:-----|
| a_act | `<act>`  |
| a_verb | `<vblex>` `<vaux>`  |
| a_actv | `<actv>` `<pass>`  |
| a_cond | `<cond>` `<cond.prt>` `<cond.prs>`  |
| a_temps | `<prs>` `<prt>`  |
| a_nom | `<n>`  |
| a_cas | `<nom>` `<acc>` `<ill>` `<ine>` `<par>` `<ess>` `<gen>` `<loc>` `<com>` `<abe>` `<lat>`  |
| a_infa | `<infa>` `<infe>` `<infma>` `<inf>`  |
| a_pers | `<p1>` `<p2>` `<p3>`  |
| a_nbr | `<sg>` `<pl>`  |
| a_adpos | `<pr>` `<po>`  |
| a_person | `<sg1>` `<du1>` `<pl1>` `<sg2>` `<du2>` `<pl2>` `<sg3>` `<du3>` `<pl3>`  |
| a_prn | `<prn>` `<prn.rel>` `<prn.res>` `<prn.ind>` `<prn.dem>` `<prn.pers>` `<prn>` `<prn.itg>` `<prn.ref>`  |
| a_poss | `<pxsg1>` `<pxsg2>` `<pxsg3>` `<pxdu1>` `<pxdu2>` `<pxdu3>` `<pxpl1>` `<pxpl2>` `<pxpl3>`  |
| a_trans | `<iv>` `<tv>`  |
| a_tense | `<pri>` `<past>` `<ind.prs>` `<ind.prt>`  |
| a_deriv | `<der_dimin.n>` `<der_at>` `<der_goahti>` `<der_l>` `<der_ahtti>` `<der_vuohta>` `<der_d>` `<der_lágan>` `<der_nammasaš>` `<der_saš>` `<der_laš>`  |
| a_sem | `<sem_act>` `<sem_act_plc>` `<sem_amount>` `<sem_amount_semcon>` `<sem_ani>` `<sem_ani_body-abstr_hum>` `<sem_ani_build_hum_txt>` `<sem_ani_build-part>` `<sem_ani_group>` `<sem_ani_group_hum>` `<sem_ani_hum>` `<sem_aniprod>` `<sem_aniprod_hum>` `<sem_aniprod_obj-clo>` `<sem_aniprod_perc-phys>` `<sem_aniprod_plc>` `<sem_ani_veh>` `<sem_body>` `<sem_body-abstr>` `<sem_body-abstr_prod-audio_semcon>` `<sem_body_clth>` `<sem_body_food>` `<sem_body_group_hum>` `<sem_body_hum>` `<sem_body_mat>` `<sem_body_measr>` `<sem_body_plc>` `<sem_body_time>` `<sem_build>` `<sem_build_edu_org>` `<sem_build_org>` `<sem_build-part>` `<sem_cat>` `<sem_clth>` `<sem_clth-jewl>` `<sem_clth-jewl_curr>` `<sem_clth-jewl_org>` `<sem_clth-part>` `<sem_ctain>` `<sem_ctain-abstr>` `<sem_ctain-clth>` `<sem_ctain-clth_veh>` `<sem_ctain_furn>` `<sem_ctain_tool>` `<sem_curr>` `<sem_dance>` `<sem_domain>` `<sem_drink>` `<sem_dummytag>` `<sem_edu>` `<sem_edu_mat>` `<sem_edu_org>` `<sem_event>` `<sem_event_food>` `<sem_event_hum>` `<sem_event_plc>` `<sem_feat>` `<sem_feat-measr>` `<sem_feat-measr_plc>` `<sem_feat-phys>` `<sem_feat-phys_tool-write>` `<sem_feat-phys_veh>` `<sem_feat-phys_wthr>` `<sem_feat_plant>` `<sem_feat-psych>` `<sem_food>` `<sem_food-med>` `<sem_food_plant>` `<sem_furn>` `<sem_game_obj-play>` `<sem_geom>` `<sem_group>` `<sem_group_hum>` `<sem_group_hum_plc>` `<sem_hum>` `<sem_hum_lang>` `<sem_hum_lang_plc>` `<sem_hum_obj>` `<sem_hum_org>` `<sem_hum_tool>` `<sem_hum_veh>` `<sem_ideol>` `<sem_lang>` `<sem_lang_tool>` `<sem_mat>` `<sem_mat_plant>` `<sem_mat_txt>` `<sem_measr>` `<sem_measr_time>` `<sem_money>` `<sem_money_obj>` `<sem_money_txt>` `<sem_obj>` `<sem_obj-clo>` `<sem_obj-el>` `<sem_obj-ling>` `<sem_obj-play>` `<sem_obj-rope>` `<sem_obj_semcon>` `<sem_obj_state>` `<sem_obj-surfc>` `<sem_org>` `<sem_org_rule>` `<sem_org_txt>` `<sem_part>` `<sem_part_prod-cogn>` `<sem_perc-emo>` `<sem_perc-phys>` `<sem_plant>` `<sem_plant-part>` `<sem_plant_plant-part>` `<sem_plc>` `<sem_plc-abstr>` `<sem_plc-abstr_rel_state>` `<sem_plc-abstr_route>` `<sem_plc-elevate>` `<sem_plc-line>` `<sem_plc_pos>` `<sem_plc_route>` `<sem_plc_substnc>` `<sem_plc_substnc_wthr>` `<sem_plc_time>` `<sem_plc_tool-catch>` `<sem_plc-water>` `<sem_plc_wthr>` `<sem_pos>` `<sem_process>` `<sem_prod>` `<sem_prod-audio>` `<sem_prod-audio_txt>` `<sem_prod-cogn>` `<sem_prod-cogn_txt>` `<sem_prod-ling>` `<sem_prod-vis>` `<sem_rel>` `<sem_route>` `<sem_rule>` `<sem_semcon>` `<sem_semcon_txt>` `<sem_sign>` `<sem_state>` `<sem_state-sick>` `<sem_substnc>` `<sem_substnc_wthr>` `<sem_sur>` `<sem_time>` `<sem_time_wthr>` `<sem_tool>` `<sem_tool-catch>` `<sem_tool-clean>` `<sem_tool-it>` `<sem_tool-measr>` `<sem_tool-music>` `<sem_tool-write>` `<sem_txt>` `<sem_veh>` `<sem_wpn>` `<sem_wthr>`  |
| a_func | `<@→A>` `<@A←>` `<@←ADVL>` `<@→ADVL>` `<@ADVL>` `<@ADVL←>` `<@ADVL→>` `<@ADVL→CS>` `<@ADVL←OBJ>` `<@ADVL→SUBJ>` `<@APP>` `<@APP-ADVL←>` `<@APP-N←>` `<@APP-Num←>` `<@APP-Pron←>` `<@APP→Pron>` `<@→CC>` `<@CNP>` `<@COMP-CS←>` `<@CVP>` `<@-F←ADVL>` `<@-FADVL>` `<@-FADVL→>` `<@-FAUXV>` `<@\+FAUXV>` `<@-FMAINV>` `<@\+FMAINV>` `<@-F←OBJ>` `<@-FOBJ>` `<@-FOBJ→>` `<@-F←OPRED>` `<@-FOPRED→>` `<@-F←SPRED>` `<@-FSPRED→>` `<@-FSUBJ→>` `<@HAB>` `<←hab→>` `<@HNOUN>` `<@INTERJ>` `<@→N>` `<@N>` `<@N←>` `<@→Num;>` `<@→Num>` `<@Num←>` `<@←OBJ>` `<@OBJ>` `<@OBJ→>` `<@OBJ→SPRED>` `<@-OPRED→>` `<@←OPRED>` `<@OPRED>` `<@OPRED→>` `<@→P>` `<@P←>` `<@PCLE>` `<@←PPRED>` `<@PPRED>` `<@→Pron>` `<@Pron←>` `<@-SPRED→>` `<@←SPRED>` `<@SPRED>` `<@SPRED→>` `<@SPRED←OBJ>` `<@←SUBJ>` `<@SUBJ>` `<@SUBJ→>` `<@SUBJ←ADVL>` `<@SUBJ←OBJ>` `<@VOC>` `<@X>`  |
| x_func | `<←ext→>` `<←hab→>`  |

    
## Macros

Macros are helper functions in apertium transfer files.



### remove-semtag1

Parametres: 1

1. **let** `tl[1]['a_sem']`  ≔ ""

### tensemood-mangler

Parametres: 1


1. **if** `sl[1]['a_tense']`  ≟ `<past>` **then**:
  1. **let** `tl[1]['a_tense']`  ≔ `<ind.prt>`
1. **elseif** `sl[1]['a_tense']`  ≟ `<pri>` **then**:
  1. **let** `tl[1]['a_tense']`  ≔ `<ind.prs>`

## Rules
    
The actual rules concerning stuff.



### REGLA: COND
    
#### Matching pattern:
    

1. cond

#### Action:
    
1. **let** `tl[1]['a_sem']`  ≔ ""1. **let** `tl[1]['x_func']`  ≔ ""1. **let** `tl[1]['a_func']`  ≔ ""1. **let** `tl[1]['a_cond']`  ≔ `<cond.prs>`
1. Output: 
  1. cond``sl[1]['a_func']` `
    1. `tl[1]['whole']` 
    

### REGLA: COND QST
    
#### Matching pattern:
    

1. cond
1. qst

#### Action:
    
1. **let** `tl[1]['a_sem']`  ≔ ""1. **let** `tl[1]['x_func']`  ≔ ""1. **let** `tl[1]['a_func']`  ≔ ""1. **let** `tl[1]['a_cond']`  ≔ `<cond.prs>`
1. Output: 
  1. cond``sl[1]['a_func']` `
    

### REGLA: CONNEG
    
#### Matching pattern:
    

1. conneg

#### Action:
    
1. **let** `tl[1]['a_sem']`  ≔ ""1. **let** `tl[1]['x_func']`  ≔ ""1. **let** `tl[1]['a_func']`  ≔ ""
1. **if** `tl[1]['a_nbr']`  ≟ `<pl>` **then**:
  1. **let** `tl[1]['a_nbr']`  ≔ ""1. **let** `tl[1]['tags']`  ≔ `tl[1]['tags']` `<p3.pl>`
1. **if** `tl[1]['a_temps']`  ≟ `<prs>` **then**:
  1. **let** `tl[1]['a_temps']`  ≔ ""
1. Output: 
  1. conneg``sl[1]['a_func']` `
    1. `tl[1]['whole']` 
    

### REGLA: pron
    
#### Matching pattern:
    

1. pron

#### Action:
    

1. remove-semtag1($1)1. **let** `tl[1]['x_func']`  ≔ ""1. **let** `tl[1]['a_func']`  ≔ ""1. **let** `tl[1]['a_poss']`  ≔ ""
1. **if** `tl[1]['a_cas']`  ≟ `<acc>` **then**:
  1. **let** `tl[1]['a_cas']`  ≔ `<par>`
1. Output: 
  1. pron``<SN>``
    1. `tl[1]['whole']` 
    

### REGLA: nom
    
#### Matching pattern:
    

1. nom

#### Action:
    

1. remove-semtag1($1)1. **let** `tl[1]['x_func']`  ≔ ""1. **let** `tl[1]['a_func']`  ≔ ""1. **let** `tl[1]['a_poss']`  ≔ ""
1. Output: 
  1. nom``<SN>``
    1. `tl[1]['whole']` 
    

### REGLA: nom kaa
    
#### Matching pattern:
    

1. nom
1. kanssa

#### Action:
    

1. remove-semtag1($1)1. **let** `tl[1]['x_func']`  ≔ ""1. **let** `tl[1]['a_func']`  ≔ ""1. **let** `tl[1]['a_poss']`  ≔ ""1. **let** `tl[1]['a_cas']`  ≔ `<com>`
1. Output: 
  1. nom``<SN>``
    1. `tl[1]['whole']` 
    

### REGLA: inf verb
    
#### Matching pattern:
    

1. inf

#### Action:
    

1. remove-semtag1($1)1. **let** `tl[1]['x_func']`  ≔ ""1. **let** `tl[1]['a_func']`  ≔ ""1. **let** `tl[1]['a_actv']`  ≔ ""1. **let** `tl[1]['a_infa']`  ≔ `<inf>`1. **let** `tl[1]['a_cas']`  ≔ ""1. **let** `tl[1]['a_nbr']`  ≔ ""
1. Output: 
  1. v``<SV>``
    1. `tl[1]['whole']` 
    

### REGLA: verb qst
    
#### Matching pattern:
    

1. verb
1. qst

#### Action:
    

1. remove-semtag1($1)1. **let** `tl[1]['x_func']`  ≔ ""1. **let** `tl[1]['a_func']`  ≔ ""1. **let** `tl[1]['a_act']`  ≔ ""
1. Output: 
  1. v``<SV>``
    

### REGLA: verb
    
#### Matching pattern:
    

1. verb

#### Action:
    

1. remove-semtag1($1)
1. tensemood-mangler($1)1. **let** `tl[1]['x_func']`  ≔ ""1. **let** `tl[1]['a_func']`  ≔ ""1. **let** `tl[1]['a_act']`  ≔ ""
1. Output: 
  1. v``<SV>``
    1. `tl[1]['lem']` `tl[1]['a_verb']` `tl[1]['a_actv']` `tl[1]['a_tense']` `tl[1]['a_pers']` `tl[1]['a_nbr']` 
    

### REGLA: ADV
    
#### Matching pattern:
    

1. adv

#### Action:
    
1. **let** `tl[1]['a_sem']`  ≔ ""1. **let** `tl[1]['x_func']`  ≔ ""1. **let** `tl[1]['a_func']`  ≔ ""1. **let** `tl[1]['a_poss']`  ≔ ""
1. Output: 
  1. default``sl[1]['a_func']` `
    1. `tl[1]['whole']` 
    

### REGLA: DEFAULT
    
#### Matching pattern:
    

1. default

#### Action:
    
1. **let** `tl[1]['a_sem']`  ≔ ""1. **let** `tl[1]['x_func']`  ≔ ""1. **let** `tl[1]['a_func']`  ≔ ""
1. Output: 
  1. default``sl[1]['a_func']` `
    1. `tl[1]['whole']` 
    

### REGLA: DEFAULT QST
    
#### Matching pattern:
    

1. default
1. qst

#### Action:
    
1. **let** `tl[1]['a_sem']`  ≔ ""1. **let** `tl[1]['x_func']`  ≔ ""1. **let** `tl[1]['a_func']`  ≔ ""
1. Output: 
  1. default``sl[1]['a_func']` `
    

- - -

Documentation for [apertium-olo-fin](//github.com/apertium/apertium-olo-fin/).
Generated with [Flammie’s apevis-xslt](https://github.com/flammie/apevis-xslt).
  