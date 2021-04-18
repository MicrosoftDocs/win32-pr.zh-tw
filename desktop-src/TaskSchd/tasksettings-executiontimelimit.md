---
title: TaskSettings.ExecutionTimeLimit 屬性
description: 針對腳本，取得或設定可以完成工作的時間量。
ms.assetid: 5b8b8d4b-e705-4407-95c9-bf8baacb58c1
keywords:
- ExecutionTimeLimit 屬性工作排程器
- ExecutionTimeLimit 屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器、ExecutionTimeLimit 屬性
topic_type:
- apiref
api_name:
- TaskSettings.ExecutionTimeLimit
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de01d68fa7fe6c21f022d8a21863887e57016c5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967358"
---
# <a name="tasksettingsexecutiontimelimit-property"></a><span data-ttu-id="47c35-106">TaskSettings.ExecutionTimeLimit 屬性</span><span class="sxs-lookup"><span data-stu-id="47c35-106">TaskSettings.ExecutionTimeLimit property</span></span>

<span data-ttu-id="47c35-107">針對腳本，取得或設定可以完成工作的時間量。</span><span class="sxs-lookup"><span data-stu-id="47c35-107">For scripting, gets or sets the amount of time that is allowed to complete the task.</span></span> <span data-ttu-id="47c35-108">根據預設，工作會在開始執行時停止72小時。</span><span class="sxs-lookup"><span data-stu-id="47c35-108">By default, a task will be stopped 72 hours after it starts to run.</span></span> <span data-ttu-id="47c35-109">您可以變更此設定來變更此設定。</span><span class="sxs-lookup"><span data-stu-id="47c35-109">You can change this by changing this setting.</span></span>

<span data-ttu-id="47c35-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="47c35-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="47c35-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="47c35-111">Syntax</span></span>


```VB
TaskSettings.ExecutionTimeLimit As String
```



## <a name="property-value"></a><span data-ttu-id="47c35-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="47c35-112">Property value</span></span>

<span data-ttu-id="47c35-113">允許完成工作的時間量。</span><span class="sxs-lookup"><span data-stu-id="47c35-113">The amount of time that is allowed to complete the task.</span></span> <span data-ttu-id="47c35-114">此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。</span><span class="sxs-lookup"><span data-stu-id="47c35-114">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="47c35-115">PT0S 的值會讓工作無限期地執行。</span><span class="sxs-lookup"><span data-stu-id="47c35-115">A value of PT0S will enable the task to run indefinitely.</span></span> <span data-ttu-id="47c35-116">當此參數設定為 [無] 時，執行時間限制為 [無限]。</span><span class="sxs-lookup"><span data-stu-id="47c35-116">When this parameter is set to Nothing, the execution time limit is infinite.</span></span>

## <a name="remarks"></a><span data-ttu-id="47c35-117">備註</span><span class="sxs-lookup"><span data-stu-id="47c35-117">Remarks</span></span>

<span data-ttu-id="47c35-118">讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-settingstype-element.md) 元素中指定。</span><span class="sxs-lookup"><span data-stu-id="47c35-118">When reading or writing XML for a task, this setting is specified in the [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="47c35-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="47c35-119">Requirements</span></span>



| <span data-ttu-id="47c35-120">需求</span><span class="sxs-lookup"><span data-stu-id="47c35-120">Requirement</span></span> | <span data-ttu-id="47c35-121">值</span><span class="sxs-lookup"><span data-stu-id="47c35-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="47c35-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="47c35-122">Minimum supported client</span></span><br/> | <span data-ttu-id="47c35-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="47c35-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="47c35-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="47c35-124">Minimum supported server</span></span><br/> | <span data-ttu-id="47c35-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="47c35-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="47c35-126">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="47c35-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="47c35-127"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="47c35-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="47c35-128">DLL</span><span class="sxs-lookup"><span data-stu-id="47c35-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47c35-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47c35-129"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47c35-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="47c35-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47c35-131">工作排程器</span><span class="sxs-lookup"><span data-stu-id="47c35-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





