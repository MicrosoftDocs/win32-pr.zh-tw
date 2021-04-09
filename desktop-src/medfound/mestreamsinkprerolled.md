---
description: 資料流程接收到足夠的向前復原資料以開始轉譯時，由資料流程接收器引發。 此事件是由支援 IMFMediaSinkPreroll 介面的媒體接收所引發。
ms.assetid: 1ecb1805-73ce-4741-b969-6eb88982ee26
title: 'MEStreamSinkPrerolled 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 312daa90c995ccbbe8667cfa5acdf47975248474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691823"
---
# <a name="mestreamsinkprerolled-event"></a><span data-ttu-id="057f0-104">MEStreamSinkPrerolled 事件</span><span class="sxs-lookup"><span data-stu-id="057f0-104">MEStreamSinkPrerolled event</span></span>

<span data-ttu-id="057f0-105">資料流程接收到足夠的向前復原資料以開始轉譯時，由資料流程接收器引發。</span><span class="sxs-lookup"><span data-stu-id="057f0-105">Raised by a stream sink when the stream has received enough pre-roll data to begin rendering.</span></span> <span data-ttu-id="057f0-106">此事件是由支援 [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) 介面的媒體接收所引發。</span><span class="sxs-lookup"><span data-stu-id="057f0-106">This event is raised by media sinks that support the [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) interface.</span></span>

## <a name="event-values"></a><span data-ttu-id="057f0-107">事件值</span><span class="sxs-lookup"><span data-stu-id="057f0-107">Event values</span></span>

<span data-ttu-id="057f0-108">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="057f0-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="057f0-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="057f0-109">VARTYPE</span></span>              | <span data-ttu-id="057f0-110">Description</span><span class="sxs-lookup"><span data-stu-id="057f0-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="057f0-111">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="057f0-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="057f0-112">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="057f0-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="057f0-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="057f0-113">Requirements</span></span>



| <span data-ttu-id="057f0-114">需求</span><span class="sxs-lookup"><span data-stu-id="057f0-114">Requirement</span></span> | <span data-ttu-id="057f0-115">值</span><span class="sxs-lookup"><span data-stu-id="057f0-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="057f0-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="057f0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="057f0-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="057f0-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="057f0-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="057f0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="057f0-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="057f0-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="057f0-120">標頭</span><span class="sxs-lookup"><span data-stu-id="057f0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="057f0-121"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="057f0-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="057f0-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="057f0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="057f0-123">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="057f0-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="057f0-124">媒體接收器</span><span class="sxs-lookup"><span data-stu-id="057f0-124">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




