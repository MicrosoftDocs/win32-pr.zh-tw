---
description: 當 IMFMediaSource：:P ause 方法以非同步方式完成時，由媒體來源引發。
ms.assetid: cca03d60-47ae-4a11-b29d-81d749e24df9
title: 'MESourcePaused 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ac346e679eb3a82ca707a14f772f1a79e2a1e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848534"
---
# <a name="mesourcepaused-event"></a><span data-ttu-id="29357-103">MESourcePaused 事件</span><span class="sxs-lookup"><span data-stu-id="29357-103">MESourcePaused event</span></span>

<span data-ttu-id="29357-104">當 [**IMFMediaSource：:P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) 方法以非同步方式完成時，由媒體來源引發。</span><span class="sxs-lookup"><span data-stu-id="29357-104">Raised by a media source when the [**IMFMediaSource::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="29357-105">事件值</span><span class="sxs-lookup"><span data-stu-id="29357-105">Event values</span></span>

<span data-ttu-id="29357-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="29357-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="29357-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="29357-107">VARTYPE</span></span>              | <span data-ttu-id="29357-108">Description</span><span class="sxs-lookup"><span data-stu-id="29357-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="29357-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="29357-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="29357-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="29357-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="29357-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="29357-111">Requirements</span></span>



| <span data-ttu-id="29357-112">需求</span><span class="sxs-lookup"><span data-stu-id="29357-112">Requirement</span></span> | <span data-ttu-id="29357-113">值</span><span class="sxs-lookup"><span data-stu-id="29357-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29357-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="29357-114">Minimum supported client</span></span><br/> | <span data-ttu-id="29357-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="29357-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="29357-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="29357-116">Minimum supported server</span></span><br/> | <span data-ttu-id="29357-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="29357-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="29357-118">標頭</span><span class="sxs-lookup"><span data-stu-id="29357-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="29357-119"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="29357-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29357-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="29357-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29357-121">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="29357-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




