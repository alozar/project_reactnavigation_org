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

- `navigation` - prop компонента Screen
- `navigation.navigate('Details')` - функция маршрутизации по адресу в собственном навигаторе стека
- `navigation.push('Details')` - функция добавления нового маршрута
- `navigation.goBack()` - функция возврата в предыдущий адрес
- `navigation.popToTop()` - функция возврата в корневой адрес
