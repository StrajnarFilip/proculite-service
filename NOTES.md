# Recorded data

Format:

```
Name - [protobuf type] : [unit]
```

- Speed - `float` : metres / second
- Cadence - `float` : metres / second
- Location:
    - Latitude - `double` : degrees
    - Longitude - `double` : degrees
    - Altitude - `float` : metres above sea level
- Power - `float` : watts
- Relative wind speed - `float` : metres / second
- Heart rate - `float` : beats / minute
- Body temperature - `float` : temperature in kelvin, can be either skin or core temperature
- Environment temperature - `float` : temperature in kelvin, can be either air temperature or water temperature
- Oxygen saturation - `float` : percentage, 0-100%, usually peripheral oxygen saturation (SpO2)
- Blood glucose - `float` : millimoles of glucose per litre of blood
- Lactic acid - `float` : millimoles of lactic acid per litre of blood
- Gradient - `float` : percentage, 0-100%
- Left-Right power balance - `float` : percentage, 0-100% for the right side (55 would imply 45% for the left side, 55% for the right side)

# Comparison of file types

[GPX](https://www.topografix.com/gpx/1/1/gpx.xsd) - GPS Exchange format

[TCX](https://www8.garmin.com/xmlschemas/TrainingCenterDatabasev2.xsd) - Garmin Training Center format

[FIT](https://developer.garmin.com/fit/protocol/) - Flexible and Interoperable Data Transfer protocol

| File type | Location | Cadence | Heart rate | Power | Wind speed | Speed | Body temperature | Environment temperature | Oxygen saturation | Blood glucose | Lactic acid | Gradient | L-R balance |
| - | - | - | - | - | - | - | - | - | - | - | - | - | - |
| GPX | 🟢 | 🔴 | 🔴 | 🔴 | 🔴 | 🔴 | 🔴 | 🔴 | 🔴 | 🔴 | 🔴 | 🔴 | 🔴 |
| TCX | 🟢 | 🟢 | 🟢 | 🔴 | 🔴 | 🔴 | 🔴 | 🔴 | 🔴 | 🔴 | 🔴 | 🔴 | 🔴 |
| FIT | 🟢 | 🟢 | 🟢 | 🟢 | 🟢 | 🟢 | 🟢 | 🟢 | 🔴 | 🔴 | 🔴 | 🟢 | 🟢 |
| Proculite JSON | 🟢 | 🟢 | 🟢 | 🟢 | 🟢 | 🟢 | 🟢 | 🟢 | 🟢 | 🟢 | 🟢 | 🟢 | 🟢 |