---
description: ReleaseBuffer 方法會將媒體範例傳回給可用媒體範例的清單。 這個方法會實 IMemAllocator：： ReleaseBuffer 方法。
ms.assetid: 35e4e426-044c-4e57-af13-2fddf8501db7
title: 'CBaseAllocator. ReleaseBuffer 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.ReleaseBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e339f3a8186e845e28261633806a61b1b15c281
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993614"
---
# <a name="cbaseallocatorreleasebuffer-method"></a>CBaseAllocator. ReleaseBuffer 方法

方法會將 `ReleaseBuffer` 媒體範例傳回給可用媒體範例的清單。 這個方法會實 [**IMemAllocator：： ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT ReleaseBuffer(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSample* 
</dt> <dd>

媒體範例物件之 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

當媒體範例的參考計數到達零時，此範例會以其本身做為參數來呼叫 **ReleaseBuffer** 。 這個方法會執行下列動作。

-   將媒體範例傳回 ([**CBaseAllocator：： m \_ lFree**](cbaseallocator-m-lfree.md)) 的可用清單。
-   呼叫 [**CBaseAllocator：： NotifySample**](cbaseallocator-notifysample.md) 方法，這個方法會釋放對 [**CBaseAllocator：： GetBuffer**](cbaseallocator-getbuffer.md) 方法的呼叫所封鎖的任何執行緒。
-   如果先前呼叫 [**CBaseAllocator：： SetNotify**](cbaseallocator-setnotify.md) 方法，則會呼叫 **IMemAllocatorNotifyCallbackTemp：： NotifyRelease** 方法。
-   當最後一個樣本釋出時，如果有擱置中的 [**CBaseAllocator：:D ecommit**](cbaseallocator-decommit.md) 呼叫，就會呼叫 [**CBaseAllocator：： Free**](cbaseallocator-free.md) 方法來釋放緩衝區記憶體。  (在基類中， **Free** 是純虛擬方法。 ) 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseAllocator 類別**](cbaseallocator.md)
</dt> </dl>

 

 




