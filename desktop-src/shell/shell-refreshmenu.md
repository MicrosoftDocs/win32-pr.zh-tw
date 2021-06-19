---
description: 深入瞭解 RefreshMenu 方法，此方法會重新整理 [開始] 功能表的內容。 只能與 Windows XP 之前的系統搭配使用。
ms.assetid: 1269c66d-61df-432d-9220-5ac975e3ad58
title: 'RefreshMenu 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.RefreshMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 90020cd128f5cbc585bd7bc9ab33a8a81c745f8e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404531"
---
# <a name="shellrefreshmenu-method"></a>RefreshMenu 方法

重新整理 [ **開始** ] 功能表的內容。 只能與 Windows XP 之前的系統搭配使用。

## <a name="syntax"></a>語法


```JScript
iRetVal = Shell.RefreshMenu()
```


```VB

Shell.RefreshMenu() As Integer
```





## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="remarks"></a>備註

**RefreshMenu** 提供的功能會在 Windows XP 或更新版本下自動處理。 請勿在該作業系統下呼叫這個方法。

## <a name="examples"></a>範例

下列範例顯示使用中的 **RefreshMenu** 。 JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。

Jscript：


```JScript
<script language="JScript">
    function fnShellRefreshMenuJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.RefreshMenu();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellRefreshMenuVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.RefreshMenu

        set objShell = nothing
    end function
 </script>
```



Visual Basic：


```VB
Private Sub fnShellRefreshMenuVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.RefreshMenu

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



 

 




