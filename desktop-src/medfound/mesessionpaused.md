---
description: 當 IMFMediaSession：:P ause 方法以非同步方式完成時引發。
ms.assetid: 72546082-83ec-4481-a24f-e82bd6c88859
title: 'MESessionPaused 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd3e8ef60426f83203cfffae3a75febfdf7032d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114621"
---
# <a name="mesessionpaused-event"></a><span data-ttu-id="1abea-103">MESessionPaused 事件</span><span class="sxs-lookup"><span data-stu-id="1abea-103">MESessionPaused event</span></span>

<span data-ttu-id="1abea-104">當 [**IMFMediaSession：:P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) 方法以非同步方式完成時引發。</span><span class="sxs-lookup"><span data-stu-id="1abea-104">Raised when the [**IMFMediaSession::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="1abea-105">事件值</span><span class="sxs-lookup"><span data-stu-id="1abea-105">Event values</span></span>

<span data-ttu-id="1abea-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="1abea-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="1abea-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="1abea-107">VARTYPE</span></span>              | <span data-ttu-id="1abea-108">Description</span><span class="sxs-lookup"><span data-stu-id="1abea-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="1abea-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="1abea-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="1abea-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="1abea-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="1abea-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="1abea-111">Requirements</span></span>



| <span data-ttu-id="1abea-112">需求</span><span class="sxs-lookup"><span data-stu-id="1abea-112">Requirement</span></span> | <span data-ttu-id="1abea-113">值</span><span class="sxs-lookup"><span data-stu-id="1abea-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1abea-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1abea-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1abea-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1abea-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1abea-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1abea-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1abea-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1abea-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1abea-118">標頭</span><span class="sxs-lookup"><span data-stu-id="1abea-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="1abea-119"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="1abea-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1abea-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1abea-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1abea-121">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="1abea-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




