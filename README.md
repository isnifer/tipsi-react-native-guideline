# tipsi-react-native-guideline
Tipsi Guideline for React-Native Development

### Event handlers
#### Bad
```js
<TextInput
  onChangeText={username => this.setState({ username })}
  onSubmitEditing={() => this.passwordInput.focus()}
/>
```
#### Good
```js
<TextInput
  onChangeText={this.handleUpdateUsername}
  onSubmitEditing={this.setPasswordInputActive}
/>
```

### String attributes
#### Bad
```js
<TextInput
  underlayColor={'#000000'}
/>
```
#### Good
```js
<TextInput
  underlayColor="#000000"
/>
```

### Reference Handler
#### Bad
```js
<TextInput
  ref={node => this.passwordInput = node}
/>
```
#### Good
```js
<TextInput
  ref={this.getPasswordInputInstance}
/>
```
