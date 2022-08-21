# Array_Methods
Notes on different Array Methods


1) Join--> The join() method returns an array as a string.
          The join() method does not change the original array.
          Any separator can be specified. The default is comma (,).

Eg: const fruits = ["Banana", "Orange", "Apple", "Mango"];
    let text = fruits.join(" and ");
    text= 'Banana and Orange and Apple and Mango'

-------------------------------------------------------------------------------
2) flat---> The flat() method creates a new array with all sub-array elements concatenated into it recursively up to the specified depth.

    EG: const arr1 = [0, 1, 2, [3, 4]];
        console.log(arr1.flat());
        output: [0, 1, 2, 3, 4]
---------------------------------------------------------------------------------------------------------

3) Push--> The push() method adds new items to the end of an array.
            The push() method changes the length of the array.
            The push() method returns the new length.
   
   EG:    const fruits = ["Banana", "Orange", "Apple", "Mango"];
          fruits.push("Kiwi", "Lemon");
        
          -->Banana,Orange,Apple,Mango,Kiwi,Lemon
 -----------------------------------------------------------------------------
 
 4) indexOf- The indexOf() method returns the position of the first occurrence of a value in a string.
            The indexOf() method returns -1 if the value is not found.
             The indexOf() method is case sensitive.
             
   EG: let text = "Hello world, welcome to the universe.";
        let result = text.indexOf("Welcome");
        output: -1
 -----------------------------------------------------------------------
 
 5) lastIndexOf-  The lastIndexOf() method returns the index (position) of the last occurrence of a specified value in a string.
            The lastIndexOf() method searches the string from the end to the beginning.
          The lastIndexOf() method returns the index from the beginning (position 0).
          The lastIndexOf() method returns -1 if the value is not found.
          The lastIndexOf() method is case sensitive.
          
         EG: let text = "Hello planet earth, you are a great planet.";
            let result = text.lastIndexOf("planet");
            
            result: 36
            
 --------------------------------------------------------------------------------------
 
 6) includes-> The includes() method returns true if a string contains a specified string.
                Otherwise it returns false.
                The includes() method is case sensitive.
                
           EG: let text = "Hello world, welcome to the universe.";
            let result = text.includes("world");
            output: true
 ------------------------------------------------------------------------------
 
 7) reverse--> The reverse() method reverses the order of the elements in an array. 
    The reverse() method overwrites the original array.
    
      EG:  const fruits = ["Banana", "Orange", "Apple", "Mango"];
        fruits.reverse();
        
        output: Mango,Apple,Orange,Banana
  -------------------------------------------------------------     
  
 8) every-->  The every() method executes a function for each array element.
              The every() method returns true if the function returns true for all elements.
              The every() method returns false if the function returns false for one element.
              The every() method does not execute the function for empty elements.
              The every() method does not change the original array
              
       EG: 
       const ages = [32, 33, 16, 40];
            function checkAge(age) {
            return age > 18;
            }
       output: false
       
----------------------------------------------------------------------------------------

9) shift--->  The shift() method removes the first item of an array.
              The shift() method changes the original array.
              The shift() method returns the shifted element. 
        EG:  const fruits = ["Banana", "Orange", "Apple", "Mango"];
              fruits.shift();
              
              output: Orange,Apple,Mango
              
------------------------------------------------------------------------------------------------------

10) splice--> The splice() method adds and/or removes array elements.
               The splice() method overwrites the original array.
               
       EG: const fruits = ["Banana", "Orange", "Apple", "Mango", "Kiwi"];
          fruits.splice(2, 2);
  
          output: Banana,Orange,Kiwi
          
-------------------------------------------------------------------------------------------------------

