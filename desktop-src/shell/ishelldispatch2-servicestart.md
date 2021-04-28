---
description: IShellDispatch2. ServiceStart 方法-啟動命名服務。
ms.assetid: 3af57cdc-f449-433d-a9e1-119038045e4c
title: 'IShellDispatch2. ServiceStart 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ServiceStart
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c0f4fa218c4def993025ff18bffd0cc54def9818
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117046"
---
# <a name="ishelldispatch2servicestart-method"></a>IShellDispatch2. ServiceStart 方法

啟動命名服務。

## <a name="syntax"></a>語法


```JScript
retVal = IShellDispatch2.ServiceStart(
  sServiceName,
  vPersistent
)
```


```VB

IShellDispatch2.ServiceStart( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a>參數

<dl> <dt>

*sServiceName* \[在\]
</dt> <dd>

類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

包含服務名稱的 **字串** 。

</dd> <dt>

*vPersistent* \[在\]
</dt> <dd>

類型： **Variant**

設定為 **true** ，讓服務控制管理員在系統啟動期間自動啟動服務。 設定為 **false** ，讓服務設定保持不變。

</dd> </dl>

## <a name="return-value"></a>傳回值

### <a name="jscript"></a>JScript

類型： **Variant \***

如果成功，則傳回 **true** ;否則 **為 false**。

### <a name="vb"></a>VB

類型： **Variant \***

如果成功，則傳回 **true** ;否則 **為 false**。

## <a name="remarks"></a>備註

這個方法是透過 [**ServiceStart**](./shell-servicestart.md) 方法來執行和存取。

如果服務已經啟動，方法會傳回 **false** 。 在呼叫這個方法之前，您可以呼叫 [**IsServiceRunning**](./shell-isservicerunning.md) 來確定服務的狀態。

Microsoft Visual Basic 目前無法使用這個方法。

## <a name="examples"></a>範例

下列範例示範如何使用 **ServiceStart** 來啟動 Messenger 服務。 JScript 和 VBScript 會顯示使用方式。

Jscript：


```JScript
<script language="JScript">
    function fnServiceStartJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStart("Messenger", true);
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnServiceStartVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ServiceStart("Messenger", true)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



 

 
