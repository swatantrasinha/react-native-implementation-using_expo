This is implementation of learning from repo : https://github.com/swatantrasinha/react-native-expo   

Below are steps to crrate and start expo app :   
<details>
  <summary>Boilerplate Code</summary>
  <p>
    


1. create expo app   

> npx create-expo-app@latest
give name of the app as **expo-learning-implementation/**

2. give reset command using bun   

> bun run reset-project

3. give install command   

> npm i

4. start the expo app   

> bunx expo start

Note if there is any network related then give below command and then above command in point 4

> EXPO_OFFLINE=1 bunx expo start

5. We will see QR code we can scan it and see output as below:   
<img width="369" height="800" alt="image" src="https://github.com/user-attachments/assets/d1ae1b8c-85b6-406d-8db6-5dd0ab6f5c5e" />   

  </p>
</details>

In index.tsx we will remove the existing code and using shortcut **rnfes** we will generate snippet   
```javascript
import { StyleSheet, Text, View } from 'react-native'
import React from 'react'

const Index = () => {
  return (
    <View>
      <Text>Index</Text>
    </View>
  )
}

export default Index

const styles = StyleSheet.create({})
```

In layout.tsx we will see below code from boiler plate   
```javascript
import { Stack } from "expo-router";

export default function RootLayout() {
  return <Stack />;
}

```
With this the layout will look like below:   
<img width="369" height="800" alt="image" src="https://github.com/user-attachments/assets/9608bed7-49a8-4c05-bf9b-d18872e44822" />    

---

Now we will modify top header in the above layout, so we will make changes in layout.tsx - add props to Stack  Component   

```javascript
import { Stack } from "expo-router";

export default function RootLayout() {
  return <Stack screenOptions={{headerShown: false}} />;
}

```

With this we can see the layout as below   
<img width="590" height="1280" alt="image" src="https://github.com/user-attachments/assets/0e2da364-e04e-4b72-a04b-ad895d8d250b" />   

here we can see 2 problems:   
- the index text is going out of top
- status bar(which shows time and notification etc) sees to be white out

We will fix this now using **useSafeAreaInsets hook**   


The final layout will look like below:   
<img width="369" height="800" alt="image" src="https://github.com/user-attachments/assets/e49f8036-866c-481d-91dc-7db3551647f7" />






