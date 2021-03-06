## ![Load Scenery Library](../images/icons/database.png "Load Scenery Library") Load Scenery Library Dialog {#load-scenery-library-dialog}

This dialog allows loading of the scenery library data from all four supported flight simulators into the _Little Navmap_ internal database. The scenery library to load can be selected in the `Simulator:` drop down box.

The dialog shows information about the currently selected database including the number of loaded airports, database version and more.

**FSX and P3D only:** The base path and the `scenery.cfg` path will be shown in two text edit fields for the currently selected simulator. These fields are populated automatically, but can be changed to any other valid location. All values are saved individually for each flight simulator type.

**X-Plane only:** X-Plane cannot be recognized automatically. You have to select the base path manually.
On Windows that can be a path like `C:\Simulators\X-Plane 11`, the executable being `C:\Simulators\X-Plane 11\X-Plane.exe`.

Loading a scenery library can take from 2 to 15 minutes depending on your setup and amount of scenery add-ons. You can speed this up by excluding directories containing neither airport nor navigation data in the `Options` dialog on the `Scenery Library Database` tab.

For FSX/P3D, all airports that are not located in the default `Scenery` directory of FSX/P3D are considered to be add-on airports. For X-Plane, all airports located in the `Custom Scenery` directory of X-Plane are considered to be add-on airports. Add-on airports are highlighted on the map using emphasized \(bold and italic\) text.

If an add-on only corrects airport elevations or navigation data, it might be undesirable to display the updated airports as add-on airports on the map. You can exclude folders populated by this add-on from the add-on recognition in the `Options` dialog on the `Scenery Library Database` tab.

