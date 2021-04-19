---
description: 時鐘提供者已中斷連線。
ms.assetid: 0a885b7a-840d-4112-85f7-ff6f2d87bb75
title: 'EC_CLOCK_UNSET (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85ead35d89eee94bbffb38a96f658ccb2bb6e6e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994718"
---
# <a name="ec_clock_unset"></a><span data-ttu-id="014f5-103">EC \_ 時鐘未設定 \_</span><span class="sxs-lookup"><span data-stu-id="014f5-103">EC\_CLOCK\_UNSET</span></span>

<span data-ttu-id="014f5-104">時鐘提供者已中斷連線。</span><span class="sxs-lookup"><span data-stu-id="014f5-104">The clock provider was disconnected.</span></span>

## <a name="parameters"></a><span data-ttu-id="014f5-105">參數</span><span class="sxs-lookup"><span data-stu-id="014f5-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="014f5-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="014f5-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="014f5-107">零個。</span><span class="sxs-lookup"><span data-stu-id="014f5-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="014f5-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="014f5-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="014f5-109">零個。</span><span class="sxs-lookup"><span data-stu-id="014f5-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="014f5-110">預設動作</span><span class="sxs-lookup"><span data-stu-id="014f5-110">Default Action</span></span>

<span data-ttu-id="014f5-111">篩選圖形管理員會在下一個 pause 或 run 命令上選擇新的參考時鐘。</span><span class="sxs-lookup"><span data-stu-id="014f5-111">The Filter Graph Manager chooses a new reference clock on the next pause or run command.</span></span> <span data-ttu-id="014f5-112">它也會將事件轉送到應用程式。</span><span class="sxs-lookup"><span data-stu-id="014f5-112">It also forwards the event to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="014f5-113">備註</span><span class="sxs-lookup"><span data-stu-id="014f5-113">Remarks</span></span>

<span data-ttu-id="014f5-114">當時鐘提供的篩選器的 pin 已中斷連線時，KSProxy 會通知此事件。</span><span class="sxs-lookup"><span data-stu-id="014f5-114">KSProxy signals this event when the pin of a clock-providing filter is disconnected.</span></span>

## <a name="requirements"></a><span data-ttu-id="014f5-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="014f5-115">Requirements</span></span>



| <span data-ttu-id="014f5-116">需求</span><span class="sxs-lookup"><span data-stu-id="014f5-116">Requirement</span></span> | <span data-ttu-id="014f5-117">值</span><span class="sxs-lookup"><span data-stu-id="014f5-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="014f5-118">標頭</span><span class="sxs-lookup"><span data-stu-id="014f5-118">Header</span></span><br/> | <dl> <span data-ttu-id="014f5-119"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="014f5-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="014f5-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="014f5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="014f5-121">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="014f5-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="014f5-122">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="014f5-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




