---
description: UninitialiseWindow 方法會釋放視窗的資源。
ms.assetid: 8c5bb0c1-1d92-4025-bbbd-1e57ddde4456
title: 'CBaseWindow. UninitialiseWindow 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.UninitialiseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c275e4d683bcc698c8f04c5a85017b081b6aad17f93c91d66e0a75f2da88692e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657490"
---
# <a name="cbasewindowuninitialisewindow-method"></a>CBaseWindow. UninitialiseWindow 方法

`UninitialiseWindow`方法會釋放視窗的資源。

## <a name="syntax"></a>語法


```C++
virtual HRESULT UninitialiseWindow();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

這個方法會釋放 [**CBaseWindow：： InitialiseWindow**](cbasewindow-initialisewindow.md) 方法所取得的資源。 [**CBaseWindow：:D onewithwindow**](cbasewindow-donewithwindow.md)方法會呼叫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseWindow 類別**](cbasewindow.md)
</dt> </dl>

 

 




