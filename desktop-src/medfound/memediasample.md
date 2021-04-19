---
description: 當媒體資料流程傳遞新範例以回應 IMFMediaStream：： RequestSample 的呼叫時，即會傳送。
ms.assetid: 01610053-786f-44b5-90d6-2cb2668cd632
title: 'MEMediaSample 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7de0cfcdbf943e0526d61a0c63424f7add078b2c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "107001776"
---
# <a name="memediasample-event"></a><span data-ttu-id="19e80-103">MEMediaSample 事件</span><span class="sxs-lookup"><span data-stu-id="19e80-103">MEMediaSample event</span></span>

<span data-ttu-id="19e80-104">當媒體資料流程傳遞新範例以回應 [**IMFMediaStream：： RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample)的呼叫時，即會傳送。</span><span class="sxs-lookup"><span data-stu-id="19e80-104">Sent when a media stream delivers a new sample in response to a call to [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample).</span></span>

## <a name="event-values"></a><span data-ttu-id="19e80-105">事件值</span><span class="sxs-lookup"><span data-stu-id="19e80-105">Event values</span></span>

<span data-ttu-id="19e80-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="19e80-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="19e80-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="19e80-107">VARTYPE</span></span>                | <span data-ttu-id="19e80-108">Description</span><span class="sxs-lookup"><span data-stu-id="19e80-108">Description</span></span>                                                                                   |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="19e80-109">VT \_ 不明</span><span class="sxs-lookup"><span data-stu-id="19e80-109">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="19e80-110">範例 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="19e80-110">Pointer to the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface of the sample.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="19e80-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="19e80-111">Requirements</span></span>



| <span data-ttu-id="19e80-112">需求</span><span class="sxs-lookup"><span data-stu-id="19e80-112">Requirement</span></span> | <span data-ttu-id="19e80-113">值</span><span class="sxs-lookup"><span data-stu-id="19e80-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19e80-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="19e80-114">Minimum supported client</span></span><br/> | <span data-ttu-id="19e80-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19e80-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="19e80-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="19e80-116">Minimum supported server</span></span><br/> | <span data-ttu-id="19e80-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19e80-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="19e80-118">標頭</span><span class="sxs-lookup"><span data-stu-id="19e80-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="19e80-119"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="19e80-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19e80-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19e80-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19e80-121">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="19e80-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="19e80-122">媒體來源</span><span class="sxs-lookup"><span data-stu-id="19e80-122">Media Sources</span></span>](media-sources.md)
</dt> </dl>

 

 




