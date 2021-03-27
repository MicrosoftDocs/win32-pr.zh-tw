---
description: 最小化桌面上的所有視窗。 這個方法的效果與在工作列上按一下滑鼠右鍵，並選取 [將舊版系統上的所有視窗最小化]，或按一下工作列上的 [顯示桌面] 圖示。
ms.assetid: 25DD56B0-221E-44a2-9FAD-FB358ADD7FF1
title: 'IShellDispatch. MinimizeAll 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.MinimizeAll
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b8b8f20ab82a6216a03d772151f852fd9c69b917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512221"
---
# <a name="ishelldispatchminimizeall-method"></a>IShellDispatch. MinimizeAll 方法

最小化桌面上的所有視窗。 這個方法的效果與在工作列上按一下滑鼠右鍵，並選取 [將舊版系統上的 **所有視窗最小化** ]，或按一下工作列上的 [ **顯示桌面** ] 圖示。

## <a name="syntax"></a>語法


```JScript
IShellDispatch.MinimizeAll()
```


```VB

IShellDispatch.MinimizeAll()
```





## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

### <a name="jscript"></a>JScript

這個方法不會傳回值。

### <a name="vb"></a>VB

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法是透過 [**MinimizeAll**](shell-minimizeall.md) 方法來執行和存取。

## <a name="examples"></a>範例

下列範例示範如何使用 **MinimizeAll** 在 JScript、VBScript 和 Visual Basic 中使用。

Jscript：


```JScript
<script language="JScript">
    function fnShellMinimizeAllJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.MinimizeAll();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellMinimizeAllVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.MinimizeAll

        set objShell = nothing
    end function
 </script>
```



Visual Basic：


```VB
Private Sub fnShellMinimizeAllVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.MinimizeAll

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



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IShellDispatch**](ishelldispatch.md)
</dt> <dt>

[**UndoMinimizeALL**](shell-undominimizeall.md)
</dt> </dl>

 

 




