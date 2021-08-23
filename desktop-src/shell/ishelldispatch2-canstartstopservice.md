---
description: IShellDispatch2. CanStartStopService 方法-決定目前使用者是否可以啟動和停止命名服務。
ms.assetid: cbb54ae9-02e6-4243-a782-e9f125c21c0d
title: 'IShellDispatch2. CanStartStopService 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.CanStartStopService
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: bae0ed1a6f60a363a360c8824d5b41f17b89f9040d3354b9e3011e0269e9d9e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032236"
---
# <a name="ishelldispatch2canstartstopservice-method"></a>IShellDispatch2. CanStartStopService 方法

判斷目前的使用者是否可以啟動和停止命名服務。

## <a name="syntax"></a>語法


```JScript
retVal = IShellDispatch2.CanStartStopService(
  sServiceName
)
```


```VB

IShellDispatch2.CanStartStopService( _
  ByVal sServiceName As String _
) As Variant
```





## <a name="parameters"></a>參數

<dl> <dt>

*sServiceName* \[在\]
</dt> <dd>

類型： **字串**

包含服務名稱的 **字串** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

### <a name="jscript"></a>JScript

類型： **Variant \***

如果使用者可以啟動和停止服務，則傳回 **true** ;否則 **為 false**。

### <a name="vb"></a>VB

類型： **Variant \***

如果使用者可以啟動和停止服務，則傳回 **true** ;否則 **為 false**。

## <a name="remarks"></a>備註

這個方法是透過 [**CanStartStopService**](./shell-canstartstopservice.md) 方法來執行和存取。

Microsoft Visual Basic 目前無法使用這個方法。

## <a name="examples"></a>範例

下列範例顯示 JScript 和 VBScript 的 **CanStartStopService** 用法。

JScript：


```JScript
<script language="JScript">
    function fnCanStartStopServiceJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;

        bReturn = objShell.CanStartStopService("service name");
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnCanStartStopServiceVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.CanStartStopService("service name")

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



 

 
