---
description: 當一般參數的值註冊 (GPRM) 變更時傳送。
ms.assetid: 3e0c400e-9ea5-458c-9eca-97d66a440590
title: 'EC_DVD_GPRM_Change (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_GPRM_Change
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: f67a8646a72689c2570462f7dc4aeee6b2474136
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998730"
---
# <a name="ec_dvd_gprm_change"></a><span data-ttu-id="7b362-103">EC \_ DVD \_ GPRM \_ 變更</span><span class="sxs-lookup"><span data-stu-id="7b362-103">EC\_DVD\_GPRM\_Change</span></span>

<span data-ttu-id="7b362-104">當一般參數的值註冊 (GPRM) 變更時傳送。</span><span class="sxs-lookup"><span data-stu-id="7b362-104">Sent when the value of a general parameter register (GPRM) changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="7b362-105">參數</span><span class="sxs-lookup"><span data-stu-id="7b362-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b362-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="7b362-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="7b362-107">已變更之 GPRM 值的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="7b362-107">The zero-based index of the GPRM value that changed.</span></span>

</dd> <dt>

<span data-ttu-id="7b362-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="7b362-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="7b362-109">較低的16個位包含新的 GPRM 值。</span><span class="sxs-lookup"><span data-stu-id="7b362-109">The lower 16 bits contains the new GPRM value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7b362-110">備註</span><span class="sxs-lookup"><span data-stu-id="7b362-110">Remarks</span></span>

<span data-ttu-id="7b362-111">此事件預設為停用。</span><span class="sxs-lookup"><span data-stu-id="7b362-111">This event is disabled by default.</span></span> <span data-ttu-id="7b362-112">若要啟用此事件，請呼叫 [**IDvdControl2：： SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) ，並將 **DVD \_ EnableLoggingEvents** 選項設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="7b362-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b362-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b362-113">Requirements</span></span>



| <span data-ttu-id="7b362-114">需求</span><span class="sxs-lookup"><span data-stu-id="7b362-114">Requirement</span></span> | <span data-ttu-id="7b362-115">值</span><span class="sxs-lookup"><span data-stu-id="7b362-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b362-116">標頭</span><span class="sxs-lookup"><span data-stu-id="7b362-116">Header</span></span><br/> | <dl> <span data-ttu-id="7b362-117"><dt>Dvdevcode (包含 Dshow) </dt></span><span class="sxs-lookup"><span data-stu-id="7b362-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b362-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7b362-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b362-119">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="7b362-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="7b362-120">DVD 事件通知碼</span><span class="sxs-lookup"><span data-stu-id="7b362-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="7b362-121">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="7b362-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="7b362-122">**IDvdInfo2::GetAllGPRMs**</span><span class="sxs-lookup"><span data-stu-id="7b362-122">**IDvdInfo2::GetAllGPRMs**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallgprms)
</dt> </dl>

 

 




