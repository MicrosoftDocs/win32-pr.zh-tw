---
description: IShellDispatch4. WindowsSecurity 方法-顯示 [Windows 安全性] 對話方塊。
title: 'IShellDispatch4. WindowsSecurity 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.WindowsSecurity
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 665c4644-7749-446e-8212-3ecc9901a035
ms.openlocfilehash: 8142867d8d0423729794460a077a0f7f12d97f5d9744a119571d3ddd2b90a592
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720710"
---
# <a name="ishelldispatch4windowssecurity-method"></a>IShellDispatch4. WindowsSecurity 方法

顯示 [ **Windows 安全性**] 對話方塊。

## <a name="syntax"></a>語法


```JScript
IShellDispatch4.WindowsSecurity()
```


```VB

IShellDispatch4.WindowsSecurity()
```





## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

### <a name="jscript"></a>JScript

這個方法不會傳回值。

### <a name="vb"></a>VB

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會顯示按下 CTRL + ALT + DELETE 或使用 [ **開始** ] 功能表上的 [安全性] 選項之後所顯示的對話方塊。

> [!Note]  
> 只有當終端機會話連線到 Microsoft 終端機伺服器時，才能使用此方法。

 

## <a name="examples"></a>範例

下列範例顯示 JScript、VBScript 和 Visual Basic 的 **WindowsSecurity** 用法。

JScript：


```JScript
<script language="JScript">
     function fnIShellDispatch4WindowsSecurityJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.WindowsSecurity();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
     function fnIShellDispatch4WindowsSecurityVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            objshell.WindowsSecurity
        set objShell = nothing
    end function
 </script>
```



Visual Basic：


```VB
Private Sub fnIShellDispatch4WindowsSecurityVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        objshell.WindowsSecurity
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



 

 




