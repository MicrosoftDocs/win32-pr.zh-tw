---
description: 當 IMFMediaSession：： Close 方法以非同步方式完成時引發。
ms.assetid: d1056ce7-5527-428a-8ace-e1c10a2124a5
title: 'MESessionClosed 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49591e602c06a9beae616ff2a88a2a71241b6e9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969271"
---
# <a name="mesessionclosed-event"></a><span data-ttu-id="ae2da-103">MESessionClosed 事件</span><span class="sxs-lookup"><span data-stu-id="ae2da-103">MESessionClosed event</span></span>

<span data-ttu-id="ae2da-104">當 [**IMFMediaSession：： Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) 方法以非同步方式完成時引發。</span><span class="sxs-lookup"><span data-stu-id="ae2da-104">Raised when the [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="ae2da-105">事件值</span><span class="sxs-lookup"><span data-stu-id="ae2da-105">Event values</span></span>

<span data-ttu-id="ae2da-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="ae2da-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="ae2da-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ae2da-107">VARTYPE</span></span>              | <span data-ttu-id="ae2da-108">Description</span><span class="sxs-lookup"><span data-stu-id="ae2da-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="ae2da-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="ae2da-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="ae2da-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="ae2da-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="ae2da-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="ae2da-111">Requirements</span></span>



| <span data-ttu-id="ae2da-112">需求</span><span class="sxs-lookup"><span data-stu-id="ae2da-112">Requirement</span></span> | <span data-ttu-id="ae2da-113">值</span><span class="sxs-lookup"><span data-stu-id="ae2da-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae2da-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ae2da-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ae2da-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ae2da-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ae2da-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ae2da-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ae2da-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ae2da-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ae2da-118">標頭</span><span class="sxs-lookup"><span data-stu-id="ae2da-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae2da-119"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="ae2da-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae2da-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ae2da-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae2da-121">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="ae2da-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




