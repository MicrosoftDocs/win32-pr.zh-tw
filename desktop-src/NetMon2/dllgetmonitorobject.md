---
description: DllGetMonitorObject 函式必須由監視器所執行。 MCSVC 會呼叫這個函式來建立監視的實例。
ms.assetid: 2c39f752-264c-4ab9-8710-a0d660c4772f
title: 'DllGetMonitorObject 回呼函數 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllGetMonitorObject
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 723c085fe86e8c24ebc13d83c760e5bfdd08eab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852107"
---
# <a name="dllgetmonitorobject-callback-function"></a>DllGetMonitorObject 回呼函式

**DllGetMonitorObject** 函式必須由監視器所執行。 MCSVC 會呼叫這個函式來建立監視的實例。

## <a name="syntax"></a>語法


```C++
HRESULT DllGetMonitorObject(
  _In_  REFIID riid,
  _Out_ LPVOID *ppObj
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*riid* \[在\]
</dt> <dd>

監視器的 UUID （如下所示），如 IMonitor .h 標頭檔中所定義。 如果提供的 UUID 無效，則函式會失敗，而且監視器必須傳回 E \_ NOINTERFACE。

``` syntax
IID_IMonitor
```

</dd> <dt>

*ppObj* \[擴展\]
</dt> <dd>

指標，指向接收在 *riid* 中要求之介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 S \_ OK (與 >aad-userreadusingalternativesecurityid-noerror) 相同。

如果函式不成功，則傳回值為失敗碼。 傳回失敗碼時，MCSVC 不會建立監視物件，也不會在介面指標上呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 方法。

## <a name="remarks"></a>備註

每次 MCSVC 嘗試建立監視的實例時，就會呼叫 **DllGetMonitorObject** 函數。 此函式刻意為較常見的 [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) 函式提供強式非常相似。 主要差異在於 CLSID 未傳遞至 **DllGetMonitorObject**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

