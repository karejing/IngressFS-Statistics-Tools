# IngressFS-Statistics-Tools
Useful tools to simplify scoring labor during IngressFS

Dependencies: [python2.7](https://www.python.org/downloads/release/python-2711/), [pandas](https://pypi.python.org/pypi/pandas/0.17.1/), [xlrd](https://pypi.python.org/pypi/xlrd), [openpyxl](https://pypi.python.org/pypi/openpyxl).

The latter three packages can be easily installed by [pip](https://pip.pypa.io/en/stable/installing/).

## 1. Merge pre-game recording sheets
Put all sheets in `PreGameRecordings` folder. All the sheets should have the same columns as `./PreGameRecordings/test1.xlsx`. Then
```bash
python Initial_Stats_Merge.py
```
`Merged_PreGameRecordingSheet.xlsx` is the merged sample.

## 2. Merge post-game recording sheets && Print the final winning agents
Put all sheets in `PostGameRecordings`. These sheets are generated by step 1 and filled in after the game<sup>[1](#footnote1)</sup>. Then
```bash
python Final_Stats_Sumup.py
```
The console should print the brief statistics of the winning agents and save it in `Recoring_Announce.txt`. `Final_Spreading_Sheet.xlsx` is the sample spreading scoring sheet.

<a name="footnote1">1</a>: The order of the recordings must not be changed! (Exactly same as the generated sheet.)
