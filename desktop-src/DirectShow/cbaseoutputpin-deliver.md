---
description: 傳遞方法會將媒體範例傳遞至連線的輸入 pin。
ms.assetid: b871df84-c69e-42eb-9da9-c25996bf08c3
title: 'CBaseOutputPin 傳遞方法 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Deliver
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f6786e9e763af26619b2dc4f6abc25aa2fd9527d7278e7da02f6042908e56bdd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119341378"
---
# <a name="cbaseoutputpindeliver-method"></a>CBaseOutputPin 傳遞方法

方法會將 `Deliver` 媒體範例傳遞到連接的輸入 pin。

## <a name="syntax"></a>語法


```C++
virtual HRESULT Deliver(
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

傳回 **HRESULT** 值。 可能的值包括下表所列的值。



| 傳回碼                                                                                           | Description                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                  | 成功。<br/>              |
| <dl> <dt>**VFW \_ E \_ 未 \_ 連線**</dt> </dl> | Pin 未連接。<br/> |



 

## <a name="remarks"></a>備註

這個方法會呼叫輸入釘選上的 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 方法。 如果 [**IMemInputPin：： ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock)方法傳回 S OK，則 **Receive** 會封鎖 \_ 。

呼叫這個方法之後，請釋放範例。 輸入 pin 可能會保存範例上的參考計數，因此請勿重複使用範例。 一律呼叫 [**CBaseOutputPin：： GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) 方法，以取得新的範例。

在呼叫這個方法之前，請先保存篩選的重要區段。 否則，pin 可能會在方法呼叫期間中斷連線。 如果篩選使用背景工作執行緒來傳遞範例，請在篩選準則準備好傳遞範例時，按住重要區段。 否則，您可以在篩選器的 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 方法中保存重要區段，篩選器會在其中處理範例。

工作者執行緒可能會產生潛在的鎖死。 當執行緒保留重要區段時，可能會等候篩選中的狀態變更。 同時，狀態變更可能會等候執行緒完成。 為了避免這種情況，狀態變更程式碼應該發出終止執行緒的事件，然後等候執行緒完成信號。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseOutputPin 類別**](cbaseoutputpin.md)
</dt> </dl>

 

 




