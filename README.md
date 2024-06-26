# SCIA XML reader
This python package allows retrieval of SCIA Engineer results from an exported xml. Basic use is done in two steps: Reading the xml and parsing the data. An example is given below.

```
from scia_xml_reader.functions import read_xml
from scia_xml_reader import parser

root = read_xml(Path("your.xml"))

scia_nodes = parser.parse_nodes(root)
scia_beams = parser.parse_beams(root)
scia_loadcases = parser.parse_loadcases(root)
scia_loadcombinations = parser.parse_loadcombinations(root)
scia_results_force_1d = parse_results_force_1d(root)
```

## Objects
Currently the `scia_xml_reader` package is able to read the following data from the xml file:
* Node
* Beam
* Loadcase
* Loadcombination
* ResultForce1D