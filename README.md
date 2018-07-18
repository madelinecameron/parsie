# Parsie

Parsing is hard. A lot of libraries get it terribly wrong or they might fall out of date with the latest happenings. 

Parsie is different. It will help you ensure your users are never frustrated or annoyed by your client-side validation. It helps guide the rough terrain of getting that input box validating juuuuuust right. 🤗

## Example

```js
const parsie = require('parsie')

module.exports = (state, emit) => {
  const parse = (data) => {
    const parsed = parsie.parse(data)

    console.log(`Perfectly parsed! ${parsed}`)
  }

  return html`
    <div>
      <input type="email" max="25" min="3" pattern=".*\@(gmail|yahoo|hotmail).com" required onchange=${parse}/>
    </div>
  `
}
```

## API

### `parse(input)`
Pass the to-be parsed input into the function and Parsie will use ML under the hood to correctly identify the type of input. After the type has been identified, Parsie will parse the input and return the now parsed input

#### Arguments:
- `input`: Anything you need parsed

## License
MIT

#### *cough* *cough*

https://medium.com/@madeline./7-ways-you-are-parsing-input-on-your-site-incorrectly-only-the-smartest-engineers-know-all-7-210bd1d99ca


