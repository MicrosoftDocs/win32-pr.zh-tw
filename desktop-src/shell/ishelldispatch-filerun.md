---
description: 向使用者顯示 [執行] 對話方塊。
ms.assetid: BC7C4C26-593D-4467-A2AA-4F2DF835C989
title: 'IShellDispatch. FileRun 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.FileRun
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 56806edf06d334d90ad038886d955c00876f8f0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691224"
---
# <a name="ishelldispatchfilerun-method"></a>IShellDispatch. FileRun 方法

向使用者顯示 [ **執行** ] 對話方塊。

## <a name="syntax"></a>語法


```JScript
IShellDispatch.FileRun()
```


```VB

IShellDispatch.FileRun()
```





## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

### <a name="jscript"></a>JScript

這個方法不會傳回值。

### <a name="vb"></a>VB

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法是透過 [**FileRun**](shell-filerun.md) 方法來執行和存取。

## <a name="examples"></a>範例

下列範例示範如何在 JScript、VBScript 和 Visual Basic 中使用 **FileRun** 。

Jscript：


```JScript
<script language="JScript">
    function fnShellFileRunJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.FileRun();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellFileRunVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.FileRun

        set objShell = nothing
    end function
 </script>
```



Visual Basic：


```VB
Private Sub fnShellFileRunVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.FileRun

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



 

 




