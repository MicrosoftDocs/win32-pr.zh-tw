---
title: EventTrigger Delay 屬性
description: 針對腳本，取得或設定值，這個值表示事件發生時間和工作啟動時間之間的時間量。
ms.assetid: 6f8b5e25-ad53-466e-adab-fe3c968e941b
keywords:
- Delay 屬性工作排程器
- Delay 屬性工作排程器，EventTrigger 物件
- EventTrigger 物件工作排程器，Delay 屬性
topic_type:
- apiref
api_name:
- EventTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcb67ca7ef12ca023bcb6c0d9d83880d4abb94af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969593"
---
# <a name="eventtriggerdelay-property"></a><span data-ttu-id="d45ce-106">EventTrigger Delay 屬性</span><span class="sxs-lookup"><span data-stu-id="d45ce-106">EventTrigger.Delay property</span></span>

<span data-ttu-id="d45ce-107">針對腳本，取得或設定值，這個值表示事件發生時間和工作啟動時間之間的時間量。</span><span class="sxs-lookup"><span data-stu-id="d45ce-107">For scripting, gets or sets a value that indicates the amount of time between when the event occurs and when the task is started.</span></span> <span data-ttu-id="d45ce-108">此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。</span><span class="sxs-lookup"><span data-stu-id="d45ce-108">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="syntax"></a><span data-ttu-id="d45ce-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d45ce-109">Syntax</span></span>


```VB
EventTrigger.Delay As String
```



## <a name="property-value"></a><span data-ttu-id="d45ce-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="d45ce-110">Property value</span></span>

<span data-ttu-id="d45ce-111">值，這個值表示發生事件的時間與啟動工作的時間之間的時間量。</span><span class="sxs-lookup"><span data-stu-id="d45ce-111">A value that indicates the amount of time between when the event occurs and when the task is started.</span></span>

## <a name="remarks"></a><span data-ttu-id="d45ce-112">備註</span><span class="sxs-lookup"><span data-stu-id="d45ce-112">Remarks</span></span>

<span data-ttu-id="d45ce-113">針對工作讀取或撰寫您自己的 XML 時，會使用工作排程器架構的 [**delay**](taskschedulerschema-delay-eventtriggertype-element.md) 元素指定事件延遲。</span><span class="sxs-lookup"><span data-stu-id="d45ce-113">When reading or writing your own XML for a task, the event delay is specified using the [**Delay**](taskschedulerschema-delay-eventtriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="d45ce-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="d45ce-114">Requirements</span></span>



| <span data-ttu-id="d45ce-115">需求</span><span class="sxs-lookup"><span data-stu-id="d45ce-115">Requirement</span></span> | <span data-ttu-id="d45ce-116">值</span><span class="sxs-lookup"><span data-stu-id="d45ce-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d45ce-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d45ce-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d45ce-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d45ce-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d45ce-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d45ce-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d45ce-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d45ce-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d45ce-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d45ce-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="d45ce-122"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d45ce-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d45ce-123">DLL</span><span class="sxs-lookup"><span data-stu-id="d45ce-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d45ce-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d45ce-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d45ce-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d45ce-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d45ce-126">工作排程器</span><span class="sxs-lookup"><span data-stu-id="d45ce-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="d45ce-127">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="d45ce-127">**EventTrigger**</span></span>](eventtrigger.md)
</dt> </dl>

 

 





