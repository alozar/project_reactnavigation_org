# Учебный проект React Native Navigation Expo

> [https://reactnavigation.org/](https://reactnavigation.org/)

## Установка:

```
npx create-expo-app ./
npm install @react-navigation/native
npx expo install react-native-screens react-native-safe-area-context
npm install @react-navigation/native-stack
```

## Запуск:

```
npx expo start
```

## Команды:

### Навигация:

- `navigation` - prop компонента Screen
- `navigation.navigate('Details')` - функция маршрутизации по адресу в собственном навигаторе стека
- `navigation.push('Details')` - функция добавления нового маршрута
- `navigation.goBack()` - функция возврата в предыдущий адрес
- `navigation.popToTop()` - функция возврата в корневой адрес

### Передача параметров

- `navigation.navigate('RouteName', { /* params go here */ })` - передача параметров по маршруту
- `route` - prop компонента Screen, из которого получем параметры

```
function DetailsScreen({ route, navigation }) {
    const { itemId, otherParam } = route.params;
    ...
```

- Инициализация начальных параметов

```
<Stack.Screen
  name="Details"
  component={DetailsScreen}
  initialParams={{ itemId: 42 }}
/>
```

- Обновление параметров Screen

```
navigation.setParams({ query: 'someText', ... });
```

> **Замечание:** Не используйте **setParams** для обновления options Screen, таких как title и т. д. Если вам нужно обновить options, вместо этого используйте **setOptions**.
