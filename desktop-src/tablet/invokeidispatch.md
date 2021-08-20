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
ms.openlocfilehash: 9708ebc5675d918c959be132d16037ac4e128650280b8243dcfe5c48834b602b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118041868"
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



| 傳回碼                                                                                  | 描述                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | *PDispatch* 的值無效。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                         |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                             |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl> |



 

 




