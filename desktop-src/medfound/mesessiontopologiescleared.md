---
description: 當 IMFMediaSession：： ClearTopologies 方法以非同步方式完成時，由媒體會話引發。
ms.assetid: 2017d13b-8dc2-48f9-a21e-7b826e174edf
title: 'MESessionTopologiesCleared 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 551e98607a8d23d9333527337bbd7d038ed0b340
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114617"
---
# <a name="mesessiontopologiescleared-event"></a><span data-ttu-id="8fa96-103">MESessionTopologiesCleared 事件</span><span class="sxs-lookup"><span data-stu-id="8fa96-103">MESessionTopologiesCleared event</span></span>

<span data-ttu-id="8fa96-104">當 [**IMFMediaSession：： ClearTopologies**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-cleartopologies) 方法以非同步方式完成時，由媒體會話引發。</span><span class="sxs-lookup"><span data-stu-id="8fa96-104">Raised by the Media Session when the [**IMFMediaSession::ClearTopologies**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-cleartopologies) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="8fa96-105">事件值</span><span class="sxs-lookup"><span data-stu-id="8fa96-105">Event values</span></span>

<span data-ttu-id="8fa96-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="8fa96-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="8fa96-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="8fa96-107">VARTYPE</span></span>              | <span data-ttu-id="8fa96-108">Description</span><span class="sxs-lookup"><span data-stu-id="8fa96-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="8fa96-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="8fa96-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="8fa96-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="8fa96-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="8fa96-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="8fa96-111">Requirements</span></span>



| <span data-ttu-id="8fa96-112">需求</span><span class="sxs-lookup"><span data-stu-id="8fa96-112">Requirement</span></span> | <span data-ttu-id="8fa96-113">值</span><span class="sxs-lookup"><span data-stu-id="8fa96-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fa96-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8fa96-114">Minimum supported client</span></span><br/> | <span data-ttu-id="8fa96-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8fa96-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8fa96-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8fa96-116">Minimum supported server</span></span><br/> | <span data-ttu-id="8fa96-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8fa96-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8fa96-118">標頭</span><span class="sxs-lookup"><span data-stu-id="8fa96-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fa96-119"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="8fa96-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fa96-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8fa96-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fa96-121">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="8fa96-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




