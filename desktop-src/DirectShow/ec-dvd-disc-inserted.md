---
description: 發出將 DVD 光碟插入磁片磁碟機的信號。
ms.assetid: ce233c94-2eae-457c-919b-7c4d8334979a
title: 'EC_DVD_DISC_INSERTED (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_DISC_INSERTED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c98d32960e2ab6a21633899164b3ff84525f2aaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990053"
---
# <a name="ec_dvd_disc_inserted"></a><span data-ttu-id="2358e-103">插入的 EC \_ DVD \_ 光碟 \_</span><span class="sxs-lookup"><span data-stu-id="2358e-103">EC\_DVD\_DISC\_INSERTED</span></span>

<span data-ttu-id="2358e-104">發出將 DVD 光碟插入磁片磁碟機的信號。</span><span class="sxs-lookup"><span data-stu-id="2358e-104">Signals that a DVD disc was inserted into the drive.</span></span>

## <a name="parameters"></a><span data-ttu-id="2358e-105">參數</span><span class="sxs-lookup"><span data-stu-id="2358e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2358e-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="2358e-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="2358e-107">零個。</span><span class="sxs-lookup"><span data-stu-id="2358e-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="2358e-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="2358e-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="2358e-109">零個。</span><span class="sxs-lookup"><span data-stu-id="2358e-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2358e-110">備註</span><span class="sxs-lookup"><span data-stu-id="2358e-110">Remarks</span></span>

<span data-ttu-id="2358e-111">插入光碟時，會自動開始播放。</span><span class="sxs-lookup"><span data-stu-id="2358e-111">Playback automatically begins when a disc is inserted.</span></span> <span data-ttu-id="2358e-112">應用程式不需要採取任何特殊動作來回應此事件。</span><span class="sxs-lookup"><span data-stu-id="2358e-112">The application does not have to take any special action in response to this event.</span></span>

<span data-ttu-id="2358e-113">此事件會在所有網域中引發。</span><span class="sxs-lookup"><span data-stu-id="2358e-113">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="2358e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="2358e-114">Requirements</span></span>



| <span data-ttu-id="2358e-115">需求</span><span class="sxs-lookup"><span data-stu-id="2358e-115">Requirement</span></span> | <span data-ttu-id="2358e-116">值</span><span class="sxs-lookup"><span data-stu-id="2358e-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2358e-117">標頭</span><span class="sxs-lookup"><span data-stu-id="2358e-117">Header</span></span><br/> | <dl> <span data-ttu-id="2358e-118"><dt>Dvdevcode (包含 Dshow) </dt></span><span class="sxs-lookup"><span data-stu-id="2358e-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2358e-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2358e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2358e-120">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="2358e-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="2358e-121">DVD 事件通知碼</span><span class="sxs-lookup"><span data-stu-id="2358e-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="2358e-122">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="2358e-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




