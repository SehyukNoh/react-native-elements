---
id: version-0.19.0-card
title: Card
original_id: card
---

![Card Component](/react-native-elements/img/card.png)

```js
const users = [
 {
    name: 'brynn',
    avatar: 'https://s3.amazonaws.com/uifaces/faces/twitter/brynn/128.jpg'
 },
 ... // more users here
]

import { View, Text, Image } from 'react-native'
import { Card, ListItem, Button } from 'react-native-elements'

// implemented without image with header
<Card title="CARD WITH DIVIDER">
  {
    users.map((u, i) => {
      return (
        <View key={i} style={styles.user}>
          <Image
            style={styles.image}
            resizeMode="cover"
            source={{ uri: u.avatar }}
          />
          <Text style={styles.name}>{u.name}</Text>
        </View>
      );
    })
  }
</Card>

// implemented without image without header, using ListItem component
 <Card containerStyle={{padding: 0}} >
  {
    users.map((u, i) => {
      return (
        <ListItem
          key={i}
          roundAvatar
          title={u.name}
          avatar={{uri:u.avatar}}
        />
      );
    })
  }
</Card>


// implemented with Text and Button as children
<Card
  title='HELLO WORLD'
  image={require('../images/pic2.jpg')}>
  <Text style={{marginBottom: 10}}>
    The idea with React Native Elements is more about component structure than actual design.
  </Text>
  <Button
    icon={{name: 'code'}}
    backgroundColor='#03A9F4'
    fontFamily='Lato'
    buttonStyle={{borderRadius: 0, marginLeft: 0, marginRight: 0, marginBottom: 0}}
    title='VIEW NOW' />
</Card>
```

### Props

* [`containerStyle`](#containerstyle)
* [`dividerStyle`](#dividerstyle)
* [`featuredTitle`](#featuredtitle)
* [`featuredTitleStyle`](#featuredtitlestyle)
* [`featuredSubtitle`](#featuredsubtitle)
* [`featuredSubtitleStyle`](#featuredsubtitlestyle)
* [`flexDirection`](#flexdirection)
* [`fontFamily`](#fontfamily)
* [`image`](#image)
* [`imageProps`](#imageprops)
* [`imageStyle`](#imagestyle)
* [`imageWrapperStyle`](#imagewrapperstyle)
* [`title`](#title)
* [`titleStyle`](#titlestyle)
* [`titleNumberOfLines`](#titlenumberoflines)
* [`wrapperStyle`](#wrapperstyle)

---

# Reference

### `flexDirection`

flex direction (row or column) (optional)

|  Type  | Default |
| :----: | :-----: |
| string | column  |

---

### `containerStyle`

outer container style (optional)

|      Type      | Default |
| :------------: | :-----: |
| object (style) |  none   |

---

### `wrapperStyle`

inner container style (optional)

|      Type      | Default |
| :------------: | :-----: |
| object (style) |  none   |

---

### `title`

optional card title (optional)

|  Type  | Default |
| :----: | :-----: |
| string |  none   |

---

### `titleStyle`

additional title styling (if title provided) (optional)

|      Type      | Default |
| :------------: | :-----: |
| object (style) |  none   |

---

### `titleNumberOfLines`

number of lines for title (optional)

|  Type  | Default |
| :----: | :-----: |
| number |  none   |

---

### `featuredTitle`

title rendered over the image (only works if image prop is present)

|  Type  | Default |
| :----: | :-----: |
| string |  none   |

---

### `featuredTitleStyle`

styling for featured title

|      Type      | Default |
| :------------: | :-----: |
| object (style) |  none   |

---

### `featuredSubtitle`

subtitle rendered over the image (only works if image prop is present)

|  Type  | Default |
| :----: | :-----: |
| string |  none   |

---

### `featuredSubtitleStyle`

styling for featured subtitle

|      Type      | Default |
| :------------: | :-----: |
| object (style) |  none   |

---

### `dividerStyle`

additional divider styling (if title provided) (optional)

|      Type      | Default |
| :------------: | :-----: |
| object (style) |  none   |

---

### `fontFamily`

specify different font family

|  Type  |                      Default                      |
| :----: | :-----------------------------------------------: |
| string | System font bold (iOS), Sans Serif Bold (android) |

---

### `imageStyle`

specify image styling if image is provided

|     Type      |      Default      |
| :-----------: | :---------------: |
| object(style) | inherited styling |

---

### `imageProps`

optional properties to pass to the image if provided e.g "resizeMode"

|           Type           | Default |
| :----------------------: | :-----: |
| object (ImageProperties) |  none   |

---

### `imageWrapperStyle`

specify styling for view surrounding image

|     Type      | Default |
| :-----------: | :-----: |
| object(style) |  none   |

---

### `image`

add an image as the heading with the image prop (optional)

|           Type            | Default |
| :-----------------------: | :-----: |
| image uri or require path |  none   |
