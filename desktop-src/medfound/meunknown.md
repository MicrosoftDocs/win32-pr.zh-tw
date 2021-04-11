---
description: 未知的事件種類。 您可以使用這個值來初始化 MediaEventType 型別的變數，但是元件絕對不能引發 MEUnknown 事件。
ms.assetid: 786b69f4-8713-41db-829a-c13512baa3f1
title: 'MEUnknown 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a768fde2939b7e32ed8d1007d2988c2e54cc6726
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943794"
---
# <a name="meunknown-event"></a><span data-ttu-id="5b7dd-104">MEUnknown 事件</span><span class="sxs-lookup"><span data-stu-id="5b7dd-104">MEUnknown event</span></span>

<span data-ttu-id="5b7dd-105">未知的事件種類。</span><span class="sxs-lookup"><span data-stu-id="5b7dd-105">Unknown event type.</span></span> <span data-ttu-id="5b7dd-106">您可以使用這個值來初始化 **MediaEventType** 型別的變數，但是元件絕對不能引發 MEUnknown 事件。</span><span class="sxs-lookup"><span data-stu-id="5b7dd-106">You can use this value to initialize variables of type **MediaEventType**, but a component should never raise the MEUnknown event</span></span>

## <a name="event-values"></a><span data-ttu-id="5b7dd-107">事件值</span><span class="sxs-lookup"><span data-stu-id="5b7dd-107">Event values</span></span>

<span data-ttu-id="5b7dd-108">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="5b7dd-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="5b7dd-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5b7dd-109">VARTYPE</span></span>              | <span data-ttu-id="5b7dd-110">Description</span><span class="sxs-lookup"><span data-stu-id="5b7dd-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="5b7dd-111">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="5b7dd-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="5b7dd-112">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="5b7dd-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="5b7dd-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b7dd-113">Requirements</span></span>



| <span data-ttu-id="5b7dd-114">需求</span><span class="sxs-lookup"><span data-stu-id="5b7dd-114">Requirement</span></span> | <span data-ttu-id="5b7dd-115">值</span><span class="sxs-lookup"><span data-stu-id="5b7dd-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b7dd-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5b7dd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5b7dd-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b7dd-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5b7dd-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5b7dd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5b7dd-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b7dd-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5b7dd-120">標頭</span><span class="sxs-lookup"><span data-stu-id="5b7dd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b7dd-121"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="5b7dd-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b7dd-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b7dd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b7dd-123">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="5b7dd-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




