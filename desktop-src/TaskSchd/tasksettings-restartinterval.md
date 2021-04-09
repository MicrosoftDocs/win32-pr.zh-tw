---
title: TaskSettings. RestartInterval 屬性
description: 針對腳本，取得或設定值，這個值會指定工作排程器嘗試重新開機工作的時間長度。
ms.assetid: ad6f254d-55a8-478e-984e-a459f22043b5
keywords:
- RestartInterval 屬性工作排程器
- RestartInterval 屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器、RestartInterval 屬性
topic_type:
- apiref
api_name:
- TaskSettings.RestartInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f511e43ebb1d61fd80f2fcab34aba092704b8338
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685638"
---
# <a name="tasksettingsrestartinterval-property"></a><span data-ttu-id="6f370-106">TaskSettings. RestartInterval 屬性</span><span class="sxs-lookup"><span data-stu-id="6f370-106">TaskSettings.RestartInterval property</span></span>

<span data-ttu-id="6f370-107">針對腳本，取得或設定值，這個值會指定工作排程器嘗試重新開機工作的時間長度。</span><span class="sxs-lookup"><span data-stu-id="6f370-107">For scripting, gets or sets a value that specifies how long the Task Scheduler will attempt to restart the task.</span></span>

<span data-ttu-id="6f370-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="6f370-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f370-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f370-109">Syntax</span></span>


```VB
TaskSettings.RestartInterval As String
```



## <a name="property-value"></a><span data-ttu-id="6f370-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="6f370-110">Property value</span></span>

<span data-ttu-id="6f370-111">值，指定工作排程器將嘗試重新開機工作的時間長度。</span><span class="sxs-lookup"><span data-stu-id="6f370-111">A value that specifies how long the Task Scheduler will attempt to restart the task.</span></span> <span data-ttu-id="6f370-112">如果設定這個屬性，也必須設定 [**RestartCount**](tasksettings-restartcount.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="6f370-112">If this property is set, the [**RestartCount**](tasksettings-restartcount.md) property must also be set.</span></span> <span data-ttu-id="6f370-113">此字串的格式為 P <days> DT <hours> H <minutes> M <seconds> S (例如，"PT5M" 為5分鐘、"PT1H" 為1小時，而 "PT20M" 為20分鐘) 。</span><span class="sxs-lookup"><span data-stu-id="6f370-113">The format for this string is P<days>DT<hours>H<minutes>M<seconds>S (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="6f370-114">允許的時間上限為31天，而允許的最短時間為1分鐘。</span><span class="sxs-lookup"><span data-stu-id="6f370-114">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f370-115">備註</span><span class="sxs-lookup"><span data-stu-id="6f370-115">Remarks</span></span>

<span data-ttu-id="6f370-116">讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [**Interval**](taskschedulerschema-interval-restarttype-element.md) 元素中指定。</span><span class="sxs-lookup"><span data-stu-id="6f370-116">When reading or writing XML for a task, this setting is specified in the [**Interval**](taskschedulerschema-interval-restarttype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f370-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="6f370-117">Requirements</span></span>



| <span data-ttu-id="6f370-118">需求</span><span class="sxs-lookup"><span data-stu-id="6f370-118">Requirement</span></span> | <span data-ttu-id="6f370-119">值</span><span class="sxs-lookup"><span data-stu-id="6f370-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f370-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6f370-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6f370-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f370-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6f370-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6f370-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6f370-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f370-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6f370-124">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="6f370-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="6f370-125"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6f370-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6f370-126">DLL</span><span class="sxs-lookup"><span data-stu-id="6f370-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f370-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f370-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f370-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6f370-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f370-129">工作排程器</span><span class="sxs-lookup"><span data-stu-id="6f370-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





