<h2>Drop it</h2>

<p>Drop the elements of an array (first argument), starting from the front, until the predicate (second argument) returns true.</p>
<p>The second argument, func, is a function you'll use to test the first elements of the array to decide if you should drop it or not.</p>
<p>Return the rest of the array, otherwise return an empty array.</p>
<ul>
<li>dropElements([1, 2, 3, 4], function(n) {return n >= 3;}) should return [3, 4].</li>
<li>dropElements([0, 1, 0, 1], function(n) {return n === 1;}) should return [1, 0, 1].</li>
<li>dropElements([1, 2, 3], function(n) {return n > 0;}) should return [1, 2, 3].</li>
<li>dropElements([1, 2, 3, 4], function(n) {return n > 5;}) should return [].</li>
<li>dropElements([1, 2, 3, 7, 4], function(n) {return n > 3;}) should return [7, 4].</li>
<li>dropElements([1, 2, 3, 9, 2], function(n) {return n > 2;}) should return [3, 9, 2].</li>
</ul>
</p><br/>
<p>======================================================</p>  
  
function dropElements(arr, func) {
  // Drop them elements.  
  var newarr=[];  
  var index;  
  index=getindex(arr);  
  
  for(var j=index;j<arr.length;j++)  
    {  
      newarr.push(arr[j]);  
    }  
  
  return newarr;  
    function getindex(arr)  
 {  
   for(var i=0;i<arr.length;i++)  
    {  
      if(func(arr[i]))  
        {  
        return i;  
        }  
    }  
 }  
}    
      
dropElements([1, 2, 3, 9, 2], function(n) {return n > 2;});  