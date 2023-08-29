# Soundlets+

Soundlets+ is a soundboard that allows you to create your own soundboard and sound bookmarklets. 
You input a name, your own Audio File's URL, and you get a bookmarklet that can be saved as a JSON or sent to people as a link.
Why is this repo seperate from ccn0.github.io? Because I wanted a seperate license for this piece of tech for people to make themes, addons, and other stuffs.
Have fun. It's all HTML, CSS, and Javascript in one file so it can't be that confusing even for beginners.

## Usage

To edit a soundboard, hover over the line below the logo header, and show the editbar.
You can add a sound using the `Name` `Audio URL` and `Speed` values and clicking `Add`.
You can add dividers `|` and breaks (like the enter key) to divide areas of your sounds.

The `Undo` button will delete the last created element. `Clear Board` will ask you to confirm if you want to clear the board.

The `Copy Link to Board` button converts your soundboard to JSON and places it after the hash.
When using this link, the page automatically loads the JSON from the URL.
Using a link also auto hides the editbar.
`Download` will download the JSON file and `Load Board` will prompt you for a JSON file and will load the board inside.

## Making a JSON file

You can create a sounboard using only a text-editor.
Create an array `[ ]`. This will be the area where the soundboard is stored.
To create a sound node, create an object containing `"name"` `"url"` and `"speed"`. If you don't provide a speed, it will default to 1.
Example of a complete sound, `{"name":"Sound","url":"https://example.com/sound.mp3","speed":1.5}`

To create a divider node, create an object containing `"divider"`. Specify which type of divider you want.
Possible dividers are, `{"divider":"break"}` and `{"divider":"line"}`.

The only current elements possible in a soundboard are Sounds, Divider Lines, and Breaks. There is a possibility that more might be added.
Remember that after every object, `{ }`, it must be followed by a comma (except the very last one).
