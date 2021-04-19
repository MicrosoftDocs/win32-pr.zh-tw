---
description: 當 IMFMediaSource：： Stop 方法以非同步方式完成時，由媒體來源引發。
ms.assetid: 0eda9aa1-3aad-43ac-9d87-ab96e4ac319d
title: 'MESourceStopped 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d08909a95cf1c867c5d8392425f25565b5a2728d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967166"
---
# <a name="mesourcestopped-event"></a><span data-ttu-id="508c0-103">MESourceStopped 事件</span><span class="sxs-lookup"><span data-stu-id="508c0-103">MESourceStopped event</span></span>

<span data-ttu-id="508c0-104">當 [**IMFMediaSource：： Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) 方法以非同步方式完成時，由媒體來源引發。</span><span class="sxs-lookup"><span data-stu-id="508c0-104">Raised by a media source when the [**IMFMediaSource::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="508c0-105">事件值</span><span class="sxs-lookup"><span data-stu-id="508c0-105">Event values</span></span>

<span data-ttu-id="508c0-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="508c0-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="508c0-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="508c0-107">VARTYPE</span></span>              | <span data-ttu-id="508c0-108">Description</span><span class="sxs-lookup"><span data-stu-id="508c0-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="508c0-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="508c0-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="508c0-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="508c0-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="508c0-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="508c0-111">Requirements</span></span>



| <span data-ttu-id="508c0-112">需求</span><span class="sxs-lookup"><span data-stu-id="508c0-112">Requirement</span></span> | <span data-ttu-id="508c0-113">值</span><span class="sxs-lookup"><span data-stu-id="508c0-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="508c0-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="508c0-114">Minimum supported client</span></span><br/> | <span data-ttu-id="508c0-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="508c0-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="508c0-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="508c0-116">Minimum supported server</span></span><br/> | <span data-ttu-id="508c0-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="508c0-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="508c0-118">標頭</span><span class="sxs-lookup"><span data-stu-id="508c0-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="508c0-119"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="508c0-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="508c0-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="508c0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="508c0-121">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="508c0-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




