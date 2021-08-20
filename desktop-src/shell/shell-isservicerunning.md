---
description: IsServiceRunning 方法-傳回指出特定服務是否正在執行的值。
ms.assetid: FDC41C2D-7462-458f-BBE6-D97260C26B6C
title: 'IsServiceRunning 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.IsServiceRunning
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 97935e986a0b192e6d6c84c317dc3da711469a035baa8225ac3116229baf9593
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117676852"
---
# <a name="shellisservicerunning-method"></a>IsServiceRunning 方法

傳回值，這個值表示特定服務是否正在執行。

## <a name="syntax"></a>語法


```JScript
retVal = Shell.IsServiceRunning(
  sServiceName
)
```


```VB

Shell.IsServiceRunning( _
  ByVal sServiceName As BSTR _
) As Variant
```





## <a name="parameters"></a>參數

<dl> <dt>

*sServiceName* \[在\]
</dt> <dd>

類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

包含服務名稱的 **字串** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

### <a name="jscript"></a>JScript

類型： **Variant \***

如果 *sServiceName* 所指定的服務正在執行，則傳回 **true** ;否則 **為 false**。

### <a name="vb"></a>VB

類型： **Variant \***

如果 *sServiceName* 所指定的服務正在執行，則傳回 **true** ;否則 **為 false**。

## <a name="remarks"></a>備註

Microsoft Visual Basic 目前無法使用這個方法。

## <a name="examples"></a>範例

下列範例示範如何使用 **IsServiceRunning** 來判斷應用程式的主題服務是否正在執行。 JScript 和 VBScript 都會顯示使用方式。

JScript：


```JScript
function fnIsServiceRunningJ()
{
    var objShell = new ActiveXObject("shell.application");
    var bReturn;

    bReturn = objShell.IsServiceRunning("Themes");
}
```



VBScript


```VB
function fnIsServiceRunningVB()
    dim objShell
    dim bReturn

    set objShell = CreateObject("shell.application")

    bReturn = objShell.IsServiceRunning("Themes")

    set objShell = nothing
end function
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



 

 
