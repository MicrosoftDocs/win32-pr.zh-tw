---
description: 表示可用的角度數目變更或目前的角度數位已變更。
ms.assetid: 0564b0e3-6434-448b-80fb-5362ab67fef7
title: 'EC_DVD_ANGLE_CHANGE (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_ANGLE_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 08914e3fcb93d38ccad25053f7c33480e900ad93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999447"
---
# <a name="ec_dvd_angle_change"></a><span data-ttu-id="f467c-103">EC \_ DVD \_ 角度 \_ 變更</span><span class="sxs-lookup"><span data-stu-id="f467c-103">EC\_DVD\_ANGLE\_CHANGE</span></span>

<span data-ttu-id="f467c-104">表示可用的角度數目變更或目前的角度數位已變更。</span><span class="sxs-lookup"><span data-stu-id="f467c-104">Signals that either the number of available angles changed or that the current angle number changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="f467c-105">參數</span><span class="sxs-lookup"><span data-stu-id="f467c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f467c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="f467c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="f467c-107">**DWORD** 值，表示可用角度的數目。</span><span class="sxs-lookup"><span data-stu-id="f467c-107">**DWORD** value indicating the number of available angles.</span></span> <span data-ttu-id="f467c-108">當可用角度的數目為1時，不會 multiangle 目前的影片。</span><span class="sxs-lookup"><span data-stu-id="f467c-108">When the number of available angles is 1, the current video is not multiangle.</span></span>

</dd> <dt>

<span data-ttu-id="f467c-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="f467c-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="f467c-110">**DWORD** 值，指出目前的角度數位。</span><span class="sxs-lookup"><span data-stu-id="f467c-110">**DWORD** value indicating the current angle number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f467c-111">備註</span><span class="sxs-lookup"><span data-stu-id="f467c-111">Remarks</span></span>

<span data-ttu-id="f467c-112">角度數位的範圍是從1到9。</span><span class="sxs-lookup"><span data-stu-id="f467c-112">Angle numbers range from 1 to 9.</span></span>

<span data-ttu-id="f467c-113">目前的角度數位可以使用在光碟上撰寫的流覽命令，以及透過使用 [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) 介面的應用程式控制，自動變更。</span><span class="sxs-lookup"><span data-stu-id="f467c-113">The current angle number can change automatically with a navigation command authored on the disc as well as through application control by using the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) interface.</span></span>

<span data-ttu-id="f467c-114">此事件會在所有網域中引發。</span><span class="sxs-lookup"><span data-stu-id="f467c-114">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="f467c-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="f467c-115">Requirements</span></span>



| <span data-ttu-id="f467c-116">需求</span><span class="sxs-lookup"><span data-stu-id="f467c-116">Requirement</span></span> | <span data-ttu-id="f467c-117">值</span><span class="sxs-lookup"><span data-stu-id="f467c-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f467c-118">標頭</span><span class="sxs-lookup"><span data-stu-id="f467c-118">Header</span></span><br/> | <dl> <span data-ttu-id="f467c-119"><dt>Dvdevcode (包含 Dshow) </dt></span><span class="sxs-lookup"><span data-stu-id="f467c-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f467c-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f467c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f467c-121">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="f467c-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="f467c-122">DVD 事件通知碼</span><span class="sxs-lookup"><span data-stu-id="f467c-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="f467c-123">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="f467c-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




