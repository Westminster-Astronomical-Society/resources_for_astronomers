# CDS SIMBAD

SIMBAD: **S**et of **I**dentifications, **M**easurements, and **B**ibliography for **A**stronomical **D**ata.

[http://simbad.cds.unistra.fr](http://simbad.cds.unistra.fr)

SIMBAD is a database that provides basic information for many astronomical
objects such as name and identification, coordinates, magnitudes, proper motions
and parallax, velocity/redshift, size, spectral or morphological type, and
bibliographic information. It is a dynamic resource that is updated daily.

As of 2023-11-07 the SIMBAD data base contains:

- 16,943,427 objects
- 61,325,632 identifiers
- 426,969 bibliographic references

SIMBAD does not contain information for Solar System bodies.

You can query SIMBAD by object ID, coordinates in sexagesimal or decimal
degrees, or by criteria (Ra, Dec, object type, magnitude, etc.). There is also a
TAP (Table Access Protocol) interface and the database can be accessed through
third party applications (Cartes du Ciel, Astroquery, etc.)

The [SIMBAD users guide](http://simbad.cds.unistra.fr/guide/index.htx) has additional information.

```{figure} _images/SIMBAD.png
---
width: 90%
name: SIMBAD-main
---
SIMBAD Object Database
```

## Query by object ID

You can query a single object ID, or several objects in a text file containing one item per line.

Wildcards and ranges can be used in identifiers.

`*` : Any string of characters (including an empty one)

`?` : Any single character.

`[abc]` : Exactly one character taken from the list.

`[A-Z]` : One character from a range.

`[^0-9]` : Any character not in the list.

You can also query all objects within a specified radius of your target.

```{figure} _images/SIMBAD_ID.png
---
width: 90%
name: SIMBAD-ID
---
SIMBAD Object ID Query
```

## Query by coordinates

You can query SIMBAD by coordinates and a search radius. You can search a single
coordinate or a list of coordinates from a text file with one coordinate per
line. For large queries the CDS X-match service is faster.

**The following coordinate formats are allowed:**

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

In general sexagesimal coordinates are in HMS DMS  and decimal coordinates are
in degrees unless a unit is specified.

```{figure} _images/SIMBAD_coord.png
---
width: 90%
name: SIMBAD-coord
---
SIMBAD Object Coordinates Query
```

## Query by criteria

You can SIMBAD for various criteria and constraints using boolean operators.
Queryable criteria and allowed operators are listed on the query by criteria
page.

| operator | description                                | example                   |
| -------- | ------------------------------------------ | ------------------------- |
| =        | equality                                   | otype = '*'               |
| !=       | not equal                                  | otype != 'galaxy'         |
| <        | less than                                  | Bmag < 8.5                |
| <=       | less than or equal                         | sptype <= 'G5'            |
| >        | greater than                               | pm > 10                   |
| >=       | greater than or equal                      | redshift >= 1.0           |
| ∼        | contains the wildcard expression           | author ∼ 'barnard*'       |
| !∼       | does not contain the wildcard expression   | author !∼ 'barnard*'      |
| in       | contains at least one value among the list | cat in ('hd','hr','sao')  |
| &        | and                                        | dec > 40d & dec < 80d     |
| \|       | or                                         | otype = 'C*' | otype = S* |

 You can also query by region or a defined shape; `circle`, `ellipse`, `zone`, `box`, `rotatedbox`, `polygon`.

 Examples:

- `dec > 85 & cat in ('hd', 'hr', 'sao') & otypes= V*`
  Get all variable stars having a declination over 85 deg, and in either the Henry Draper,
  Yale Bright Star or SAO catalogs.

- `region(circle, 'M81', 2d) & otype = 'G' & (Bmag < 14 | Vmag < 14 | Rmag < 14)`
  Find all galaxies in a 2 deg radius circle around Messier 81 and B, V, or R mag less than 14.

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
SQL should find it familiar others would most likely prefer alternate interfaces
such as astroquery.

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

The information returned by a SIMBAD query includes:

- Basic data (coords, magnitudes, pm, parallax, etc.)
- An Aladin thumbnail of the region around the target
- Linked objects, children and parents
- A list of identifiers
- List of bibliographic references
- List of measurements (pm, plx, distances, etc.)
- Links to external archives and to the catalogues in VizieR

```{figure} _images/SIMBAD_1.png
---
width: 90%
name: SIMBAD-results
---
SIMBAD SIMBAD Query
```
