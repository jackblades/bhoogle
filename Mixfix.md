


f :: [a] -> Maybe b -> Asum Int String -> Amap Symbol Expr ->
f :many a+ :opt b? (x : int | string) (m : { *(field, ',') })

    - one or more a's
    - optionally b  ( the labels are required for these operations or we couldn't parse it )
    - x parses a number or string at the call site (can't be a variable, must be statically known)


f [ a1 a2 ] Nothing 0 
f many [ a1 a2 ] 0 
f many a1 many a2 0
f many a1 many a2 opt b "hello world"


























