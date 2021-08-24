---
description: 當物件從輸出圖釘接收媒體範例時，會呼叫接收方法。 衍生的類別必須執行此方法。
ms.assetid: ef45388b-b038-4838-b76b-dbbdc5388495
title: 'CPullPin 的 Receive 方法 (Pullpin .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fdf38c9c873dd8d95ae60341fc2f7dba02abff1f8b34fd89d0d1f720dc59b55f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831538"
---
# <a name="cpullpinreceive-method"></a>CPullPin 接收方法

`Receive`當物件從輸出圖釘接收媒體範例時，會呼叫方法。 衍生的類別必須執行此方法。

## <a name="syntax"></a>語法


```C++
virtual HRESULT Receive(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSample* 
</dt> <dd>

媒體範例的 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 傳回 S 以外的值 \_ 將會停止資料提取執行緒。

## <a name="remarks"></a>備註

每當有新的範例從輸出圖釘抵達時，就會呼叫這個方法。 以與 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 方法相同的方式來撰寫這個方法。

範例上的時間戳記會指定位元組位移，相對於 [**CPullPin：： Seek**](cpullpin-seek.md) 方法中指定的原始開始位置。

開始位置會向下舍入至最接近的對齊界限，而停止位置會進位到最接近的對齊界限。 此外，如果停止位置超過總持續時間，則會改用持續時間。

所有時間戳記都會以位元組位移乘以10000000（定義為常數單位）來提供。 因此，notionally 一秒是1個位元組。 若要尋找實際的位元組位移，請呼叫 [**IMediaSample：： GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) ，並依單位除以結果。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Pullpin。h</dt> </dl>                                                                                                       |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPullPin 類別**](cpullpin.md)
</dt> </dl>

 

 




