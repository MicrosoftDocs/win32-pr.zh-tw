---
description: TrayProperties 方法-顯示 [工作列] 和 [開始功能表屬性] 對話方塊。 這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [屬性] 相同。
ms.assetid: 0d82d847-9e6f-461e-b938-fe8fd49a636f
title: 'TrayProperties 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.TrayProperties
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3ef9ed639383b468b68f75e43f1b38b2952795ceb1990f580a766174334dadd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452824"
---
# <a name="shelltrayproperties-method"></a>TrayProperties 方法

顯示 [ **工作列] 和 [開始功能表屬性** ] 對話方塊。 這個方法的效果與在工作列上按一下滑鼠右鍵，然後選取 [ **屬性**] 相同。

## <a name="syntax"></a>語法


```JScript
iRetVal = Shell.TrayProperties()
```


```VB

Shell.TrayProperties() As Integer
```





## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="examples"></a>範例

下列範例顯示使用中的 **TrayProperties** 。 JScript、VBScript 和 Visual Basic 都會顯示適當的使用方式。

JScript：


```JScript
<script language="JScript">
    function fnShellTrayPropertiesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.TrayProperties();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellTrayPropertiesVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.TrayProperties

        set objShell = nothing
    end function
 </script>
```



Visual Basic：


```VB
Private Sub fnShellTrayPropertiesVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.TrayProperties

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



 

 




