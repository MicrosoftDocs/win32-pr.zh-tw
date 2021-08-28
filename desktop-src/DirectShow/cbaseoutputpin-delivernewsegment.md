---
description: DeliverNewSegment 方法會將新區段通知傳遞至連接的輸入 pin。
ms.assetid: 304f0267-88e0-4642-98a2-68ce973bdeab
title: 'CBaseOutputPin. DeliverNewSegment 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverNewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f4c89bb14377cf46e5395fc106807133d53cd090c0ba9e0eae8e103b438d69fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910599"
---
# <a name="cbaseoutputpindelivernewsegment-method"></a>CBaseOutputPin. DeliverNewSegment 方法

方法會將 `DeliverNewSegment` 新區段通知傳遞至連接的輸入 pin。

## <a name="syntax"></a>語法


```C++
virtual HRESULT DeliverNewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*tStart* 
</dt> <dd>

區段的開始媒體位置，以 100-毫微秒單位表示。

</dd> <dt>

*tStop* 
</dt> <dd>

區段的結束媒體位置，以 100-毫微秒單位表示。

</dd> <dt>

*dRate* 
</dt> <dd>

此區段的處理速率（以原始費率的百分比表示）。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所列的值。



| 傳回碼                                                                                           | 描述                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                  | 成功。<br/>              |
| <dl> <dt>**VFW \_ E \_ 未 \_ 連線**</dt> </dl> | Pin 未連接。<br/> |



 

## <a name="remarks"></a>備註

這個方法會呼叫輸入釘選上的 [**IPin：： NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseOutputPin 類別**](cbaseoutputpin.md)
</dt> </dl>

 

 




