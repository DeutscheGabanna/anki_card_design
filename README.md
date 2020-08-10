# Anki 95

## What is it?
This is a respository containing CSS and HTML code that, if imported into Anki, let's you not only style your cards in the Windows 95 theme, but also use a list of features.

![Sample look](https://preview.redd.it/n4gtwm93bef51.png?width=1024&auto=webp&s=340352a6b592e2851cbfc7c804be7a234f3542e4)

## How to use it?
1. Download [\_windows.css](.\_windows.css) file
1. Put the CSS file into this Anki folder:
   - **Windows**:  C:\Users\Administrator\AppData\Roaming\Anki2\yourankiaccountname\collection.media\
   - **Linux**:  ~\.local\share\Anki2\collection.media\\
2. Download the file: [Sample deck Anki 95](https://github.com/DeutscheGabanna/anki_card_design/blob/master/Sample%20deck%20Anki%2095.apkg)
   - The file contains everything except for the CSS code you've pasted earlier.
3. Import the deck.
   - Open Anki
   - File > Import
   - Choose [Sample deck Anki 95](https://github.com/DeutscheGabanna/anki_card_design/blob/master/Sample%20deck%20Anki%2095.apkg) file
4. Enjoy

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
