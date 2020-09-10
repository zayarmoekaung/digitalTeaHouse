# digitalTeaHouse

***This is the code documentation for Digital Tea House site***

***Features***

1. Search
2. Filters
3. Audio player
4. CMS

***Search***
includes/navbar.php 

The Below codes are for Search Bar in Mobile View. 

    <header class="mnavbar">
     <a href="<?php echo BASE_URL ?>"><img class="mlogo" src="<?php echo BASE_URL . 'static/images/Logo.png' ?>"></a>
     <label class="mmenu" onclick="appear()">menu</label>
  
  By clicking the label, the appear function is called to show mobile menu bar.
  
     <img class="msearch" src="<?php echo BASE_URL . 'static/images/search.png' ?>" onclick="appear2()">
  
  By clicking the search icon appear2 function is called to show mobile search bar.
 


      <div id="searchpg" class="msearchbox">
        <form action="<?php echo BASE_URL . 'search.php' ?>" method="post"  >
          <img class="mbacks" src="<?php echo BASE_URL . 'static/images/back.png'?>" onclick="appear2()">
    <input type="text" id="key_word" name="key_word" placeholder="ဘာကိုရှာချင်ပါသလည်း?" style="top: 30.06%;">
    <svg height="210" width="100%">
    <line x1="0" y1="0" x2="200%" y2="0" style="stroke:rgb(0,0,0);stroke-width:2" />
    </svg>
    </form>
    </div>
    </header>
 
 These above codes will show mobile search page.
 
    <header class="wnavbar"  >


    <h1><a class="navlogo" href="<?php echo BASE_URL ?>"><img class="img-fluid" src="<?php echo BASE_URL . 'static/images/Logo.png'?>" alt="Digital Tea House" style="width: auto; height: auto; max-width: 200px; max-height: 180px; margin-left: 30px;"></a></h1>
     <div class="navmenulist"> 
    <label class="teext" style="cursor: pointer;" onclick=location.href="<?php echo BASE_URL . 'index.php' ?>">  ပင်မစာမျက်နှာ </label>
     <label class="teext" style="cursor: pointer;" onclick=location.href="<?php echo BASE_URL . 'articlelist.php'?>"> ဒစ်ဂျစ်တယ်ဖတ်စရာများ </label>
    <label class="teext" style="cursor: pointer;" onclick=location.href="<?php echo BASE_URL . 'materials.php'?>"> စာအုပ်စင် </label>
     <label class="teext" style="cursor: pointer;" onclick=location.href="<?php echo BASE_URL . 'digitalradio.php'?>"> ဒစ်ဂျစ်တယ်ရေဒီယို </label>
     <label class="teext" style="cursor: pointer;" onclick=location.href="<?php echo BASE_URL . 'about.php'?>"> လဖက်ရည်ဆိုင်အကြောင်း </label>
        <img src="<?php echo BASE_URL . 'static/images/search.png'?>" style="width: 24px; height: 24px; cursor: pointer;" onclick="appear2()">
    </div>
    
     
     
  
   
</header>

The Above codes will show web menu bar. By clicking the search icon appear2 function is called to show search popup box.
 
 
 
    <div id="searchpg2" class="wsearchbox"> 
    <form action="<?php echo BASE_URL . 'search.php' ?>" method="post"  >
    <input type="text"  id="key_word" name="key_word" placeholder="ဘာကိုရှာချင်ပါသလည်း?" class="wsearchf">
    <input type="submit" name="Search" class="wsearchbtn"></input>
    </form>
  
    </div>  

These above codes will show web search popup box

On submit the form action will submit the keyword to search result page search.php.
      
    if (isset($_POST['key_word'])) {
    $arts = getSearchArt($_POST['key_word']);
    $pods = getSearchPod($_POST['key_word']);
    $mats = getSearchMat($_POST['key_word']);
    }
     if (empty($_POST['key_word'])) {
  	$arts = getSearchArt('null');
    $pods = getSearchPod('null');
    $mats = getSearchMat('null');
    }
    
   This will check if  the key work is empty and call the functions in dth_function.php to find the key word in three tables and retrive the query.
   The rest of the codes in file  will show the search result.
   
   
   
    




