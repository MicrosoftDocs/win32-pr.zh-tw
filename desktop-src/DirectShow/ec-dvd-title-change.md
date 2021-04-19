---
description: 指出目前的 DVD 標題編號何時變更。
ms.assetid: 9888f2ec-fc2d-4d6d-a03d-b381373337eb
title: 'EC_DVD_TITLE_CHANGE (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_TITLE_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 9539d29704797b1c7b001d426250762d2ed27b3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981108"
---
# <a name="ec_dvd_title_change"></a><span data-ttu-id="63aaf-103">EC \_ DVD \_ 標題 \_ 變更</span><span class="sxs-lookup"><span data-stu-id="63aaf-103">EC\_DVD\_TITLE\_CHANGE</span></span>

<span data-ttu-id="63aaf-104">指出目前的 DVD 標題編號何時變更。</span><span class="sxs-lookup"><span data-stu-id="63aaf-104">Indicates when the current DVD title number changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="63aaf-105">參數</span><span class="sxs-lookup"><span data-stu-id="63aaf-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63aaf-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="63aaf-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="63aaf-107">表示新標題編號的 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="63aaf-107">**DWORD** value indicating the new title number.</span></span>

</dd> <dt>

<span data-ttu-id="63aaf-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="63aaf-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="63aaf-109">零個。</span><span class="sxs-lookup"><span data-stu-id="63aaf-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="63aaf-110">備註</span><span class="sxs-lookup"><span data-stu-id="63aaf-110">Remarks</span></span>

<span data-ttu-id="63aaf-111">標題編號的範圍為1到99。</span><span class="sxs-lookup"><span data-stu-id="63aaf-111">Title numbers range from 1 to 99.</span></span> <span data-ttu-id="63aaf-112">此數位表示 TTN，也就是與整個光碟相關的標題編號，而不是 VTS TTN，也就 \_ 是相對於目前 VTS 的標題編號。</span><span class="sxs-lookup"><span data-stu-id="63aaf-112">This number indicates the TTN, which is the title number with respect to the whole disc, not the VTS\_TTN which is the title number with respect to just a current VTS.</span></span>

<span data-ttu-id="63aaf-113">此事件會在標題網域中引發。</span><span class="sxs-lookup"><span data-stu-id="63aaf-113">This event is raised in the title domain.</span></span>

## <a name="requirements"></a><span data-ttu-id="63aaf-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="63aaf-114">Requirements</span></span>



| <span data-ttu-id="63aaf-115">需求</span><span class="sxs-lookup"><span data-stu-id="63aaf-115">Requirement</span></span> | <span data-ttu-id="63aaf-116">值</span><span class="sxs-lookup"><span data-stu-id="63aaf-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63aaf-117">標頭</span><span class="sxs-lookup"><span data-stu-id="63aaf-117">Header</span></span><br/> | <dl> <span data-ttu-id="63aaf-118"><dt>Dvdevcode (包含 Dshow) </dt></span><span class="sxs-lookup"><span data-stu-id="63aaf-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63aaf-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="63aaf-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63aaf-120">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="63aaf-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="63aaf-121">DVD 事件通知碼</span><span class="sxs-lookup"><span data-stu-id="63aaf-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="63aaf-122">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="63aaf-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




