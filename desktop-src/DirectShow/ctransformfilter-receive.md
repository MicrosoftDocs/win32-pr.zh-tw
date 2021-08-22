---
description: Receive 方法會接收媒體範例、處理它，然後將輸出範例傳遞給下游篩選器。
ms.assetid: 036b209a-3535-4922-b7e9-dbed25b812f5
title: 'CTransformFilter 的 Receive 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a0c57cf6826274169a5984dd794e1ba9a5b8e78c7ffb774b00b05f16384e4a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953407"
---
# <a name="ctransformfilterreceive-method"></a>CTransformFilter 接收方法

`Receive`方法會接收媒體範例、進行處理，並將輸出範例傳遞給下游篩選器。

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



| 傳回碼                                                                             | 描述                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | 上游篩選應停止傳送範例。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>    | 成功。<br/>                                         |



 

## <a name="remarks"></a>備註

篩選的輸入 pin 會在收到範例時呼叫這個方法。 這個方法會呼叫 [**CTransformFilter：： InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) 方法，以準備新的輸出範例。 然後，它會呼叫衍生類別必須執行的 [**CTransformFilter：： Transform**](ctransformfilter-transform.md) 方法。 **轉換** 方法會處理輸入資料並產生輸出資料。

如果 **轉換** 方法傳回 \_ FALSE，則方法會卸載 `Receive` 此範例。 在第一個捨棄的範例中，篩選準則會將 [**EC \_ 品質 \_ 變更**](ec-quality-change.md) 事件傳送至篩選圖形管理員。 否則，如果 **轉換** 方法傳回 S \_ OK，則篩選會傳遞輸出範例。 若要這樣做，它會對下游輸入 pin 呼叫 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransformFilter 類別**](ctransformfilter.md)
</dt> </dl>

 

 




