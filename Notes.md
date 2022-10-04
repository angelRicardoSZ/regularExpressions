reference
https://learn.microsoft.com/en-us/dotnet/standard/base-types/regular-expression-language-quick-reference


expression  --  usage

-----------------------------------------------------------------------------------------------

'*'         --  Matches the previous element zero or more times  
            
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
'+'        Matches the previous element one or more times.
           
           example:            
            
           regex = 0+c   -- search the character '0' before c, 1 or more times
           
           test_text = qwe123c456rty  
           pattern selected = does not match the subject string.
           
           test_text = qwe1230c456rty  
           pattern selected =0c
           
           
-----------------------------------------------------------------------------------------------
'?'         Matches the previous element zero or one time.

            example:      
            
            regex = 0?c   -- search the character '0' before c, 0 or one time
            
            test_text = qwe123c456rty  
            pattern selected = c
            
            test_text = qwe1230c456rty  
            pattern selected = 0c
            
            test_text = qwe123000000c456rty  
            pattern selected = 0c
            
            
-----------------------------------------------------------------------------------------------
'.'         Wildcard: Matches any single character except \n 

            example:      
            
            regex = a.e   -- any character except newline between a and e
            
            test_text = ae
            pattern selected = the regular expression does not match the subject string.
            
            test_text = ade
            pattern selected = ade
            
            test_text = acce
            pattern selected = the regular expression does not match the subject string.
            
            
            regex = ab.cd
            
            test_text = ab1cd
            pattern selected = ab1cd
            
            test_text = ab1cd
            pattern selected = ab1cd
            
            test_text = ab44cd
            pattern selected = ab44cd
            
            
            regex = a.*e
            
            test_text = ae
            pattern selected = ae
            
            test_text = a1#$()58e
            pattern selected = a1#$()58e
            


-----------------------------------------------------------------------------------------------
            
'{ n }'      Matches the previous element exactly n times
            
             regex = ",\d{3}"
            
             pattern = ",043" in "1,043.6", ",876", ",543", and ",210" in "9,876,543,210"
            
 '{ n , m } ' Matches the previous element at least n times, but no more than m times. 
 
            regex = \d{3,5}
            
            test_text = 193024
            pattern selected = "166", "17668", "19302"
            
 -----------------------------------------------------------------------------------------------
 
 '*?'       Matches the previous element zero or more times, but as few times as possible.
 
            regex = a.*?c
            
            test_text = abcbc
            pattern selected = abc
            
            test_text = abcabcabc
            pattern selected = abc, abc, abc
            
    -----------------------------------------------------------------------------------------------
    '+?'    Matches the previous element one or more times, but as few times as possible.
            regex = be+?
            
            test_text = been
            pattern selected = be
            
            
     -----------------------------------------------------------------------------------------------
     Problema: define a pattern that matches all lines except the last one, the one with letters
     555658
     56-58-11
     56.58.11
     56.78-98
     65 09 87
     76y87r98
     '(\d{2}\W?){3}'  -- search the pattern "digit digit nonword" three times           
     
     
     -----------------------------------------------------------------------------------------------
     
     
     
            
            
            
            
  
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
           
           
        
           
           
           
            
            
            
            
            
            
            
            
            
            

            
            