See [Options](OPTIONS.md#scenery-library-database) for more information about excluding scenery.

If you cancel the loading process or if the loading process fails, the previous scenery library database is restored immediately.

The menu `Scenery Library` -&gt; `Flight Simulators` is synchronized with the simulator selection in the dialog. Once a database is successfully loaded, the display, flight plan and search switch instantaneously to the newly loaded simulator data.

Note that the final number of airports, navaids and other objects shown in the `Load Scenery Library` dialog are lower than the counts shown in the progress dialog, because, after the data has been loaded, a separate process removes duplicates and deletes stock airports that were replaced by add-ons.

**FSX or P3D only:** The program tries to find the base paths and `Scenery.cfg` files automatically. The typical locations of the `Scenery.cfg` for Windows 7/8/10 are:

* **Flight Simulator X:** `C:\ProgramData\Microsoft\FSX\Scenery.cfg`
* **Flight Simulator - Steam Edition:** `C:\ProgramData\Microsoft\FSX-SE\Scenery.cfg`
* **Prepar3D v2:** `C:\Users\YOUR_ACCOUNT_NAME\AppData\Roaming\Lockheed Martin\Prepar3D v2\Scenery.cfg`
* **Prepar3D v3:** `C:\ProgramData\Lockheed Martin\Prepar3D v3\Scenery.cfg`
* **Prepar3D v4:** `C:\ProgramData\Lockheed Martin\Prepar3D v4\Scenery.cfg`

An error dialog is shown after loading if any files could not be read or directories were not found. In this case you should check if the airports of the affected sceneries display correctly and show the correct information. The error dialog allows copy and paste of formatted text which is useful for error reporting.

The `Load Scenery Library` dialog shows the last time of loading \(`Last Update:`\), the program and the database version. Major database version differences indicate incompatible databases. The program will ask if the incompatible databases can be erased on startup before the scenery database can be reloaded. Minor database differences indicate compatible changes where a reload is recommended but not required.

### X-Plane Airports and Navdata {#load-scenery-library-dialog-xp-apt-navdata}

*Little Navmap* reads airport and navaid data from X-Plane's `*.dat` files. To check a version of a file you can open it in a text editor that is capable of dealing with large files. The first lines of the file will look like:

```
A
1100 Generated by WorldEditor 1.6.0r1

1   1549 0 0 0A4 Johnson City STOLport
...
```
The first number in the second line is the file version. Here it is `1100`.

*Little Navmap* can read the following X-Plane scenery files:

* **Airports \(**`apt.dat`**\):** Version 850 up to 1100. This covers X-Plane 10 airports and older add-on scenery. Newer files than 1100 might work but are not tested.
* **Navdata \(**`earth_awy.dat`**, **`earth_fix.dat`** and **`earth_nav.dat`**\):** Version 850 up to 1100. This excludes X-Plane 10 navdata files. Newer files than 1100 might work but are not tested.
* **Procedures \(**`ICAO.dat`** in the **`CIFP`**directory\):** All procedures from X-Plane 11.
* **Airspaces \(**`*.txt`**\):** The included `usa.txt` and all files in OpenAir format. See next chapter for more information.

Additionally the files `user_fix.dat` and `user_nav.dat` in the X-Plane directory `Custom Data` are read.

### X-Plane Airspaces {#load-scenery-library-dialog-xp-airspaces}

All files in [OpenAir airspace format](http://www.winpilot.com/UsersGuide/UserAirspace.asp) will be loaded when reading the X-Plane scenery library.

You can also copy airspaces from a present FSX or Prepar3D database if you own these simulators. See [Copy Airspaces to X-Plane Database](MENUS.md#copy-airspaces-to-xplane).

Note that airspace files can have errors which may prevent the loading of an airspace file. These hard errors are reported after loading the scenery library. Other errors only affecting single airspaces or the geometry are reported in the log file only.

X-Plane 11 comes with a single airspace file that can be found in `YOUR_XPLANE_DIRECTORY/Resources/default data/airspaces/usa.txt`.
Additional airspace files can be downloaded from the [OpenAirspace Directory](http://www.winpilot.com/openair/index.asp), [Soaring Services](http://soaringweb.org/), [openAIP](https://www.openaip.net/) or [Luftraumdaten Deutschland](https://www.daec.de/fachbereiche/luftraum-flugbetrieb/luftraumdaten) for example.

Airspace files must have a `.txt` extension and are loaded from the following directories by *Little Navmap*:

* `YOUR_XPLANE_DIRECTORY/Resources/default data/airspaces`
* `YOUR_XPLANE_DIRECTORY/Custom Data/Airspaces`
* `YOUR_ACCOUNT_NAME/Documents/Little Navmap/X-Plane Airspaces` where `Documents` is the documents directory in your language.

The files can be encoded in any [UTF](https://en.wikipedia.org/wiki/Unicode#UTF) format but must have a [BOM](https://en.wikipedia.org/wiki/Byte_order_mark) to be recognized properly. Otherwise Windows ANSI coding \(`Windows-1252`\) is used. Special characters like umlauts or accents are not displayed correctly in names if the encoding is not correct. All other functionality is unaffected.

You can convert the files using any advanced editor like [Notepad++](https://notepad-plus-plus.org/) for example.

Airspaces will appear as duplicates in the map if an airspace file is found in more than one of these directories.

**If X-Plane crashes when loading certain airspace files, move these files to the folder `Documents/Little Navmap/X-Plane Airspaces` instead. This way, the airspaces are at least available in *Little Navmap* which is more error tolerant.**

### Load Scenery Library Dialog Options {#load-scenery-library-dialog-options}

* `Simulator`: Select the simulator to load, show database statistics in the label above.
* `Reset Paths`: Reset all paths back to default values.
* `Flight Simulator Base Path` and `Select ...`: The path to the base directory of the selected flight simulator. This usually the directory containing the `FSX.exe` or `Prepar3D.exe`. This is the base for all relative paths found in the `scenery.cfg` file.
* `Scenery Configuration File` and `Select ...` \(only FSX and P3D\): The file `scenery.cfg` of the simulator. You can also create copies of the original file, modify them by removing or adding sceneries and select them here for loading.
* `Read inactive Scenery Entries` \(only FSX and P3D\): This will read all scenery entries, also the inactive/disabled ones. This is helpful if you use a tool to disable scenery before flying but still want to see all add-on sceneries in _Little Navmap_ without reloading.
* `Read Prepar3D add-on.xml packages` \(only P3D v3 and v4\): If enabled, reads P3D v4 or v3 `add-on.xml` packages. These are read from subdirectories of `C:\Users\YOURUSERNAME\Documents\Prepar3D v4 Files\Add-ons` and `C:\Users\YOURUSERNAME\Documents\Prepar3D v4 Add-ons`.
* `Load`: Starts the database loading process. You can stop the loading process at any time and the previous database is restored. The dialog is closed and the program will switch to show the loaded database once it is successfully loaded.
* `Close`: Keep all settings and changes in the dialog and close it without loading anything.

![Load Scenery Dialog](../images/loadscenery.jpg "Load Scenery Dialog")

_**Picture above:** Load Scenery Dialog. Scenery data is already loaded for FSX._

![Load Scenery Progress Dialog](../images/loadsceneryprogress.jpg "Load Scenery Progress Dialog")

_**Picture above:** Progress dialog shown while loading the scenery library into Little Navmap's internal database._

