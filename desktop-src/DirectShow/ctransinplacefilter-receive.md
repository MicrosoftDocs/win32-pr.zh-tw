---
description: Receive 方法會接收媒體範例、處理它，然後將它傳遞給下游篩選器。
ms.assetid: 87126353-b73a-45f5-a8e7-b719efdf9d76
title: 'CTransInPlaceFilter 的 Receive 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 390d0243631e4ac31da779ca01197500f1d3df18127a3b86f0cf1ea834283f0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053458"
---
# <a name="ctransinplacefilterreceive-method"></a>CTransInPlaceFilter 接收方法

`Receive`方法會接收媒體範例、進行處理，並將其傳遞至下游篩選器。

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

範例上 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所示的值。



| 傳回碼                                                                                  | 描述                 |
|----------------------------------------------------------------------------------------------|-----------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | Success<br/>          |
| <dl> <dt>**E 未 \_ 預期**</dt> </dl> | 未預期的錯誤<br/> |



 

## <a name="remarks"></a>備註

篩選的輸入 pin 會在收到範例時呼叫這個方法。 篩選準則會呼叫 [**轉換**](ctransinplacefilter-transform.md) 方法，而衍生類別必須執行此方法。 **轉換** 方法會處理資料。 如果篩選只使用一個配置器，它會將 *pSample* 直接傳遞至 **轉換** 方法。 否則，它會複製 *pSample* 並傳遞複本。

如果 **轉換** 方法傳回 \_ FALSE，則方法會卸載 `Receive` 範例。 在第一個捨棄的範例中，篩選準則會將 [**EC \_ 品質 \_ 變更**](ec-quality-change.md) 事件傳送至篩選圖形管理員。 否則，如果 **轉換** 方法傳回 S \_ OK，則篩選會傳遞輸出範例。 若要這樣做，它會對下游輸入 pin 呼叫 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transip (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransInPlaceFilter 類別**](ctransinplacefilter.md)
</dt> </dl>

 

 




