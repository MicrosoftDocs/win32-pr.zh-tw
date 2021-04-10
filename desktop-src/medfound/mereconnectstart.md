---
description: 表示媒體來源嘗試重新連線到伺服器的信號。
ms.assetid: c5975279-c710-4046-9152-d1e1c62eb785
title: 'MEReconnectStart 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d21944e937f52205416b5e6e2b52d18c3a3c768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114625"
---
# <a name="mereconnectstart-event"></a><span data-ttu-id="e2552-103">MEReconnectStart 事件</span><span class="sxs-lookup"><span data-stu-id="e2552-103">MEReconnectStart event</span></span>

<span data-ttu-id="e2552-104">表示媒體來源嘗試重新連線到伺服器的信號。</span><span class="sxs-lookup"><span data-stu-id="e2552-104">Signals that a media source is attempting to reconnect to the server.</span></span>

<span data-ttu-id="e2552-105">在重新連接嘗試開始時由媒體來源引發。</span><span class="sxs-lookup"><span data-stu-id="e2552-105">Raised by a media source at the start of a reconnection attempt.</span></span> <span data-ttu-id="e2552-106">如果網路來源嘗試重新連線到伺服器，就會引發此事件。</span><span class="sxs-lookup"><span data-stu-id="e2552-106">The network source raises this event if it attempts to reconnect to the server.</span></span> <span data-ttu-id="e2552-107">媒體會話將此事件轉送到應用程式。</span><span class="sxs-lookup"><span data-stu-id="e2552-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="e2552-108">事件值</span><span class="sxs-lookup"><span data-stu-id="e2552-108">Event values</span></span>

<span data-ttu-id="e2552-109">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="e2552-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="e2552-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e2552-110">VARTYPE</span></span>              | <span data-ttu-id="e2552-111">Description</span><span class="sxs-lookup"><span data-stu-id="e2552-111">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="e2552-112">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="e2552-112">VT\_EMPTY</span></span><br/> | <span data-ttu-id="e2552-113">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="e2552-113">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="e2552-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2552-114">Requirements</span></span>



| <span data-ttu-id="e2552-115">需求</span><span class="sxs-lookup"><span data-stu-id="e2552-115">Requirement</span></span> | <span data-ttu-id="e2552-116">值</span><span class="sxs-lookup"><span data-stu-id="e2552-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2552-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e2552-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e2552-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2552-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e2552-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e2552-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e2552-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2552-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e2552-121">標頭</span><span class="sxs-lookup"><span data-stu-id="e2552-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2552-122"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="e2552-122"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2552-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2552-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2552-124">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="e2552-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




