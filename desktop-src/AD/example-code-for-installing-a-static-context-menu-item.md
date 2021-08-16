---
title: 安裝靜態內容功能表項目的範例程式碼
description: 下列程式碼範例會使用兩個腳本。
ms.assetid: 22d6a220-7712-4b07-a6d9-67dd748358a6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16e4ff9890aa73b1107fe511c3e41480b5db7f1bb68a8a264a990cf58a94ea4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962317"
---
# <a name="example-code-for-installing-a-static-context-menu-item"></a>安裝靜態內容功能表項目的範例程式碼

下列程式碼範例會使用兩個腳本。 第一個腳本 (Frommenu.vbs) 是在選取功能表項目時所執行的命令。 第二個腳本 (Addmenu.vbs) 會安裝顯示規範內容功能表項目，以執行腳本 Frommenu.vbs。 此範例假設地區設定 409 (美式英文) ，並在 Active Directory 系統管理嵌入式管理單元中擴充使用者物件的內容功能表。

執行範例程式碼

1.  複製下列 Frommenu.vbs 程式碼，開啟記事本，將程式碼貼入記事本，將檔案儲存為 C： \\frommenu.vbs，然後關閉記事本。
2.  複製下列 Addmenu.vbs 程式碼，開啟記事本，將程式碼貼入記事本，將檔案儲存為 C： \\addmenu.vbs，然後關閉記事本。
3.  執行 Addmenu.vbs。
4.  啟動 Active Directory 消費者和電腦嵌入式管理單元。

FROMMENU.VBS


```VB
'Frommenu.vbs is the script run when the menu item is chosen.
 
''''''''''''''''''''
' Parse the arguments
' First arg is ADsPath of the selected object. Second is Class.
''''''''''''''''''''
On Error Resume Next
 
Set oArgs = WScript.Arguments
sText = "This script was run from a display specifier context menu." & vbCrLf & "Selected Item:"
If oArgs.Count > 1 Then
    sText = sText & vbCrLf & "  ADsPath: " & oArgs.item(0)
    sText = sText & vbCrLf & "  Class: " & oArgs.item(1)
Else
    sText = sText & vbCrLf & "Arg Count: " & oArgs.Count
End If
show_items sText
Err.Number = 0
sBind = oArgs.item(0)
Set dsobj= GetObject(sBind)
If (Err.Number <> 0) Then
    BailOnFailure Err.Number, "on GetObject method"
End If
objname = dsobj.Get("name")
If (Err.Number <> 0) Then
    BailOnFailure Err.Number, "on Get method"
End If
sText = "Use ADsPath from first argument to bind and get RDN (name) property."
sText = sText & vbCrLf & "Name: " & objname
show_items sText
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
Sub show_items(strText)
    MsgBox strText, vbInformation, "Script from Context Menu"
End Sub
 
Sub BailOnFailure(ErrNum, ErrText)    strText = "Error 0x" & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



ADDMENU.VBS


```VB
' Addmenu.vbs adds the menu item to run Frommenu.vbs 
' from user object's context menu in the admin snap-ins.
On Error Resume Next
Set root= GetObject("LDAP://rootDSE")
If (Err.Number <> 0) Then
    BailOnFailure Err.Number, "on GetObject method"
End If
sConfig = root.Get("configurationNamingContext")
'hardcoded for user class.
sClass = "user"
'hardcoded for US English
sLocale = "409"
sPath = "LDAP://cn=" & sClass & "-Display,cn=" & sLocale & ",cn=DisplaySpecifiers," & sConfig
show_items "Display Specifier: " & sPath
Set obj= GetObject(sPath)
If (Err.Number <> 0) Then
    BailOnFailure Err.Number, "on GetObject method"
End If
'TODO--check if this is already there.
'Add the value for the context menu
sValue = "5,Run My Test Script,c:\frommenu.vbs"
vValue = Array(sValue)
obj.PutEx 3, "adminContextMenu", vValue
If (Err.Number <> 0) Then
    BailOnFailure Err.Number, "on IADs::PutEx method"
End If
' Commit the change.
obj.SetInfo
If (Err.Number <> 0) Then
    BailOnFailure Err.Number, "on IADs::SetInfo method"
End If
 
show_items "Success! Added value to adminContextMenu property of user-Display: " & sValue
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
Sub show_items(strText)
    MsgBox strText, vbInformation, "Add admin context menu"
End Sub
 
Sub BailOnFailure(ErrNum, ErrText)    strText = "Error 0x" & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



 

 




