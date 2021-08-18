---
description: ShouldDrawSampleNow 方法會判斷是否應該繪製影片，而不需要使用時鐘來設定計時器建議連結。
ms.assetid: 2cbefc66-0d99-4559-b210-3163cd413dbf
title: 'CBaseVideoRenderer. ShouldDrawSampleNow 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ShouldDrawSampleNow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e3c0297ccf670de12380c5f02af2c67d6050bac29dd1fa7e7e89a6e6c7c20592
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074683"
---
# <a name="cbasevideorenderershoulddrawsamplenow-method"></a>CBaseVideoRenderer. ShouldDrawSampleNow 方法

此 `ShouldDrawSampleNow` 方法會決定是否應繪製影片，而不需要使用時鐘來設定計時器建議連結。

## <a name="syntax"></a>語法


```C++
virtual HRESULT ShouldDrawSampleNow(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *ptrStart,
   REFERENCE_TIME *ptrEnd
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMediaSample* 
</dt> <dd>

範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。

</dd> <dt>

*ptrStart* 
</dt> <dd>

開始呈現的時間指標。

</dd> <dt>

*ptrEnd* 
</dt> <dd>

停止轉譯的時間指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 傳回 \_ [OK] 表示一次繪製一次，而不等候，S \_ FALSE 表示在時間 *ptrStart* 繪製，或使用錯誤表示不繪製樣本; 也就是說，略過以節省時間。

## <a name="remarks"></a>備註

此成員函式會覆寫 [**CBaseRenderer：： ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseVideoRenderer 類別**](cbasevideorenderer.md)
</dt> </dl>

 

 




