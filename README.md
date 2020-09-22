<div align="center">

## Quickly retrieve the lines from a text file


</div>

### Description

This function quickly retrieves a range of lines from a text file.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Bob Brown](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/bob-brown.md)
**Level**          |Intermediate
**User Rating**    |3.0 (21 globes from 7 users)
**Compatibility**  |Delphi 5, Delphi 4, Pre Delphi 4
**Category**       |[Delphi function enhancement](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/delphi-function-enhancement__7-25.md)
**World**          |[Delphi](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/delphi.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/bob-brown-quickly-retrieve-the-lines-from-a-text-file__7-290/archive/master.zip)





### Source Code

<hr>
<b>Quickly retrieve the lines from a text file</b><br><br>
If you need a quick function to get a line from a text file, try this one. It's very simple to use, for example:<br><br>
Writeln('The 2nd line in c:\autoexec.bat is '+GetLinesFromFile('c:\autoexec.bat',2,2)[0]);
<br><br>
<b>function  GetLinesFromFile(filename:string; linestart, lineend:integer) : TStringList;</b><br>
(*<br>
// Name   : GetLinesFromFile<br>
// Purpose : Returns a series of lines from a text file, starting at linestart and going to lineend<br>
// Date   : 12 Feb 2001<br>
// Comments :<br>
*)<br>
var<br>
&nbsp;&nbsp;fn : textfile;<br>
&nbsp;&nbsp;c : word;<br>
&nbsp;&nbsp;Line : String;<br>
begin<br>
&nbsp;&nbsp;Result:=TStringList.Create;<br>
&nbsp;&nbsp;AssignFile(fn,filename);<br>
&nbsp;&nbsp;Reset(fn);<br>
&nbsp;&nbsp;for c:=0 to LineStart do<br>
&nbsp;&nbsp;&nbsp;&nbsp;ReadLn(fn,Line);<br>
&nbsp;&nbsp;for c:=LineStart to LineEnd do<br>
&nbsp;&nbsp;begin<br>
&nbsp;&nbsp;&nbsp;&nbsp;Result.Add(Line);<br>
&nbsp;&nbsp;&nbsp;&nbsp;ReadLn(fn,Line);<br>
&nbsp;&nbsp;end;<br>
&nbsp;&nbsp;CloseFile(fn);<br>
end;<br>
<br>
Please vote for this code!

