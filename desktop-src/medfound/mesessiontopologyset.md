---
description: 在 IMFMediaSession：： SetTopology 方法以非同步方式完成之後引發。 媒體會話會在將拓撲解析成完整拓撲之後引發此事件，並將拓撲排入佇列以供播放。
ms.assetid: 22a298b7-d32b-44ed-b0a1-4e0398ecfe04
title: 'MESessionTopologySet 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 338668b0ec9b4dd81140edfb55a823a5a595459b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943796"
---
# <a name="mesessiontopologyset-event"></a><span data-ttu-id="5a2bb-104">MESessionTopologySet 事件</span><span class="sxs-lookup"><span data-stu-id="5a2bb-104">MESessionTopologySet event</span></span>

<span data-ttu-id="5a2bb-105">在 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) 方法以非同步方式完成之後引發。</span><span class="sxs-lookup"><span data-stu-id="5a2bb-105">Raised after the [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) method completes asynchronously.</span></span> <span data-ttu-id="5a2bb-106">媒體會話會在將拓撲解析成完整拓撲之後引發此事件，並將拓撲排入佇列以供播放。</span><span class="sxs-lookup"><span data-stu-id="5a2bb-106">The Media Session raises this event after it resolves the topology into a full topology and queues the topology for playback.</span></span>

## <a name="event-values"></a><span data-ttu-id="5a2bb-107">事件值</span><span class="sxs-lookup"><span data-stu-id="5a2bb-107">Event values</span></span>

<span data-ttu-id="5a2bb-108">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="5a2bb-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="5a2bb-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5a2bb-109">VARTYPE</span></span>                | <span data-ttu-id="5a2bb-110">Description</span><span class="sxs-lookup"><span data-stu-id="5a2bb-110">Description</span></span>                                                                                              |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a2bb-111">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="5a2bb-111">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="5a2bb-112">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="5a2bb-112">No event data.</span></span><br/> <br/>                                                                    |
| <span data-ttu-id="5a2bb-113">VT \_ 不明</span><span class="sxs-lookup"><span data-stu-id="5a2bb-113">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="5a2bb-114">完整拓撲之 [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="5a2bb-114">Pointer to the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) interface of the full topology.</span></span><br/> <br/> |



## <a name="examples"></a><span data-ttu-id="5a2bb-115">範例</span><span class="sxs-lookup"><span data-stu-id="5a2bb-115">Examples</span></span>

<span data-ttu-id="5a2bb-116">下列範例會從 MESessionTopologySet 事件中取出 [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) 指標。</span><span class="sxs-lookup"><span data-stu-id="5a2bb-116">The following example retrieves the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) pointer from an MESessionTopologySet event.</span></span>


```
HRESULT GetTopologyFromEvent(IMFMediaEvent *pEvent, IMFTopology **ppTopology)
{
    HRESULT hr = S_OK;
    PROPVARIANT var;

    PropVariantInit(&var);
    hr = pEvent->GetValue(&var);
    if (SUCCEEDED(hr))
    {
        if (var.vt != VT_UNKNOWN)
        {
            hr = E_UNEXPECTED;
        }
    }
    if (SUCCEEDED(hr))
    {
        hr = var.punkVal->QueryInterface(__uuidof(IMFTopology), (void**)ppTopology);
    }
    PropVariantClear(&var);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="5a2bb-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a2bb-117">Requirements</span></span>



| <span data-ttu-id="5a2bb-118">需求</span><span class="sxs-lookup"><span data-stu-id="5a2bb-118">Requirement</span></span> | <span data-ttu-id="5a2bb-119">值</span><span class="sxs-lookup"><span data-stu-id="5a2bb-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a2bb-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5a2bb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5a2bb-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a2bb-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5a2bb-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5a2bb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5a2bb-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a2bb-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5a2bb-124">標頭</span><span class="sxs-lookup"><span data-stu-id="5a2bb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a2bb-125"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="5a2bb-125"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a2bb-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5a2bb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a2bb-127">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="5a2bb-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




