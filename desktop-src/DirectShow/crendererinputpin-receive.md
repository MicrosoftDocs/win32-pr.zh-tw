---
description: Receive 方法會接收資料流程中的下一個媒體範例。 這個方法會覆寫 CBaseInputPin：： Receive 方法。
ms.assetid: b09140f0-2e3a-47b1-ace7-954043dd62eb
title: 'CRendererInputPin 的 Receive 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d3ddac3f456e1ab24574a4743983d20a828896e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993661"
---
# <a name="crendererinputpinreceive-method"></a>CRendererInputPin 接收方法

`Receive`方法會接收資料流程中的下一個媒體範例。 這個方法會覆寫 [**CBaseInputPin：： Receive**](cbaseinputpin-receive.md) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT Receive(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMediaSample* 
</dt> <dd>

範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

這個方法會呼叫篩選器的 [**CBaseRenderer：： Receive**](cbaserenderer-receive.md) 方法，它會處理呈現。 如果該方法失敗，則 pin 會傳送 EC \_ ERRORABORT 事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CRendererInputPin 類別**](crendererinputpin.md)
</dt> </dl>

 

 




