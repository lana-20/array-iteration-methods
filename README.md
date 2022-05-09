Array Iteration: 

        Learn eight methods to iterate through an array in JavaScript! Methods include: forEach, map, filter, reduce, some, every, find, findIndex.

            8 Methods:

                1. forEach, 
                2. map, 
                3. filter, 
                4. reduce, 
                5. some, 
                6. every, 
                7. find, 
                8. findIndex


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

     Run the code in the console terminal:b 
     
          const ints = [1, 2, 3];
          const evens = ints.filter(function (item) {
            return item % 2 === 0;
          });
          console.log(evens);

     The output in the console is:
     
        [2] // even is now 2

     In this example, doesn't actually put back into the array, because ints still equals [1, 2, 3]

4. reduce

      Take an array and do smth and pass the result to the next iteration along with the next item in the array
      that's why we are putting (result, item) in this example
      the first time it goes through the array, it's going to have a result
      it's gonna send that result to the next iteration and then add an item
      the number at the end (0) is what the initial result is going to be
      if you don't put the number at the end like this - {...}, 0); - the initial result reuslt will be the first item in the array
      the first time you go through this the result is going to be 0, then we add the first item in the array [1, ..., ...]
      it's gonna go through the array again and the result is now 1
      and it's going to add the item two [..., 2, ...], so one plus two is three 
      go though it again, there's the result three, it's going to add the third item in the array [..., ..., 3]
      that's going to result in six

      Run the code in the console terminal:
      
          const sum = [1, 2, 3].reduce(function (result, item) {
            return result + item;
          }, 0);
          console.log(sum);
          
      The output in the console is:
      
          6

5. some

      With some() you just check if any item is in the array
      here are all the items [1, 2, 3, -1, 4] in the array hasNegativeNumbers
      some means does any item in the entire array meet this condition item < 0
      if any item in the array meets the condition is less than zero, it's going to be true
      is no items meet the condition then it's going to be false
      it's going to return true, because one of the itens in the array is negative

      Run the code in the console terminal:
      
          const hasNegativeNumbers = [1, 2, 3, -1, 4].some(function (item) {
            return item < 0;
          });
          console.log(hasNegativeNumbers);

      The output in the console is:
      
          true // has negative number -1 in the array



6. every

     every() is kind of similar to some() but now every number has to meet the condition
     we have the array allPositiveNumbers, we pass in [1, 2, -3]
     run the callback (function (item), pass in each item
     if each item is more than zero, then we're going to put true
     but also we make just one item negative, when we run the code, we get false
     it's either all or nothing

     Run the code in the console terminal:
     
        const allPositiveNumbers = [1, 2, -3].every(function (item) {
          return item > 0;
        });
        console.log(allPositiveNumbers);
                
     The output in the console is:
     
         false
