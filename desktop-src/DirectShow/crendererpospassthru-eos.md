---
description: EOS 方法會在結束資料流程通知之後，更新快取的時間戳記。
ms.assetid: 7fb2f964-ec15-47f5-902b-29b9b121e876
title: 'CRendererPosPassThru 的 Ctlutil 方法 (. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.EOS
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10f87fbb66f8ad1d89ff31c6653780b3fde23ecbaf55d72b6f3de2f59546b49b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073412"
---
# <a name="crendererpospassthrueos-method"></a>CRendererPosPassThru. EOS 方法

方法會在 `EOS` 結束資料流程通知之後，更新快取的時間戳記。

## <a name="syntax"></a>語法


```C++
HRESULT EOS();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所列的值。



| 傳回碼                                                                            | 描述                                               |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>   | 成功。<br/>                                       |
| <dl> <dt>**E \_ 失敗**</dt> </dl> | 失敗。 可能是篩選未串流處理。<br/> |



 

## <a name="remarks"></a>備註

當此篩選接收資料流程結束通知時 ([**IPin：： EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)) ，就應該呼叫這個方法。 方法會將快取的時間戳記設為等於停止位置，以確保 [**IMediaSeeking：： GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) 方法會傳回資料流程結尾的正確值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




