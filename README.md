<?php

$bottoken ="248179972:AAHeU8Ru1-rg3g6I6kwvx4QiBLym9VecFYE";
$website = "https://api.telegram.org/bot".$bottoken;
$update = file_get_contents($website."/getupdates");
$updatearry = json_decode($update, true);
$chatid =    $updatearry["result"][0]["message"]["chat"]["id"];
file_get_contents($website."/sendmessage?chat_id=".$chatid."&text=test");    


    
?>
