# Project.github.io
<!"연습">
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>SelectBox Multiple Option Sort</title>
</head>
<body>
  https://choiinh.github.io/Project.github.io/
<script src="https://choiinh.github.io/Project.github.io/"></script>
<script src="https://choiinh.github.io/Project.github.io/"></script>
  
<button type="button" id="up">"UP"</button>  
<button type="button" id="down">"DOWN"</button>
  
<select id="test" multiple style="width:300px;height:400px;">
  <option value="1">1111</option>
  <option value="2">2222</option>
  <option value="3">3333</option>
  <option value="4">4444</option>
</select>

<script>
  

  var count = $("#test option").length;
  
  $("#down").click(function() {
    
    $($("#test option:selected").get().reverse()).each(function(i){
      var index = $(this).index() + 1;
      console.log(count + ":" + index);
      if (index < (count - i)) $("#test option:eq(" + index + ")").after(this);
    });
  });
  
  $("#up").click(function() {

    $("#test option:selected").each(function(i){
      var index = $(this).index() - 1;
      console.log(count + ":" + index);
      if (index >= i) $("#test option:eq(" + index + ")").before(this);
    });
  });
</script>
  
</body>
</html>
