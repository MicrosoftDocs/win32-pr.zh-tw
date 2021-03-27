---
description: 在 FolderItem 物件的集合上執行動詞。 這個方法是 InvokeVerb 方法的擴充功能，可讓您透過一組旗標來進行作業的額外控制。
ms.assetid: 2c02985d-8877-4a02-a232-6aeb1716928c
title: 'FolderItems2. InvokeVerbEx 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems2.InvokeVerbEx
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: aa9b986b5cb76f14cc950f522e1e289224c17b58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971880"
---
# <a name="folderitems2invokeverbex-method"></a>FolderItems2. InvokeVerbEx 方法

在 [**FolderItem**](folderitem.md) 物件的集合上執行動詞。 這個方法是 [**InvokeVerb**](folderitem-invokeverb.md) 方法的擴充功能，可讓您透過一組旗標來進行作業的額外控制。

## <a name="syntax"></a>語法


```JScript
iRetVal = FolderItems2.InvokeVerbEx(
  [ vVerb ],
  [ vArgs ]
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*vVerb* \[在中，選擇性\]
</dt> <dd>

類型： **Variant**

具有對應至要執行之命令的動詞字串的 **變異** 。 如果未指定任何動詞，則會執行預設的動詞命令。

</dd> <dt>

*vArgs* \[在中，選擇性\]
</dt> <dd>

類型： **Variant**

由 *vVerb* 所指定之命令具有一個或多個引數的字串所組成的 **Variant** 。 這個字串的格式取決於特定的動詞。

</dd> </dl>

## <a name="remarks"></a>備註

動詞命令是用來指定與專案或專案集合相關聯之特定動作的字串。 一般來說，呼叫動詞會啟動相關的應用程式。 例如，呼叫 .txt 檔案上的 **open** 動詞通常會以文字編輯器（通常是 Microsoft 記事本）開啟檔案。 如需動詞的進一步討論，請參閱 [啟動應用程式](launch.md)。

## <a name="examples"></a>範例

下列範例會使用 **InvokeVerbEx** 來叫用 **我的電腦** 上 ( "open" ) 的預設動詞。 JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。

Jscript：


```JScript
<script language="JScript">
    function fnFolderItems2InvokeVerbExJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder;
        var ssfDRIVES = 17;
        
        objFolder = objShell.NameSpace(ssfDRIVES);
        if (objFolder != null)
        {
            var objFolderItems2;
            
            objFolderItems2 = objFolder.Items();
            if (objFolderItems2 != null)
            {
                objFolderItems2.InvokeVerbEx();
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnFolderItems2InvokeVerbExVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfDRIVES
                
            ssfWINDOWS = 17
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItems2
                        
                set objFolderItems2 = objFolder.Items()
                if (not objFolderItems2 is nothing) then
                    objFolderItems2.InvokeVerbEx
                end if
                set objFolderItems2 = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



Visual Basic：


```VB
Private Sub fnFolderItems2InvokeVerbExVB()
    Dim objShell      As Shell
    Dim objFolder     As Folder2
    Dim ssfDRIVES     As Long
    
    ssfDRIVES = 17
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfDRIVES)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItems2 As FolderItems
            
            Set objFolderItems2 = objFolder.Items
                If (Not objFolderItems2 Is Nothing) Then
                    objFolderItems2.InvokeVerbEx
                End If
            Set objFolderItems2 = Nothing
        End If
    Set objFolder = Nothing
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

[**FolderItems2**](folderitems2-object.md)
</dt> <dt>

[**InvokeVerb**](folderitem-invokeverb.md)
</dt> </dl>

 

 




