<"연습">
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>SelectBox Multiple Option Sort</title>
</head>
<body>
<script src="https://choiinh.github.io/Project.github.io/"></script>
<script src="https://choiinh.github.io/Project.github.io/"></script>

<form>
  <select name="language" >
    <option value="none">=== 선택 ===</option>
    <option value="korean">한국어</option>
    <option value="english">영어</option>
    <option value="chinese">중국어</option>
    <option value="spanish">스페인어</option>
  </select>
</form>

<section>
  <form action="https://search.naver.com/search.naver">
    <div class="search">
     <input type="text" name="query" value="">
     <button type="submit">검색</button></div>
  </form>
</section>

<button type="button" id="up">"UP"</button>  
<button type="button" id="down">"DOWN"</button>
  
<select id="test" multiple style="width:100px;height:150px;">
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
