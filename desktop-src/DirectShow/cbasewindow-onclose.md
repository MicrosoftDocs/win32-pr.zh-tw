---
description: OnClose 方法會處理 WM \_ 關閉訊息。
ms.assetid: e562add4-752e-4665-a75e-a5526fb7f045
title: CBaseWindow) 的方法 (Winutil
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnClose
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 880e82ca527972b5074ac290fda34ad1c7868a33cbbe1cad12885b56720cef99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635138"
---
# <a name="cbasewindowonclose-method"></a>CBaseWindow： OnClose 方法

`OnClose`方法會處理 WM \_ 關閉訊息。

## <a name="syntax"></a>語法


```C++
virtual BOOL OnClose();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **TRUE**。

## <a name="remarks"></a>備註

在基類中，此方法只會隱藏視窗。 一般而言，衍生類別會覆寫這個方法，讓它也會傳送 [**EC \_ USERABORT**](ec-userabort.md) 事件。 請勿覆寫方法以損毀視窗。 相反地，當擁有篩選準則終結時，請呼叫 [**CBaseWindow：:D onewithwindow**](cbasewindow-donewithwindow.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseWindow 類別**](cbasewindow.md)
</dt> </dl>

 

 




