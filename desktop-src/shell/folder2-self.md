---
description: 包含資料夾的 FolderItem 物件。
ms.assetid: 0964505d-4138-4444-91d4-46c707c45688
title: 'Folder2： Self 屬性 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2.Self
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f49666096f35f9871f8a3b3c141d4bc169dea0c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191046"
---
# <a name="folder2self-property"></a>Folder2。 Self 屬性

包含資料夾的 [**FolderItem**](folderitem.md) 物件。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
Self = Folder2.Self
```



## <a name="property-value"></a>屬性值

評估為資料夾 [**FolderItem**](folderitem.md) 物件的物件。

## <a name="examples"></a>範例

下列範例會使用 **Self** 來取得 C [](folderitem.md) ： Windows 資料夾的 FolderItem \\ 。 JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。

Jscript：


```JScript
<script language="JScript">
    function fnFolder2ObjectSelfJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder2 = new Object;
        
        objFolder2 = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder2 != null)
        {
            var objFolderItem = new Object;
            
            objFolderItem = objFolder2.Self;
            if (objFolderItem != null)
            {
                //Add code here.
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnFolder2ObjectSelfVB()
        dim objShell
        dim objFolder2

        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder2 is nothing) then
            dim objFolderItem
            
            set objFolderItem = objFolder2.Self

            if (not objFolderItem is nothing) then
                'Add code here.
            end if
        end if

        set objFolder2 = nothing
        set objShell = nothing
    end function
</script>
```



Visual Basic：


```VB
Private Sub btnFolder2Self_Click()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2

    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder2 Is Nothing) Then
        Dim objFolderItem As FolderItem
        
        Set objFolderItem = objFolder2.Self()

        If (Not objFolderItem Is Nothing) Then
            'Add code here.
        End If

        Set objFolderItem = Nothing
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Folder2**](folder2-object.md)
</dt> <dt>

[**資料夾**](folder.md)
</dt> </dl>

 

 




