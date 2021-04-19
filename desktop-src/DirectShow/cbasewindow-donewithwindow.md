---
description: DoneWithWindow 方法會終結視窗。
ms.assetid: 03c97884-7d91-4b59-b867-dda231d2a184
title: 'CBaseWindow. DoneWithWindow 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoneWithWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc31e893a4015aa8b4356d265ca4065ee336c3ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995627"
---
# <a name="cbasewindowdonewithwindow-method"></a>CBaseWindow. DoneWithWindow 方法

方法會終結 `DoneWithWindow` 視窗。

## <a name="syntax"></a>語法


```C++
virtual HRESULT DoneWithWindow();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

從衍生物件的「析構函式」方法呼叫這個方法。

如果從建立視窗的相同執行緒呼叫這個方法，則此方法會執行下列動作：

-   呼叫 [**CBaseWindow：： InactivateWindow**](cbasewindow-inactivatewindow.md) 方法，該方法會停用視窗。
-   呼叫 [**CBaseWindow：： UninitialiseWindow**](cbasewindow-uninitialisewindow.md) 方法，該方法會釋放視窗所使用的資源。
-   終結視窗。

如果呼叫的執行緒 `DoneWithWindow` 不是建立視窗的執行緒，則方法會將「終結」私用訊息傳送至視窗。 當視窗收到這個訊息時，它會 `DoneWithWindow` 自行呼叫。  (如果 [**CBaseWindow：： m \_ BDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) 為 **TRUE**，則視窗會張貼訊息。 ) 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseWindow 類別**](cbasewindow.md)
</dt> </dl>

 

 




