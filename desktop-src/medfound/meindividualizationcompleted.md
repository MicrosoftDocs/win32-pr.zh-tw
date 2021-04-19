---
description: 在完成工作時由原則引擎引發。 如需詳細資訊，請參閱 MEIndividualizationStart 事件。
ms.assetid: 44a4956f-19ba-410d-b96c-e7774cbe2d7e
title: 'MEIndividualizationCompleted 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7143274d12a9ad113f714062ff8f88c1fb8277cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982328"
---
# <a name="meindividualizationcompleted-event"></a><span data-ttu-id="4805b-104">MEIndividualizationCompleted 事件</span><span class="sxs-lookup"><span data-stu-id="4805b-104">MEIndividualizationCompleted event</span></span>

<span data-ttu-id="4805b-105">在完成工作時由原則引擎引發。</span><span class="sxs-lookup"><span data-stu-id="4805b-105">Raised by the policy engine when individualization is complete.</span></span> <span data-ttu-id="4805b-106">如需詳細資訊，請參閱 [MEIndividualizationStart](meindividualizationstart.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="4805b-106">For more information, see [MEIndividualizationStart](meindividualizationstart.md) event.</span></span>

## <a name="event-values"></a><span data-ttu-id="4805b-107">事件值</span><span class="sxs-lookup"><span data-stu-id="4805b-107">Event values</span></span>

<span data-ttu-id="4805b-108">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="4805b-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="4805b-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="4805b-109">VARTYPE</span></span>              | <span data-ttu-id="4805b-110">Description</span><span class="sxs-lookup"><span data-stu-id="4805b-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="4805b-111">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="4805b-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="4805b-112">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="4805b-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="4805b-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="4805b-113">Requirements</span></span>



| <span data-ttu-id="4805b-114">需求</span><span class="sxs-lookup"><span data-stu-id="4805b-114">Requirement</span></span> | <span data-ttu-id="4805b-115">值</span><span class="sxs-lookup"><span data-stu-id="4805b-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4805b-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4805b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4805b-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4805b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4805b-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4805b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4805b-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4805b-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4805b-120">標頭</span><span class="sxs-lookup"><span data-stu-id="4805b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4805b-121"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="4805b-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4805b-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4805b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4805b-123">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="4805b-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




