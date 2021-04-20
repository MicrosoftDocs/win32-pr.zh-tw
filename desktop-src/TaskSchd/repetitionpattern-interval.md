---
title: RepetitionPattern. Interval 屬性
description: 針對腳本，取得或設定每次重新開機工作之間的時間量。
ms.assetid: c48bd304-21f3-435e-99f5-3b2da0078bb8
keywords:
- Interval 屬性工作排程器
- Interval 屬性工作排程器，RepetitionPattern 物件
- RepetitionPattern 物件工作排程器，Interval 屬性
topic_type:
- apiref
api_name:
- RepetitionPattern.Interval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1e81920fffe5c9fd58dd36a028b924f54ebe6dd
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734173"
---
# <a name="repetitionpatterninterval-property"></a><span data-ttu-id="88050-106">RepetitionPattern. Interval 屬性</span><span class="sxs-lookup"><span data-stu-id="88050-106">RepetitionPattern.Interval property</span></span>

<span data-ttu-id="88050-107">針對腳本，取得或設定每次重新開機工作之間的時間量。</span><span class="sxs-lookup"><span data-stu-id="88050-107">For scripting, gets or sets the amount of time between each restart of the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="88050-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="88050-108">Syntax</span></span>


```VB
RepetitionPattern.Interval As String
```



## <a name="property-value"></a><span data-ttu-id="88050-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="88050-109">Property value</span></span>

<span data-ttu-id="88050-110">每次重新開機工作之間的時間量。</span><span class="sxs-lookup"><span data-stu-id="88050-110">The amount of time between each restart of the task.</span></span> <span data-ttu-id="88050-111">此字串的格式為 `P<days>DT<hours>H<minutes>M<seconds>S` (例如，"PT5M" 為5分鐘、"PT1H" 為1小時，而 "PT20M" 為20分鐘) 。</span><span class="sxs-lookup"><span data-stu-id="88050-111">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="88050-112">允許的時間上限為31天，而允許的最短時間為1分鐘。</span><span class="sxs-lookup"><span data-stu-id="88050-112">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

## <a name="remarks"></a><span data-ttu-id="88050-113">備註</span><span class="sxs-lookup"><span data-stu-id="88050-113">Remarks</span></span>

<span data-ttu-id="88050-114">如果您指定工作的重複持續時間，您也必須指定重複間隔。</span><span class="sxs-lookup"><span data-stu-id="88050-114">If you specify a repetition duration for a task, you must also specify the repetition interval.</span></span>

<span data-ttu-id="88050-115">讀取或寫入工作的 XML 時，會在工作排程器架構的 [**interval**](taskschedulerschema-interval-repetitiontype-element.md) 元素中指定重複間隔。</span><span class="sxs-lookup"><span data-stu-id="88050-115">When reading or writing XML for a task, the repetition interval is specified in the [**Interval**](taskschedulerschema-interval-repetitiontype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="88050-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="88050-116">Requirements</span></span>



| <span data-ttu-id="88050-117">需求</span><span class="sxs-lookup"><span data-stu-id="88050-117">Requirement</span></span> | <span data-ttu-id="88050-118">值</span><span class="sxs-lookup"><span data-stu-id="88050-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88050-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="88050-119">Minimum supported client</span></span><br/> | <span data-ttu-id="88050-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="88050-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="88050-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="88050-121">Minimum supported server</span></span><br/> | <span data-ttu-id="88050-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="88050-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="88050-123">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="88050-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="88050-124"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="88050-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="88050-125">DLL</span><span class="sxs-lookup"><span data-stu-id="88050-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88050-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88050-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88050-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="88050-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88050-128">工作排程器</span><span class="sxs-lookup"><span data-stu-id="88050-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





