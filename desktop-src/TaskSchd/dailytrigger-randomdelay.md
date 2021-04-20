---
title: DailyTrigger. RandomDelay 屬性
description: 針對腳本，取得或設定隨機加入至觸發程式開始時間的延遲時間。 |DailyTrigger. RandomDelay 屬性
ms.assetid: 0494a963-bdaf-4f3f-a2e3-9482409ecda4
keywords:
- RandomDelay 屬性工作排程器
- RandomDelay 屬性工作排程器，DailyTrigger 物件
- DailyTrigger 物件工作排程器、RandomDelay 屬性
topic_type:
- apiref
api_name:
- DailyTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303192d578a2681e250784c1e1eb2831c98482cc
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734103"
---
# <a name="dailytriggerrandomdelay-property"></a><span data-ttu-id="b8e80-107">DailyTrigger. RandomDelay 屬性</span><span class="sxs-lookup"><span data-stu-id="b8e80-107">DailyTrigger.RandomDelay property</span></span>

<span data-ttu-id="b8e80-108">針對腳本，取得或設定隨機加入至觸發程式開始時間的延遲時間。</span><span class="sxs-lookup"><span data-stu-id="b8e80-108">For scripting, gets or sets a delay time that is randomly added to the start time of the trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8e80-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8e80-109">Syntax</span></span>


```VB
DailyTrigger.RandomDelay As String
```



## <a name="property-value"></a><span data-ttu-id="b8e80-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="b8e80-110">Property value</span></span>

<span data-ttu-id="b8e80-111">隨機新增至觸發程式開始時間的延遲時間。</span><span class="sxs-lookup"><span data-stu-id="b8e80-111">The delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="b8e80-112">此字串的格式為 `P<days>DT<hours>H<minutes>M<seconds>S` (例如，P2DT5S 是2天、5秒的延遲) 。</span><span class="sxs-lookup"><span data-stu-id="b8e80-112">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, P2DT5S is a 2 day, 5 second delay).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8e80-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8e80-113">Requirements</span></span>



| <span data-ttu-id="b8e80-114">需求</span><span class="sxs-lookup"><span data-stu-id="b8e80-114">Requirement</span></span> | <span data-ttu-id="b8e80-115">值</span><span class="sxs-lookup"><span data-stu-id="b8e80-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8e80-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b8e80-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b8e80-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8e80-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b8e80-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b8e80-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b8e80-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8e80-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b8e80-120">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="b8e80-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="b8e80-121"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b8e80-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b8e80-122">DLL</span><span class="sxs-lookup"><span data-stu-id="b8e80-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8e80-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8e80-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8e80-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8e80-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8e80-125">**DailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="b8e80-125">**DailyTrigger**</span></span>](dailytrigger.md)
</dt> <dt>

[<span data-ttu-id="b8e80-126">工作排程器</span><span class="sxs-lookup"><span data-stu-id="b8e80-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





