---
description: InitializeOutputSample 方法會捕獲新的輸出範例，並將它初始化。
ms.assetid: a4f8f514-cf1a-4f8f-ac17-17378705c2ea
title: " (Transfrm 的 CTransformFilter.InitializeOutputSample 方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.InitializeOutputSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 083867f2ef6b2e40462112036dbbb000c25bc3ad2bb443f011235e36bf245ab2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953617"
---
# <a name="ctransformfilterinitializeoutputsample-method"></a>CTransformFilter.InitializeOutputSample 方法

`InitializeOutputSample`方法會抓取新的輸出範例，並將其初始化。

## <a name="syntax"></a>語法


```C++
HRESULT InitializeOutputSample(
   IMediaSample *pSample,
   IMediaSample **ppOutSample
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSample* 
</dt> <dd>

輸入範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。

</dd> <dt>

*ppOutSample* 
</dt> <dd>

接收輸出範例 **IMediaSample** 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK 或其他 **HRESULT** 值。

## <a name="remarks"></a>備註

[**CTransformFilter：： Receive**](ctransformfilter-receive.md)方法會呼叫這個方法來準備輸出範例。 一般而言，您不需要在衍生類別中呼叫這個方法，除非您覆寫 **Receive** 方法。

這個方法會從輸出釘選配置器抓取新的範例。 然後，它會將範例屬性從輸入範例複製到輸出範例。 範例屬性是在 [**AM \_ sample2.xml \_ 屬性**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) 結構中定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransformFilter 類別**](ctransformfilter.md)
</dt> </dl>

 

 




