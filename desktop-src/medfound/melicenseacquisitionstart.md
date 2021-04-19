---
description: 當授權取得即將開始時，由原則引擎引發。 授權取得是使用 IMFContentProtectionManager 介面的應用程式實作為執行。
ms.assetid: c328743c-a69b-431e-8a05-0e140aad9b4d
title: 'MELicenseAcquisitionStart 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 914d2580c95cf40986a844a994c1e284c5ad9e22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989301"
---
# <a name="melicenseacquisitionstart-event"></a><span data-ttu-id="605c3-104">MELicenseAcquisitionStart 事件</span><span class="sxs-lookup"><span data-stu-id="605c3-104">MELicenseAcquisitionStart event</span></span>

<span data-ttu-id="605c3-105">當授權取得即將開始時，由原則引擎引發。</span><span class="sxs-lookup"><span data-stu-id="605c3-105">Raised by the policy engine when license acquisition is about to begin.</span></span> <span data-ttu-id="605c3-106">授權取得是使用應用程式的 [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) 介面實作為執行。</span><span class="sxs-lookup"><span data-stu-id="605c3-106">License acquisition is performed using the application's implementation of the [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) interface.</span></span>

## <a name="event-values"></a><span data-ttu-id="605c3-107">事件值</span><span class="sxs-lookup"><span data-stu-id="605c3-107">Event values</span></span>

<span data-ttu-id="605c3-108">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="605c3-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="605c3-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="605c3-109">VARTYPE</span></span>              | <span data-ttu-id="605c3-110">Description</span><span class="sxs-lookup"><span data-stu-id="605c3-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="605c3-111">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="605c3-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="605c3-112">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="605c3-112">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="605c3-113">備註</span><span class="sxs-lookup"><span data-stu-id="605c3-113">Remarks</span></span>

<span data-ttu-id="605c3-114">當授權取得完成時，原則引擎會引發 [MELicenseAcquisitionCompleted](melicenseacquisitioncompleted.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="605c3-114">When license acquisition is completed, the policy engine raises the [MELicenseAcquisitionCompleted](melicenseacquisitioncompleted.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="605c3-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="605c3-115">Requirements</span></span>



| <span data-ttu-id="605c3-116">需求</span><span class="sxs-lookup"><span data-stu-id="605c3-116">Requirement</span></span> | <span data-ttu-id="605c3-117">值</span><span class="sxs-lookup"><span data-stu-id="605c3-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="605c3-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="605c3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="605c3-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="605c3-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="605c3-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="605c3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="605c3-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="605c3-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="605c3-122">標頭</span><span class="sxs-lookup"><span data-stu-id="605c3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="605c3-123"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="605c3-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="605c3-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="605c3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="605c3-125">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="605c3-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




