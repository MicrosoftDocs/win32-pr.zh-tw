---
description: OnSize 方法會處理 WM \_ 大小的訊息。
ms.assetid: 21d867a4-4321-478a-9beb-5d3053569369
title: 'CBaseWindow. OnSize 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9020510030d3b3d4b30e066adfe67367618fb3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990538"
---
# <a name="cbasewindowonsize-method"></a>CBaseWindow. OnSize 方法

`OnSize`方法會處理 WM \_ 大小的訊息。

## <a name="syntax"></a>語法


```C++
virtual BOOL OnSize(
   LONG Width,
   LONG Height
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*寬度* 
</dt> <dd>

工作區的寬度（以圖元為單位）。

</dd> <dt>

*高度* 
</dt> <dd>

用戶端區域的高度（以圖元為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **TRUE**。

## <a name="remarks"></a>備註

這個方法會儲存新的寬度和高度。 若要取出這些值，請呼叫 [**CBaseWindow：： GetWindowHeight**](cbasewindow-getwindowheight.md) 和 [**CBaseWindow：： GetWindowWidth**](cbasewindow-getwindowwidth.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseWindow 類別**](cbasewindow.md)
</dt> </dl>

 

 




