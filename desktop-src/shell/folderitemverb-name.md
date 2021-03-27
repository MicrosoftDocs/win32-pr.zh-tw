---
description: 包含動詞的名稱。
ms.assetid: d18fddac-eb51-4031-a572-1bfef2f757a9
title: 'FolderItemVerb.Name 屬性 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItemVerb.Name
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5d352f02486f1d7304d4c474aa836401bfef635e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971872"
---
# <a name="folderitemverbname-property"></a>FolderItemVerb.Name 屬性

包含動詞的名稱。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
strName = FolderItemVerb.Name
```



## <a name="property-value"></a>屬性值

可接收 Name 屬性之 [**BSTR**](/previous-versions/windows/desktop/automat/bstr) 類型的變數。

## <a name="examples"></a>範例

下列範例會使用 **名稱** ，在使用者的程式資料夾回應的動詞集合中取出第一個專案的名稱。 JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。

Jscript：


```JScript
<script language="JScript">
    function fnFolderItemVerbNameJ()
    {
        var objShell    = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objVerbs;
            
            objVerbs = objFolder.Self.Verbs();
            if (objVerbs != null)
            {
                var szReturn = "";
                
                szReturn = objVerbs.Item(0).Name;
                alert(szReturn);
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnFolderItemVerbNameVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfPROGRAMS
            
            ssfPROGRAMS = 2
            set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objVerbs
                
                set objVerbs = objFolder.Self.Verbs
                    if (not objVerbs is nothing) then
                        dim szReturn
                        
                        szReturn = objVerbs.Item(0).Name
                        alert(szReturn)
                    end if
                set objVerbs = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



Visual Basic：


```VB
Private Sub fnFolderItemVerbNameVB()
    Dim objShell    As Shell
    Dim objFolder2  As Folder2
    Dim ssfPROGRAMS As Long
            
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfPROGRAMS)
    If (Not objFolder2 Is Nothing) Then
        Dim objVerbs As FolderItemVerbs
        
        Set objVerbs = objFolder2.Self.Verbs
            If (Not objVerbs Is Nothing) Then
                Dim szReturn As String
                
                szReturn = objVerbs.Item(0).Name
                Debug.Print szReturn
            End If
        Set objVerbs = Nothing
    End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (4.71 版或更新版本) </dt> </dl> |



 

 
