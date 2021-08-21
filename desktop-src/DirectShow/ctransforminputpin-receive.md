---
description: CTransformInputPin 接收方法-Receive 方法會接收資料流程中的下一個媒體範例。 這個方法會實 IMemInputPin：： Receive 方法。
ms.assetid: 65e4f8f5-2aa2-435b-84b4-e65af3f51afc
title: 'CTransformInputPin 的 Receive 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 51ae6614544cd7045689f674ce90e672e3bce4ea8ee36486775892f95a5385fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538541"
---
# <a name="ctransforminputpinreceive-method"></a>CTransformInputPin 接收方法

`Receive`方法會接收資料流程中的下一個媒體範例。 這個方法會實 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 方法。

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

範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所示的值。



| 傳回碼                                                                             | 描述                                                |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Pin 目前正在排清;已拒絕範例。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>    | 成功。<br/>                                        |



 

## <a name="remarks"></a>備註

這個方法會呼叫釘選的 [**CBaseInputPin：： Receive**](cbaseinputpin-receive.md) 方法，它會檢查 pin 的串流狀態，並檢查媒體類型中的格式變更。 然後，它會呼叫篩選器的 [**CTransformFilter：： Receive**](ctransformfilter-receive.md) 方法，該方法會處理範例並將它傳遞給下游。

如果此方法傳回之後，篩選準則需要存取範例，則應該在範例上呼叫 **IUnknown：： AddRef** 方法來保存參考計數。 例如，某些解碼器篩選器需要目前的範例，才能解碼下一個範例。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




