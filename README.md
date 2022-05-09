# array-iteration-methods
Learn eight methods to iterate through an array in JavaScript! Methods include: forEach, map, filter, reduce, some, every, find, findIndex.              8 Methods:                  1. forEach,                  2. map,                  3. filter,                  4. reduce,                  5. some,                  6. every,                  7. find,                  8. findIndex


To iterate means that you're going through the array and doing something with each item of the array.
        Some methods don't necessarily go through each item. The below captioned examples cover that. Most do.
        

    1. forEach

        Pass in the array [1, 2, 3] forEach()
        forEach does something for each item in the array
        Pass in the item or the index of the item of the array 
        And forEach, in this example, console.log the index

        Run the code in the console terminal:

                [1, 2, 3].forEach(function (item, index) {
                    console.log(item, index);
                });
                
        The output in the console is: 
          1 0  // the index of item 1 is 0
          2 1  // the index of item 2 is 1
          3 2  // the index of item 3 is 2

    2. map

         Map takes an item from the array three = [1, 2, 3].
         It does some thing to it.
         Puts that same item back in that same place in the array.

         In this example, assign it to doubled.
         Iterate with the method three.map().
         Double each item - return item * 2.
         Instead of the array being [1, 2, 3], there's a new thing in place of each item in the array.

         Run the code in the console terminal:
         
                const three = [1, 2, 3];
                const doubled = three.map(function (item) {
                return item * 2;
                });
                console.log(doubled);
              
         The output in the console is:
            [2, 4, 6] // all items have been doubled
            
            
    3. filter
        
         Take the array ints = [1, 2, 3], check each item in the array.
         It gets a condition to check if it's true or false.
         If it's true, put the item back in the array.
         If it's false, do not put the item back in the array.
         Each of the items makes a brand new array.

         Pass in the numbers one, two three to the array ints = [1, 2, 3].
         The condition is item % 2 === 0.
         For each of the items check if the condition is true.
         This is just a way to find out even numbers.

         Run the code in the console terminal:
         
              const ints = [1, 2, 3];
              const evens = ints.filter(function (item) {
                return item % 2 === 0;
              });
              console.log(evens);

         The output in the console is:
             [2] // even is now 2.

         In this example, doesn't actually put back into the array, because ints still equals [1, 2, 3].
