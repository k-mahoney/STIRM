# STIRM: Web Content Guide

#### Server Access

Note: If you're connecting from outside the JHU network, you must first connect to the JH VPN (JHPulse). Information about the VPN is at http://www.it.johnshopkins.edu/services/network/JHPulse/ as well as directions on installing and configuring it.

**Mac OSX**

1. In the Finder menu select `Go` then the last option, `Connect to Server`.
2. In the `Server Address` field enter `https://webdav.johnshopkins.edu/your-JHED-id` where “your-JHED-id” is your JHED account name.
3. Click the button with the plus sign to add this to the `Favorite Servers` menu.
4. Click `Connect`.
5. Enter your JHED ID and password in the pop-up window.

For directions on other operating systems, see the JHU page on [WebDav Access](https://it.johnshopkins.edu/services/webservices/webdav/).

#### Fieldwork

To add a new point to the **Fieldwork** map, first you'll have to add a new location (e.g. `loc5`) to the listing beneath `function initialize()`. Then, add a new variable declaration to the listing beginning with `var marker1 = new google.maps.Marker`. Refer to the code excerpt below:

	function initialize() {
		loc1 = new google.maps.LatLng(-35.909,-72.733);
		loc2 = new google.maps.LatLng(-43.53,172.620278);
		loc3 = new google.maps.LatLng(32.128,-115.303);
		loc4 = new google.maps.LatLng(40.638967,-74.251099);
		
		// NEW LOCATION EXAMPLE
		newLoc = new google.maps.LatLng(LATITUDE,LONGITUDE);

		var mapOptions = {
			center: new google.maps.LatLng(12,0),
			zoom: 2.13
		};
		var map = new google.maps.Map(document.getElementById("map-canvas"), mapOptions);
		var marker1 = new google.maps.Marker({
			position: loc1,
			map: map,
			title: 'Chile, 2010'
		});
		var marker2 = new google.maps.Marker({
			position: loc2,
			map: map,
			title: 'Christchurch, 2010-2011'
		});
		var marker3 = new google.maps.Marker({
			position: loc3,
			map: map,
			title: 'Easter Earthquake, 2010'
		});
		var marker4 = new google.maps.Marker({
			position: loc4,
			map: map,
			title: 'Hurricane Sandy, 2012'
		});
		
		// NEW MARKER EXAMPLE
		var newMarker = new google.maps.Marker({
			position: newLoc,
			map: map,
			title: 'Field Work Location Title Here'
		});
		
	}
	google.maps.event.addDomListener(window, 'load', initialize);
	
To add a new listing below the **Fieldwork** map, add the following below the `<!-- Page Content -->` comment header and the second `<div class="row">` header:

    <div class="col-md-6">
        <table>
            <tr>
                <td>
                    <img class="img-circle img-responsive" src="assets/images/FIELDWORK Photo" alt="">
                </td>
                <td></td>
                <td>
                    <h4><b>Location, Date</b></h4>
    				<p>Description of fieldwork.</p>
                    <br>
    				<a href="LINK TO PHOTOS"><i class="fa fa-file-image-o"></i> Photos</a>
    				<br>
                 </td>
             </tr>
        </table>
    </div>
            
#### People

*To be updated.*
