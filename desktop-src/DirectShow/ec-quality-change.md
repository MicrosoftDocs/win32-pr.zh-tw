---
description: 圖形正在卸載範例，以提供品質控制。
ms.assetid: a21fe766-58a5-4851-a282-883374287e18
title: 'EC_QUALITY_CHANGE (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5752db30c8ad6ed85655948cf2adb9ef7ac8078
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982260"
---
# <a name="ec_quality_change"></a><span data-ttu-id="e2dd1-103">EC \_ 品質 \_ 變更</span><span class="sxs-lookup"><span data-stu-id="e2dd1-103">EC\_QUALITY\_CHANGE</span></span>

<span data-ttu-id="e2dd1-104">圖形正在卸載範例，以提供品質控制。</span><span class="sxs-lookup"><span data-stu-id="e2dd1-104">The graph is dropping samples, for quality control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e2dd1-105">參數</span><span class="sxs-lookup"><span data-stu-id="e2dd1-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2dd1-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="e2dd1-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="e2dd1-107">零個。</span><span class="sxs-lookup"><span data-stu-id="e2dd1-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="e2dd1-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="e2dd1-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="e2dd1-109">零個。</span><span class="sxs-lookup"><span data-stu-id="e2dd1-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="e2dd1-110">預設動作</span><span class="sxs-lookup"><span data-stu-id="e2dd1-110">Default Action</span></span>

<span data-ttu-id="e2dd1-111">無。</span><span class="sxs-lookup"><span data-stu-id="e2dd1-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2dd1-112">備註</span><span class="sxs-lookup"><span data-stu-id="e2dd1-112">Remarks</span></span>

<span data-ttu-id="e2dd1-113">如果篩選器卸載範例以回應品質控制訊息，則會傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="e2dd1-113">A filter sends this event if it drops samples in response to a quality control message.</span></span> <span data-ttu-id="e2dd1-114">它只會在調整品質層級時傳送事件，而不是針對它所卸載的每個樣本。</span><span class="sxs-lookup"><span data-stu-id="e2dd1-114">It sends the event only when it adjusts the quality level, not for each sample that it drops.</span></span> <span data-ttu-id="e2dd1-115">如需詳細資訊，請參閱 [品質控制管理](quality-control-management.md)。</span><span class="sxs-lookup"><span data-stu-id="e2dd1-115">For more information, see [Quality-Control Management](quality-control-management.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2dd1-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2dd1-116">Requirements</span></span>



| <span data-ttu-id="e2dd1-117">需求</span><span class="sxs-lookup"><span data-stu-id="e2dd1-117">Requirement</span></span> | <span data-ttu-id="e2dd1-118">值</span><span class="sxs-lookup"><span data-stu-id="e2dd1-118">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e2dd1-119">標頭</span><span class="sxs-lookup"><span data-stu-id="e2dd1-119">Header</span></span><br/> | <dl> <span data-ttu-id="e2dd1-120"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="e2dd1-120"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2dd1-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2dd1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2dd1-122">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="e2dd1-122">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="e2dd1-123">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="e2dd1-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




