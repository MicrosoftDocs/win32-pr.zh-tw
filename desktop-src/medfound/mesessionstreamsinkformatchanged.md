---
description: 當媒體接收器的格式變更時，由媒體會話引發。
ms.assetid: f56419f8-7f50-4eda-bf4a-fcdbbe46e180
title: 'MESessionStreamSinkFormatChanged 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bed59b9600cbaf8cb942a42beb6bed46d62fc15f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191907"
---
# <a name="mesessionstreamsinkformatchanged-event"></a><span data-ttu-id="c46d2-103">MESessionStreamSinkFormatChanged 事件</span><span class="sxs-lookup"><span data-stu-id="c46d2-103">MESessionStreamSinkFormatChanged event</span></span>

<span data-ttu-id="c46d2-104">當媒體接收器的格式變更時，由媒體會話引發。</span><span class="sxs-lookup"><span data-stu-id="c46d2-104">Raised by the Media Session when the format changes on a media sink.</span></span>

## <a name="event-values"></a><span data-ttu-id="c46d2-105">事件值</span><span class="sxs-lookup"><span data-stu-id="c46d2-105">Event values</span></span>

<span data-ttu-id="c46d2-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="c46d2-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="c46d2-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c46d2-107">VARTYPE</span></span>              | <span data-ttu-id="c46d2-108">Description</span><span class="sxs-lookup"><span data-stu-id="c46d2-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="c46d2-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="c46d2-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="c46d2-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="c46d2-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="c46d2-111">屬性</span><span class="sxs-lookup"><span data-stu-id="c46d2-111">Attributes</span></span>

<span data-ttu-id="c46d2-112">此事件會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="c46d2-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="c46d2-113">屬性</span><span class="sxs-lookup"><span data-stu-id="c46d2-113">Attribute</span></span>                                                                    | <span data-ttu-id="c46d2-114">描述</span><span class="sxs-lookup"><span data-stu-id="c46d2-114">Description</span></span>                                                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c46d2-115">**MF \_ 事件 \_ 輸出 \_ 節點**</span><span class="sxs-lookup"><span data-stu-id="c46d2-115">**MF\_EVENT\_OUTPUT\_NODE**</span></span>](mf-event-output-node-attribute.md)<br/> | <span data-ttu-id="c46d2-116">識別其格式已變更之媒體接收器的拓撲節點。</span><span class="sxs-lookup"><span data-stu-id="c46d2-116">Identifies the topology node for the media sink whose format changed.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="c46d2-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="c46d2-117">Requirements</span></span>



| <span data-ttu-id="c46d2-118">需求</span><span class="sxs-lookup"><span data-stu-id="c46d2-118">Requirement</span></span> | <span data-ttu-id="c46d2-119">值</span><span class="sxs-lookup"><span data-stu-id="c46d2-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c46d2-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c46d2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c46d2-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c46d2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c46d2-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c46d2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c46d2-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c46d2-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c46d2-124">標頭</span><span class="sxs-lookup"><span data-stu-id="c46d2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c46d2-125"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="c46d2-125"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c46d2-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c46d2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c46d2-127">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="c46d2-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




