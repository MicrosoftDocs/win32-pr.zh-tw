---
description: GetSampleTimes 方法會從範例中取出時間戳記。
ms.assetid: a8fead22-a12c-489d-9c42-d5b61f480c25
title: 'CBaseRenderer. GetSampleTimes 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetSampleTimes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d759cbcf2a9638b54e6194bcac7e7b24254c0d37987995d511fb4ffce85f1ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954957"
---
# <a name="cbaserenderergetsampletimes-method"></a>CBaseRenderer. GetSampleTimes 方法

`GetSampleTimes`方法會從範例抓取時間戳記。

## <a name="syntax"></a>語法


```C++
virtual HRESULT GetSampleTimes(
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

接收開始時間之變數的指標。

</dd> <dt>

*pEndTime* 
</dt> <dd>

接收結束時間之變數的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所示的值。



| 傳回碼                                                                                                    | 描述                                                                        |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                           | 範例應立即轉譯。<br/>                              |
| <dl> <dt>**S \_ FALSE**</dt> </dl>                        | 此範例應根據時間戳記來排程轉譯。<br/> |
| <dl> <dt>**E \_ 失敗**</dt> </dl>                         | 請勿呈現此範例。<br/>                                              |
| <dl> <dt>**VFW \_ E \_ 開始 \_ 時間 \_ \_ 結束**</dt> </dl> | 錯誤的時間戳記：結束時間早于開始時間。<br/>            |



 

## <a name="remarks"></a>備註

篩選準則會呼叫這個方法來判斷它應該如何處理範例。 如果傳回值為 S \_ OK，則篩選會立即呈現範例。 如果傳回值為 \_ FALSE，則篩選會根據時間戳記來排程轉譯的範例。 如果傳回值是錯誤碼，則篩選會拒絕範例。

如果此範例沒有 \_ 時間戳記，或篩選沒有參考時鐘，則這個方法會傳回 [確定]。 否則，它會傳回 [**CBaseRenderer：： ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md) 方法的值。 在基類中， **ShouldDrawSampleNow** 一律會傳回 \_ FALSE。 衍生的類別可以覆寫這個行為。 例如，如果衍生類別會執行品質控制管理，它可能會傳回 E \_ 無法卸載範例。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




