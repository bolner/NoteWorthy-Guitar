NoteWorthy Composer - Guitar Chords plugin
------------------------------------------

The [GuitarChord plugin](https://forum.noteworthycomposer.com/?topic=9081.0) for [NoteWorthy Composer](https://noteworthycomposer.com) was created by Mike Shawaluk in 2015. I created this repository for keeping track of some changes I needed.

# Original documentation

This plugin draw a guitar chord chart and optionally strums the chord when the song is played. A variety of notation is shown, including the chord name, open and excluded strings, barre positions, fret position and optional finger numbers.

When adding a new chord, the user can choose from 35 predefined chords, or can choose "(Custom)" to create a chord chart from scratch. The chord chart can be positioned vertical by changing the object marker position.

When a chord is added to a staff, if there is another GuitarChord object earlier in the staff, it will inherit the style and properties of that object.

- `@Name`: The name of the chord. It is displayed using a font which displays 'b' and '#' as flat and sharp symbols.
- `@Style`: This determines the font style to be used for the chord name and label text. The possible values are Serif (MusikChordSerif, Times New Roman), Sans (MusikChordSans, Arial) and Swing (SwingChord, SwingText). The default setting is Serif.
- `@Finger`: The fingerings for each string, entered from low to high pitch, separate by spaces. Each position can be a number, indicating the fret position, or a 'o' or 'x' for open or unplayed strings, respectively. For example, the fingering for a G major chord would be "3 2 o o o 3". Each numeric fret position can be appended with ':' and a number, to indicate the finger number to be used for that string; the number will be drawn inside the fingering dot. When finger numbers are being used, the chart size will generally need to be 2 or larger for the numbers to be readable.
- `@Barre`: Optional groups of strings to be held down by a particular finger, displayed by an arc over the fingering dots. Each barre to be drawn is indicated by the starting and ending string numbers, separated by ':'. For example, 2:5 would add a barre between the second and fifth strings. Note that the fingering positions for each end of a barre should be the same for the barre to be drawn correctly. 
- `@Size`: The size of the chord chart, ranging from 1.0 to 5.0. The default is 1.
- `@Frets`: The number of fret positions to show in the chart, ranging from 1 to 10. The default is 4.
- `@Capo`: For playback, indicates that the pitch for each string should be transposed upward the specified number of steps. The default is 0.
- `@TopFret`: The top fret number displayed in the chart. When the value is 1, the top border of the chart will be thicker. For larger values, '# fr.' will be displayed to the right of the chart. The default is 1.
- `@Span`: For playback, the number of notes/rests that the chord should span. A value of 0 will disable playback. The default is 0.
- `@FretTextPosition`: Specifies whether the fret text is displayed next to the top or bottom row of fingering dots, when Top Fret is greater than 1. The default is top.
- `@Strum`: For playback, the direction in which the chord is strummed: down (low- to high-pitched strings) or up (high- to low-pitched strings). The default is down.
- `@TopBarreOffset`: When a barre is present on the top fret and there are open (o) or excluded (x) strings within the barre, this setting can be used to move the barre upward a specified distance, to avoid collision with those labels. This will also move the Chord Name upward. The default value is 0.0.
- `@Anticipated`: This specifies that the strum should anticipate (precede) the chord, so that the final played note occurs on the chord's beat position. When unchecked, the first played note of the strummed chord is at the chord's beat position. The default setting is on (checked).
