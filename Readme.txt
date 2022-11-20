A & B) Language Grammer:

<Program> --> `Letsgo ` `[` { <stmt> `;` } `]` `phewDone `

<stmt> --> <wooho_stmt> | <oneLo_stmt>  | <assignStmt> | <varAssign>

<wooho_stmt> --> `wohoo` `( ` <bool_exp>`)` `[` <stmt> `]`  { `nohoo``[` <stmt> `]` } 

<oneLo_stmt> --> `oneLoo` `(` <bool_exp> `)` { `[` <stmt> `]`}

<assignStmt> --> `id` `= ` <expr>

<expr> --> <leastPrec>   `*` <leastPrec> | <leastPrec>

<LeastPrec> --> <LitPrec> `/` <litPrec> | <litPrec>

<litPrec> --> <muchPrec> { (`+` | `-`) <muchPrec> } | <muchPrec>

<muchPrec> --> `id` | `microN` | `nanoN` | `picoN` | `{` <expr `}`

<bool_exp> --> <expr> ( < | > | <= | >= | == | != ) <expr>

varAssign = varType varName ;

varType = `microN` | `nanoN` | `picoN`

varName --> ^[a-z] [a-zA-Z_]{5,8}

PartB:

variable types are only 3 which are microN, nanoN and picoN
wooho_stmt is basically a if/else statement
oneLo_stmt is basically a while loop

PartC: it is llgrammer as the grammer stated above is starting from top 
        the program to the bottom(or left to right)

PartD: This grammer is not ambiguous as no rule in this grammer goes to 2 different places.

Part G: The four files with the code are
        correct Code: PrChecker, corSy2
        Syntax Error: errSyn
        Lexical Error: errLex

Parth: Correct Code examples: LRCorrectCode1 and LRCorrectCode2
Incorrect Code examples:        LRWrCode1: if doesnt exist in the grammer
                                LRWrCode2: += doent exist in the grammer
