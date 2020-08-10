# Anki 95

## What is it?
This is a respository containing CSS and HTML code that, if imported into Anki, let's you not only style your cards in the Windows 95 theme, but also use a list of features.

![Sample look](https://preview.redd.it/n4gtwm93bef51.png?width=1024&auto=webp&s=340352a6b592e2851cbfc7c804be7a234f3542e4)

## How to use it?
1. put the CSS into this Anki folder:
   - **Windows**:  C:\Users\Administrator\AppData\Roaming\Anki2\yourankiaccountname\collection.media\
   - **Linux**:  ~\.local\share\Anki2\collection.media\
2. When naming the file, append _ symbol at the beginning, otherwise Anki will delete the file when checking the media (for example "\_styling.css")
3. Put the HTML for Front card in the front field, and Back card HTML in the Back field.
4. Create or modify the necessary fields for the note type:
   - Front
   - Back
   - Front language (default ENG)
   - Back language (default PL)
   - Image
   - Decorative image
   - Extra

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
