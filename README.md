# index.php
wp_nav_menu(array(
        'theme_location' => 'bootrtrap-menu',
        'menu_class' => 'nav navbar-nav',
        'depth'             => 7,
        'walker'            => new wp_bootstrap_navwalker()
    ));
    
    
    
    
    
# add to your jquery file
(function($){
                $(document).ready(function(){
                    $('ul.dropdown-menu [data-toggle=dropdown]').on('click', function(event) {
                        event.preventDefault();
                        event.stopPropagation();
                        $(this).parent().siblings().removeClass('open');
                        $(this).parent().toggleClass('open');
                    });
                });
})(jQuery);



    
    
# add to your css file
.dropdown-menu {
     top:0;
     left:100%;
     margin-top:-6px;
     margin-left:-1px;
 }
.navbar-nav>li>.dropdown-menu {
    margin-top: 50px;
    margin-left: -103px;
}
.dropdown-menu>.active>a, .dropdown-menu>.active>a:focus, .dropdown-menu>.active>a:hover{
    color: #000;
}
.dropdown-menu .caret{
    transform: rotate(-95deg);
}
.navbar {
    border-radius: 0;
}
