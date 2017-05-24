# samples
 http://math.hashcode.ru/questions/4908/%D0%BA%D0%BE%D0%BC%D0%B1%D0%B8%D0%BD%D0%B0%D1%82%D0%BE%D1%80%D0%B8%D0%BA%D0%B0-%D0%BA%D0%BE%D0%BB%D0%B8%D1%87%D0%B5%D1%81%D1%82%D0%B2%D0%BE-%D0%BA%D0%BE%D0%BC%D0%BF%D0%BE%D0%B7%D0%B8%D1%86%D0%B8%D0%B9-%D1%87%D0%B8%D1%81%D0%BB%D0%B0-%D1%81-%D0%BE%D0%B3%D1%80%D0%B0%D0%BD%D0%B8%D1%87%D0%B5%D0%BD%D0%B8%D1%8F%D0%BC%D0%B8-%D0%BD%D0%B0-%D1%81%D0%BB%D0%B0%D0%B3%D0%B0%D0%B5%D0%BC%D1%8B%D0%B5
<html>
<head></head>
<body>
  <script>
    // function fibonacci(n) {
    //   result = (Math.pow(((1 + Math.sqrt(5)) / 2), n) - Math.pow(((1 - Math.sqrt(5)) / 2), n)) / Math.sqrt(5);
    //   console.log(result);
    //   alert('n:' + result);
    // }
    // fibonacci(77);

    // function fib(n) {
    //   var a = 1,
    //     b = 1;
    //   for (var i = 3; i <= n; i++) {
    //     var c = a + b;
    //     a = b;
    //     b = c;
    //   }
    //   return b;
    // }

    // function xxx(n) {
    //   var a = 1,
    //     b = 1,
    //     v = 0;

    //   for (var i = 4; i <= n; i++) {
    //     var c = a + b + v;
    //     v = b
    //     b = a;
    //     a = c;
    //   }
    //   return a;
    // }

    // function trib(n) {
    //   var a0 = 1,
    //     a1 = 1,
    //     a2 = 0;
    //   for (var i = 4; i <= n; i++) {
    //     var c = a0 + a1 + a2;
    //     a2 = a1
    //     a1 = a0;
    //     a0 = c;
    //   }
    //   return a0;
    // }

    // function sily(n, k = 6) {//6) {
    //   // if ((n == 0) || ((k - 2) >= n)) return 0;
    //   // n = n + k - 1;
    //   result = []

    //   result[0] = 1;
    //   result[1] = 1;
    //   for (var i = 2; i <= k - 1; i++) {
    //       result.push(0);
    //   }
    //     console.log(result)

    //   for (var i = 2/*i = 1 + k*/; i <= n; i++) {
    //     var c = 0;

    //     for (var j = k-1; j >= 1; j--) {
    //     // console.log('A0' + result[0] + ' j: ' + j)
    //     // console.log('A1' + result[1])
    //     // console.log('A2' + result[2])
    //       c += result[j];
    //       result[j] = result[j-1];
    //     }
    //     c += result[0];

    //     console.log('C:' + c)

    //     result[0] = c;
    //   }
    //   // console.log(result)
    //   return result[0];
    // }
// alert(
//   'sily: ' + sily(610,6) + '\n' 
// )
    var cache = [];
    let fib = function(cache,a) { 
      // console.log(cache[a])
      // return cache[a] = cache[a] === undefined ? a > 3 ? fib(cache,a-1) + fib(cache,a-2) + fib(cache,a-3) : a > 1 ? 1 : 0 : cache[a]; 
      return cache[a] = cache[a] === undefined ? a > 6 ? fib(cache,a-1) + fib(cache,a-2) + fib(cache,a-3) + fib(cache,a-4) + fib(cache,a-5) + fib(cache,a-6) : a > 4 ? 1 : 0 : cache[a]; 
    }

    // var size = 10;
    // var steps = [1, 2, 3, 4, 5, 6];
    // var count = 0;
    // let counter = function(current) {
    //   if (current == size) {
    //     count++;
    //     return;
    //   }
    //   if (current < size)
    //     for (let i = 0; i < steps.length; i++) {
    //       counter(current + steps[i]);
    //     }
    // }
    // counter(0);
    // console.log(count);

    let fib6 = function(cache, a) {
        return cache[a] = cache[a] === undefined ? a > 0 ? fib6(cache, a - 1) + fib6(cache, a - 2) + fib6(cache, a - 3) + fib6(cache, a - 4) + fib6(cache, a - 5) + fib6(cache, a - 6) : a == 0 ? 1 : 0 : cache[a];
    }
    var cache = [];
    // for (let i = 1; i < 1040; i++)
        //console.log(" " + i + " " + fib6(cache, 10));

    console.log(fib6(cache,610));

    alert(
    //   '0: ' + fib(cache,0) + '\n' +
    //   '1: ' + fib(cache,1) + '\n' +
    //   '2: ' + fib(cache,2) + '\n' +
    //   '3: ' + fib(cache,3) + '\n' +
    //   '4: ' + fib(cache,4) + '\n' +
    //   '5: ' + fib(cache,5) + '\n' +
    //   '6: ' + fib(cache,6) + '\n' +
    //   '7: ' + fib(cache,7) + '\n' +
    //   '8: ' + fib(cache,8) + '\n' +
    //   '9: ' + fib(cache,9) + '\n' +
    //   '10: ' + fib(cache,10) + '\n' +
    //   '11: ' + fib(cache,11) + '\n' +
    //   '12: ' + fib(cache,12) + '\n' +
    //   '13: ' + fib(cache,13) + '\n' +
    //   '14: ' + fib(cache,14) + '\n' +
    //   '15: ' + fib(cache,15) + '\n' +
      '610: ' + fib(cache, 610)
    )

    // alert(trib(10));
    // first version
    // var cache = [];
    // let fib = function(a) { 
    //   return cache[a] = cache[a] === undefined ? a > 1 ? fib(a-1) + fib(a-2) : 1 : cache[a]; 
    // }
    
    // for(let j = 0; j< 100000000; j+=10000)
    //   console.log(fib(j));

    // // second version 
    // let cache = [];
    // let fib = function(cache,a) { 
    //   return cache[a] = cache[a] === undefined ? a > 1 ? fib(cache,a-1) + fib(cache,a-2) : 1 : cache[a]; 
    // }


  </script>
</body>
</html>
