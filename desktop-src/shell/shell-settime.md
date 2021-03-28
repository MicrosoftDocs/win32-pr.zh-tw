---
description: 顯示 [日期和時間屬性] 對話方塊。 這個方法的效果與以滑鼠右鍵按一下工作列狀態區域中的時鐘，然後選取 [調整日期/時間]。
ms.assetid: 01694607-3fc2-4d0d-ba48-5bdbb40da000
title: 'SetTime 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.SetTime
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b610effe87bd9e4ab33a6e8396e90f79e7bbbe9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973253"
---
# <a name="shellsettime-method"></a>SetTime 方法

顯示 [ **日期和時間屬性** ] 對話方塊。 這個方法的效果與以滑鼠右鍵按一下工作列狀態區域中的時鐘，然後選取 [ **調整日期/時間**]。

## <a name="syntax"></a>語法


```JScript
iRetVal = Shell.SetTime()
```


```VB

Shell.SetTime() As Integer
```





## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="examples"></a>範例

下列範例顯示使用中的 **SetTime** 。 JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。

Jscript：


```JScript
<script language="JScript">
    function fnShellSetTimeJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.SetTime();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellSetTimeVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.SetTime
 
        set objShell = nothing
    end function
 </script>
```



Visual Basic：


```VB
Private Sub fnShellSetTimeVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.SetTime
 
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



 

 




