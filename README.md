# mirai
<!DOCTYPE html>
<html lang="ja">

<head>
<title>Document</title>
</head>

<body>
<h3>あなたに当てはまる項目はいくつある???</h3>
　　　　　　　　　　　　　　　　
<script type="text/javascript">

<!--

function myCheck()
{myCnt = 0;

for( i=0;i<document.myForm.length-1;　i++ ){

if ( document.myForm.elements[i].checked == true ){myCnt++;}}

if ( myCnt == 0 ) myMess = "正常";

else if ( myCnt <= 2 ) myMess = "ちょヤバ";

else if ( myCnt <= 4 ) myMess = "危険気味";
else myMess = "完璧に危険";

myComment = "危険度チェック　診断結果→→→あなたは、" + myMess + "です！";alert ( myComment );}// -->


</script>

<!--コメント -->
<form name="myForm">

<input type="checkbox">たばこは１日60本以上吸う<br>

<input type="checkbox">お酒を飲むと気が大きくなり、100万円単位でお金を使い始める。<br>

<input type="checkbox">車を運転すると性格が豹変し、時速200キロは出さないと安心できない。<br>

<input type="checkbox">包丁を手にすると、食べ物よりも誰かに刃先を向けたくなる<br>

<input type="checkbox">ピストルを10丁以上、所持しているが、使わなければ安心だと思っている。<br>
<p></p>
👉👉👉そんなあなたの性格は?
<p></p>

<input type="button" onclick="myCheck()" value="診断"><br></form>
<p>
</p>
<p>
<a 
href="チェック2.html">➝反転</a>
</p>
<img src="file:///storage/emulated/0/Download/20200707-0602_3483e590ebcc3365de8fc73a0bc0dc3b.jpg"　 
width="300" height="140">

<style>
</style>
</body>
</html>


