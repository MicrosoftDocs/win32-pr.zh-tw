---
description: AttemptConnection 方法會使用指定的媒體類型連接到另一個 pin。
ms.assetid: b80cf2c0-7266-4dac-8633-d30a871c57d9
title: 'CBasePin. AttemptConnection 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.AttemptConnection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72f80d81b5f105f528292a23f8b58257066b425e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976241"
---
# <a name="cbasepinattemptconnection-method"></a>CBasePin. AttemptConnection 方法

`AttemptConnection`方法會使用指定的媒體類型連接到另一個 pin。

## <a name="syntax"></a>語法


```C++
virtual HRESULT AttemptConnection(
         IPin       *pReceivePin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pReceivePin* 
</dt> <dd>

接收釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。

</dd> <dt>

*Pmt* 
</dt> <dd>

指定媒體類型之 [**CMediaType**](cmediatype.md) 物件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表中的值。



| 傳回碼                                                                                                | Description                                  |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                       | 成功。<br/>                          |
| <dl> <dt>**\_ \_ \_ 未接受 VFW E \_ 類型**</dt> </dl> | 媒體類型無法接受。<br/> |



 

## <a name="remarks"></a>備註

這個方法會嘗試連接具有特定媒體類型的兩個 pin。 如果類型無法接受，則方法會失敗，而不會嘗試其他媒體類型。

如果媒體類型是可接受的，這個方法會呼叫接收釘選的 [**IPin：： ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) 方法。 然後，它會呼叫 [**CBasePin：： CompleteConnect**](cbasepin-completeconnect.md) 方法來完成連接。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




