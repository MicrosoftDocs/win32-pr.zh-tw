---
description: 篩選未收到足夠的資料。
ms.assetid: c9cdfe46-02bb-4ea9-ac58-7d63e03c26d8
title: 'EC_STAR加值稅ION (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 988d550b93ecb9a3c2f78f2d07f50a3965be945d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998697"
---
# <a name="ec_starvation"></a><span data-ttu-id="0cd1b-103">EC \_ 耗盡</span><span class="sxs-lookup"><span data-stu-id="0cd1b-103">EC\_STARVATION</span></span>

<span data-ttu-id="0cd1b-104">篩選未收到足夠的資料。</span><span class="sxs-lookup"><span data-stu-id="0cd1b-104">A filter is not receiving enough data.</span></span>

## <a name="parameters"></a><span data-ttu-id="0cd1b-105">參數</span><span class="sxs-lookup"><span data-stu-id="0cd1b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cd1b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="0cd1b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="0cd1b-107">零個。</span><span class="sxs-lookup"><span data-stu-id="0cd1b-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="0cd1b-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="0cd1b-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="0cd1b-109">零個。</span><span class="sxs-lookup"><span data-stu-id="0cd1b-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="0cd1b-110">預設動作</span><span class="sxs-lookup"><span data-stu-id="0cd1b-110">Default Action</span></span>

<span data-ttu-id="0cd1b-111">此事件不會傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="0cd1b-111">The event is not sent to the application.</span></span> <span data-ttu-id="0cd1b-112">如果篩選圖形正在執行，則篩選圖形管理員會暫停圖形，並等候暫停完成。</span><span class="sxs-lookup"><span data-stu-id="0cd1b-112">If the filter graph is running, the filter graph manager pauses the graph and waits for the pause to complete.</span></span> <span data-ttu-id="0cd1b-113">然後，它會再次執行圖形。</span><span class="sxs-lookup"><span data-stu-id="0cd1b-113">Then it runs the graph again.</span></span> <span data-ttu-id="0cd1b-114">傳送事件的篩選不應完成其轉換為暫停，直到它有足夠的資料可繼續為止。</span><span class="sxs-lookup"><span data-stu-id="0cd1b-114">The filter sending the event should not complete its transition to paused until it has enough data to resume.</span></span> <span data-ttu-id="0cd1b-115">如果篩選圖形未執行，則篩選圖形管理員會忽略此事件。</span><span class="sxs-lookup"><span data-stu-id="0cd1b-115">If the filter graph is not running, the filter graph manager ignores this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cd1b-116">備註</span><span class="sxs-lookup"><span data-stu-id="0cd1b-116">Remarks</span></span>

<span data-ttu-id="0cd1b-117">如果資料太少，剖析器或來源篩選器可以傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="0cd1b-117">A parser or source filter can send this event if too little data is arriving.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cd1b-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="0cd1b-118">Requirements</span></span>



| <span data-ttu-id="0cd1b-119">需求</span><span class="sxs-lookup"><span data-stu-id="0cd1b-119">Requirement</span></span> | <span data-ttu-id="0cd1b-120">值</span><span class="sxs-lookup"><span data-stu-id="0cd1b-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0cd1b-121">標頭</span><span class="sxs-lookup"><span data-stu-id="0cd1b-121">Header</span></span><br/> | <dl> <span data-ttu-id="0cd1b-122"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="0cd1b-122"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cd1b-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0cd1b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cd1b-124">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="0cd1b-124">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="0cd1b-125">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="0cd1b-125">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




