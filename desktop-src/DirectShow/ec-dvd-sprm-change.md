---
description: 當系統參數的值註冊 (SPRM) 變更時傳送。
ms.assetid: 266b6de1-740d-4b3d-8487-5a9570d6c852
title: 'EC_DVD_SPRM_Change (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_SPRM_Change
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 1af5b8637a197973bca2129a8b8a0198d20248eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994203"
---
# <a name="ec_dvd_sprm_change"></a><span data-ttu-id="485a7-103">EC \_ DVD \_ SPRM \_ 變更</span><span class="sxs-lookup"><span data-stu-id="485a7-103">EC\_DVD\_SPRM\_Change</span></span>

<span data-ttu-id="485a7-104">當系統參數的值註冊 (SPRM) 變更時傳送。</span><span class="sxs-lookup"><span data-stu-id="485a7-104">Sent when the value of a system parameter register (SPRM) changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="485a7-105">參數</span><span class="sxs-lookup"><span data-stu-id="485a7-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="485a7-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="485a7-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="485a7-107">已變更之 SPRM 值的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="485a7-107">The zero-based index of the SPRM value that changed.</span></span>

</dd> <dt>

<span data-ttu-id="485a7-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="485a7-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="485a7-109">較低的16個位包含新的 SPRM 值。</span><span class="sxs-lookup"><span data-stu-id="485a7-109">The lower 16 bits contains the new SPRM value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="485a7-110">備註</span><span class="sxs-lookup"><span data-stu-id="485a7-110">Remarks</span></span>

<span data-ttu-id="485a7-111">此事件預設為停用。</span><span class="sxs-lookup"><span data-stu-id="485a7-111">This event is disabled by default.</span></span> <span data-ttu-id="485a7-112">若要啟用此事件，請呼叫 [**IDvdControl2：： SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) ，並將 **DVD \_ EnableLoggingEvents** 選項設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="485a7-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="485a7-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="485a7-113">Requirements</span></span>



| <span data-ttu-id="485a7-114">需求</span><span class="sxs-lookup"><span data-stu-id="485a7-114">Requirement</span></span> | <span data-ttu-id="485a7-115">值</span><span class="sxs-lookup"><span data-stu-id="485a7-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="485a7-116">標頭</span><span class="sxs-lookup"><span data-stu-id="485a7-116">Header</span></span><br/> | <dl> <span data-ttu-id="485a7-117"><dt>Dvdevcode (包含 Dshow) </dt></span><span class="sxs-lookup"><span data-stu-id="485a7-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="485a7-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="485a7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="485a7-119">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="485a7-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="485a7-120">DVD 事件通知碼</span><span class="sxs-lookup"><span data-stu-id="485a7-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="485a7-121">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="485a7-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="485a7-122">**IDvdInfo2::GetAllSPRMs**</span><span class="sxs-lookup"><span data-stu-id="485a7-122">**IDvdInfo2::GetAllSPRMs**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallsprms)
</dt> </dl>

 

 




