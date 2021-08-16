---
description: Shell. NameSpace 方法-建立並傳回指定資料夾的資料夾物件。
ms.assetid: c0d61bc6-6851-4b47-a62d-4c24d2958b98
title: 'Shell. NameSpace 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.NameSpace
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 41542f133961104180257b9c15b1843f3458bf6d9d2dd156fa3d97ea7b9ca87d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857737"
---
# <a name="shellnamespace-method"></a>Shell. NameSpace 方法

建立並傳回指定資料夾的 [**資料夾**](folder.md) 物件。

## <a name="syntax"></a>語法


```JScript
retVal = Shell.NameSpace(
  vDir
)
```


```VB

Shell.NameSpace( _
  ByVal vDir As Variant _
) As Folder
```





## <a name="parameters"></a>參數

<dl> <dt>

*vDir* \[在\]
</dt> <dd>

類型： **Variant**

要建立 [**資料夾**](folder.md) 物件的資料夾。 這可以是指定資料夾路徑或其中一個 [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) 值的字串。 請注意，在 **ShellSpecialFolderConstants** 中找到的常數名稱可以在 Visual Basic 中使用，但不能在 VBScript 或 JScript 中使用。 在這些情況下，必須在其位置使用數值。

</dd> </dl>

## <a name="return-value"></a>傳回值

### <a name="jscript"></a>JScript

類型： **[**資料夾**](folder.md)\*\***

指定資料夾之 [**資料夾**](folder.md) 物件的物件參考。 如果未成功建立資料夾，此值會傳回 **null**。

### <a name="vb"></a>VB

類型： **[**資料夾**](folder.md)\*\***

指定資料夾之 [**資料夾**](folder.md) 物件的物件參考。 如果未成功建立資料夾，此值會傳回 **null**。

## <a name="examples"></a>範例

下列範例顯示使用中的 **命名空間** 。 JScript、VBScript 和 Visual Basic 都會顯示適當的使用方式。

JScript：


```JScript
<script language="JScript">
    function fnShellNameSpaceJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfWINDOWS = 36
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            alert(objFolder.Title);
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellNameSpaceVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\\")

        if (not objFolder is nothing) then
            alert(objFolder.Title)
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



Visual Basic：


```VB
Private Sub fnShellNameSpaceVB()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPERSONAL)

    If (Not objFolder Is Nothing) Then
        Debug.Print objFolder.Title
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (4.71 版或更新版本) </dt> </dl> |



 

 




