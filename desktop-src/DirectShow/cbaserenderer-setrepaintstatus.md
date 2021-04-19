---
description: SetRepaintStatus 方法會啟用或停用重新繪製事件。
ms.assetid: 94ae4935-459e-4009-9f64-c7c5b14504ae
title: 'CBaseRenderer. SetRepaintStatus 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetRepaintStatus
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39822b535680a699654e969abc316c10c54ba51b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994883"
---
# <a name="cbaserenderersetrepaintstatus-method"></a>CBaseRenderer. SetRepaintStatus 方法

`SetRepaintStatus`方法會啟用或停用重新繪製事件。

## <a name="syntax"></a>語法


```C++
void SetRepaintStatus(
   BOOL bRepaint
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bRepaint* 
</dt> <dd>

指出是否已啟用重新繪製事件的布林值。 若 **為 TRUE**，則篩選會將 [**EC 重新 \_ 繪製**](ec-repaint.md) 事件傳送至篩選圖形管理員。 否則，它不會傳送 EC 重新 \_ 繪製事件。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法可確保篩選圖形管理員不會溢滿重複的 EC 重新 \_ 繪製事件。 在篩選傳送 EC 重新 [**\_ 繪製**](ec-repaint.md) 事件之後，它會呼叫此方法並傳回 **TRUE** 值。 篩選不會傳送更多的 EC 重新 \_ 繪製事件，直到接收到更多資料為止。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




