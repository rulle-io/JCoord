This is a repo of the 2006 [Jcoord](http://www.jstott.me.uk/jcoord) project so that it can be maintained by the open-source community.

Please see commits for history beyond the author's original 1.1-b version.

Below is the original readme.txt

```
--------------------------------------------------------------------------
 Jcoord
 readme.txt
 
 (c) 2006 Jonathan Stott
 
 Created on 11-Feb-2006
--------------------------------------------------------------------------

Jcoord is a collection of Java classes that provide functions for handling
various co-ordinate systems and converting between them. Currently, OSGB
(Ordnance Survey of Great Britain) grid references, UTM (Universal Transverse
Mercator) references and latitude/longitude are supported. A function is 
also provided to find the surface distance between two points of latitude
and longitude.

When using the OSGB conversions, the majority of applications use the
WGS84 datum rather than the OSGB36 datum. Conversions between the two
data were added in v1.1 - the conversions should be accurate to within
5m or so. If accuracy is not important (i.e. to within 200m or so),
then it isn't necessary to perform the conversions.

Examples of how to use the classes in Jcoord can be found in the
uk.me.jstott.jcoord.Test class

See http://www.jstott.me.uk/jcoord/ for latest releases and information.


DISCLAIMER

Accuracy of the co-ordinate conversions contained within the Jcoord
package is not guaranteed. Use of the conversions is entirely at your
own risk and I cannot be held responsible for any consequences of
errors created by the conversions. I do not recommend using the package
for mission-critical applications.


LICENSING

This software product is available under the GNU General Public License
(GPL). Terms of the GPL can be read at http://www.jstott.me.uk/gpl/.
Any commercial use requires the purchase of a license - contact me at
jcoord@jstott.me.uk for details.


VERSION HISTORY

 1.1 -
  - Added Junit unit test suite in the uk.me.jstott.jcoord.junit package.
  - Added NotDefinedOnUTMGridException which is thrown whenever an attempt is
    made to convert a LatLng object to a UTMRef object where the latitude falls
    outside the defined UTM grid.
  - Can format a latitude/longitude into a String in degrees-minutes-seconds
    format.
  - Added a class for Military Grid Reference System (MGRS) to allow for
    conversrions between MGRS and UTM and latitude/longitude.
  - Documentation (javadoc) improvements.
  - LatLng.getLat() has been deprecated. Use LatLng.getLatitude() instead.
  - LatLng.getLng() has been deprecated. Use LatLng.getLongitude() instead.
  - LatLng constructor now validates parameters and throws an
    IllegalArgumentException if either the latitude or longitude are invalid.
  - UTMRef(double,double,char,int) constructor has been deprecated and
    replaced with UTMRef(int,char,double,double). This is to make the order of
    the parameters more sensible.
  - Fixed slight error with values for converting between WGS84 and OSGB36.
  - New method: LatLng.distanceMiles(LatLng) to calculate the distance between
    two points of latitude/longitude in miles.
  - New constructors in LatLng to allow for specifying a datum and/or the
    latitude and longitude as degrees/minutes/seconds.
  - Added IrishRef class to allow conversion between latitude and longitude and
    Irish National Grid References.
  - Added new uk.me.jstott.jcoord.datum package with a number of data that
    all extend uk.me.jstott.jcoord.datum.Datum.
  - Added new uk.me.jstott.jcoord.ellipsoid package with a number of definitions
    of reference ellipsoids that all extend
    uk.me.jstott.jcoord.ellipsoid.Ellipsoid.
  - Fixed slight errors in OSRef to LatLng conversions.
 1.0 - 11 Feb 2006
  - Initial version created from PHPcoord v2.2.
```