---
description: IShellDispatch 方法-建立並傳回 ShellWindows 物件。 此物件代表屬於 Shell 的所有已開啟視窗的集合。
ms.assetid: 788E2106-3534-4e22-801F-677FD02BDFE0
title: 'IShellDispatch 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Windows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 16991d6a251909e8f3b277894a96e6ad08a7f9a4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117166"
---
# <a name="ishelldispatchwindows-method"></a>IShellDispatch 方法

建立並傳回 [**ShellWindows**](shellwindows.md) 物件。 此物件代表屬於 Shell 的所有已開啟視窗的集合。

## <a name="syntax"></a>語法


```JScript
retVal = IShellDispatch.Windows()
```


```VB

IShellDispatch.Windows() As IDispatch
```





## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

### <a name="jscript"></a>JScript

類型： **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***

[**ShellWindows**](shellwindows.md)物件的物件參考。

### <a name="vb"></a>VB

類型： **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***

[**ShellWindows**](shellwindows.md)物件的物件參考。

## <a name="remarks"></a>備註

這個方法是透過 [**Shell. Windows**](shell-windows.md) 方法來執行和存取。

## <a name="examples"></a>範例

下列範例會使用 **Windows** 抓取 [**ShellWindows**](shellwindows.md) 物件，並顯示它所包含的專案數計數。 JScript、VBScript 和 Visual Basic 會顯示使用方式。

Jscript：


```JScript
<script language="JScript">
    function fnShellWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objshell.Windows();

        if (objShellWindows != null)
        {
            alert(objShellWindows.Count);
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellWindowsVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Windows

        if (not objShellWindows is nothing) then
            alert(objShellWindows.Count)
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



Visual Basic：


```VB
Private Sub fnShellWindowsVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Windows

    If (Not objShellWindows Is Nothing) Then
        Debug.Print objShellWindows.Count
    End If

    Set objShellWindows = Nothing
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



 

 
