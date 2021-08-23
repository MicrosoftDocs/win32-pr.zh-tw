---
description: 連線方法會將釘選連接到另一個 pin。 這個方法會實 IPin：：連線方法。
ms.assetid: 8ea99d2f-09da-4b15-a3b0-04ceb7888bc1
title: 'CBasePin.連線方法 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Connect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a134b87e9c7c4d0f665ae37df7ec9cd0ecb3a37c0d0548f27835ead7b8ecca21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074792"
---
# <a name="cbasepinconnect-method"></a>CBasePin.連線方法

方法會將 `Connect` 釘選連接到另一個 pin。 這個方法會實 [**IPin：：連線**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect)方法。

## <a name="syntax"></a>語法


```C++
HRESULT Connect(
         IPin          *pReceivePin,
   const AM_MEDIA_TYPE *pmt
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

[**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構的指標，指定連接的媒體類型。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表中的值。



| 傳回碼                                                                                                  | 描述                                                                        |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                         | 成功。<br/>                                                                |
| <dl> <dt>**VFW \_ E \_ 已 \_ 連線**</dt> </dl>    | Pin 已連線。<br/>                                           |
| <dl> <dt>**VFW \_ E \_ 沒有 \_ 可接受的 \_ 類型**</dt> </dl> | 找不到可接受的媒體類型。<br/>                                |
| <dl> <dt>**VFW \_ E \_ 未 \_ 停止**</dt> </dl>          | 篩選準則為使用中，且 pin 不支援動態重新連接。<br/> |
| <dl> <dt>**\_ \_ \_ 未接受 VFW E \_ 類型**</dt> </dl>   | 無法接受指定的媒體類型。<br/>                             |



 

## <a name="remarks"></a>備註

*Pmt* 參數可以是 **Null**。 它也可以指定部分媒體類型，且 \_ 主要類型、子類型或格式的值為 GUID Null。

在基類中，這個方法會測試是否已連接釘選，以及是否停止篩選。 它會將連接進程的其餘部分委派給 [**CBasePin：： AgreeMediaType**](cbasepin-agreemediatype.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




