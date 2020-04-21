# GlorifiedPig's Localization & Internationalization Library
This is designed to easily incorporate different languages into your addons.

# Installation
Place the `sh_i18n.lua` file into your `autorun` folder.

# Functions
```lua
i18n.RegisterPhrase( languageIdentifier :: string, phraseId :: string, text :: string )
```
- Make sure `languageIdentifier` is the language code that exists in the ConVar `gmod_language`.
- `phraseId` is the unique identifier you will be using to get the phrase.
- `text` is the translated text.

```lua
i18n.RegisterPhrases( languageIdentifier :: string, phraseTbl :: table )
```
- Registers a list of phrases from a `table`.

```lua
i18n.GetPhrase( phraseId :: string )
```
- Returns a `string` that matches up with the language set in the convar `gmod_language`.
- Needs to be registered. If the language does not exist, it defaults to English.