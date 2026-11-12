# Turtle to Helper

Use the tool here: https://adituv.github.io/turtle-to-helper

## Description

"Turtle to Helper" converts the data from exporting scout locations on [Turtle Scouter](https://scout.turtlehunts.app/) into the format used by the
Dalamud plugin [Hunt Helper](https://github.com/img02/HuntHelper).  This in theory allows hunt train conductors that use the plugin for organization
to avoid rescouting the train before they run it.  (Please use your own judgement though: if the scout is old, better to check it anyway!)

## Technical Details

Hunt Helper exports data as a base64-encoded, gzip-compressed, json array of objects.  One example object is:

```json
{
    "Name": "Hulder",
    "MapName": "Labyrinthos",
    "Instance": 0,
    "Position": { "X": "10.6", "Y": "19.3" },
    "MobID": 10624,
    "TerritoryId": 956,
    "MapID": 695,
    "Dead": false,
    "LastSeenUTC": "2026-11-12T01:13:24.6620000Z"
}
```

I haven't looked at the source for Hunt Helper to verify which fields are required, so this project produces JSON identical to that of a
Hunt Helper export.  As it uses internal FFXIV ids for the monster, territory and map, there is a lot of hardcoded data.

## AI Usage

The HTML and CSS for the page were AI generated.  The Javascript was handwritten.
