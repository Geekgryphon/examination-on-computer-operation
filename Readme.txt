上機測驗-物件&演算法

一 物件導向-繼承/介面

二 資料處理-字串

三 資料處理-陣列

  1. 計算出奇數值總和減去偶數值總和

  $arr = [0,1,2,3,4,5,6,7,8,9];
	
	$odd_num_sum = 0;
	$even_num_sum = 0;
	
	for($i=0; $i < count($arr); $i++){
	  if($arr[$i] %2 == 0){
	    $even_num_sum += $arr[$i];
	  }else{
	    $odd_num_sum += $arr[$i];
	  }
	  
	}
	
	echo ($odd_num_sum - $even_num_sum);
  
  2. 分割成二陣列分別存放偶數值及奇數值
  
  $arr = [0,1,2,3,4,5,6,7,8,9];
  
  $new_arr = array();

	
  for($i=0; $i < count($arr); $i++){
    if($arr[$i] %2 == 0){
      $new_arr[1][] = $arr[$i];
    }else{
      $new_arr[0][] = $arr[$i];
    }
  }
	
  sort($new_arr);
	
  var_dump($new_arr);

四 資料排序-正序

 不用到語法糖
 
 $arr = [77,5,5,22,13,55,97,4,796,1,0,9];
	
 for($i = 0; $i < count($arr); $i ++) {
    for($j = 0; $j < count($arr)-1; $j ++){
        if($arr[$j] > $arr[$j+1]) {
            $temp = $arr[$j+1];
            $arr[$j+1]=$arr[$j];
            $arr[$j]=$temp;
        }       
    }
  }
  
  var_dump($arr);

五 邏輯處理-交集 差集 聯集

$arr_a = array(77,5,5,22,13,55,97,4,796,1,0,9);
$arr_b = array(0,1,2,3,4,5,6,7,8,9);
$arr_c = array();
$arr_d = array();
$arr_e = array();

for($i = 0; $i < count($arr_a); $i++){
  if(in_array($arr_a[$i], $arr_b)){
    $arr_c[] = $arr_a[$i];
  }
  
  if(!in_array($arr_a[$i], $arr_b)){
    $arr_d[] = $arr_a[$i];
  }
}

for($i = 0; $i < count($arr_a); $i++){
  if(!in_array($arr_a[$i], $arr_e)){
    $arr_e[] = $arr_a[$i];
  }
}

for($i = 0; $i < count($arr_b); $i++){
  if(!in_array($arr_b[$i], $arr_e)){
    $arr_e[] = $arr_b[$i];
  }
}


var_dump($arr_c);
var_dump($arr_d);
var_dump($arr_e);




六 兩數總和
