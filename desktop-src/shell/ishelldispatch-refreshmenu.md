---
description: 瞭解 IShellDispatch RefreshMenu 方法，這會重新整理 [開始] 功能表的內容。 只能搭配 Windows XP 之前的系統使用。
ms.assetid: D36FA5A0-AF03-4627-86E0-869BF1440958
title: 'IShellDispatch. RefreshMenu 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.RefreshMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ac5bb37f5880011fcabcfcc0e923196857694012a547b0391326a9fe5d8424f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969057"
---
# <a name="ishelldispatchrefreshmenu-method"></a>IShellDispatch. RefreshMenu 方法

重新整理 [ **開始** ] 功能表的內容。 只能搭配 Windows XP 之前的系統使用。

## <a name="syntax"></a>語法


```JScript
IShellDispatch.RefreshMenu()
```


```VB

IShellDispatch.RefreshMenu()
```





## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

### <a name="jscript"></a>JScript

這個方法不會傳回值。

### <a name="vb"></a>VB

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法是透過 [**TrayProperties**](shell-trayproperties.md) 方法來執行和存取。

**RefreshMenu** 提供的功能會在 Windows XP 或更新版本下自動處理。 請勿在 Windows XP 或更新版本上呼叫這個方法。

## <a name="examples"></a>範例

下列範例示範如何在 JScript、VBScript 和 Visual Basic 中使用 **RefreshMenu** 。

JScript：


```JScript
<script language="JScript">
    function fnShellRefreshMenuJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.RefreshMenu();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellRefreshMenuVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.RefreshMenu

        set objShell = nothing
    end function
 </script>
```



Visual Basic：


```VB
Private Sub fnShellRefreshMenuVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.RefreshMenu

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



 

 




