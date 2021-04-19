---
description: 由非同步媒體基礎轉換 (MFT) 傳送，以回應 MFT \_ 訊息 \_ 命令 \_ 標記訊息。
ms.assetid: d0c0d62d-9133-4d4b-8606-c2ae1d4c9f0a
title: 'METransformMarker 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab79c47e2ddb26f2366aff075548f7905807df1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974588"
---
# <a name="metransformmarker-event"></a><span data-ttu-id="f8225-103">METransformMarker 事件</span><span class="sxs-lookup"><span data-stu-id="f8225-103">METransformMarker event</span></span>

<span data-ttu-id="f8225-104">由非同步媒體基礎轉換 (MFT) 傳送，以回應 **MFT \_ 訊息 \_ 命令 \_ 標記** 訊息。</span><span class="sxs-lookup"><span data-stu-id="f8225-104">Sent by an asynchronous Media Foundation transform (MFT) in response to an **MFT\_MESSAGE\_COMMAND\_MARKER** message.</span></span>

## <a name="event-values"></a><span data-ttu-id="f8225-105">事件值</span><span class="sxs-lookup"><span data-stu-id="f8225-105">Event values</span></span>

<span data-ttu-id="f8225-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="f8225-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="f8225-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="f8225-107">VARTYPE</span></span>              | <span data-ttu-id="f8225-108">Description</span><span class="sxs-lookup"><span data-stu-id="f8225-108">Description</span></span>               |
|----------------------|---------------------------|
| <span data-ttu-id="f8225-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="f8225-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="f8225-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="f8225-110">No event data.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="f8225-111">屬性</span><span class="sxs-lookup"><span data-stu-id="f8225-111">Attributes</span></span>

<span data-ttu-id="f8225-112">此事件會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="f8225-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="f8225-113">屬性</span><span class="sxs-lookup"><span data-stu-id="f8225-113">Attribute</span></span>                                                      | <span data-ttu-id="f8225-114">描述</span><span class="sxs-lookup"><span data-stu-id="f8225-114">Description</span></span>                                                                                                                |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f8225-115">MF \_ 事件 \_ MFT \_ 內容</span><span class="sxs-lookup"><span data-stu-id="f8225-115">MF\_EVENT\_MFT\_CONTEXT</span></span>](mf-event-mft-context.md)<br/> | <span data-ttu-id="f8225-116">來自 **MFT \_ 訊息 \_ 命令 \_ 標記** 訊息的 *ulParam* 參數值。</span><span class="sxs-lookup"><span data-stu-id="f8225-116">The value of the *ulParam* parameter from the **MFT\_MESSAGE\_COMMAND\_MARKER** message.</span></span><br/><span data-ttu-id="f8225-117">*需要 ()*</span><span class="sxs-lookup"><span data-stu-id="f8225-117">*(Required)*</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f8225-118">備註</span><span class="sxs-lookup"><span data-stu-id="f8225-118">Remarks</span></span>

<span data-ttu-id="f8225-119">非同步 MFTs 透過 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) 介面傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="f8225-119">Asynchronous MFTs send this event through the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="f8225-120">同步 MFTs 不會傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="f8225-120">Synchronous MFTs never send this event.</span></span>

<span data-ttu-id="f8225-121">非同步 MFT 的用戶端可以藉由呼叫 [**IMFTransform：:P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) 與 **MFT \_ 訊息 \_ 命令 \_ 標記** 訊息，將標記放置於資料流程中。</span><span class="sxs-lookup"><span data-stu-id="f8225-121">The client of an asynchronous MFT can place a marker in the stream by calling [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) with the **MFT\_MESSAGE\_COMMAND\_MARKER** message.</span></span> <span data-ttu-id="f8225-122">*UlParam* 參數包含應用程式定義的資料。</span><span class="sxs-lookup"><span data-stu-id="f8225-122">The *ulParam* parameter contains application-defined data.</span></span>

<span data-ttu-id="f8225-123">當 MFT 完成處理 [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) 呼叫時可用的所有輸入資料時，mft 會將 METransformMarker 事件排在佇列中。</span><span class="sxs-lookup"><span data-stu-id="f8225-123">When the MFT finishes processing all of the input data that was available at the time of the [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) call, the MFT queues an METransformMarker event.</span></span> <span data-ttu-id="f8225-124">事件的 [MF \_ 事件 \_ MFT \_ 上下文](mf-event-mft-context.md) 屬性包含 *ulParam* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="f8225-124">The [MF\_EVENT\_MFT\_CONTEXT](mf-event-mft-context.md) attribute of the event contains the value of the *ulParam* parameter.</span></span> <span data-ttu-id="f8225-125">如需詳細資訊，請參閱 [非同步 MFTs](asynchronous-mfts.md)。</span><span class="sxs-lookup"><span data-stu-id="f8225-125">For more information, see [Asynchronous MFTs](asynchronous-mfts.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8225-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8225-126">Requirements</span></span>



| <span data-ttu-id="f8225-127">需求</span><span class="sxs-lookup"><span data-stu-id="f8225-127">Requirement</span></span> | <span data-ttu-id="f8225-128">值</span><span class="sxs-lookup"><span data-stu-id="f8225-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8225-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f8225-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f8225-130">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f8225-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="f8225-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f8225-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f8225-132">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f8225-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="f8225-133">標頭</span><span class="sxs-lookup"><span data-stu-id="f8225-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8225-134"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="f8225-134"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8225-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f8225-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8225-136">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="f8225-136">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="f8225-137">非同步 MFTs</span><span class="sxs-lookup"><span data-stu-id="f8225-137">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 




