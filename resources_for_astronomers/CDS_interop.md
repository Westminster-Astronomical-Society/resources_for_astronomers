# Interoperability and APIs

## SAMP

The Simple Application Messaging Protocol (SAMP) is a communications protocol
that allows client software to exchange images and data. It was developed by the
International Virtual Observatory Alliance (IVOA) and is used widely in
astronomy.

The CDS website is SAMP enabled and wherever you see the small antenna icon,
that means you can send that image or table to any SAMP client. You must have a
SAMP hub running on your computer and one or more SAMP clients.

```{figure} _images/SAMP_1.png
---
width: 90%
name: cds_samp
---
SAMP enabled CDS
```

The software listed below are SAMP enabled. TOPCAT and Aladin are both hubs and
clients the others are clients only. There is also a standalone SAMP hub that
comes with [Astropy](https://docs.astropy.org/en/stable/samp/) that can be
started from the command line with the command `$ samp_hub`.

## CDS Aladin

Aladin ( [http://aladin.cds.unistra.fr/](http://aladin.cds.unistra.fr/) ) is an
interactive sky atlas for visualizing astronomical images and interactively
exploring astronomical catalogs and databases. The Aladin Sky Atlas comes in two
versions, Aladin Desktop to run locally on your computer and Aladin Lite, a
Javascript web application.

The Aladin Sky Atlas is well integrated with CDS and is SAMP enabled, obviously.
You can display and explore astronomical images from a large number of sources
in HiPS, FITS, and JPG or PNG formats, and overlay astronomical data from SIMBAD,
VizieR, and numerous other data sources. You can search for object IDs or
coordinates from the command bar or explore images and catalogs interactively
from the collections data tree. You can exchange data and images with other
applications (Carte du Ciel, DS9, TOPCAT, etc.) via SAMP. Clicking on the image
in the field will send coordinates to Carte du Ciel and vice versa.

See the Aladin [documentation](http://aladin.cds.unistra.fr/AladinDesktop/#Documentation)
for more information.

```{figure} _images/aladin_1.png
---
width: 90%
name: aladin_sky_atlas
---
Aladin Sky Atlas
```

There is also a Jupyter Aladin Lite extension that will enable interactive sky
visualization in Jupyter notebooks.
See the [CDS/ipyaladin](https://github.com/cds-astro/ipyaladin) Github page for
installation instructions and usage.

## TOPCAT

Tool for OPerations on Catalogues And Tables (TOPCAT) is an interactive
graphical viewer and editor for tabular data. TOPCAT is a SAMP hub and client
and can send and receive data from SAMP enabled applications and websites. It
can also query CDS and many other data repositories directly. It can filter,
compute statistics and plot information in astronomical data tables.

For additional information see the [TOPCAT help pages](https://www.star.bris.ac.uk/~mbt/topcat/sun253/index.html).

```{figure} _images/topcat_1.png
---
width: 90%
name: topcat_table_editor
---
TOPCAT table editor
```

## Carte du Ciel

Cartes du Ciel is a free and opensource skychart program that is very useful in
planning observations. It is SAMP enabled and can send and receive coordinates,
images and catalog data from other SAMP enabled applications and websites. You
can also load VO Tables from CDS as catalogs and search SIMBAD or Vizier by
object name or coordinates from the object properties menu.

For additional information see the
[Cartes du Ciel documentation](https://www.ap-i.net/skychart/en/documentation/start).

```{figure} _images/cdc_details.png
---
width: 90%
name: Cartes_du_Ciel
---
Carte du Ciel & CDS
```

```{figure} _images/cdc_vo_1.png
---
width: 90%
name: Cartes_du_Ciel_VO_1
---
Virtual Observatory Catalog
```

```{figure} _images/cdc_vo_2.png
---
width: 90%
name: Cartes_du_Ciel_VO_2
---
Virtual Observatory Catalog
```

```{figure} _images/cdc_vo_3.png
---
width: 90%
name: Cartes_du_Ciel_VO_3
---
Virtual Observatory Catalog
```

```{figure} _images/cdc_samp.png
---
width: 90%
name: Cartes_du_Ciel_samp
---
Carte du Ciel SAMP client
```

## Image viewers

SAOImage DS9 is an image display and visualization tool for astronomical data. It
can display astronomical images in the FITS format. It is a SAMP enabled client
and can send, receive, and display images and data from other SAMP clients. It
can also query many astronomical databases directly.

```{figure} _images/ds9_1.png
---
width: 90%
name: ds9_image_viewer
---
ds9 image viewer
```

## Online sky atlases

There are several online sky atlases the are built on and utilize CDS data.

- Aladin Lite [http://aladin.cds.unistra.fr/AladinLite](http://aladin.cds.unistra.fr/AladinLite)
- ESA Sky [https://sky.esa.int/esasky](https://sky.esa.int/esasky)
- World Wide Telescope [https://www.worldwidetelescope.org/webclient](https://www.worldwidetelescope.org/webclient)
