[<img src="https://github.com/Novsochetra/react-native-circular-chart/blob/main/assets/thumbnail.png" width="250"/>](image.png)
 

## React Native Circular Chart Documentation

### Import components

1. `yarn add rn-circular-chart`
2. `yarn add react-native-svg` install peer dependencies
3. use with ES6 syntax to import components `import { DonutChart } from "rn-circular-chart";`

### Quick Example
```js
import { DonutChart } from "rn-circular-chart";

<View style={styles.sectionWrapper}>
  <DonutChart
    data={[
                    {name: "my Name", value: 1000, color:'#AA86F7'},
                    {name: "Name", value: 3000, color:'#94D5FA'},
                    {name: "ac Name", value: 4000, color:'#8F9FF5'}
                ]}
    strokeWidth={15}
    radius={90}
    containerWidth={width - PADDING * 2} // width comes from Dimensions
    containerHeight={105 * 2}
    type="round"
    startAngle={0}
    endAngle={360}
    animationType="slide"
    centerLabel={ {"label":'CURRENT VALUE',"labelValue":"₹20,34,343" }}
  />
</View>

const styles = StyleSheet.create({
  sectionWrapper: {
    justifyContent: "center",
    alignItems: "center",
    borderWidth: 1,
    borderRadius: 8,
    borderColor: "lightgray",
    backgroundColor: "#ffffff",
    marginVertical: 8,

    shadowColor: "#000",
    shadowOffset: {
      width: 0,
      height: 1,
    },
    shadowOpacity: 0.2,
    shadowRadius: 1.41,

    elevation: 2,
  },
});

```

### Circule Props

| Property                      | Type                 | Description                                                                                            |
| ----------------------------- | -------------------- | ------------------------------------------------------------------------------------------------------ |
| data                          | Array<{name: string; value: number; color: string;}>  | Defines the data for circular                                         |
| containerWidth                | number               | Defines the width of container                                                                         |
| containerHeight               | number               | Defines the height of container                                                                        |
| radius                        | number               | Defines the radius of circular                                                                         |
| startAngle                    | number (degree)      | Defines the start point of the circular. default start from -115 deg                                   |
| endAngle                      | number (degree)      | Defines the start point of the circular. default start from 115 deg                                    |
| strokeWidth                   | number               | Defines the thickness of circular item                                                                 |
| type                          | 'butt', 'round'      | Defines the type of circular item                                                                      |
| animationType                 | 'fade', 'slide'      | Defines the animation type for chart item                                                              |
| labelValueStyle               | StyleProp<TextStyle> | Defines the style for data.value                                                                       |
| labelTitleStyle               | StyleProp<TextStyle> | Defines the style for data.name                                                                        |
| labelWrapperStyle             | StyleProp<ViewStyle> | Defines the style for wrapper of data.value and data.name                                              |
| containerStyle                | StyleProp<ViewStyle> | Defines the style for container of chart                                                               |

### More information
This library is built on top of the following open-source projects:
- react-native-svg (https://github.com/react-native-svg/react-native-svg)
