# Anki 95

## What is it?
This is a respository containing CSS and HTML code that, if imported into Anki, let's you not only style your cards in the Windows 95 theme, but also use a list of features.

![Sample look](https://preview.redd.it/n4gtwm93bef51.png?width=1024&auto=webp&s=340352a6b592e2851cbfc7c804be7a234f3542e4)

## How to use it?
1. Download [\_windows.css](https://github.com/DeutscheGabanna/anki_card_design/blob/master/_windows.css) file
1. Put the CSS file into this Anki folder:
   - **Windows**:  C:\Users\Administrator\AppData\Roaming\Anki2\yourankiaccountname\collection.media\
   - **Linux**:  ~\.local\share\Anki2\collection.media\\
2. Download the file: [Sample deck Anki 95](https://github.com/DeutscheGabanna/anki_card_design/raw/master/Sample%20deck%20Anki%2095.apkg)
   - The file contains everything except for the CSS code you've pasted earlier.
3. Import the deck.
   - Open Anki
   - File > Import
   - Choose [Sample deck Anki 95](https://github.com/DeutscheGabanna/anki_card_design/raw/master/Sample%20deck%20Anki%2095.apkg) file
4. Enjoy

## FAQ
### How do I add more programmable commands in different languages on card's HTML?

Either see the HTML of Front card of the Basic card in the sample deck, or look at this comment I left in ![front_card_thetobruk.html](https://github.com/DeutscheGabanna/anki_card_design/blob/master/front_card_thetobruk.html)

```
<!--within this comment is a SHORT GUIDE on adding commands in different languages for the automatic picker-->
			
	<!--'p' means paragraph and is used to separate the commands from one another-->
	<!--'lang' contains the language code of your choosing to be caught by CSS according to the algorithm-->
	<!--'class' contains all the necessary info for the automatic picker to decide which message to show-->
	<!--{{Card}} is used as the basis if the user did not specify anything in the language fields (here: Front language and Back language).
		
	If you name your card "cs_ENG ct_GER", you're telling the picker to ASSUME that the Front is in English, and the back is in German.
		cs_ here means "card source (language)" and ct_ means "card target (language)".
		cs_ and ct_ prefixes are important here, because otherwise the code wouln't be able to distinguish between ENG in the card name and ENG in the fields.
	Naming your card like this saves you time, because otherwise you'd have to specify the language in the fields every you make a new card.-->
			
	<!--If the fields are indeed specify (you wrote something in the "Front language" or "Back language" fields), then you're basically telling the card this:
		"I know the card usually contains an English term on the first field and German translation on the back field, but this time make an exception - the front's in Jewish and the back's in Finnish"
		fs_ here means "field source (language" and ft_ means "field target (language)"
	Fields always have a priority over the card name.-->
			
	<p lang="PL" class="{{Card}} fs_{{Front language}} ft_{{Back language}}">Rozwiń koncept:</p>
	<p lang="ENG" class="{{Card}} fs_{{Front language}} ft_{{Back language}}">Expound on:</p>
	<p lang="GER" class="{{Card}} fs_{{Front language}} ft_{{Back language}}">Erkläre es:</p>
			
<!--you can add as many supported commands as you please following this pattern-->
```

## Other stuff worth mentioning
### Tables
All the good practises of creating tables in HTML apply here.

Here's a sample table representing easy ways of formatting the table and letting the CSS do the rest.

```
<table>
   <thead>
      <th colspan=3>Header spanning three cells</th>
      <th>One-cell header</th>
   </thead>
   <tr>
      <th width=10%>Vertical header on the left</th>
      <td>one</td>
      <td>two</td>
      <td>three</td>
   </tr>
   <tr>
      <td>bip</td>
      <td>bop</td>
      <td colspan=2>boop</td>
</table>
```

This creates a table like this:

![sample table](https://i.imgur.com/55jwCbv.png)
