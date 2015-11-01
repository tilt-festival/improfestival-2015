(function ($, root, undefined) {

    $(function () {

        'use strict';


        // Init FB library
        (function (d, s, id) {
            var js, fjs = d.getElementsByTagName(s)[0];
            if (d.getElementById(id)) return;
            js = d.createElement(s);
            js.id = id;
            js.src = "//connect.facebook.net/en_US/all.js#xfbml=1";
            fjs.parentNode.insertBefore(js, fjs);
        }(document, 'script', 'facebook-jssdk'));

        // Manipulate event list chevrons
        var iconRight = 'fa-chevron-circle-right';
        var iconDown = 'fa-chevron-circle-down';
        $('.event-item .collapse').on('hide.bs.collapse', function () {
            $(this).parent().find('i').removeClass(iconDown).addClass(iconRight);
        }).on('show.bs.collapse', function () {
            $(this).parent().find('i').removeClass(iconRight).addClass(iconDown);
        });

        $('.menu-toggle').sidr({
            source: '#sidebar-nav nav',
            displace: false,
            renaming: false
        });

        $('#sidr').onePageNav({
            end: function () {
                $.sidr('close', 'sidr');
            }
        });


        // Open Google Maps on location link click
        $('.map-link').click(function(){
            $(this).closest('.row').find('.modal').modal().on('shown.bs.modal', function(){

                // Fix map resize bug
                google.maps.event.trigger($(this).find('.em-locations-map').get(0), "resize");
            });
        });
    });

})(jQuery, this);
