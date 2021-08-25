---
description: Receive 方法會將媒體範例傳遞給輸入 pin。
ms.assetid: a8ee0988-8955-48d0-be1b-24eea72d560d
title: 'COutputQueue 的 Receive 方法 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8fb896429e53c16b30dbc4301f2e54fca5a2087dc1c89635fa33395f68ba0f5b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871498"
---
# <a name="coutputqueuereceive-method"></a>COutputQueue 接收方法

方法會將 `Receive` 媒體範例傳遞給輸入圖釘。

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



| 傳回碼                                                                             | 描述                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | 在處理這個範例之前，收到的資料流程結束通知。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>    | 成功。<br/>                                                           |



 

## <a name="remarks"></a>備註

這個方法會呼叫 [**COutputQueue：： ReceiveMultiple**](coutputqueue-receivemultiple.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Outputq (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COutputQueue 類別**](coutputqueue.md)
</dt> </dl>

 

 




