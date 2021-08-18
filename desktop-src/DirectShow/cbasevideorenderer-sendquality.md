---
description: SendQuality 方法會傳送品質訊息，以指出供應商應該如何處理品質。
ms.assetid: 9ce11c35-958c-4eda-9130-1139c4074bf7
title: 'CBaseVideoRenderer. SendQuality 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.SendQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: acda4bd9b00434e33c24ac44625b3c1d45350d45b4ec0b242d2638333ad11ed9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074762"
---
# <a name="cbasevideorenderersendquality-method"></a>CBaseVideoRenderer. SendQuality 方法

`SendQuality`方法會傳送品質訊息，以指出供應商應該如何處理品質。

## <a name="syntax"></a>語法


```C++
virtual HRESULT SendQuality(
   REFERENCE_TIME trLate,
   REFERENCE_TIME trRealStream
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*trLate* 
</dt> <dd>

框架延遲的時間量。

</dd> <dt>

*trRealStream* 
</dt> <dd>

Currentstream 時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

此成員函式會傳送上游的品質控制訊息來控制品質管制。 品質訊息的本質 (也就是，是否要減少或增加) 的樣本數目是否可在此衍生類別的品質管制執行中決定 (請參閱 [**CBaseVideoRenderer：： ShouldDrawSampleNow**](cbasevideorenderer-shoulddrawsamplenow.md)) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseVideoRenderer 類別**](cbasevideorenderer.md)
</dt> </dl>

 

 




