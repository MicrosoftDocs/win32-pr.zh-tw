---
description: 當目前的影片標題設定 (VTS) 變更時傳送。
ms.assetid: 7b8849c8-c71e-44d6-b33a-8e80247bdb22
title: 'EC_DVD_TITLE_SET_CHANGE (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_TITLE_SET_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c5685cfb909a7fa24c39dff969076269845a663e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993294"
---
# <a name="ec_dvd_title_set_change"></a><span data-ttu-id="3cc47-103">EC \_ DVD \_ 標題 \_ 設定 \_ 變更</span><span class="sxs-lookup"><span data-stu-id="3cc47-103">EC\_DVD\_TITLE\_SET\_CHANGE</span></span>

<span data-ttu-id="3cc47-104">當目前的影片標題設定 (VTS) 變更時傳送。</span><span class="sxs-lookup"><span data-stu-id="3cc47-104">Sent when current Video Title Set (VTS) changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="3cc47-105">參數</span><span class="sxs-lookup"><span data-stu-id="3cc47-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cc47-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="3cc47-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="3cc47-107">新的影片標題集號碼 (VTSN) 。</span><span class="sxs-lookup"><span data-stu-id="3cc47-107">The new Video Title Set Number (VTSN).</span></span>

</dd> <dt>

<span data-ttu-id="3cc47-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="3cc47-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="3cc47-109">零個。</span><span class="sxs-lookup"><span data-stu-id="3cc47-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3cc47-110">備註</span><span class="sxs-lookup"><span data-stu-id="3cc47-110">Remarks</span></span>

<span data-ttu-id="3cc47-111">此事件預設為停用。</span><span class="sxs-lookup"><span data-stu-id="3cc47-111">This event is disabled by default.</span></span> <span data-ttu-id="3cc47-112">若要啟用此事件，請呼叫 [**IDvdControl2：： SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) ，並將 **DVD \_ NotifyPositionChange** 選項設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="3cc47-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_NotifyPositionChange** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cc47-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="3cc47-113">Requirements</span></span>



| <span data-ttu-id="3cc47-114">需求</span><span class="sxs-lookup"><span data-stu-id="3cc47-114">Requirement</span></span> | <span data-ttu-id="3cc47-115">值</span><span class="sxs-lookup"><span data-stu-id="3cc47-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cc47-116">標頭</span><span class="sxs-lookup"><span data-stu-id="3cc47-116">Header</span></span><br/> | <dl> <span data-ttu-id="3cc47-117"><dt>Dvdevcode (包含 Dshow) </dt></span><span class="sxs-lookup"><span data-stu-id="3cc47-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cc47-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3cc47-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cc47-119">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="3cc47-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="3cc47-120">DVD 事件通知碼</span><span class="sxs-lookup"><span data-stu-id="3cc47-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="3cc47-121">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="3cc47-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




