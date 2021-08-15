---
description: GetDeliveryBuffer 方法會抓取包含空緩衝區的媒體範例。
ms.assetid: 5a20c11b-50f8-443e-a4d5-6bcffde741d5
title: 'CBaseOutputPin. GetDeliveryBuffer 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.GetDeliveryBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d118e21ea67932529c41b35595619c6e03b907718708ba285aa2a6578177f7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823607"
---
# <a name="cbaseoutputpingetdeliverybuffer-method"></a>CBaseOutputPin. GetDeliveryBuffer 方法

`GetDeliveryBuffer`方法會抓取包含空緩衝區的媒體範例。

## <a name="syntax"></a>語法


```C++
virtual HRESULT GetDeliveryBuffer(
   IMediaSample   **ppSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime,
   DWORD          dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppSample* 
</dt> <dd>

接收緩衝區 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面指標的變數位址。

</dd> <dt>

*pStartTime* 
</dt> <dd>

範例開始時間的指標，或 **Null**。

</dd> <dt>

*pEndTime* 
</dt> <dd>

樣本的結束時間指標，或 **為 Null**。

</dd> <dt>

*dwFlags* 
</dt> <dd>

[**IMemAllocator：： GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer)介面所支援之旗標的位元組合。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所列的值。



| 傳回碼                                                                                   | Description                        |
|-----------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 成功。<br/>                |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl> | 沒有可用的配置器。<br/> |



 

## <a name="remarks"></a>備註

這個方法會在配置器上呼叫 **IMemAllocator：： GetBuffer** 方法，並將參數傳遞給該方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseOutputPin 類別**](cbaseoutputpin.md)
</dt> </dl>

 

 