11)  find-->  The find() method returns the value of the first element that passes a test.
              The find() method executes a function for each array element.
              The find() method returns undefined if no elements are found.
              The find() method does not execute the function for empty elements.
              The find() method does not change the original array.
              
           EG:  const ages = [3, 10, 18, 20];
           function checkAge(age) {
              return age > 18;
              }
            output: 20
 ----------------------------------------------------------------------------------------
 
 12) unshift-->   The unshift() method adds new elements to the beginning of an array.
                  The unshift() method overwrites the original array.
 
                   EG: const fruits = ["Banana", "Orange", "Apple", "Mango"];
                                    fruits.unshift("Lemon","Pineapple");
                                    output: Lemon,Pineapple,Banana,Orange,Apple,Mango
  --------------------------------------------------------------------------------------------------
  
  13) findIndex-->  The findIndex() method executes a function for each array element.
                    The findIndex() method returns the index (position) of the first element that passes a test.
                    The findIndex() method returns -1 if no match is found.
                    The findIndex() method does not execute the function for empty array elements.
                    The findIndex() method does not change the original array.
                    
                    EG: const ages = [3, 10, 18, 20];
                      ages.findIndex(checkAge);

                      function checkAge(age) {
                        return age > 18;
                      }
                      
                      output: 3
 ------------------------------------------------------------------------------------
 
 14) filter--> The filter() method creates a new array filled with elements that pass a test provided by a function.
              The filter() method does not execute the function for empty elements.
              The filter() method does not change the original array. 
 EG:
       const ages = [32, 33, 16, 40];
      const result = ages.filter(checkAdult);

      function checkAdult(age) {
        return age >= 18;
      }
             
 -------------------------------------------------------------
 15) forEach---> The forEach() method calls a function for each element in an array.
                  The forEach() method is not executed for empty elements.
                  
           EG:  const fruits = ["apple", "orange", "cherry"];
                fruits.forEach(myFunction);
                
                output: 0: apple
                        1: orange
                        2: cherry
                        
-------------------------------------------------------------------------------

16) map--> map() creates a new array from calling a function for every array element.
          map() calls a function once for each element in an array.
          map() does not execute the function for empty elements.
          map() does not change the original array.
          
          EG: const numbers = [65, 44, 12, 4];
          const newArr = numbers.map(myFunction)

          function myFunction(num) {
            return num * 10;
          }
          
          output: 650,440,120,40
          
 ----------------------------------------------------------------------------------
 
 17) pop--> The pop() method removes (pops) the last element of an array.
            The pop() method changes the original array.
            The pop() method returns the removed element.
            
         EG: const fruits = ["Banana", "Orange", "Apple", "Mango"];
              fruits.pop();
              output: Banana,Orange,Apple
 ----------------------------------------------------------------
 
 18) reduce--> The reduce() method executes a reducer function for array element.
               The reduce() method returns a single value: the function's accumulated result.
               The reduce() method does not execute the function for empty array elements.
               The reduce() method does not change the original array.
               
        EG: const array1 = [1, 2, 3, 4];

                    // 0 + 1 + 2 + 3 + 4
                    const initialValue = 0;
                    const sumWithInitial = array1.reduce(
                      (previousValue, currentValue) => previousValue + currentValue,
                      initialValue
                    );

                    console.log(sumWithInitial);
               output: 10
----------------------------------------------------------------

19) slice-->The slice() method returns selected elements in an array, as a new array.
            The slice() method selects from a given start, up to a (not inclusive) given end.
            The slice() method does not change the original array.

        EG:
         const fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
        const citrus = fruits.slice(1, 3);
        output--> Orange,Lemon
---------------------------------------------

20) some--> The some() method checks if any array elements pass a test (provided as a callback function).
            The some() method executes the callback function once for each array element.
            The some() method returns true (and stops) if the function returns true for one of the array elements.
            The some() method returns false if the function returns false for all of the array elements.
            The some() method does not execute the function for empty array elements.
            The some() method does not change the original array.
            
            EG: const ages = [3, 10, 18, 20];
                ages.some(checkAdult);
                function checkAdult(age) {
                  return age > 18;
                }
                
                output: true
