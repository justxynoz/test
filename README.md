SOLARSYSTEM
PyPI version Documentation Status Build Status codecov Downloads

Our Solar System consists of:

our Star, the Sun
8 Planets: Mercury, Venus, Earth, Mars, Jupiter, Saturn, Uranus and Neptune
Some dwarf Planets: Pluto, Ceres, Eris, (Haumea, Makemake, Quaoar, Sedna, Orcus, 2007 OR10, not yet included here)
Some Centaurs: Chiron (onlyone included here)
Many moons orbiting planets. Our Moon (Selene in Greek or Luna in Latin) is orbiting Earth
solarsystem is a python library for finding position of planets around Sun or around Earth.

Also with solarsystem we can find positions around Sun/Earth of dwarf planets (only 3 planets so far) and Chiron Centaur and position of moon around Earth

Furthermore we compute sunrise/sunset, moonrise/moonset and moon phase for given place (geocoordinates).

Except all computation above with this library a set of usefull functions are included with which we can convert between coordinate systems:

Transform spherical to rectangular projection.
Transform rectangular to spherical projection.
Transform ecliptic to equatorial projection.
Transform equatorial to ecliptic projection.
Transform eclipitc to spherical projection.
Transform spherical to eclipitc projection.
     

Quick start
import solarsystem
Initialize class

H = solarsystem.Heliocentric(year=2020, month=1, day=1, hour=12, minute=0 )
Compute position of planets around sun

planets_dict=H.planets()
print('Planet','   \t','Longitude','   \t','Latitude','   \t','Distance in AU')
for planet in planets_dict:
    pos=planets_dict[planet]
    print(planet,'   \t',round(pos[0],2),'   \t',round(pos[1],2),'   \t',round(pos[2],2))
# Planet      Longitude    Latitude    Distance in AU
# Mercury     263.83       -4.06        0.47
# Venus       5.23         -3.22        0.73
# Earth       100.53        0.0         0.98
# Mars        214.38        0.49        1.59
# Jupiter     276.1         0.1         5.23
# Saturn      292.51        0.05        10.05
# Uranus      35.35         359.52      19.81
# Neptune     348.02       -1.04        29.91
# Pluto       292.75        359.33      33.88
# Ceres       290.87       -5.4         2.92
# Chiron      4.33          2.94        18.81
# Eris        23.55        -11.74       96.0
     

Examples - Use Cases
Solar System Live: https://github.com/IoannisNasios/solarsystem/blob/master/examples/Solar_System_Live.ipynb.

Plot planets around Sun, watch where planets are around Sun
Get the Geocentric positions of Sun, planets, nano planets, our Moon and 1 Centaur
RiseSet Calendar : https://github.com/IoannisNasios/solarsystem/blob/master/examples/RiseSet_Calendar.ipynb.

Time of sun rise and set within each day Time of moon rise and set within each day Moon phase - percent of illumination
     

Documentation
The full documentation is available at solarsystem.readthedocs.io    

Alternatively you can build documentation:

install sphinx

Go to docs/ directory

cd docs
Build html files

make html
Open _build/html/index.html in browser.

     

Installation
install from Pypi:

pip install solarsystem
Latest version from source:

pip install git+https://github.com/IoannisNasios/solarsystem
     

Requirements
No requirements, no additional libraries needs to be installed.

Exception: example notebook Solar System Live, matplotlib is needed in order to view the plot

     

Python versions
solarsystem is tested and runs normal for python versions 3.4+ and 2.7
running solarsystem on previous python versions should also run but use with caution.
     

Citing
If you find this library useful, please consider citing:

@misc{Nasios:2020,
  Author = {Ioannis Nasios},
  Title = {solarsystem},
  Year = {2020},
  Publisher = {GitHub},
  Journal = {GitHub repository},
  Howpublished = {\url{https://github.com/IoannisNasios/solarsystem}}
}
     

License
solarsystem is MIT-licensed. Read License