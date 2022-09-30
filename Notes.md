reference
https://learn.microsoft.com/en-us/dotnet/standard/base-types/regular-expression-language-quick-reference


expression  --  usage

*           --  Matches the previous element zero or more times  
            
            example:
            
            regex = 0*c
            input = 454dsfsdfc4564
            selected = c
            
            regex = 0*c
            input = 454dsfsdf0c4564
            selected = 0c
            
            regex = 0*c
            input = 454dsfsdf0c4564
            selected = 0c
            
            regex = l0*c
            input = 454dsfsdfl0c4564
            selected = l0c
            
