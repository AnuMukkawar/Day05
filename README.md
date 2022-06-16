# Day05

Q1.Do the below programs in anonymous function & IIFE

A) Print odd numbers in an array

Ans-

      var arr=[1,5,4,6,7,3,9,11,17,24];
      var res=[];
    
       //Anonymous function
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
    
    
      var arr=[1,5,4,6,7,3,9,11,17,24];
      var res=[];
      //IIFE function
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
