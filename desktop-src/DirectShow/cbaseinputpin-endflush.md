---
description: EndFlush 方法會結束清除作業。 實行 IPin：： EndFlush 方法。
ms.assetid: d4110eb4-26c5-4312-b33f-4af31e1bf2ae
title: 'CBaseInputPin. EndFlush 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 403ee5aa100309084090dc241724067f9dd3aa5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994217"
---
# <a name="cbaseinputpinendflush-method"></a>CBaseInputPin. EndFlush 方法

`EndFlush`方法會結束清除作業。 實行 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

這個方法會將 [**CBaseInputPin：： m \_ bFlushing**](cbaseinputpin-m-bflushing.md) 旗標設定為 **TRUE**，這 [**會讓 CBaseInputPin：： Receive**](cbaseinputpin-receive.md) 方法接受範例。

衍生的類別必須覆寫這個方法，並執行下列步驟：

1.  釋放任何緩衝的資料，並等候所有已排入佇列的樣本被捨棄。
2.  清除任何擱置中的 [**EC \_ 完成**](ec-complete.md) 通知。
3.  呼叫基類方法。
4.  對下游輸入 pin 呼叫 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) 。 如果 pin 尚未提供任何下游媒體範例，您可以略過此步驟。 如果您的輸出圖釘衍生自 [**CBaseOutputPin**](cbaseoutputpin.md) 類別，您可以呼叫 [**CBaseOutputPin：:D eliverendflush**](cbaseoutputpin-deliverendflush.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseInputPin 類別**](cbaseinputpin.md)
</dt> </dl>

 

 




