---
description: 自訂事件種類。
ms.assetid: a54a446c-0e96-467b-90f6-0f64a7c1727d
title: 'MEExtendedType 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d5551110fc3637a40834a7bf9251826f151ec62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983396"
---
# <a name="meextendedtype-event"></a><span data-ttu-id="a571c-103">MEExtendedType 事件</span><span class="sxs-lookup"><span data-stu-id="a571c-103">MEExtendedType event</span></span>

<span data-ttu-id="a571c-104">自訂事件種類。</span><span class="sxs-lookup"><span data-stu-id="a571c-104">Custom event type.</span></span> <span data-ttu-id="a571c-105">您可以使用此事件種類來定義元件的自訂事件。</span><span class="sxs-lookup"><span data-stu-id="a571c-105">You can use this event type to define custom events for your component.</span></span> <span data-ttu-id="a571c-106">使用擴充的事件種類來識別事件。</span><span class="sxs-lookup"><span data-stu-id="a571c-106">Use the extended event type to identify the event.</span></span> <span data-ttu-id="a571c-107">擴充的事件種類是與事件相關聯的 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="a571c-107">The extended event type is a GUID value associated with the event.</span></span> <span data-ttu-id="a571c-108">如需詳細資訊，請參閱 [**IMFMediaEvent：： GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype)。</span><span class="sxs-lookup"><span data-stu-id="a571c-108">For more information, see [**IMFMediaEvent::GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype).</span></span>

## <a name="event-values"></a><span data-ttu-id="a571c-109">事件值</span><span class="sxs-lookup"><span data-stu-id="a571c-109">Event values</span></span>

<span data-ttu-id="a571c-110">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="a571c-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="a571c-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="a571c-111">VARTYPE</span></span>              | <span data-ttu-id="a571c-112">Description</span><span class="sxs-lookup"><span data-stu-id="a571c-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="a571c-113">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="a571c-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="a571c-114">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="a571c-114">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="a571c-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="a571c-115">Requirements</span></span>



| <span data-ttu-id="a571c-116">需求</span><span class="sxs-lookup"><span data-stu-id="a571c-116">Requirement</span></span> | <span data-ttu-id="a571c-117">值</span><span class="sxs-lookup"><span data-stu-id="a571c-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a571c-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a571c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a571c-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a571c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a571c-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a571c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a571c-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a571c-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a571c-122">標頭</span><span class="sxs-lookup"><span data-stu-id="a571c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a571c-123"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="a571c-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a571c-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a571c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a571c-125">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="a571c-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




