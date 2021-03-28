---
description: Windows Shell 提供一組強大的自動化物件，可讓您以 Microsoft Visual Basic 和指令碼語言（例如 Microsoft JScript）來設計 Shell， (與 ECMA 262 語言規格相容) 和 Microsoft Visual Basic Scripting Edition (VBScript) 。 您可以使用這些物件來存取許多 Shell 的功能和對話方塊。 例如，您可以存取檔案系統、啟動程式，以及變更系統設定。
title: 可編寫腳本的 Shell 物件
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 09455fad-a769-42ef-83ba-b745ac819bf3
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4c39e7e58a9715598056fb74aa154ed8a850f523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973605"
---
# <a name="scriptable-shell-objects"></a>可編寫腳本的 Shell 物件

Windows Shell 提供一組強大的自動化物件，可讓您以 Microsoft Visual Basic 和指令碼語言（例如 Microsoft JScript）來設計 Shell， (與 ECMA 262 語言規格相容) 和 Microsoft Visual Basic Scripting Edition (VBScript) 。 您可以使用這些物件來存取許多 Shell 的功能和對話方塊。 例如，您可以存取檔案系統、啟動程式，以及變更系統設定。

本節介紹可編寫腳本的 Shell 物件。

-   [Shell 版本](#shell-versions)
-   [具現化 Shell 物件](#instantiating-shell-objects)
    -   [晚期繫結](#late-binding)
    -   [HTML 物件元素](#html-object-element)
-   [Shell 物件](#shell-object)
    -   [安全性](#security)
-   [資料夾物件](#folder-objects)

## <a name="shell-versions"></a>Shell 版本

許多 Shell 物件在 Shell 的 [4.71 版](versions.md) 中都有提供。 其他則可在5.00 版和更新版本中使用。 Windows 2000 已可使用5.00 版。 下表列出物件變成可用之 Shell 版本底下的每個 Shell 物件。



| 版本4.71                                            | 版本5.00                                          |
|---------------------------------------------------------|-------------------------------------------------------|
| [**資料夾**](folder.md)                                | [**DIDiskQuotaUser**](didiskquotauser-object.md)     |
| [**FolderItemVerb**](folderitemverb.md)                | [**DiskQuotaControl**](diskquotacontrol-object.md)   |
| [**FolderItemVerbs**](folderitemverbs.md)              | [**Folder2**](folder2-object.md)                     |
| [**殼層**](shell.md)                                  | [**FolderItem**](folderitem.md)                      |
| [**ShellFolderView**](shellfolderview.md)              | [**FolderItems**](folderitems.md)                    |
| [**ShellUIHelper**](shelluihelper.md)                  | [**FolderItems2**](folderitems2-object.md)           |
| [**ShellWindows**](shellwindows.md)                    | [**IShellDispatch2**](ishelldispatch2-object.md)     |
| [**WebViewFolderContents**](../lwef/webviewfoldercontents.md) | [**IShellLinkDual2**](ishelllinkdual2-object.md)     |
|                                                         | [**ShellFolderItem**](shellfolderitem-object.md)     |
|                                                         | [**ShellFolderViewOC**](shellfolderviewoc-object.md) |
|                                                         | [**ShellLinkObject**](shelllinkobject-object.md)     |



 

## <a name="instantiating-shell-objects"></a>具現化 Shell 物件

若要在使用早期繫結的 Visual Basic 應用程式中具現化 Shell 物件，請在您的專案中新增下列程式庫的參考：

-   Microsoft Internet Controls (Shdocvw.dll) 
-   Microsoft Shell 控制項和自動化 (Shell32) 

### <a name="late-binding"></a>晚期繫結

您也可以使用晚期繫結將許多 Shell 物件具現化。 這種方法適用于 Visual Basic 應用程式和腳本。 下列範例顯示如何在 JScript 中具現化 [**Shell**](shell.md) 物件。


```
<SCRIPT LANGUAGE="JScript">
<!--
    function fnCreateShell()    
    {
        // Instantiate the Shell object and invoke its FileRun method.
        var oShell = new ActiveXObject("shell.application");
        oshell.FileRun;
    }
-->
</SCRIPT>
```



下列範例顯示如何在 VBScript 中具現化 [**資料夾**](folder.md) 物件。


```
<SCRIPT LANGUAGE="VBScript">
<!--
    function fnCreateFolder()
        dim oShell    
        dim oFolder
        dim sDir

        sDir = "C:\SomePath" 
        set oShell = CreateObject("shell.application")
        set oFolder = oShell.NameSpace(sDir)  
    end function
-->  
</SCRIPT>
```



在上述範例中， *sDir* 是 [**資料夾**](folder.md) 物件的路徑。 請注意，腳本中無法使用 [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) 列舉值。

下表顯示每個 Shell 物件的 ProgID。



| Object                                                  | ProgID                                                                                  |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**DIDiskQuotaUser**](didiskquotauser-object.md)       | DiskQuota. 1                                                                   |
| [**DiskQuotaControl**](diskquotacontrol-object.md)     | 無法晚期繫結                                                                        |
| [**資料夾**](folder.md)                                | 殼。Shell \_ 應用程式。命名空間 ( "..." )                                                |
| [**Folder2**](folder2-object.md)                       | 殼。Shell \_ 應用程式。命名空間 ( "..." )                                                |
| [**FolderItem**](folderitem.md)                        | 殼。Shell \_ 應用程式。命名空間 ( "..." ) 。Self 或 Folder. 專案或資料夾. ParseName |
| [**FolderItems**](folderitems.md)                      | 資料夾。專案                                                                            |
| [**FolderItems2**](folderitems2-object.md)             | 資料夾。專案                                                                            |
| [**FolderItemVerb**](folderitemverb.md)                | Shell. NameSpace ( "..." ) 。Self. () 的專案                                                |
| [**FolderItemVerbs**](folderitemverbs.md)              | FolderItem，或 Shell. NameSpace ( "..." ) 。自我動詞                                   |
| [**IShellDispatch2**](ishelldispatch2-object.md)       | 殼。Shell \_ 應用程式                                                                |
| [**IShellLinkDual2**](ishelllinkdual2-object.md)       | Shell. NameSpace ( "..." ) 。GetLink 或 Shell. NameSpace ( "..." ) 。 () 專案。GetLink           |
| [**殼層**](shell.md)                                  | 殼。Shell \_ 應用程式                                                                |
| [**ShellFolderItem**](shellfolderitem-object.md)       | Shell. NameSpace ( "..." ) 。Self 或 Shell. NameSpace ( "..." ) 。專案 ()                            |
| [**ShellFolderView**](shellfolderview.md)              | 無法晚期繫結                                                                        |
| [**ShellFolderViewOC**](shellfolderviewoc-object.md)   | 無法晚期繫結                                                                        |
| [**ShellLinkObject**](shelllinkobject-object.md)       | Shell. NameSpace ( "..." ) 。GetLink 或 Shell. NameSpace ( "..." ) 。 () 專案。GetLink           |
| [**ShellUIHelper**](shelluihelper.md)                  | 無法晚期繫結                                                                        |
| [**ShellWindows**](shellwindows.md)                    | 殼。Shell \_ 視窗或 ShellWindows。 \_NewEnum                                          |
| [**WebViewFolderContents**](../lwef/webviewfoldercontents.md) | 無法晚期繫結                                                                        |



 

### <a name="html-object-element"></a>HTML 物件元素

您也可以使用 [**OBJECT**](https://msdn.microsoft.com/library/ms535859(v=VS.85).aspx) 元素，在 HTML 網頁上具現化 Shell 物件。 若要這樣做，請將 **物件** 專案的 **ID** 屬性設定為您將在腳本中使用的變數名稱，並使用其註冊的數位 (CLASSID) 來識別物件。 下列 HTML 會使用 **object** 元素來建立 [**ShellFolderItem**](shellfolderitem-object.md)物件的實例。


```
<OBJECT ID="oShFolderItem" 
    NAME="Shell Folder Item Object"
    CLASSID="clsid:2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e">
</OBJECT>
```



下表列出每個 Shell 物件及其各自的 CLASSID。



|                                                         |                                      |
|---------------------------------------------------------|--------------------------------------|
| [**DIDiskQuotaUser**](didiskquotauser-object.md)       | 7988B571-EC89-11cf-9C00-00AA00A14F56 |
| [**DiskQuotaControl**](diskquotacontrol-object.md)     | 7988B571-EC89-11cf-9C00-00AA00A14F56 |
| [**資料夾**](folder.md)                                | BBCBDE60-C3FF-11CE-8350-444553540000 |
| [**Folder2**](folder2-object.md)                       | f0d2d8ef-3890-11d2-bf8b-00c04fb93661 |
| [**FolderItem**](folderitem.md)                        | 744129E0-CBE5-11CE-8350-444553540000 |
| [**FolderItems**](folderitems.md)                      | 744129E0-CBE5-11CE-8350-444553540000 |
| [**FolderItems2**](folderitems2-object.md)             | C94F0AD0-F363-11d2-A327-00C04F8EEC7F |
| [**FolderItemVerb**](folderitemverb.md)                | 08EC3E00-50B0-11CF-960C-0080C7F4EE85 |
| [**FolderItemVerbs**](folderitemverbs.md)              | 1F8352C0-50B0-11CF-960C-0080C7F4EE85 |
| [**IShellDispatch2**](ishelldispatch2-object.md)       | A4C6892C-3BA9-11d2-9DEA-00C04FB16162 |
| [**IShellLinkDual2**](ishelllinkdual2-object.md)       | 317EE249-F12E-11d2-B1E4-00C04F8EEB3E |
| [**殼層**](shell.md)                                  | 13709620-C279-11CE-A49E-444553540000 |
| [**ShellFolderItem**](shellfolderitem-object.md)       | 2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e |
| [**ShellFolderView**](shellfolderview.md)              | 62112AA1-EBE4-11cf-A5FB-0020AFE7292D |
| [**ShellFolderViewOC**](shellfolderviewoc-object.md)   | 4a3df050-23bd-11d2-939f-00a0c91eedba |
| [**ShellLinkObject**](shelllinkobject-object.md)       | 11219420-1768-11d1-95BE-00609797EA4F |
| [**ShellUIHelper**](shelluihelper.md)                  | 64AB4BB7-111E-11D1-8F79-00C04FC2FBE1 |
| [**ShellWindows**](shellwindows.md)                    | 9BA05972-F6A8-11CF-A442-00A0C90A8F39 |
| [**WebViewFolderContents**](../lwef/webviewfoldercontents.md) | 1820FED0-473E-11D0-A96C-00C04FD705A2 |



 

## <a name="shell-object"></a>Shell 物件

[**Shell**](shell.md)物件代表 shell 中的物件。 您可以使用 Shell 物件所公開的方法來：

-   開啟、流覽和流覽資料夾。
-   將開啟的視窗最小化、還原、重迭顯示或並排顯示。
-   啟動主控台的應用程式。
-   顯示系統對話方塊。

使用者可能最熟悉從 [ **開始** ] 功能表和工作列的快捷方式功能表存取的命令。 當使用者以滑鼠右鍵按一下工作列時，會出現工作列的快捷方式功能表。 下列 HTML 應用程式 (HTA) 會產生具有可執行許多 [**Shell**](shell.md) 物件方法之按鈕的起始頁。 其中一些方法會在 [ **開始** ] 功能表和工作列的快捷方式功能表上執行功能。


```
<HTML>
<HEAD>
    <TITLE>Start Page</TITLE>
    
    <OBJECT ID="oShell"
        CLASSID="clsid:13709620-C279-11CE-A49E-444553540000">
    </OBJECT>
    
    <STYLE>
        INPUT {width: 200} 
    </STYLE>  
    
    <SCRIPT LANGUAGE="VBScript">
    <!--
        function fnStart(sMethod)
            select case sMethod
              case 0    
                  'Minimizes all windows on the desktop
                oshell.Shell_MinimizeAll
              case 1  
                  'Displays the Run dialog box
                oshell.FileRun
              case 2  
                  'Displays the Shut Down Windows dialog box
                oshell.Shell_ShutdownWindows
              case 3  
                  'Displays the Find dialog box
                oshell.Shell_FindFilesr
              case 4  
                  'Displays the Date/Time dialog box
                oshell.Shell_SetTime 
              case 5  
                  'Displays the Internet Properties dialog box
                oshell.Shell_ControlPanelItem "INETCPL.cpl"
              case 6  
                  'Explores the My Documents folder
                oshell.Shell_Explore "C:\My Documents"
              case 7  
                  'Enables user to select folder from Program Files
                oshell.Shell_BrowseForFolder 0, "My Programs", 0, "C:\Program Files" 
              case 8  
                  'Opens the Favorites folder
                oshell.Shell_Open "C:\WINDOWS\Favorites"
              case 9  
                  'Displays the Taskbar Properties dialog box
                oshell.Shell_TrayProperties
            end select  
        end function      
    -->
    </SCRIPT>
</HEAD>

<BODY>
    <H1>Start...</H1>
    <INPUT type="button" value="Edit Taskbar Properties" onclick="fnStart(9)"><br>
    <INPUT type="button" value="Open Favorites Folder" onclick="fnStart(8)"><br>
    <INPUT type="button" value="Browse Program Files" onclick="fnStart(7)"><br>
    <INPUT type="button" value="Explore My Documents" onclick="fnStart(6)"><br>
    <INPUT type="button" value="Modify Internet Properties" onclick="fnStart(5)"><br>
    <INPUT type="button" value="Set System Time" onclick="fnStart(4)"><br>
    <INPUT type="button" value="Find a File or Folder" onclick="fnStart(3)"><br>
    <INPUT type="button" value="Shut Down Windows" onclick="fnStart(2)"><br>
    <INPUT type="button" value="Run" onclick="fnStart(1)">     
    <INPUT type="button" value="Minimize All Windows" onclick="fnStart(0)">     
</BODY>
</HTML>
```



### <a name="security"></a>安全性

以應用程式來說，HTA 會在與網頁不同的安全性模型下執行。 若要與執行 Shell 物件功能的網頁互動，使用者必須啟用 [ **初始化] 和 [編寫 ActiveX 控制項未標示為安全的 ActiveX 控制項** ] 選項，以供他們在其中查看頁面的安全性區域使用。

## <a name="folder-objects"></a>資料夾物件

[**Folder**](folder.md)物件代表 Shell 資料夾。 您可以使用資料夾物件所公開的方法來：

-   取得資料夾的相關資訊。
-   建立子資料夾。
-   將檔案物件複製並移至資料夾。

[**FolderItem**](folderitem.md)物件代表 Shell 資料夾中的專案。 它的屬性可讓您取得專案的相關資訊。 您可以使用此物件所公開的方法來執行專案的動詞，或取得專案之 [**FolderItemVerbs**](folderitemverbs.md) 物件的相關資訊。

[**FolderItems**](folderitems.md)物件代表 Shell 資料夾中的專案集合。 它的方法和屬性可讓您取得集合的相關資訊。

下列 Visual Basic 範例會顯示數個資料夾物件之間的關聯性，以及如何搭配使用它們。 當使用者按一下名為 **cmdGetPath** 的命令按鈕時，程式會顯示一個對話方塊，讓使用者從 **我的電腦** 選取資料夾，其中 SsfDRIVES 是 **我的電腦** 的 [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants)列舉值。 當使用者選擇資料夾時，該資料夾的路徑會顯示在名為 **txtPath** 的文字方塊中。


```
Private Sub cmdGetPath_Click()
    Dim oShell As New Shell
    Dim oFolder As Folder
    Dim oFolderItem As FolderItem
 
    Set oFolder = oshell.Shell_BrowseForFolder(Me.hWnd, "Select a Folder", 0, ssfDrives)
   
    Set oFolderItem = oFolderItems.Item

    txtPath.Text = oFolderItem.Path
End Sub
```



在 VBScript 中，此函式會稍有不同，因為腳本中無法使用 [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) 的列舉值。 下列範例顯示前一個範例的 VBScript 對等專案。


```
<SCRIPT LANGUAGE="VBScript">
<!--
    function fnGetMyPathVB() 
        dim oShell
        dim oFolder
        dim oFolderItem
        
        set oShell = CreateObject("shell.application")      
        set oFolder = oshell.Shell_BrowseForFolder(0, "Choose a Folder", 0)             
        set oFolderItem = oFolder.Items.Item         
        
        document.all.item("myPath").innerText = oFolderItem.Path                                
    end function
-->
</SCRIPT>
```



在下列 JScript 範例中（這是先前 VBScript 範例的直接轉譯），請注意如何使用空括弧 ' () ' 來叫用 [**專案**](folder-items.md) 和 [**專案**](folderitems-item.md) 方法。


```
<SCRIPT LANGUAGE="JavaScript">
<!--
    function fnGetMyPathJ() 
    {       
        var oShell = new ActiveXObject("shell.application");
                    
        var oFolder = new Object;                   
        oFolder = oshell.Shell_BrowseForFolder(0, "Choose a folder", 0);
                                
        var oFolderItem = new Object;       
        oFolderItem = oFolder.Items().Item();                               
        
        document.all.item("myPath").innerText = oFolderItem.Path;
    }    
-->
</SCRIPT>
```



 

 
