---
title: MonthlyDOWTrigger. RandomDelay 屬性
description: 針對腳本，取得或設定隨機加入至觸發程式開始時間的延遲時間。 |MonthlyDOWTrigger. RandomDelay 屬性
ms.assetid: e5cb6c1d-8003-43f4-bf35-da490a6097f0
keywords:
- RandomDelay 屬性工作排程器
- RandomDelay 屬性工作排程器，MonthlyDOWTrigger 物件
- MonthlyDOWTrigger 物件工作排程器、RandomDelay 屬性
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e781941e927547a4ea25935fb21299777c34b3ea
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734123"
---
# <a name="monthlydowtriggerrandomdelay-property"></a><span data-ttu-id="42829-107">MonthlyDOWTrigger. RandomDelay 屬性</span><span class="sxs-lookup"><span data-stu-id="42829-107">MonthlyDOWTrigger.RandomDelay property</span></span>

<span data-ttu-id="42829-108">針對腳本，取得或設定隨機加入至觸發程式開始時間的延遲時間。</span><span class="sxs-lookup"><span data-stu-id="42829-108">For scripting, gets or sets a delay time that is randomly added to the start time of the trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="42829-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="42829-109">Syntax</span></span>


```VB
MonthlyDOWTrigger.RandomDelay As String
```



## <a name="property-value"></a><span data-ttu-id="42829-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="42829-110">Property value</span></span>

<span data-ttu-id="42829-111">隨機新增至觸發程式開始時間的延遲時間。</span><span class="sxs-lookup"><span data-stu-id="42829-111">The delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="42829-112">此字串的格式為 `P<days>DT<hours>H<minutes>M<seconds>S` (例如，P2DT5S 是2天、5秒的延遲) 。</span><span class="sxs-lookup"><span data-stu-id="42829-112">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, P2DT5S is a 2 day, 5 second delay).</span></span>

## <a name="requirements"></a><span data-ttu-id="42829-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="42829-113">Requirements</span></span>



| <span data-ttu-id="42829-114">需求</span><span class="sxs-lookup"><span data-stu-id="42829-114">Requirement</span></span> | <span data-ttu-id="42829-115">值</span><span class="sxs-lookup"><span data-stu-id="42829-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="42829-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="42829-116">Minimum supported client</span></span><br/> | <span data-ttu-id="42829-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42829-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="42829-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="42829-118">Minimum supported server</span></span><br/> | <span data-ttu-id="42829-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42829-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="42829-120">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="42829-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="42829-121"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="42829-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="42829-122">DLL</span><span class="sxs-lookup"><span data-stu-id="42829-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42829-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42829-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42829-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42829-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42829-125">工作排程器</span><span class="sxs-lookup"><span data-stu-id="42829-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="42829-126">**MonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="42829-126">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
</dt> </dl>

 

 





