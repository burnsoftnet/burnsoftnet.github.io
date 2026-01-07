---
layout: default
---

[<--Home](README.md)
# Using the Command Line Arguments in your Application

**Date Posted:** 3/28/2007 5:16:19 PM
**Product:** Visual Basic.NET 2005/ .NET Framework 2.0

The following code will get the commands passed to the application.  With this code you can set a switch to a true or false value such as /USECONSOLE or get the value from a switch,  such as /SERVER=MyServer.  This Code was used for some VB.NET 2005 Code.

`‌Function GetCommandValue(ByVal strValue As String) As String 
     strValue = Replace(strValue, "/", "" )
     strValue = Replace(strValue, "--", "" )
     Dim strSplit() As String = Split(strValue, "=" )
     Dim intBound As Integer = UBound(strSplit)
     Dim sAns As String = ""
     Dim i As Integer = 0
     If intBound = 0 Then
          sAns = strValue
      Else
          sAns = strSplit(intBound)
      End If
     Return UCase(sAns)
  End Function

 Function GetCommandName(ByVal strValue As String) As String 
     strValue = Replace(strValue, "/", "" )
     strValue = Replace(strValue, "--", "" )
     Dim strSplit() As String = Split(strValue, "= " )
     Dim intBound As Integer = UBound(strSplit)
     Dim sAns As String = ""
     Dim i As Integer = 0
     If intBound = 0 Then 
          sAns = strValue
      Else
          sAns = strSplit(LBound(strSplit))
     End If 
     Return UCase(sAns)
 End Function 
Sub Main()
     Dim cmdLine() As String = System.Environment.GetCommandLineArgs
     Dim i As Integer = 0
     Dim intCount As Integer = cmdLine.Length
     If intCount > 1 Then
          For i = 1 To intCount - 1 '1 to end, 0 will hold the application and path
               Select Case GetCommandName(cmdLine(i))
                    case "SWITCH"
                           'Do Some Action
                     case "SWITCHWITHVALUE"
                            'Get the values that you want to set
                             MyValue = GetCommandValue(cmdLine(i))
               End Select
          Next i
     End If
End Sub 

`