---
description: 以水準方式並排顯示桌面上的所有視窗。 這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [並排 Windows]。
ms.assetid: b0e06766-1bd4-4744-81f3-139b018aa72c
title: 'TileHorizontally 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.TileHorizontally
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: da11496ca9993c87f78a9209a2c6d04bc0167349a6c0b955a3b2823335f30464
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709478"
---
# <a name="shelltilehorizontally-method"></a>TileHorizontally 方法

以水準方式並排顯示桌面上的所有視窗。 這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [**並排 Windows**]。

## <a name="syntax"></a>語法


```JScript
iRetVal = Shell.TileHorizontally()
```


```VB

Shell.TileHorizontally() As Integer
```





## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="examples"></a>範例

下列範例顯示使用中的 **TileHorizontally** 。 JScript、VBScript 和 Visual Basic 都會顯示適當的使用方式。

JScript：


```JScript
<script language="JScript">
    function fnShellTileHorizontallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.TileHorizontally();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellTileHorizontallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.TileHorizontally

        set objShell = nothing
    end function
 </script>
```



Visual Basic：


```VB
Private Sub fnShellTileHorizontallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.TileHorizontally

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



 

 




