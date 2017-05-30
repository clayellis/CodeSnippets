# CodeSnippets
Xcode code snippets that I use

## Installation

1. `git clone https://github.com/clayellis/CodeSnippets.git`
2. `cp CodeSnippets/*.codesnippet ~/Library/Developer/Xcode/UserData/CodeSnippets/`

## Overview

### localizable-strings.codesnippet
When developing iOS apps, I like to put all of my user-facing strings into a `Localizable.strings` file to:
1. Have a centralized location for editing strings
2. Be able to translate the app quickly without having to change any code

To improve the process of adding strings to `Localizable.strings` I wrote a Swift script called [Localize](link) that parses files for `NSLocalizedString(...)` and pulls out the key, value, and comment if provided. I like providing all three by default. But since Xcode only code completes for `NSLocalizedString(_ key: String, comment: String)` it can be cumbersome to always add `value: String`. You could create a global function with those parameters, but I try to avoid adding global functions when possible.

Start typing `NSLocalizableString` add get a nice completion for `NSLocalizedString(_ key: String, value: String, comment: String)` (which is a totally valid flavor of the macro.)
