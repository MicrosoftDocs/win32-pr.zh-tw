---
description: Connect 方法會將 pin 連接到另一個 pin。 這個方法會實 IPin：： Connect 方法。
ms.assetid: 8ea99d2f-09da-4b15-a3b0-04ceb7888bc1
title: 'CBasePin 連接方法 (Amfilter .h) '
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
ms.openlocfilehash: ed8bcdab7e0909e59e7d9ec00645786f8ce48c02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995499"
---
# <a name="cbasepinconnect-method"></a>CBasePin 方法

方法會將 `Connect` 釘選連接到另一個 pin。 這個方法會實 [**IPin：： Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) 方法。

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



| 傳回碼                                                                                                  | Description                                                                        |
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

 

 




