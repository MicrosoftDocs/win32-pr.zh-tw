---
description: Shell. ToggleDesktop 方法-顯示或隱藏桌面。
title: 'ToggleDesktop 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ToggleDesktop
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: BD07F7F2-A588-4189-95F4-3A8E2905E8F5
ms.openlocfilehash: 2007b133e6ef13ab4c4284ddff8486307c5beb6e0450b067699a0f6316df8d7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968507"
---
# <a name="shelltoggledesktop-method"></a>ToggleDesktop 方法

顯示或隱藏桌面。

## <a name="syntax"></a>語法


```JScript
Shell.ToggleDesktop()
```


```VB

Shell.ToggleDesktop()
```





## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

### <a name="jscript"></a>JScript

這個方法不會傳回值。

### <a name="vb"></a>VB

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法的效果與工作列上的 [ **顯示桌面** ] 按鈕相同。 它會隱藏所有開啟的視窗以顯示桌面，或顯示所有開啟的視窗來隱藏桌面。 **ToggleDesktop** 方法不會顯示使用者介面，它只會叫用切換動作。

## <a name="examples"></a>範例

下列範例示範如何適當地使用 JScript、VBScript 和 Visual Basic 的 **ToggleDesktop** 。

JScript：


```JScript
<script language="JScript">
    function fnIShellDispatch4ToggleDesktopJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ToggleDesktop();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnIShellDispatch4ToggleDesktopVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            objShell.ToggleDesktop
        set objShell = nothing
    end function
 </script>
```



Visual Basic：


```VB
Private Sub fnIShellDispatch4ToggleDesktopVB()
    Dim objShell As Shell
            
    Set objShell = New Shell
        objShell.ToggleDesktop
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (6.0 版或更新版本) </dt> </dl> |



 

 




