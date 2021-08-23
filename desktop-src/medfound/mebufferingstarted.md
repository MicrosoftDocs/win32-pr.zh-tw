---
description: 表示媒體來源已開始緩衝資料的信號。
ms.assetid: 8637dfcd-2e0c-4cf4-a216-4089c201bfc6
title: 'MEBufferingStarted 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e55a691b723fc2e09487752ee8f5226e32504d60a6d68a4652bbb2b5b3e5aa7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119724268"
---
# <a name="mebufferingstarted-event"></a>MEBufferingStarted 事件

表示媒體來源已開始緩衝資料的信號。

如果來源在媒體會話執行時緩衝資料，則媒體來源可以傳送此事件。 當媒體會話收到此事件時，它會暫停呈現時鐘，直到媒體來源傳送 [MEBufferingStopped](mebufferingstopped.md) 事件為止。 媒體會話也會將 MEBufferingStarted 事件轉送到應用程式。

執行 [**IMFByteStreamBuffering**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) 介面的位元組資料流程也會傳送此事件。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE              | 描述                           |
|----------------------|---------------------------------------|
| VT \_ 空白<br/> | 沒有事件資料。<br/> <br/> |



## <a name="remarks"></a>備註

如果媒體來源傳送 MEBufferingStarted 事件，它必須在停止緩衝資料時傳送 [MEBufferingStopped](mebufferingstopped.md) 事件。 媒體來源必須針對每個 MEBufferingStarted 事件傳送相符的 MEBufferingStopped 事件。 在呼叫來源的 [**IMFMediaSource：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) 方法之前，或呼叫來源的 [**IMFMediaSource：： Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) 方法之後，媒體來源不應轉寄這些事件。

如果您是從媒體基礎網路來源進行串流處理，您可以藉由查詢 **MFNETSOURCE \_ BUFFERPROGRESS \_ 識別碼** 統計資料來取得緩衝進度。 如需詳細資訊，請參閱 [**MFNETSOURCE \_ 統計資料 \_ 識別碼**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids)。

## <a name="examples"></a>範例


```C++
HRESULT GetBufferProgress(IMFMediaSession *pSession, DWORD *pProgress)
{
    IPropertyStore *pProp = NULL;
    PROPVARIANT var;

    // Get the property store from the media session.
    HRESULT hr = MFGetService(
        pSession, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_PPV_ARGS(&pProp)
        );

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_BUFFERPROGRESS_ID;

        hr = pProp->GetValue(key, &var);
    }

    if (SUCCEEDED(hr))
    {
        *pProgress = var.lVal;
    }

    PropVariantClear(&var);
    SafeRelease(&pProp);
    return hr;
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> <dt>

[媒體基礎中的網路功能](networking-in-media-foundation.md)
</dt> </dl>

 

 




