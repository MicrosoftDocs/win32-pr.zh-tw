---
description: 在 Shell 專案上執行動詞命令。
ms.assetid: aac3f338-6074-4b1f-9b2f-e6206db52419
title: 'ShellFolderItem. InvokeVerbEx 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderItem.InvokeVerbEx
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 627c2b40869ac9c509dcd645ec259de7db118235
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972452"
---
# <a name="shellfolderiteminvokeverbex-method"></a>ShellFolderItem. InvokeVerbEx 方法

在 Shell 專案上執行動詞命令。

## <a name="syntax"></a>語法


```JScript
iRetVal = ShellFolderItem.InvokeVerbEx(
  [ vVerb ],
  [ vArgs ]
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*vVerb* \[在中，選擇性\]
</dt> <dd>

類型： **Variant**

**Variant** ，包含對應至要執行之命令的動詞字串。 它必須是專案的 [**Name**](folderitemverb-name.md) 屬性所傳回的其中一個值。 如果未指定任何動詞，則會執行預設的動詞命令。

</dd> <dt>

*vArgs* \[在中，選擇性\]
</dt> <dd>

類型： **Variant**

由 *vVerb* 所指定之命令具有一個或多個引數的字串所組成的 **Variant** 。 這個字串的格式取決於特定的動詞。

</dd> </dl>

## <a name="remarks"></a>備註

動詞命令是用來指定專案所支援之特定動作的字串。 一般來說，呼叫動詞會啟動相關的應用程式。 例如，呼叫 .txt 檔案上的 **open** 動詞通常會以文字編輯器（通常是 Microsoft 記事本）開啟檔案。 [**FolderItemVerbs**](folderitemverbs.md)物件表示與專案相關聯的動詞集合。 如需動詞的進一步討論，請參閱 [啟動應用程式](launch.md)。

這個方法類似于 [**InvokeVerb**](folderitem-invokeverb.md)，但它可讓您指定命令的引數以及命令本身。

## <a name="examples"></a>範例

下列範例示範如何在 JScript、VBScript 和 Visual Basic 中正確使用這個方法。

Jscript：


```JScript
<script language="JScript">
    function fnFolderItem2InvokeVerbExJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("NOTEPAD.EXE");
            if (objFolderItem != null)
            {
                objFolderItem.InvokeVerbEx("open", "c:\\autoexec.bat");
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnFolderItemInvokeVerbExVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.Self
                if (not objFolderItem is nothing) then
                    objFolderItem.InvokeVerbEx()
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



Visual Basic：


```VB
Private Sub fnFolderItem2InvokeVerbExVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem2 As Object
            
            Set objFolderItem2 = objFolder2.ParseName("NOTEPAD.EXE")
                If (Not objFolderItem2 Is Nothing) Then
                    objFolderItem2.InvokeVerbEx ("open")
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem2 = Nothing
        Else
            'Folder object returned nothing.
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

[**ShellFolderItem**](shellfolderitem-object.md)
</dt> <dt>

[**InvokeVerb**](folderitem-invokeverb.md)
</dt> </dl>

 

 




