---
description: ReceiveMultiple 方法會接收範例陣列。 這個方法會實 IMemInputPin：： ReceiveMultiple 方法。
ms.assetid: 21e757c7-f623-4ccb-8e37-512ee4dd7aa7
title: 'CBaseInputPin. ReceiveMultiple 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.ReceiveMultiple
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5725b7d8b70c8f7c61eb44231812997a903ba41a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984876"
---
# <a name="cbaseinputpinreceivemultiple-method"></a>CBaseInputPin. ReceiveMultiple 方法

`ReceiveMultiple`方法會接收範例的陣列。 這個方法會實 [**IMemInputPin：： ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT ReceiveMultiple(
   IMediaSample **pSamples,
   long         nSamples,
   long         *nSamplesProcessed
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSamples* 
</dt> <dd>

[**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample)指標陣列的位址，其大小為 *nSamples*。

</dd> <dt>

*nSamples* 
</dt> <dd>

要處理的樣本數。

</dd> <dt>

*nSamplesProcessed* 
</dt> <dd>

變數的指標，此變數會接收已處理的樣本數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所列的值。



| 傳回碼                                                                                             | Description                                                |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                    | 成功。<br/>                                        |
| <dl> <dt>**S \_ FALSE**</dt> </dl>                 | Pin 目前正在排清;已拒絕範例。<br/> |
| <dl> <dt>**E \_ 指標**</dt> </dl>               | **Null** 指標引數。<br/>                      |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | 媒體類型無效。<br/>                             |
| <dl> <dt>**VFW \_ E \_ 運行時 \_ 錯誤**</dt> </dl>   | 發生執行階段錯誤。<br/>                      |
| <dl> <dt>**VFW \_ E \_ 錯誤的 \_ 狀態**</dt> </dl>     | 已停止 pin。<br/>                             |



 

## <a name="remarks"></a>備註

這個方法的行為就像是 [**CBaseInputPin：： Receive**](cbaseinputpin-receive.md) 方法，但是會收到範例陣列。 在基類中，方法會在陣列中執行迴圈，並呼叫每個範例的 **Receive** 。 如果您的篩選可以更有效率地處理樣本批次，而不是一次處理一個樣本，請覆寫此函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseInputPin 類別**](cbaseinputpin.md)
</dt> </dl>

 

 




