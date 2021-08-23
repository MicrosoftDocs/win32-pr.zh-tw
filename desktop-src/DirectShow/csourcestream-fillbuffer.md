---
description: FillBuffer 方法會以資料填滿媒體範例。
ms.assetid: dddad8c7-44f1-4ba3-8fb1-7e7e88e40941
title: 'CSourceStream. FillBuffer 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.FillBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b9a522dd2b10e7ced60b65c84621bb1817be4b8abbca8656ba23f49e95fe3892
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687398"
---
# <a name="csourcestreamfillbuffer-method"></a>CSourceStream. FillBuffer 方法

`FillBuffer`方法會以資料填滿媒體範例。

## <a name="syntax"></a>語法


```C++
virtual HRESULT FillBuffer(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSample* 
</dt> <dd>

範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所示的值。



| 傳回碼                                                                             | 描述              |
|-----------------------------------------------------------------------------------------|--------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | 資料流程結尾<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>    | Success<br/>       |



 

## <a name="remarks"></a>備註

衍生的類別必須執行此方法。

提供給這個方法的媒體範例沒有時間戳記。 衍生類別應該呼叫 [**IMediaSample：： SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) 方法來設定時間戳記。 如果適用于媒體類型，則衍生類別也應該透過呼叫 [**IMediaSample：： SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) 方法來設定媒體時間。 如需詳細資訊，請參閱[DirectShow 中的時間和時鐘](time-and-clocks-in-directshow.md)。

在 \_ 資料流程結尾傳回 FALSE。 這會導致 **CSourceStream** 類別傳送資料流程結束通知，並中止緩衝區處理迴圈。 如需詳細資訊，請參閱 [**CSourceStream：:D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>來源 .h (包含) 的資料流程 </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceStream 類別**](csourcestream.md)
</dt> </dl>

 

 




