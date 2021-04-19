---
description: 在授權取得完成時引發。 如需詳細資訊，請參閱 MELicenseAcquisitionStart。
ms.assetid: f577131b-887a-4912-8278-1165a801c2b3
title: 'MELicenseAcquisitionCompleted 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 545fa012f974637f5d268a7d8257daaf9b393f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106984187"
---
# <a name="melicenseacquisitioncompleted-event"></a><span data-ttu-id="b8e87-104">MELicenseAcquisitionCompleted 事件</span><span class="sxs-lookup"><span data-stu-id="b8e87-104">MELicenseAcquisitionCompleted event</span></span>

<span data-ttu-id="b8e87-105">在授權取得完成時引發。</span><span class="sxs-lookup"><span data-stu-id="b8e87-105">Raised when license acquisition is complete.</span></span> <span data-ttu-id="b8e87-106">如需詳細資訊，請參閱 [MELicenseAcquisitionStart](melicenseacquisitionstart.md)。</span><span class="sxs-lookup"><span data-stu-id="b8e87-106">For more information, see [MELicenseAcquisitionStart](melicenseacquisitionstart.md).</span></span>

## <a name="event-values"></a><span data-ttu-id="b8e87-107">事件值</span><span class="sxs-lookup"><span data-stu-id="b8e87-107">Event values</span></span>

<span data-ttu-id="b8e87-108">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="b8e87-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="b8e87-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="b8e87-109">VARTYPE</span></span>              | <span data-ttu-id="b8e87-110">Description</span><span class="sxs-lookup"><span data-stu-id="b8e87-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="b8e87-111">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="b8e87-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="b8e87-112">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="b8e87-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="b8e87-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8e87-113">Requirements</span></span>



| <span data-ttu-id="b8e87-114">需求</span><span class="sxs-lookup"><span data-stu-id="b8e87-114">Requirement</span></span> | <span data-ttu-id="b8e87-115">值</span><span class="sxs-lookup"><span data-stu-id="b8e87-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8e87-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b8e87-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b8e87-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8e87-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b8e87-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b8e87-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b8e87-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8e87-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b8e87-120">標頭</span><span class="sxs-lookup"><span data-stu-id="b8e87-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8e87-121"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="b8e87-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8e87-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8e87-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8e87-123">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="b8e87-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




