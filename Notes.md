reference
https://learn.microsoft.com/en-us/dotnet/standard/base-types/regular-expression-language-quick-reference


expression  --  usage

-----------------------------------------------------------------------------------------------

*           --  Matches the previous element zero or more times  
            
            example:
            
            
            regex = 0*c   -- search the character '0' before c, zero or more times
            
            test_text = qwe123c456rty
            pattern selected = c
            
            test_text = qwe1230c456rty
            pattern selected = 0c
            
            test_text = qwe1230200c456rty
            pattern selected = 00c
            
            test_text = qwe12302000c456rty
            pattern selected = 000c
            
            
            
            regex = 10*c5   -- search the character '0' between c5 and 1, zero or more times         
            
            test_text = 1a1c56
            pattern selected = 1c5
            
            test_text = 1a0c56
            pattern selected = none
            
            test_text = 1a10c56
            pattern selected = 10c5
            
            test_text = 1a100000c56
            pattern selected = 100000c5
            
            regex = 1230*c456 -- search the character '0' between '123' and 'c456', zero or more times
                        
            test_text = abc123c456def
            pattern selected = 123c456
            
            test_text = abc1230c456def
            pattern selected = 1230c456
            
            test_text = abc12300c456def
            pattern selected = 12300c456
            
            
-----------------------------------------------------------------------------------------------
+          Matches the previous element one or more times.
           
           example:            
            
           regex = 0+c   -- search the character '0' before c, 1 or more times
           
           test_text = qwe123c456rty  
           pattern selected = does not match the subject string.
           
           test_text = qwe1230c456rty  
           pattern selected =0c
           
           
           
           
            
            
            
            
            
            
            
            
            
            

            
            
