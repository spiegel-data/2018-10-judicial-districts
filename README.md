# Judicial districts in Germany

This repository hosts .geojson files with German *Landgerichtsbezirke* and *Oberlandesgerichtsbezirke*.

The Federal and State Ministries of Justice don't provide such geodata. For an article on [different degrees of penalty by judicial districts](http://www.spiegel.de/panorama/justiz/studie-wo-deutschlands-strengste-richter-sitzen-a-1230399.html) we created that geodata ourselves to be able to show the differences on a map.

How we did it: We scraped the responsible courts for all municipalities from the official [court directory](https://justiz.de/OrtsGerichtsverzeichnis/index.php) (using Python) and added missing information manually (using QGIS). Then we merged this data set with open data [shape files by the Federal Government for Geo-Information and Geodesy](http://www.geodatenzentrum.de/geodaten/gdz_rahmen.gdz_div?gdz_spr=deu&gdz_akt_zeile=5&gdz_anz_zeile=1&gdz_unt_zeile=0&gdz_user_id=0) and dissolved the municipalities' borders by the responsible courts (using Python/Geopandas).

The data represent the judicial districts in Germany as they have existed since 2013 until at least today (October 2018). (The former Landgerichtsbezirk Bautzen, as it existed until 2012, is part of the Landgerichtsbezirk Görlitz, now.)

Feel free to reuse and distribute the files (or add the missing ECLI codes for the Landgerichtsbezirke). Despite great care, we cannot guarantee the validity of the data set.