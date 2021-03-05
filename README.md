# buga-solar-data
Daten der Solaranlage für den Farmbot auf der Bundesgartenschau 2019

Die Daten sind in mehreren Dateien, die Header sind pro Datei unterschiedlich!


| Spalte             | Format  | Erklärung                                                                     |
|--------------------|---------|-------------------------------------------------------------------------------|
| name               | String  | Bezeichnung für den Datensatz (im vorliegenden Datensatz immer waittimes)     |
| time               | Integer | fortlaufende Anzahl der Nanosekunden seit dem 1. Januar 1970 (Unix-Timestamp) |
| BatteryCurrent     | Float   | Batteriestrom in Ampere (positiv -> laden, negativ -> entladen)               |
| BatteryVoltage     | Float   | Batteriespannung in Volt                                                      |
| ChargeCurrent      | Float   | Ladestrom in Ampere                                                           |
| ChargeState        | Integer | Ladezustand: 0 = Off, 2 = Fault, 3 = Bulk, 4 = Absorption, 5 = Float          |
| ChargerTemperature | Float   | Temperatur des Ladereglers in °C                                              |
| LoadCurrent        | Float   | Strom der Last in Ampere                                                      |
| LoadOutputVoltage  | Float   | Spannung an der Last                                                          |
| LoadPower          | Float   | Energieverbrauch* der Last in Watt                                            |
| SolarPower         | Float   | Aktuelle Energieerzeugung* in Watt                                            |
| SolarPowerNew      | Float   | Aktuelle Energieerzeugung* in Watt (als float, nicht immer vorhanden)         |
| SolarVoltage       | Float   | Spannung des/der Solarpanels in Volt                                          |
| YieldTotal         | Float   | Gesamte erzeugte* Energie                                                     |

\* Irgendwas von wegen "Energie wird gar nicht erzeugt, sondern umgewandelt": Technisch korrekt, aber in diesem Kontext nicht eindeutig verständlich.