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
ms.openlocfilehash: ceeadd0ec7a61422f0127c957125caa9a01dcefb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993666"
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

 

 




