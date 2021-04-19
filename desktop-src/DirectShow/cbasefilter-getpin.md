---
description: GetPin 方法會抓取 pin。 CEnumPins 類別會呼叫這個方法來列舉篩選上的釘選。
ms.assetid: e3ec3f11-1e7d-40b6-810e-3759f0511cb2
title: 'CBaseFilter. GetPin 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bb8341bfd86b96a7358fb23036b71844f77d17a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999254"
---
# <a name="cbasefiltergetpin-method"></a>CBaseFilter. GetPin 方法

**GetPin** 方法會抓取 pin。 [**CEnumPins**](cenumpins.md)類別會呼叫這個方法來列舉篩選上的釘選。

## <a name="syntax"></a>語法


```C++
virtual CBasePin* GetPin(
   int n
) = 0;
```



## <a name="parameters"></a>參數

<dl> <dt>

*n* 
</dt> <dd>

以零為基底的釘選索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 [**CBasePin**](cbasepin.md) 物件的指標，該物件會執行釘選。

## <a name="remarks"></a>備註

您必須在衍生類別中執行此純虛擬方法。 傳回這個篩選的第 *n* 個圖釘的指標，從零開始編制索引。 只要順序是固定的，您就可以選擇任意的索引編制順序。 如果篩選準則加入或刪除 pin，或在執行時間針對某個其他原因進行順序變更，請呼叫 [**CBaseFilter：： IncrementPinVersion**](cbasefilter-incrementpinversion.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseFilter 類別**](cbasefilter.md)
</dt> </dl>

 

 




