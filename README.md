simple-paralaxv1
================

Simple paralax jQuery

Here's the script

    $(document).ready(function(){
        $(document).scroll(function(){
            topdistace = $('#cont-2').offset().top;
            windscroll = $(window).scrollTop();
            topdistan = windscroll-topdistace;
            windowheis = $(window).height();
            totalhietgh = windscroll+windowheis;
            
            $('span').text(windscroll+windowheis+' '+topdistace);
                    
            if(totalhietgh >= topdistace) {
                ehidsd = topdistace-windscroll;
                totslit = ehidsd-windowheis;
                lowspeed = totslit/3;
                $('span').text(lowspeed);
                $('#cont-2').css('background-position', '0px '+lowspeed+'px');
            } 
            else {};
        });
});


By Klooid.com
