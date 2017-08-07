> This project is currently in __beta and APIs are subject to change.__

# React Native Parallax Swiper
Configurable parallax swiper based on an iOS pattern. Uses [Native Driver](http://facebook.github.io/react-native/blog/2017/02/14/using-native-driver-for-animated.html) for super smooth parallax.

## Ways to use this component

1. You have a background image that parallaxes while your UI moves at the ScrollView speed

![Example 1](https://raw.githubusercontent.com/zachgibson/react-native-parallax-swiper/master/example-1.gif)

2. You have no background image and all of your UI parallaxes

![Example 2](https://raw.githubusercontent.com/zachgibson/react-native-parallax-swiper/master/example-2.gif)

☝️ *[React Native Zoomable](https://github.com/LeBlaaanc/react-native-zoomable) for image zoom.*
*Artwork by [Daniel Mackey](https://dribbble.com/danielmackeyart).*

You can see this effect in apps like:
- [iOS Photos (Camera Roll)](https://goo.gl/GY3bFQ)
- [Twitter Moments](https://goo.gl/CvzCQA)
- [Kylie Jenner app](https://goo.gl/yDB69S) 😅
- [Vevo app (older version)](https://goo.gl/FMSSeF)

## Add it to your project
Run ```npm install react-native-parallax-swiper --save```


## Usage
```javascript
import ParallaxSwiper from 'react-native-parallax-swiper';
```

```javascript
<ParallaxSwiper
  parallaxStrength={80}
  dividerWidth={8}
  dividerColor="black"
  backgroundColor="#bae"
  onMomentumScrollEnd={() => console.log('💩')}
>
  <View
    style={{
      flex: 1,
      alignItems: 'center',
      justifyContent: 'center',
     }}
     backgroundImage={'https://goo.gl/7Mvjji'}
    >
    <Text>Pass Arbitrary JSX to ParallaxSwiper as Children</Text>
  </View>
</ParallaxSwiper>
```

## Props
| Prop | Type | Default | Description |
|---|---|---|---|
| __`parallaxStrength`__ | _Number_ | `80` | This number determines how slow parallax’ing element moves. Lower number yields a subtler parallax effect, higher number increases parallax effect. |
| __`dividerWidth`__ | _Number_ | `8` | The width of the divider between each slide. (horizontal only) |
| __`dividerColor`__ | _String_ | `black` | Color of divider. |
| __`backgroundImage`__ | _String_ | `N/A` | The image source. If used this becomes the background image that parallaxes. (remote URL only for now) |
| __`backgroundImageResizeMode`__ | _String_ | `cover` | Determines how to resize the image. |
| __`backgroundColor`__ | _String_ | `black` | The main view’s background color. |
| __`onMomentumScrollEnd`__ | _Function_ | `N/A` | Called when ScrollView stops scrolling. |
| __`children`__ | _ReactComponents_ | `N/A` | JSX to inject into the slide. |
| __`vertical`__ | _Boolean_ | `false` | When true, ParallaxSwiper’s children are arranged vertically in a column instead of horizontally in a row. |
| __`showsHorizontalScrollIndicator`__ | _Boolean_ | `false` | When true, shows a horizontal scroll indicator. The default value is false. |
| __`showsVerticalScrollIndicator`__ | _Boolean_ | `false` | When true, shows a vertical scroll indicator. The default value is false. |

## Copyright
Copyright (c) 2017 [Zachary Gibson](http://zachgibsondesign.com/) Licensed under the MIT license.
