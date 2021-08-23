---
description: ShouldDrawSampleNow 方法會決定如何排程範例以進行轉譯。
ms.assetid: 92994f1f-53d5-42d4-90a2-2984b693e4c0
title: 'CBaseRenderer. ShouldDrawSampleNow 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ShouldDrawSampleNow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 818a7682fed504028ebee1c3a5ff5d35a268e1daad8756b110bcfcb2ca8d9f80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016866"
---
# <a name="cbaserenderershoulddrawsamplenow-method"></a>CBaseRenderer. ShouldDrawSampleNow 方法

`ShouldDrawSampleNow`方法會決定如何排程範例以進行轉譯。

## <a name="syntax"></a>語法


```C++
virtual HRESULT ShouldDrawSampleNow(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMediaSample* 
</dt> <dd>

範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。

</dd> <dt>

*pStartTime* 
</dt> <dd>

變數的指標，其中包含範例的開始時間。

</dd> <dt>

*pEndTime* 
</dt> <dd>

變數的指標，其中包含範例的結束時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 \_ FALSE。 如果衍生類別覆寫這個方法，則傳回下表所示的其中一個值。



| 傳回碼                                                                               | 描述                                                                        |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>      | 範例應立即轉譯。<br/>                              |
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | 此範例應根據時間戳記來排程轉譯。<br/> |
| <dl> <dt>**錯誤碼**</dt> </dl> | 請勿呈現此範例。<br/>                                              |



 

## <a name="remarks"></a>備註

[**CBaseRenderer：： GetSampleTimes**](cbaserenderer-getsampletimes.md)方法會呼叫這個方法。 根據預設，範例一律會根據其時間戳記排程進行轉譯。 衍生的類別可以覆寫這個方法。例如，執行品質控制。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




