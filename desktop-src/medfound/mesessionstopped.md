---
description: 當 IMFMediaSession：： Stop 方法以非同步方式完成時引發。
ms.assetid: 9cac9040-f652-4509-bbab-f2a41959d836
title: 'MESessionStopped 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e1bd74c168931cc4ac68ae3c990a156664e4b9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320748"
---
# <a name="mesessionstopped-event"></a><span data-ttu-id="f4296-103">MESessionStopped 事件</span><span class="sxs-lookup"><span data-stu-id="f4296-103">MESessionStopped event</span></span>

<span data-ttu-id="f4296-104">當 [**IMFMediaSession：： Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) 方法以非同步方式完成時引發。</span><span class="sxs-lookup"><span data-stu-id="f4296-104">Raised when the [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="f4296-105">事件值</span><span class="sxs-lookup"><span data-stu-id="f4296-105">Event values</span></span>

<span data-ttu-id="f4296-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="f4296-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="f4296-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="f4296-107">VARTYPE</span></span>              | <span data-ttu-id="f4296-108">Description</span><span class="sxs-lookup"><span data-stu-id="f4296-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="f4296-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="f4296-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="f4296-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="f4296-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="f4296-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4296-111">Requirements</span></span>



| <span data-ttu-id="f4296-112">需求</span><span class="sxs-lookup"><span data-stu-id="f4296-112">Requirement</span></span> | <span data-ttu-id="f4296-113">值</span><span class="sxs-lookup"><span data-stu-id="f4296-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4296-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f4296-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f4296-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4296-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f4296-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f4296-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f4296-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4296-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f4296-118">標頭</span><span class="sxs-lookup"><span data-stu-id="f4296-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4296-119"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="f4296-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4296-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4296-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4296-121">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="f4296-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




