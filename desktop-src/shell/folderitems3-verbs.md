---
description: 取得所有資料夾專案通用的動詞命令清單。
ms.assetid: f72f5dcc-35e0-4a23-ae4c-355da2858aab
title: FolderItems3)  (的動詞屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems3.Verbs
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 7e07da0b4901b4d4ba7a1bda1f20d3f58298f9d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689244"
---
# <a name="folderitems3verbs-property"></a>FolderItems3 動詞屬性

取得所有資料夾專案通用的動詞命令清單。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
Verbs = FolderItems3.Verbs
```



## <a name="property-value"></a>屬性值

指向動詞集合之指標的位址。 請參閱 [**FolderItemVerbs**](folderitemverbs.md)。

## <a name="examples"></a>範例

下列範例顯示 JScript、VBScript 和 Visual Basic 的 **動詞動詞** 正確用法。

Jscript：


```JScript
<script language="JScript">
    function fnFolderItems3VerbsJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder;
        var ssfWINDOWS = 17;
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            var objFolderItems3;
            
            objFolderItems3 = objFolder.Items();
            if (objFolderItems3 != null)
            {
                var objFolderItemVerbs;
                
                objFolderItemVerbs = objFolderItems3.Verbs;
                alert(objFolderItemVerbs.Item(0));
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnFolderItems3VerbsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfDRIVES
                
            ssfWINDOWS = 17
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItems3
                        
                set objFolderItems3 = objFolder.Items()
                if (not objFolderItems3 is nothing) then
                    dim objFolderItemVerbs
                    
                    set objFolderItemVerbs = objFolderItems3.Verbs
                        if (not objFolderItemVerbs is nothing) then
                            alert(objFolderItemVerbs.Item(0))
                        end if
                    set objFolderItemVerbs = nothing
                end if
                set objFolderItems3 = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



Visual Basic：


```VB
Private Sub fnFolderItems3VerbsVB()
    Dim objShell   As Shell
    Dim objFolder  As Folder
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItems3 As FolderItems3
            
            Set objFolderItems3 = objFolder.Items
                If (Not objFolderItems3 Is Nothing) Then
                    Dim objFolderItemVerbs As FolderItemVerbs
                    
                    Set objFolderItemVerbs = objFolderItems3.Verbs
                        If (Not objFolderItemVerbs Is Nothing) Then
                            Debug.Print objFolderItemVerbs.Item(0)
                        End If
                    Set objFolderItemVerbs = Nothing
                End If
            Set objFolderItems3 = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                                                   |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (6.0 版或更新版本) </dt> </dl> |



 

 




