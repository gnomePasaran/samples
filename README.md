# samples
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

    function fib(n) {
      var a = 1,
        b = 1;
      for (var i = 3; i <= n; i++) {
        var c = a + b;
        a = b;
        b = c;
      }
      return b;
    }

    function xxx(n) {
      var a = 1,
        b = 1,
        v = 0;

      for (var i = 4; i <= n; i++) {
        var c = a + b + v;
        v = b
        b = a;
        a = c;
      }
      return a;
    }

    function trib(n) {
      var a0 = 1,
        a1 = 1,
        a2 = 0;
      for (var i = 4; i <= n; i++) {
        var c = a0 + a1 + a2;
        a2 = a1
        a1 = a0;
        a0 = c;
      }
      return a0;
    }

    function sily(n, k = 3) {//6) {
      result = []
      for (var i = 0; i <= k - 1; i++) {
        result.push(1);
      }
      result[k-1] = 0
        console.log(result)

      for (var i = 1 + k; i <= n; i++) {
        var c = 0;

        for (var j = k-1; j >= 1; j--) {
        // console.log('A0' + result[0] + ' j: ' + j)
        // console.log('A1' + result[1])
        // console.log('A2' + result[2])
          c += result[j];
          result[j] = result[j-1];
        }
        c += result[0];

        console.log('C:' + c)

        result[0] = c;
      }
      // console.log(result)
      return result[0];
    }

    alert(
      '3: ' + sily(3) + '\n' +
      '4: ' + sily(4) + '\n' +
      '5: ' + sily(5) + '\n' +
      '6: ' + sily(6) + '\n' +
      '7: ' + sily(7) + '\n' +
      '8: ' + sily(8)
    )
    // alert(trib(10));
  </script>
</body>
</html>
