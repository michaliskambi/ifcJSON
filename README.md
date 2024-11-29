# Python scripts to do IFC JSON <-> IFC (STEP) conversion

## About this fork (michaliskambi/ifcJSON)

This is a fork of https://github.com/buildingsmart-community/ifcJSON to make the Python conversion (_IFCJSON->IFC (STEP)_) script work:

- on latest Debian/Ubuntu systems,
- with latest IfcOpenShell,
- IFC JSON files produced by latest [BonsaiBIM](https://bonsaibim.org/) and [Castle Game Engine](https://castle-engine.io/ifc) (with `type="IFC.JSON"` inside).

Summary of usage:

```
# install dependencies
sudo apt install python-is-python3
pip install ifcopenshell

# If above answers "error: externally-managed-environment",
# - Read what it says.
# - Consider using a virtual environment, as advised there.
# - If you want a quick way, on your own head be it:
pip install ifcopenshell --break-system-packages

# clone this repo
git clone https://github.com/michaliskambi/ifcJSON

# use the script, replace filenames with your own
cd ifcJSON/file_converters
python json2ifc.py -i ~/Desktop/input.ifcjson -o ~/Desktop/output.ifc
# proper output should look like this:
# > Reading ifcJson file: ....
# > Conversion took  ....  seconds
```

# ifcJSON-4
This repository contains the specification for ifcJSON-4 - version in sync with IFC EXPRESS Schema.

## What
JSON is used throughout the world for exchanging and using data. Building data needs to be available in JSON. Therefore, IFC needs to be available in JSON format.

ifcJSON aims primarily at addressing the following problems with IFC:
1. Many developers have never seen/used EXPRESS or STP instance files before, which increases the effort required to extract data required from them.
2. IFC instance populations are typically exchanged as files, which is at odds with linked, distributed, and rapidly changing data seen on most design and construction projects and products.

ifcJSON seeks the best balance between a best practice JSON representation AND compatibility with the IFC source schema.

Main focus:
- Backward compatibility
- Round-trip
- Parallel to EXPRESS schema

To a lesser degree (Due to adhering to the IFC schema):
- Human-readability
- Integration with code
- Clear referencing structure
- Direct usability

The initial standard will be developed based on IFC4 and more specifically IFC4.3.
IFC5 developments will be closely followed, especially for expected improvements in human-readability.

## Getting started
The repository is organised in different sections:
- [Documentation](Documentation): your starting point to find out what this ifcJSON is about
- [Samples](Samples): ifcJSON data examples
- [Schema](Schema): ifcJSON schemas
- [File converters](file_converters): Python tools for reading and converting between ifcJSON and IFC SPF
- [Schema converters](schema_converters): Python tools for converting IFC schemas into JSON-Schema

## More information
Contributions are welcome in all possible ways. Your first starting point is creating GitHub issues. Feel free to get in touch with the people in the ifcJSON-team.
