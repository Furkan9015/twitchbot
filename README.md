## TwitchBot

The twitchbot package provides a set of functions that control a basic Twitch.tv chat bot. The package also exposes an interface which can be used to create a custom chat bot.

### Installation

Run `go get github.com/Furkan9015/twitchbot`

### Importing

Import this package by including `github.com/Furkan9015/twitchbot` in your import block.

e.g.

```go
package main

import(
    ...
    "github.com/Furkan9015/twitchbot"
)
```

### Usage

Basic usage:

```go
package main

import (
	"github.com/Furkan9015/twitchbot"
	"time"
)

func main() {

	// Replace the channel name, bot name, and the path to the private directory with your respective
	// values.
	myBot := twitchbot.BasicBot{
		Channel:     "twitch",
		MsgRate:     time.Duration(20/30) * time.Millisecond,
		Name:        "TwitchBot",
		Port:        "6667",
		PrivatePath: "../private/oauth.json",
		Server:      "irc.chat.twitch.tv",
	}
	myBot.Start()
}
```

_That's all, enjoy!_
