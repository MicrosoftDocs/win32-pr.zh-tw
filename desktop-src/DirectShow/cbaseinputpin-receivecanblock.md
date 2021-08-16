---
description: ReceiveCanBlock 方法會判斷 IMemInputPin：： Receive 方法的呼叫是否可能封鎖。 這個方法會實 IMemInputPin：： ReceiveCanBlock 方法。
ms.assetid: db96e389-e1bc-4b38-8d0a-a20f0d3a4460
title: 'CBaseInputPin. ReceiveCanBlock 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.ReceiveCanBlock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ece7243c145d34ed06e29b2a29ae9847e682981337b96a47976c20eb76272d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823850"
---
# <a name="cbaseinputpinreceivecanblock-method"></a>CBaseInputPin. ReceiveCanBlock 方法

`ReceiveCanBlock`方法會判斷 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)方法的呼叫是否可能封鎖。 這個方法會實 [**IMemInputPin：： ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT ReceiveCanBlock();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所列的值。



| 傳回碼                                                                             | 描述                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Pin 不會封鎖 **接聽** 的呼叫。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>    | Pin 可能會封鎖 **接聽** 的呼叫。<br/>    |



 

## <a name="remarks"></a>備註

\_如果保證無法封鎖 **接收** 方法的呼叫，則傳回 FALSE。 否則，請傳回 \_ [確定] 或錯誤碼。 如果 **接收** 方法呼叫下游 Pin 的 **receive** ，則下游 pin 可能會封鎖; `ReceiveCanBlock` 必須將該因素列入考慮。

上游篩選器可以使用這個方法來判斷它的執行緒策略。 如果 **接收** 方法可能會封鎖，上游篩選可能會決定使用可緩衝資料的背景工作執行緒。 如需此策略的執行，請參閱 [**COutputQueue**](coutputqueue.md) 類別。

在基類中， \_ 當下列任一條件成立時，這個方法會傳回 S OK：

-   篩選沒有輸出圖釘。
-   連線到此篩選的輸入 pin 可能會封鎖。
-   連接到此篩選的輸入 pin 不支援 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 介面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseInputPin 類別**](cbaseinputpin.md)
</dt> </dl>

 

 




