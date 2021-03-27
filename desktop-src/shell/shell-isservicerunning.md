---
description: 傳回值，這個值表示特定服務是否正在執行。
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
ms.openlocfilehash: c3a65be4955c6f49e8e6baa49cd9dedb82fc5cc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849363"
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

類型： **Variant \** _

如果 *sServiceName* 所指定的服務正在執行，則傳回 _ *true**。否則 **為 false**。

### <a name="vb"></a>VB

類型： **Variant \** _

如果 *sServiceName* 所指定的服務正在執行，則傳回 _ *true**。否則 **為 false**。

## <a name="remarks"></a>備註

Microsoft Visual Basic 目前無法使用這個方法。

## <a name="examples"></a>範例

下列範例示範如何使用 **IsServiceRunning** 來判斷應用程式的主題服務是否正在執行。 JScript 和 VBScript 會顯示使用方式。

Jscript：


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
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



 

 
