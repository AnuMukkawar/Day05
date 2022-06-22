# Day05

Q1.Do the below programs in anonymous function & IIFE

A) Print odd numbers in an array

Ans-

//Anonymous function


      var arr=[1,5,4,6,7,3,9,11,17,24];
      var res=[];
       var odd=function(arr){
         for(var i=0;i<arr.length;i++)
            {
                if(arr[i]%2!=0)
                {
                    res.push(arr[i]);
                }
            }
            return res;
        }
        console.log(odd(arr));
 
 
//IIFE function
    
      var arr=[1,5,4,6,7,3,9,11,17,24];
      var res=[];
      (function(arr){
            for(var i=0;i<arr.length;i++)
            {
                if(arr[i]%2!=0)
                {
                    res.push(arr[i]);
                }
            }
            console.log(res);
        })(arr);
         
O/p-[1,5,7,3,9,11,17]


B) Convert all the strings to title caps in a string array

Ans-

            //Anonymous function
            var titleCase= function(str) {
              str = str.toLowerCase().split(' ');
              for (var i = 0; i < str.length; i++) {
                str[i] = str[i].charAt(0).toUpperCase() + str[i].slice(1); 
              }
              return str.join(' ');
            }
            console.log(titleCase("I am a student"));

            //IIFE function
             (function titleCase(str) {
              str = str.toLowerCase().split(' ');
              for (var i = 0; i < str.length; i++) {
                str[i] = str[i].charAt(0).toUpperCase() + str[i].slice(1); 
              }
              console.log(str.join(' '));
            })("I am a student");
            
   O/p-I Am A Student
          
          
C) Sum of all numbers in an array

Ans-

  //Anynomous function
  
            var s=0;
            var sum=function(arr){
                for(var i=0;i<arr.length;i++)
                {
                    s+=arr[i] ;      
                }
                return s;
            }
            console.log(sum([1,2,3,6]));


            //IIFE function
            var s=0;
            (function sum(arr){
                for(var i=0;i<arr.length;i++)
                {
                    s+=arr[i] ;      
                }
                console.log(s);
            })([1,2,3,6]);

o/p-12

D)Return all the prime numbers in an array

Ans-

//Anynomous function

            var arr=[17,3,7,4,2,19];
            var arr1=[];
            var isPrime=function(arr) {
                for(var number=0;number<arr.length;number++)
                {
                    if (arr[number] <= 1) {
                        false;
                      }else 
                          {
                            for (let i = 2; i <= arr[number]; i++) {
                              if (arr[number] % i != 0 || arr[number]==2) {
                                arr1.push(arr[number]);
                                break;
                              }
                              else
                                 break;
                            }
                      }
                }
                return arr1;
            }
            console.log(isPrime(arr));
            
//IIFE function

            var arr1=[];
            (function isPrime(arr) {
                for(var number=0;number<arr.length;number++)
                {
                    if (arr[number] <= 1) {
                        false;
                      }else 
                          {
                            for (let i = 2; i <= arr[number]; i++) {
                              if (arr[number] % i != 0 || arr[number]==2) {
                                arr1.push(arr[number]);
                                break;
                              }
                              else
                                 break;
                            }
                      }
                }
                console.log(arr1);
            })([17,3,7,4,2,19]);
            
o/p- [17,3,7,2,19]

E) Return all the palindromes in an array

Ans-

//Anonymous function 


             var arr=[];
             var isPalindrome=function (elements){
                for(var i in elements)
                {
                  var arrayValues = elements[i].toString().split('');

                    // reverse the array values
                    var reverseArrayValues = arrayValues.reverse();

                    // convert array to string
                    var reverseString = reverseArrayValues.join('');

                    if(elements[i] == reverseString) {
                        arr.push(elements[i]);
                    }

                }
              return arr;
            }
            
       console.log( isPalindrome([151,"madam",1221,1431,"hiii"]));
 
 //IIFE function   
 
 
             var arr=[];
            (function  isPalindrome(elements){
                for(var i in elements)
                {
                  var arrayValues = elements[i].toString().split('');

                    // reverse the array values
                    var reverseArrayValues = arrayValues.reverse();

                    // convert array to string
                    var reverseString = reverseArrayValues.join('');

                    if(elements[i] == reverseString) {
                        arr.push(elements[i]);
                    }

                }
               console.log(arr);
            })([151,"madam",1221,1431,"hiii"]);
            
  o/p-[ 151, 'madam', 1221 ]
  
F) Return median of two sorted arrays of the same size

Ans-

//Anonymous function

            var arr1=[1, 12, 15, 26, 38];
            var arr2=[2, 13, 17, 30, 45];
            var arr3=[...arr1,...arr2];
            arr3.sort(function(a, b){return a-b});

            var res= function(arr3){
                return ((arr3[arr3.length/2-1]+arr3[arr3.length/2])/2);
            }

            console.log(res(arr3));
            
  
