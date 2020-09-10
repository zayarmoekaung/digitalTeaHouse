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
 
 <div id="searchpg2" class="wsearchbox">
  <form action="<?php echo BASE_URL . 'search.php' ?>" method="post"  >
  <input type="text"  id="key_word" name="key_word" placeholder="ဘာကိုရှာချင်ပါသလည်း?" class="wsearchf">
 <input type="submit" name="Search" class="wsearchbtn"></input>
  </form>
  
</div>  

These above codes will show web search popup box

 
 
 
 On submit the form action will submit the keyword to search result page.
      





