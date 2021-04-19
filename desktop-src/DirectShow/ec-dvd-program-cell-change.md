---
description: 當 DVD 程式號碼或儲存格編號變更時傳送。
ms.assetid: a500e86d-cd42-4716-9c57-828a72c4e1df
title: 'EC_DVD_PROGRAM_CELL_CHANGE (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PROGRAM_CELL_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: d41f691016c3e41cfc3e14ed1ce6fff276dcc70e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989725"
---
# <a name="ec_dvd_program_cell_change"></a><span data-ttu-id="a760b-103">EC \_ DVD \_ 程式 \_ 儲存格 \_ 變更</span><span class="sxs-lookup"><span data-stu-id="a760b-103">EC\_DVD\_PROGRAM\_CELL\_CHANGE</span></span>

<span data-ttu-id="a760b-104">當 DVD 程式號碼或儲存格編號變更時傳送。</span><span class="sxs-lookup"><span data-stu-id="a760b-104">Sent when the DVD program number or cell number changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="a760b-105">參數</span><span class="sxs-lookup"><span data-stu-id="a760b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a760b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="a760b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="a760b-107">新的程式編號。</span><span class="sxs-lookup"><span data-stu-id="a760b-107">The new program number.</span></span>

</dd> <dt>

<span data-ttu-id="a760b-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="a760b-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="a760b-109">新的儲存格編號。</span><span class="sxs-lookup"><span data-stu-id="a760b-109">The new cell number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a760b-110">備註</span><span class="sxs-lookup"><span data-stu-id="a760b-110">Remarks</span></span>

<span data-ttu-id="a760b-111">此事件預設為停用。</span><span class="sxs-lookup"><span data-stu-id="a760b-111">This event is disabled by default.</span></span> <span data-ttu-id="a760b-112">若要啟用此事件，請呼叫 [**IDvdControl2：： SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) ，並將 **DVD \_ NotifyPositionChange** 選項設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="a760b-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_NotifyPositionChange** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a760b-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="a760b-113">Requirements</span></span>



| <span data-ttu-id="a760b-114">需求</span><span class="sxs-lookup"><span data-stu-id="a760b-114">Requirement</span></span> | <span data-ttu-id="a760b-115">值</span><span class="sxs-lookup"><span data-stu-id="a760b-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a760b-116">標頭</span><span class="sxs-lookup"><span data-stu-id="a760b-116">Header</span></span><br/> | <dl> <span data-ttu-id="a760b-117"><dt>Dvdevcode (包含 Dshow) </dt></span><span class="sxs-lookup"><span data-stu-id="a760b-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a760b-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a760b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a760b-119">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="a760b-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="a760b-120">DVD 事件通知碼</span><span class="sxs-lookup"><span data-stu-id="a760b-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="a760b-121">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="a760b-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




