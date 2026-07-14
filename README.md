# WebGPU Capability Check

Eine einzelne HTML-Datei, die in Sekunden zeigt, ob dein Browser/Gerät WebGPU
unterstützt – und vor allem, welche Features und Limits konkret verfügbar
sind. Kein Build, keine Abhängigkeiten, kein Server nötig: einfach öffnen.

## Warum

WebGPU-Unterstützung ist auf Mobilgeräten sehr uneinheitlich: unterschiedliche
Chrome-Versionen, GPU-Hersteller (Mali, Adreno, Apple) und sogar einzelne
GPU-Generationen innerhalb eines Herstellers unterstützen unterschiedliche
Feature-Sets. Optionale Erweiterungen wie `shader-f16` fehlen auf vielen
Geräten komplett, auch wenn WebGPU selbst grundsätzlich läuft.

Wer eine WebGPU-Compute-Pipeline plant, sollte das **zuerst am echten Gerät
prüfen**, bevor Zeit in Shader-Code investiert wird, der am Ende mangels
Adapter oder fehlender Extension gar nicht ausführbar ist.

## Was der Check zeigt

- Ob `navigator.gpu` überhaupt existiert
- Ob `requestAdapter()` einen nutzbaren Adapter liefert
- Adapter-Info (Vendor, Architektur, Gerätebezeichnung, sofern vom Browser
  preisgegeben)
- Verfügbare Features, u.a. `shader-f16`
- Ob sich erfolgreich ein `GPUDevice` erstellen lässt
- Zentrale Compute-Limits (`maxComputeWorkgroupSizeX`,
  `maxStorageBufferBindingSize`, `maxComputeInvocationsPerWorkgroup`)

## Nutzung

Datei öffnen (lokal oder über GitHub Pages) – der Check läuft automatisch
beim Laden und zeigt das Ergebnis direkt auf der Seite an. Kein Tippen, kein
Klicken nötig.

## Hinweis

Das Ergebnis gilt nur für die konkrete Kombination aus Gerät, GPU-Treiber und
Browser-Version, mit der die Seite geöffnet wurde – nicht allgemein für ein
Geräte- oder Chipmodell. Browser-Updates können die unterstützten Features
jederzeit ändern (in beide Richtungen).


## Lizenz / License

MIT License

Copyright (c) 2026 Hazeberry

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## Entstehung / Development

Entwickelt von [Hazeberry](https://github.com/Hazeberry), unter Mitarbeit von Claude (Anthropic) — iterativ getestet und verifiziert.
Developed by [Hazeberry](https://github.com/Hazeberry), with assistance from Claude (Anthropic) — iteratively tested and verified.

