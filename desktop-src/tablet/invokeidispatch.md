---
description: 叫用 IDispatch 介面的 helper 功能。
ms.assetid: ccef47af-d9dd-48c3-93d3-ee997dacf7a8
title: InvokeIDispatch 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InvokeIDispatch
api_type:
- LibDef
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: e4989e3ec23a1ffa97ba317831143ecf0920ef9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000289"
---
# <a name="invokeidispatch-function"></a>InvokeIDispatch 函式

叫用 IDispatch 介面的 helper 功能。

此函式不適合應用程式程式碼使用。

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI InvokeIDispatch(
        IDispatch  *pDispatch,
        DISPID     dispid,
        DISPPARAMS *pDisp,
  _Out_ VARIANT    *pVarResult
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDispatch* 
</dt> <dd>

IDispatch 介面的實例。

</dd> <dt>

*dispid* 
</dt> <dd>

要傳入的方法、屬性或引數。

</dd> <dt>

*pDisp* 
</dt> <dd>

要傳入的參數。

</dd> <dt>

*pVarResult* \[擴展\]
</dt> <dd>

接收已抓取值的結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，它會傳回 S \_ OK。 如果失敗，可能的傳回碼包括（但不限於）下表所示的值。



| 傳回碼                                                                                  | Description                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | *PDispatch* 的值無效。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                         |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                             |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl> |



 

 




