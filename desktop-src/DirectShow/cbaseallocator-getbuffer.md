---
description: GetBuffer 方法會抓取包含緩衝區的媒體範例。 這個方法會實 IMemAllocator：： GetBuffer 方法。
ms.assetid: 81694b9c-b325-47c8-94e4-f54d1329a684
title: 'CBaseAllocator. GetBuffer 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a183079e954b3a0d8b07fc1d7daf039db8fcc840243a6ea421b2390ce02a3625
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118661680"
---
# <a name="cbaseallocatorgetbuffer-method"></a>CBaseAllocator. GetBuffer 方法

`GetBuffer`方法會抓取包含緩衝區的媒體範例。 這個方法會實 [**IMemAllocator：： GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT GetBuffer(
   IMediaSample   **ppBuffer,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime,
   DWORD          dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppBuffer* 
</dt> <dd>

接收緩衝區 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。 呼叫端必須釋放介面。

</dd> <dt>

*pStartTime* 
</dt> <dd>

範例開始時間的指標。

</dd> <dt>

*pEndTime* 
</dt> <dd>

範例結束時間的指標。

</dd> <dt>

*dwFlags* 
</dt> <dd>

零或多個旗標的位元組合。 基類支援下列旗標。



| 值                                                                                                                                                          | 意義                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="AM_GBF_NOWAIT"></span><span id="am_gbf_nowait"></span><dl> <dt>**AM \_ GBF \_ NOWAIT**</dt> </dl> | 請勿等候緩衝區變成可用。 <br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個 **HRESULT** 值。



| 傳回碼                                                                                           | 描述                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                  | 成功。<br/>                     |
| <dl> <dt>**VFW \_ E \_ 未 \_ 認可**</dt> </dl> | 未認可配置器。<br/> |
| <dl> <dt>**VFW \_ E \_ TIMEOUT**</dt> </dl>        | 逾時。<br/>                   |



 

## <a name="remarks"></a>備註

除非呼叫端在 *dwFlags* 中指定 **AM \_ GBF \_ NOWAIT** 旗標，否則這個方法會封鎖，直到下一個範例可供使用為止。

抓取的媒體範例具有已配置緩衝區的有效指標。 呼叫端負責設定範例上的任何其他屬性，例如時間戳記、媒體時間或同步點屬性。 如需詳細資訊，請參閱 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample)。

在基類中， *pStartTime* 和 *pEndTime* 參數會被忽略。 衍生的類別可以使用這些值。 例如， [影片](video-renderer-filter.md) 轉譯器篩選器的配置器會使用這些值，在 DirectDraw 表面之間進行同步切換。

如果此方法需要等候範例，則會將等待物件的計數遞增 ([**CBaseAllocator：： m \_ LCount**](cbaseallocator-m-lcount.md)) ，而信號 ([**CBaseAllocator：： m \_ HSem**](cbaseallocator-m-hsem.md)) 上的呼叫 [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)函數。 當範例變成可用時，它會在配置器上呼叫 [**CBaseAllocator：： ReleaseBuffer**](cbaseallocator-releasebuffer.md) 方法，這會增加 **m \_ lCount** (的信號計數，藉此釋出等候中的執行緒) 並將 **\_ lCount** 回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseAllocator 類別**](cbaseallocator.md)
</dt> </dl>

 

