A) Language Grammer:

<Program> --> `Letsgo ` <stmt_list> `phewDone `

<stmt_list> --> `[ ` { <stmt>  } `] `

<stmt> --> <wooho_stmt> | <oneLo_stmt>  | <assignStmt> | <varAssign>

<wooho_stmt> --> `wohoo` `( ` <bool_exp>`)` `[` <stmt> `]`  { `nohoo``[` <stmt> `]` } 

<oneLo_stmt> --> `oneLoo` `(` <bool_exp> `)` { `[` <stmt> `]`}

<assignStmt> --> `id` `= ` <expr>

<expr> --> <leastPrec>   (* | /) <leastPrec> | <leastPrec>

<leastPrec> --> <litPrec> `/ <litPrec> | <litPrec>

<litPrec> --> <muchPrec> { (`+` | `-`) <muchPrec> } | <muchPrec>

<muchPrec> --> `id` | `microN` | `nanoN` | `picoN` | `{` <expr `}`

<bool_exp> --> expr ( < | > | <= | >= | == | != ) <E>

varAssign = varType varName ;

varType = `microN` | `nanoN` | `picoN`

varName --> ^[a-z] [a-zA-Z_]{5,8}

PartC: 

PartD: This grammer is not ambiguous as no rule in this grammer goes to 2 different places.
