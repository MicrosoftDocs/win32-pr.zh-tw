---
description: Invoke 方法會提供物件所公開之方法和屬性的存取權。
ms.assetid: d9539b89-b7c2-4b4d-b6d6-6275cc6d7e7c
title: 'CDeferredCommand： Invoke 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 268cfc3d4665eeacafbd695b974f55445747e151
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990677"
---
# <a name="cdeferredcommandinvoke-method"></a>CDeferredCommand 方法

`Invoke`方法會提供物件所公開之方法和屬性的存取權。

## <a name="syntax"></a>語法


```C++
HRESULT Invoke();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

\_ \_ \_ 如果 **m \_ pQueue** 為 **Null**，則傳回 VFW E 已取消。 否則，會傳回對 **IDispatch：： GetTypeInfo** 或 **IUnknown：： QueryInterface** 的呼叫所產生的 **HRESULT** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDeferredCommand 類別**](cdeferredcommand.md)
</dt> </dl>

 

 




