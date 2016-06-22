# Module: random_quotes

The `random_quotes` module returns a random quote based on the category set. Supplied quotes are courtesy
of http://brainyquote.com. Since there is no API for BrainQuote.com, you will have to manually add new ones.
See the section on `Updating Quotes` below.

## Installing the module
Clone this repository in your `~/MagicMirror/modules/` folder
````javascript
git clone https://github.com/KirAsh4/random_quotes
````

## Using the module
To use this module, add it to the modules array in the `config/config.js` file:
````javascript
modules: [
			{
				module: 'random_quotes',
				position: 'lower_third',
				config: {
						// The config property is optional
						// Without a config, a random quote is shown,
						// selected from all of the categories available.
				}
			}
]
````

## Configuration options
The `random_quotes` module allows you to pick quotes randomly from all the provided categories, or you can
set it to only use one category. Specifying multiple categories is curently not supported.

<table>
	<thead>
		<tr>
			<th>Options</th>
			<th>Description</th>
			<th>Default</th>
		</tr>
	</thead>
	<tfoot>
		<tr>
			<th colspan="3"><em>More options may get added later.</em></th>
		</tr>
	</tfoot>
	<tbody>
		<tr>
			<td><code>updateInterval</code></td>
			<td>How often a new quote gets displayed. <strong>Value is in SECONDS.</strong></td>
			<td><code>300</code> seconds (every 5 minutes)</td>
		</tr>
		<tr>
			<td><code>fadeSpeed</code></td>
			<td>How fast <strong>(in SECONDS)</strong> to fade out and back in when changing quotes.</td>
			<td><code>4</code> seconds</td>
		</tr>
		<tr>
			<td><code>category</code></td>
			<td>What category to pick from.</td>
			<td><code>random</code> - The <code>random</code> setting will pick a random quote out of all the available categories. Or you can set it to a specific category: <code>inspirational</code>, <code>life</code>, <code>love</code>, <code>motivational</code>, <code>positive</code>, or <code>success</code>.</td>
		</tr>
	</tbody>
</table>

## Updating Quotes
Because BrainyQuote.com does not proide an API for their database, you will have to update/change the quotes manually.
You can edit the `random_quotes.js` file and add/remove quotes from the various sections. You may even delete an entire
section.

Most random quotes APIs out there only allow for a single 'quote of the day'. If you want to have a random quote
each time you send a request, most of them will require a paid subscription. In keeping this module 'free', I opted
to not force anyone to have to pay for a service.
