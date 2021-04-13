---
title: TaskSettings. StartWhenAvailable 屬性
description: 針對腳本，取得或設定布林值，指出工作排程器可以在經過排程的時間之後隨時啟動工作。
ms.assetid: 911de67c-baf8-4346-9b4c-e39e5f96c0fe
keywords:
- StartWhenAvailable 屬性工作排程器
- StartWhenAvailable 屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器、StartWhenAvailable 屬性
topic_type:
- apiref
api_name:
- TaskSettings.StartWhenAvailable
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63325fbf7aa9186e5748294c2ef57302efa0c79b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466405"
---
# <a name="tasksettingsstartwhenavailable-property"></a><span data-ttu-id="1100f-106">TaskSettings. StartWhenAvailable 屬性</span><span class="sxs-lookup"><span data-stu-id="1100f-106">TaskSettings.StartWhenAvailable property</span></span>

<span data-ttu-id="1100f-107">針對腳本，取得或設定布林值，指出工作排程器可以在經過排程的時間之後隨時啟動工作。</span><span class="sxs-lookup"><span data-stu-id="1100f-107">For scripting, gets or sets a Boolean value that indicates that the Task Scheduler can start the task at any time after its scheduled time has passed.</span></span>

<span data-ttu-id="1100f-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="1100f-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1100f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1100f-109">Syntax</span></span>


```VB
TaskSettings.StartWhenAvailable As Boolean
```



## <a name="property-value"></a><span data-ttu-id="1100f-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="1100f-110">Property value</span></span>

<span data-ttu-id="1100f-111">若為 True，則屬性會指出工作排程器可以在經過排程的時間之後隨時啟動工作。</span><span class="sxs-lookup"><span data-stu-id="1100f-111">If True, the property indicates that the Task Scheduler can start the task at any time after its scheduled time has passed.</span></span> <span data-ttu-id="1100f-112">預設值是 False。</span><span class="sxs-lookup"><span data-stu-id="1100f-112">The default is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="1100f-113">備註</span><span class="sxs-lookup"><span data-stu-id="1100f-113">Remarks</span></span>

<span data-ttu-id="1100f-114">這個屬性只適用于以時間為基礎的工作，其結束界限或以時間為基礎的工作設定為無限期地重複。</span><span class="sxs-lookup"><span data-stu-id="1100f-114">This property applies only to time-based tasks with an end boundary or time-based tasks that are set to repeat infinitely.</span></span>

<span data-ttu-id="1100f-115">在排程的時間之後啟動的工作已通過 (，因為 [**StartWhenAvailable**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable) 屬性設定為 True) 會在工作的工作排程器服務佇列中排入佇列，而且會在延遲之後啟動。</span><span class="sxs-lookup"><span data-stu-id="1100f-115">Tasks that are started after the scheduled time has passed (because of the [**StartWhenAvailable**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable) property being set to True) are queued in the Task Scheduler service's queue of tasks and they are started after a delay.</span></span> <span data-ttu-id="1100f-116">預設延遲為10分鐘。</span><span class="sxs-lookup"><span data-stu-id="1100f-116">The default delay is 10 minutes.</span></span>

<span data-ttu-id="1100f-117">讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [**StartWhenAvailable**](taskschedulerschema-startwhenavailable-settingstype-element.md) 元素中指定。</span><span class="sxs-lookup"><span data-stu-id="1100f-117">When reading or writing XML for a task, this setting is specified in the [**StartWhenAvailable**](taskschedulerschema-startwhenavailable-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="1100f-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="1100f-118">Requirements</span></span>



| <span data-ttu-id="1100f-119">需求</span><span class="sxs-lookup"><span data-stu-id="1100f-119">Requirement</span></span> | <span data-ttu-id="1100f-120">值</span><span class="sxs-lookup"><span data-stu-id="1100f-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1100f-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1100f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1100f-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1100f-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="1100f-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1100f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1100f-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1100f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1100f-125">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="1100f-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="1100f-126"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1100f-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1100f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="1100f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1100f-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1100f-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1100f-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1100f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1100f-130">工作排程器</span><span class="sxs-lookup"><span data-stu-id="1100f-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





