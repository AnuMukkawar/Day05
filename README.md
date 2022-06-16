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
         
