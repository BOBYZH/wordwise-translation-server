# wordwise-translation-server
- A translation server with Amazon Word-Wise-like feature
- Forked from [auphone's project](https://github.com/auphone/wordwise-translation-server)

## Installation
```sh
git clone https://github.com/BOBYZH/wordwise-translation-server.git
cd wordwise-translation-server
npm install
```

## Build
```sh
npm run build
```

## Run
```sh
npm run start
```

# API
#### GET: `/api/levels`
Return the number of levels available in translation server

#### Response
```js
{
  level: 3 
}
```

<br>

#### POST: `/api/translate`
Filter and translate difficult words by specific level
#### Request
```js
{
  "level": 3,
  "words": [ "apple", "cappuccino" ],
  "lang": "zh-TW"
}
```

#### Response
```js
{
  "cappuccino": "熱奶咖啡"
}
```

<br>

## Options
#### words (Required)
- Array of words to be filtered / translated

#### level
- Level 1-3, level 1 will translate almost all words except stop words
- Default: `1`

#### lang
- Any language code supported by google translate
- Default: `zh-TW`

#### password (Optional)
- A super simple and configurable password in `config.json` to restrict the use of translate API

<br>

## Projects using this server
https://github.com/auphone/wordwise-chrome-extension.git

## License
ISC

## Original Author
[github/auphone](https://github.com/auphone)

<br>

Good luck!