//IIFE function

            var arr1=[1, 12, 15, 26, 38];
            var arr2=[2, 13, 17, 30, 45];
            var arr3=[...arr1,...arr2];
            arr3.sort(function(a, b){return a-b});

            (function(arr3){
                console.log((arr3[arr3.length/2-1]+arr3[arr3.length/2])/2);
            })(arr3);
            
  o/p-16
   
G) Remove duplicates from Array

Ans-

//Anonymous function

            var arr=[1,1,2,3,4,4,5,6,5,3,7,8];
            var arr1=[];
            arr=arr.sort();
            var removeDuplicate=function(arr){
              for(var i=0;i<arr.length;i++)
              {
                for(var j=i+1;j<arr.length;j++)
                {
                  if(arr[i]!=arr[j])
                  {
                     arr1.push(arr[i]);  
                     break;
                  }
                  else 
                    break;
                }
              }
              arr1.push(arr[arr.length-1]);
              return arr1;
            }

            console.log(removeDuplicate(arr));
       
//IIFE function

            var arr=[1,1,2,3,4,4,5,6,5,3,7,8];
            var arr1=[];
            arr=arr.sort();
            (function  removeDuplicate(arr){
              for(var i=0;i<arr.length;i++)
              {
                for(var j=i+1;j<arr.length;j++)
                {
                  if(arr[i]!=arr[j])
                  {
                     arr1.push(arr[i]);  
                     break;
                  }
                  else 
                    break;
                }
              }
              arr1.push(arr[arr.length-1]);
              console.log(arr1);
            })(arr);
            
 o/p- [ 1, 2, 3, 4, 5, 6, 7, 8 ]

H) Rotate an array by K times

Ans-

//Anonymous function

            let Array = [1, 2, 3, 4, 5];
            let N = Array.length;
            let K = 2;
            let arr1=[];

            var RightRotate=function(a, n, k)
            {
                k = k % n;

                for (let i = 0; i < n; i++) {
                    if (i < k) {
                        arr1.push(a[n + i - k]);
                    }
                    else {
                        arr1.push((a[i - k]));
                    }
                }
               return arr1;
            }

            console.log(RightRotate(Array, N, K));


//IIFE function

            let Array = [1, 2, 3, 4, 5];
            let N = Array.length;
            let K = 2;
            let arr1=[];

            (function RightRotate(a, n, k)
            {
                k = k % n;

                for (let i = 0; i < n; i++) {
                    if (i < k) {
                        arr1.push(a[n + i - k]);
                    }
                    else {
                        arr1.push((a[i - k]));
                    }
                }
                console.log(arr1);
            })(Array, N, K);
            
            
  o/p- [4,5,1,2,3]
            
            
Q3.Do the below programs in arrow functions

A) Print odd numbers in an array
Ans-

      var res=[];
      //Arrow function
      var odd=(arr)=>{
         for(var i=0;i<arr.length;i++)
            {
                if(arr[i]%2!=0)
                {
                    res.push(arr[i]);
                }
            }
            return res;
        }
        console.log(odd([1,3,7,6]));
        
O/p-[1,3,7]

B) Convert all the strings to title caps in a string array
Ans-

//Arrow function

            var titleCase=(str)=> {
              str = str.toLowerCase().split(' ');
              for (var i = 0; i < str.length; i++) {
                str[i] = str[i].charAt(0).toUpperCase() + str[i].slice(1); 
              }
              return str.join(' ');
            }
            console.log(titleCase("I am a student"));

C) Sum of all numbers in an array
Ans-

      //Arrow function
      var s=0;
      var sum=(arr)=>{
          for(var i=0;i<arr.length;i++)
          {
              s+=arr[i] ;      
          }
          return s;
      }
      console.log(sum([1,2,3,6]));
 o/p-12

D) Return all the prime numbers in an array

Ans-

 //Arrow function
            
            var arr1=[];
            var isPrime=(arr)=> {
                for(var number=0;number<arr.length;number++)
                {
                    if (arr[number] <= 1) {
                        false;
                      }else 
                          {
                            for (let i = 2; i <= arr[number]; i++) {
                              if (arr[number] % i != 0 || arr[number]==2) {
                                arr1.push(arr[number]);
                                break;
                              }
                              else
                                 break;
                            }
                      }
                }
                return arr1;
            }
            console.log(isPrime([17,3,7,4,2,19]));
            
o/p- [17,3,7,2,19]
                       
E) Return all the palindromes in an array

Ans-

            var arr=[];
                    var isPalindrome=(elements)=>{
                            for(var i in elements)
                            {
                              var arrayValues = elements[i].toString().split('');

                                // reverse the array values
                                var reverseArrayValues = arrayValues.reverse();

                                // convert array to string
                                var reverseString = reverseArrayValues.join('');

                                if(elements[i] == reverseString) {
                                    arr.push(elements[i]);
                                }

                            }
                          return arr;
                        }

                console.log( isPalindrome([151,"madam",1221,1431,"hiii"]));
 o/p-[151, 'madam', 1221]
