# CDS SIMBAD

SIMBAD: **S**et of **I**dentifications, **M**easurements, and **B**ibliography for **A**stronomical **D**ata.

[http://simbad.cds.unistra.fr](http://simbad.cds.unistra.fr)

SIMBAD is a dynamic database that provides basic information for many astronomical
objects such as name and identification, coordinates, magnitudes, proper motions
and parallax, velocity/redshift, size, spectral or morphological type, and
bibliographic information.

As of 2023-11-07 the SIMBAD data base contains:

- 16,943,427 objects
- 61,325,632 identifiers
- 426,969 bibliographic references

The only astronomical objects specifically excluded from SIMBAD are Solar System bodies.

You can query SIMBAD by object ID, coordinates, or by criteria (Ra, Dec, object
type, magnitude, etc.). There is also a TAP interface and the database can be
accessed through third party applications (Cartes du Ciel, Astroquery, etc.)

The [SIMBAD users guide](http://simbad.cds.unistra.fr/guide/index.htx) has additional information.


```{figure} _images/SIMBAD.png
---
width: 90%
name: SIMBAD-main
---
SIMBAD Object Database
```

## Query by object ID

You can query a single object ID, several objects using wildcards or a list. You can
also query all objects in a specified radius of your target.

```{figure} _images/SIMBAD_ID.png
---
width: 90%
name: SIMBAD-ID
---
SIMBAD Object ID Query
```

## Query by coordinates

You can query SIMBAD by coordinates and a search radius.

**The following formats are allowed:**

HMS DMS
: 16 41 41.6 +36 27 40.7  
16:41:41.6 +36:27:40.7  
16h41m41.6s +36d27m40.7s

DMS DMS
: 250d25m24.5s +36d27m40.7s

DH DD
:  16.694898h +36.461319d

DD DD
: 250.42347 +36.461319

You can search a single coordinate or a list of coordinates from a text file
with one coordinate per line. For large queries the CDS X-match service is
faster.

```{figure} _images/SIMBAD_coord.png
---
width: 90%
name: SIMBAD-coord
---
SIMBAD Object Coordinates Query
```

## Query by criteria

You can SIMBAD for various criteria and constraints using boolean operators.
Queriable criteria and allowed operators are listed on the query by criteria
page.

| operator | description                                | example                   |
| -------- | ------------------------------------------ | ------------------------- |
| =        | equality                                   | otype = '*'               |
| !=       | not equal                                  | otype != 'galaxy'         |
| <        | less than                                  | ubv.v < 5.5               |
| <=       | less than or equal                         | sptype <= 'G5'            |
| >        | greater than                               | pm > 10                   |
| >=       | greater than or equal                      | redshift >= 1.0           |
| ∼        | contains the wildcard expression           | author ∼ 'egret*'         |
| !∼       | does not contain the wildcard expression   |                           |
| in       | contains at least one value among the list | cat in ('hd','hip','ppm') |
| &        | and                                        | otype = '*'               |
| \|       | or                                         | otype = '*'               |

 You can also query by region or a defined shape; `circle`, `ellipse`, `zone`, `box`, `rotatedbox`, `polygon`.
 
 Examples:

- `dec > 85 & (cat = 'hip' | cat = 'ppm') & radvel > 10`
  Get all objects having a declination over 85 deg, a radial velocity over 10
  km/sec and being in either the hipparcos or the ppm catalog.

- `region(GAL,180 0,2d) & otype = 'G' & (nbref >= 10|bibyear >= 2000)`
  Find all galaxies in a 2 deg radius circle around the anti galactic center and
  having not less than 10 bibliographic references or references earlier then
  2000.

See the [SIMBAD users guide](http://simbad.cds.unistra.fr/guide/sim-fsam.htx) for additional information.


```{figure} _images/SIMBAD_criteria.png
---
width: 90%
name: SIMBAD-criteria
---
SIMBAD Object Criteria Query
```

## TAP query

The Table Access Protocol (TAP) is an access protocol used across many sites to
access astronomical data. TAP queries are written in the Astronomical Data Query
Language (ADQL) which is a superset of SQL. Those who have some experience with
SQL should find it familiar others will most likely not.

See the [SIMBAD ADQL guide](http://simbad.cds.unistra.fr/simbad/tap/help/adqlHelp.html)
for more information.

```{figure} _images/SIMBAD_TAP.png
---
width: 90%
name: SIMBAD-TAP
---
SIMBAD TAP Query
```

## Query results

```{figure} _images/SIMBAD_1.png
---
width: 90%
name: SIMBAD-TAP
---
SIMBAD TAP Query
```
