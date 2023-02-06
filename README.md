# syntax-tree-of-micro_compiler-using-python
syntax tree of micro_compiler using python with her presentation interface including Constant and variable declaration.  and If-then-else condition.
_______________________________________________


this project consists of two parts:

1.building the syntax-tree

   a.the syntax-tree of Constant and variable declaration.
   
   Input:
   
         exemple="ab=x+y-55*7*6/77/66-99"
         
   Output:
   
         [['='], ['ab'], [['+'], ['=x'], [['-'], ['y'], [['-'], [['/'], [['*'], ['55'], [['*'], ['7'], ['6']]], [['/'], ['77'], ['66']]], ['99']]]]]
         
   b.the syntax-tree If-then-else condition.
   
   Input:
   
         exemple="""
         if (x>a+6) then {
            if (x>a+6) then {
                x=v+7;
            }
            else {
                if (x>a+6) then {
                     x=v+72;
                }
                else {
                    x=v+73;
                }  
            } 
        } 
        else {
             if (x>a+6) then {
                x=v+74;
             }
             else {
                 x=v+75;
             } 
        }
        """
   Output:
   
          ['if', [['>'], ['x'], [['+'], ['a'], ['6']]], 'then', '{', ['if', [['>'], ['x'], [['+'], ['a'], ['6']]], 'then', '{', [[['='], ['x'], [['+'], ['v'], ['7']]]], '}', 'else', '{', ['if', [['>'], ['x'], [['+'], ['a'], ['6']]], 'then', '{', [[['='], ['x'], [['+'], ['v'], ['72']]]], '}', 'else', '{', [[['='], ['x'], [['+'], ['v'], ['73']]]], '}'], '}'], '}', 'else', '{', ['if', [['>'], ['x'], [['+'], ['a'], ['6']]], 'then', '{', [[['='], ['x'], [['+'], ['v'], ['74']]]], '}', 'else', '{', [[['='], ['x'], [['+'], ['v'], ['75']]]], '}'], '}'] 
          
2.the presentation interface

  a.interface of Constant and variable declaration.
  
  Input:
  
       arbre=[['='], ['x'], [['/'], [['*'], ['5'], [['*'], ['6'], [['*'], ['44'], ['5']]]], ['32']]]
       
       (this input is the output of the syntax-tree of Constant and variable declaration)
       
  Output:
  
  <img width="371" alt="Capture d'écran_20230206_225923" src="https://user-images.githubusercontent.com/96086924/217101987-22e09c16-1b80-4907-828b-71d7233d4ca1.png">


         
  b.interface of If-then-else condition.
  
  Input:
  
       arbre=['if', [['>'], ['x'], [['+'], ['a'], ['6']]], 'then', '{', [[['='], ['x'], [['+'], ['v'], ['7']]]], '}', 'else', '{', [[['='], ['v'], ['66']]], '}']
       (this input is the output of the syntax-tree of If-then-else condition)
       
       
       
  Output:
  
  
  <img width="430" alt="Capture d'écran_20230206_232354" src="https://user-images.githubusercontent.com/96086924/217101866-5b3a9978-c6fc-4e46-b879-67931ca44fec.png">

