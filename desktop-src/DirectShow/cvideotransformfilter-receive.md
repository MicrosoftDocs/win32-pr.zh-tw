---
description: Receive 方法會接收媒體範例、處理它，然後將輸出範例傳遞給下游篩選器。 這個方法會覆寫 CTransformFilter：： Receive 方法。
ms.assetid: 35e22a63-471e-4ca8-be3b-d84920cec7cb
title: 'CVideoTransformFilter 的 Receive 方法 (Vtrans .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bdc33773a31a7c9ddfd7adb0f3fb20f8fcf6d520
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977542"
---
# <a name="cvideotransformfilterreceive-method"></a>CVideoTransformFilter 接收方法

`Receive`方法會接收媒體範例、進行處理，並將輸出範例傳遞給下游篩選器。 這個方法會覆寫 [**CTransformFilter：： Receive**](ctransformfilter-receive.md) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSample* 
</dt> <dd>

輸入範例上 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值如下：



| 傳回碼                                                                             | Description                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | 上游篩選應停止傳送範例。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>    | 成功。<br/>                                         |



 

## <a name="remarks"></a>備註

這個方法會呼叫 [**CVideoTransformFilter：： ShouldSkipFrame**](cvideotransformfilter-shouldskipframe.md) 來判斷它是否應該傳遞此範例，或只是捨棄它。 如果 **ShouldSkipFrame** 傳回 **FALSE** (表示應將範例傳遞) ，方法會執行下列動作：

1.  呼叫 [**CTransformFilter：： InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) 來準備輸出範例
2.  呼叫 [**CTransformFilter：： Transform**](ctransformfilter-transform.md) 來處理輸入範例。 這個方法是純虛擬的，而且必須在衍生類別中執行。
3.  呼叫 [**CBaseOutputPin：:D eliver**](cbaseoutputpin-deliver.md) 以傳遞輸出範例。

此外，這個方法會藉由呼叫 [**IMediaSample：： GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype)，檢查輸入或輸出範例上的格式變更。 如果有格式變更，方法會在對應的 pin 上設定連線類型。 在設定新型別之前，它會呼叫 **StopStreaming**。 在設定新的型別之後，它會呼叫 **StartStreaming**。 衍生的類別可以使用這些方法來更新其內部狀態。 衍生類別可能也需要在其 **轉換** 方法中檢查新的格式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Vtrans (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CVideoTransformFilter 類別**](cvideotransformfilter.md)
</dt> </dl>

 

 




