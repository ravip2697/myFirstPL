# myFirstPL
<Program> --> `Letsgo ` <stmt_list> `phewDone `
<stmt_list> --> `[ ` <stmt> `; '`] `
<stmt> --> <wooho_stmt> | <booho_stmt>  | <assignStmt>
<wooho_stmt> --> `wohoo``( ` <bool_exp> `] ` <stmt> ]
booho_stmt --> `booho` '[` <bool_exp> `]` <stmt>
<assignStmt> --> `id` `= ` <expr>
<expr> --> <leastPrec>   `*` <leastPrec> 
<leastPrec> --> <litPrec> `/` <litPrec>
<litPrec> --> <muchPrec> { (`+` | `-`) <muchPrec> } 
<muchPrec> --> `id` | `microN` | `nanoN` | `picoN` | `{` <expr `}`
                                                               
                                                               
                                                               
                                                               
                                                          
                                                             
