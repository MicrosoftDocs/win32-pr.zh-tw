---
description: 篩選圖形正在進行終結之前，正在關閉。
ms.assetid: f1b3fc87-16ec-485b-b659-fc7d975c4a22
title: 'EC_SHUTTING_DOWN (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 471b746df3980afd96bbfc122a164ccd30561846
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976040"
---
# <a name="ec_shutting_down"></a><span data-ttu-id="77cd2-103">EC \_ 關機 \_</span><span class="sxs-lookup"><span data-stu-id="77cd2-103">EC\_SHUTTING\_DOWN</span></span>

<span data-ttu-id="77cd2-104">篩選圖形正在進行終結之前，正在關閉。</span><span class="sxs-lookup"><span data-stu-id="77cd2-104">The filter graph is shutting down, prior to being destroyed.</span></span>

## <a name="parameters"></a><span data-ttu-id="77cd2-105">參數</span><span class="sxs-lookup"><span data-stu-id="77cd2-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77cd2-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="77cd2-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="77cd2-107">零個。</span><span class="sxs-lookup"><span data-stu-id="77cd2-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="77cd2-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="77cd2-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="77cd2-109">零個。</span><span class="sxs-lookup"><span data-stu-id="77cd2-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="77cd2-110">預設動作</span><span class="sxs-lookup"><span data-stu-id="77cd2-110">Default Action</span></span>

<span data-ttu-id="77cd2-111">此事件不會傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="77cd2-111">This event is not sent to the application.</span></span> <span data-ttu-id="77cd2-112">篩選圖形管理員會將它傳送至外掛程式散發者，以通知圖形正在關閉。</span><span class="sxs-lookup"><span data-stu-id="77cd2-112">The filter graph manager sends it to plug-in distributors, to notify them that the graph is shutting down.</span></span> <span data-ttu-id="77cd2-113">應用程式無法覆寫此事件的預設動作。</span><span class="sxs-lookup"><span data-stu-id="77cd2-113">Applications cannot override the default action of this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="77cd2-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="77cd2-114">Requirements</span></span>



| <span data-ttu-id="77cd2-115">需求</span><span class="sxs-lookup"><span data-stu-id="77cd2-115">Requirement</span></span> | <span data-ttu-id="77cd2-116">值</span><span class="sxs-lookup"><span data-stu-id="77cd2-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="77cd2-117">標頭</span><span class="sxs-lookup"><span data-stu-id="77cd2-117">Header</span></span><br/> | <dl> <span data-ttu-id="77cd2-118"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="77cd2-118"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77cd2-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="77cd2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77cd2-120">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="77cd2-120">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="77cd2-121">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="77cd2-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




