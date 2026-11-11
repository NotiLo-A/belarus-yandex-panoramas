# Belarus yandex panoramas

<img width="250" height="150" alt="image" src="https://github.com/user-attachments/assets/0e74cae2-1483-47c4-b9ed-f8428ba939e9" />
<img width="250" height="150" alt="image" src="https://github.com/user-attachments/assets/3d3c9632-c423-45ee-ac46-6f52c0e346d9" />
<img width="250" height="150" alt="image" src="https://github.com/user-attachments/assets/1ce82e89-5c8d-4aa5-a5a1-f0bace0bb708" />

## About
Yandex Street View panorama dataset across Belarus - including coordinates, panorama IDs (`oid`, `imageId`), street names, capture dates and timestamps, camera origin, nearby address markers, companies, and historical panorama links - along with a browser-based parser ([`index.html`](index.html)) to collect your own. Ready-to-use datasets are available on the [Releases](https://github.com/NotiLo-A/belarus-yandex-panoramas/releases) page. Useful for maps, GeoGuessr-style games, and geospatial projects.

## Dataset Overview and Spatial Distribution
The dataset presented herein was systematically acquired on **November 3, 2026**. It aggregates a total of 259,536 precise geospatial coordinate points across six major administrative subdivisions. The proportional distribution of panoramic points is illustrated below:

<img width="500" alt="chart" src="https://github.com/user-attachments/assets/d5d635f3-ea38-44a5-9b61-3e3b844af75a" />


| Administrative Division | Coordinate Points | Proportion |
|-------------------------|-------------------|------------|
| Minsk                   | 145,193           | 55.94%     |
| Gomel                   | 36,983            | 14.25%     |
| Brest                   | 21,784            | 8.39%      |
| Grodno                  | 19,924            | 7.68%      |
| Mogilev                 | 19,270            | 7.42%      |
| Vitebsk                 | 16,382            | 6.31%      |

## How it works
Open [`index.html`](index.html) through a local server, pick a starting point, and the page walks through connected Yandex panoramas directly in your browser. It handles rate limits automatically, saves progress in `IndexedDB` so you can pause and resume anytime, and lets you export the results as `.geojson` or `.coordinates.txt`.

## How to use
If you just want the data, download the ready-made files from [Releases](https://github.com/NotiLo-A/belarus-yandex-panoramas/releases).

To run the parser yourself, start a local HTTP server in this folder (needed for OpenStreetMap tiles to load properly):

```bash
npx serve
```

```bash
python3 -m http.server
```

1. Open the local URL in your browser (for example, `http://localhost:3000` or `http://localhost:8000`).
2. Pick a city from the list, or add your own with **`+ add city`**.
3. Choose where to start: check **`start by clicking the map`** and click on the map, press **`City center`**, or paste an OID, link, or coordinates into **`Panorama OID`**.
4. Hit **`Start`** (you can **`Pause`** or **`Stop`** anytime) and export **`panoramas (.geojson)`** or **`Coordinates (.txt)`**.
