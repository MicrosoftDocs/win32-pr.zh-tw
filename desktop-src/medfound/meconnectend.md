---
description: 當網路來源完成開啟 URL 時引發。
ms.assetid: 737aec32-24f4-4825-ad34-8d2fc889bc09
title: 'MEConnectEnd 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9801b1af38f7bf0a0107680d77a399b3927a616e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974094"
---
# <a name="meconnectend-event"></a><span data-ttu-id="abe14-103">MEConnectEnd 事件</span><span class="sxs-lookup"><span data-stu-id="abe14-103">MEConnectEnd event</span></span>

<span data-ttu-id="abe14-104">當網路來源完成開啟 URL 時引發。</span><span class="sxs-lookup"><span data-stu-id="abe14-104">Raised by the network source when it finishes opening a URL.</span></span>

## <a name="event-values"></a><span data-ttu-id="abe14-105">事件值</span><span class="sxs-lookup"><span data-stu-id="abe14-105">Event values</span></span>

<span data-ttu-id="abe14-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="abe14-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="abe14-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="abe14-107">VARTYPE</span></span>              | <span data-ttu-id="abe14-108">Description</span><span class="sxs-lookup"><span data-stu-id="abe14-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="abe14-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="abe14-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="abe14-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="abe14-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="abe14-111">備註</span><span class="sxs-lookup"><span data-stu-id="abe14-111">Remarks</span></span>

<span data-ttu-id="abe14-112">網路來源會透過應用程式的 [**IMFSourceOpenMonitor：： OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) 方法，將此事件直接傳送至應用程式，而不是透過一般 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) 介面。</span><span class="sxs-lookup"><span data-stu-id="abe14-112">The network source sends this event directly to the application through the application's [**IMFSourceOpenMonitor::OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) method, not through the usual [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="abe14-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="abe14-113">Requirements</span></span>



| <span data-ttu-id="abe14-114">需求</span><span class="sxs-lookup"><span data-stu-id="abe14-114">Requirement</span></span> | <span data-ttu-id="abe14-115">值</span><span class="sxs-lookup"><span data-stu-id="abe14-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abe14-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="abe14-116">Minimum supported client</span></span><br/> | <span data-ttu-id="abe14-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="abe14-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="abe14-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="abe14-118">Minimum supported server</span></span><br/> | <span data-ttu-id="abe14-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="abe14-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="abe14-120">標頭</span><span class="sxs-lookup"><span data-stu-id="abe14-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="abe14-121"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="abe14-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abe14-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="abe14-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abe14-123">**IMFSourceOpenMonitor**</span><span class="sxs-lookup"><span data-stu-id="abe14-123">**IMFSourceOpenMonitor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor)
</dt> <dt>

[<span data-ttu-id="abe14-124">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="abe14-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




