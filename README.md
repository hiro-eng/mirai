# mirai
<html> <head> <!--コメント -->

<script type="text/javascript">

hayasa=30; 	
coin=10; 	 
mes='残念！コインを使い果たしてしまいました!ゲーム終了!'; 			
	rate1=5; 			
	rate2=10; 	kekka=coin; 	nums=new Array('','',''); 	timers=0; 	e1=0;e2=0;e3=0; 	
	
	function hajime()	{ 	
					
						kekka=coin; 		document.form1.kekka.value=coin; 		document.form1.text1.value=" "; 		document.form1.text2.value=" "; 		document.form1.text3.value=" "; 		} 	function srot() 		{ 		if(e1 < 1000) 			{ 			nums[0]=Math.floor(Math.random()*46); 			for(i1=0,j1=9,k1=j1; i1 < 10; i1++) 				{ 				if(nums[0] < k1 || nums[0] == 45) 					{ 					if(i1+1 == 10)nums[0]=0; 					else nums[0]=i1+1; 					break; 					} 				j1--; 				k1+=j1; 				} 			document.form1.text1.value=nums[0]; 			e1++; 			clearTimeout(timers); 			timers=setTimeout('srot()',hayasa); 			} 		if(e2 < 1000) 			{ 			nums[1]=Math.floor(Math.random()*46); 			for(i2=0,j2=9,k2=j2; i2 < 10; i2++) 				{ 				if(nums[1] < k2 || nums[1] == 45) 					{ 					if(i2+1 == 10)nums[1]=0; 					else nums[1]=i2+1; 					break; 					} 				j2--; 				k2+=j2; 				} 			document.form1.text2.value=nums[1]; 			e2++; 			clearTimeout(timers); 			timers=setTimeout('srot()',hayasa); 			} 		if(e3 < 1000) 			{ 			nums[2]=Math.floor(Math.random()*46); 			for(i3=0,j3=9,k3=j3; i3 < 10; i3++) 				{ 				if(nums[2] < k3 || nums[2] == 45) 					{ 					if(i3+1 == 10)nums[2]=0; 					else nums[2]=i3+1; 					break; 					} 				j3--; 				k3+=j3; 				} 			document.form1.text3.value=nums[2]; 			e3++; 			clearTimeout(timers); 			timers=setTimeout('srot()',hayasa); 			} 		if(e1 >= 1000)stop(); 		else if(e2 >= 1000)stop(); 		else if(e3 >= 1000)stop(); 		} 	function stop() 		{ 		document.form1.text1.value=nums[0]; 		document.form1.text2.value=nums[1]; 		document.form1.text3.value=nums[2]; 		if(e1 >= 1000 && e2 >= 1000 && e3 >= 1000) 			{ 			if(nums[0] == nums[1] && nums[1] == nums[2]) 				{ 				if(nums[0] == 0)kekka+=10*rate1; 				else kekka+=nums[0]*rate1; 				} 			else if(nums[0] == nums[1]+1 && nums[1] == nums[2]+1) 				{ 				if(nums[0] == 0)kekka+=10*rate2; 				else kekka+=nums[0]*rate2; 				} 			else if(nums[2] == nums[1]+1 && nums[1] == nums[0]+1) 				{ 				if(nums[0] == 0)kekka+=10*rate2; 				else kekka+=nums[0]*rate2; 				} 			document.form1.kekka.value=kekka; 			} 		} 	function starts(e) 		{ 		e=eval(e); 		if(e == 0) 			{ 			if(kekka<1) 				{ 				alert(mes); 				document.form1.kekka.value=0; 				} 			else 				{ 				kekka--; 				document.form1.kekka.value=kekka; 				e1=0;e2=0;e3=0; 				srot(); 				} 			} 		else if(e == 1)e1=1000; 		else if(e == 2)e2=1000; 		else if(e == 3)e3=1000; 		} //--> </script> </head> <body onLoad="hajime();".fontsize(7);> 
<div></div>
	<div class="fade"><center><h4><i>スロット</i></h4></center></div>
	
	<div　style="font-size:20pt">
	<h3><form name="form1"><table border="3" align="center"　font-size="30px"><tr> <td align="center"><input type="text" size="1<" name="text1"></td></h3> <td align="center"><input type="text" size="1" name="text2"></td> <td align="center"><input type="text" size="1" name="text3"></td> </tr> <tr> <td align="center"><input type="button" value="Stop!" onClick="starts(1);"></td> <td align="center"><input type="button" value="Stop!" onClick="starts(2);"></td> <td align="center"><input type="button" value="Stop!" onClick="starts(3);"></td> <tr> <td colspan="3" align="center"> <input type="button" value="Start!" onClick="starts(0);"> <input type="button" value="Reset" onClick="hajime();"> </td> </tr> <tr> <td colspan="5">手持ちコインはあと<input type="text" size="5" name="kekka">枚。</td> </tr> </table> </form></h3>
	</div>
	
	<style type="text/css"media="screen">

　　table{height:80px;}

body{
				background-color:#008080;
				
				}

.fade{
         font-size: 40px;
         font-weight: bold;
       animation-name: fadein;
       animation-duration:2s;
       
         }

							
							@keyframes fadein { 
									from {
        opacity: 0;
  transform: translateY(20px);
            }
    to {
         opacity: 1;
    transform: translateY(0);
         }


							 }
h4{
				color:white;
				}

</style>
<div class="fade"><center><input type="button" value="ゲームのルール" 
onclick="i=0; msg='💲💲💲💲💲これは、皆さんよくご存知のスロットマシンです。まず初めにスタートボタンを押してゲームを開始し、それから一つずつストップボタンを押してください。ゾロ目なら、コインが5倍、連番なら10倍になるよ。さあ、皆さん、億万長者になりましょう!💲💲💲💲💲';
 timerID=setInterval('if(i<=msg.length){document.all.div1.innerText=msg.substring(0,i); i++;}if(i>msg.length){clearInterval(timerID);}',80);"></center></div>

<div id=div1></div>
	
	 </body> </html>
