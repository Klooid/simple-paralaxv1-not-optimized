simple-paralaxv1
================

Simple paralax jQuery

Here's the script

1. html

    <span>Text</span>
    
    <div id='cont-1'>
        
    </div>
    
    <div id='cont-2'>
        <h1>
            KLOOID
        </h1>
        <p>
            Networking solutions
        </p>
    </div>
    
    <div id='cont-3'>
        
    </div>


1. jQuery

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
