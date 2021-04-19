---
description: 表示媒體來源已開始緩衝資料的信號。
ms.assetid: 8637dfcd-2e0c-4cf4-a216-4089c201bfc6
title: 'MEBufferingStarted 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eb3baf8e66d44eb67ee4c1bbc54ae2e197db081
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977790"
---
# <a name="mebufferingstarted-event"></a><span data-ttu-id="65221-103">MEBufferingStarted 事件</span><span class="sxs-lookup"><span data-stu-id="65221-103">MEBufferingStarted event</span></span>

<span data-ttu-id="65221-104">表示媒體來源已開始緩衝資料的信號。</span><span class="sxs-lookup"><span data-stu-id="65221-104">Signals that a media source has started to buffer data.</span></span>

<span data-ttu-id="65221-105">如果來源在媒體會話執行時緩衝資料，則媒體來源可以傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="65221-105">A media source can send this event if the source buffers data while the Media Session is running.</span></span> <span data-ttu-id="65221-106">當媒體會話收到此事件時，它會暫停呈現時鐘，直到媒體來源傳送 [MEBufferingStopped](mebufferingstopped.md) 事件為止。</span><span class="sxs-lookup"><span data-stu-id="65221-106">When the Media Session receives this event, it pauses the presentation clock until the media source sends the [MEBufferingStopped](mebufferingstopped.md) event.</span></span> <span data-ttu-id="65221-107">媒體會話也會將 MEBufferingStarted 事件轉送到應用程式。</span><span class="sxs-lookup"><span data-stu-id="65221-107">The Media Session also forwards the MEBufferingStarted event to the application.</span></span>

<span data-ttu-id="65221-108">執行 [**IMFByteStreamBuffering**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) 介面的位元組資料流程也會傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="65221-108">Byte streams that implement the [**IMFByteStreamBuffering**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) interface also send this event.</span></span>

## <a name="event-values"></a><span data-ttu-id="65221-109">事件值</span><span class="sxs-lookup"><span data-stu-id="65221-109">Event values</span></span>

<span data-ttu-id="65221-110">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="65221-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="65221-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="65221-111">VARTYPE</span></span>              | <span data-ttu-id="65221-112">Description</span><span class="sxs-lookup"><span data-stu-id="65221-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="65221-113">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="65221-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="65221-114">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="65221-114">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="65221-115">備註</span><span class="sxs-lookup"><span data-stu-id="65221-115">Remarks</span></span>

<span data-ttu-id="65221-116">如果媒體來源傳送 MEBufferingStarted 事件，它必須在停止緩衝資料時傳送 [MEBufferingStopped](mebufferingstopped.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="65221-116">If a media source sends the MEBufferingStarted event, it must send the [MEBufferingStopped](mebufferingstopped.md) event when it stops buffering data.</span></span> <span data-ttu-id="65221-117">媒體來源必須針對每個 MEBufferingStarted 事件傳送相符的 MEBufferingStopped 事件。</span><span class="sxs-lookup"><span data-stu-id="65221-117">The media source must send a matching MEBufferingStopped event for every MEBufferingStarted event.</span></span> <span data-ttu-id="65221-118">在呼叫來源的 [**IMFMediaSource：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) 方法之前，或呼叫來源的 [**IMFMediaSource：： Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) 方法之後，媒體來源不應轉寄這些事件。</span><span class="sxs-lookup"><span data-stu-id="65221-118">The media source should not forward these events before the source's [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method is called, or after the source's [**IMFMediaSource::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) method is called.</span></span>

<span data-ttu-id="65221-119">如果您是從媒體基礎網路來源進行串流處理，您可以藉由查詢 **MFNETSOURCE \_ BUFFERPROGRESS \_ 識別碼** 統計資料來取得緩衝進度。</span><span class="sxs-lookup"><span data-stu-id="65221-119">If you are streaming from the Media Foundation network source, you can get the buffering progress by querying the **MFNETSOURCE\_BUFFERPROGRESS\_ID** statistic.</span></span> <span data-ttu-id="65221-120">如需詳細資訊，請參閱 [**MFNETSOURCE \_ 統計資料 \_ 識別碼**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids)。</span><span class="sxs-lookup"><span data-stu-id="65221-120">For more information, see [**MFNETSOURCE\_STATISTICS\_IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).</span></span>

## <a name="examples"></a><span data-ttu-id="65221-121">範例</span><span class="sxs-lookup"><span data-stu-id="65221-121">Examples</span></span>


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



## <a name="requirements"></a><span data-ttu-id="65221-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="65221-122">Requirements</span></span>



| <span data-ttu-id="65221-123">需求</span><span class="sxs-lookup"><span data-stu-id="65221-123">Requirement</span></span> | <span data-ttu-id="65221-124">值</span><span class="sxs-lookup"><span data-stu-id="65221-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65221-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="65221-125">Minimum supported client</span></span><br/> | <span data-ttu-id="65221-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65221-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="65221-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="65221-127">Minimum supported server</span></span><br/> | <span data-ttu-id="65221-128">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65221-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="65221-129">標頭</span><span class="sxs-lookup"><span data-stu-id="65221-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="65221-130"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="65221-130"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65221-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65221-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65221-132">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="65221-132">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="65221-133">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="65221-133">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




