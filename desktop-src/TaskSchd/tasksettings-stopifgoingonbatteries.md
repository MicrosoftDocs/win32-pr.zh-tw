---
title: TaskSettings. StopIfGoingOnBatteries 屬性
description: 針對腳本，取得或設定布林值，這個值表示如果電腦正進入電池，工作將會停止。
ms.assetid: a133cba0-c93e-4963-83a3-7587e323fc6e
keywords:
- StopIfGoingOnBatteries 屬性工作排程器
- StopIfGoingOnBatteries 屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器、StopIfGoingOnBatteries 屬性
topic_type:
- apiref
api_name:
- TaskSettings.StopIfGoingOnBatteries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aced436d653b6bbc02b4b36edea9046e3ac62392
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466400"
---
# <a name="tasksettingsstopifgoingonbatteries-property"></a><span data-ttu-id="dd799-106">TaskSettings. StopIfGoingOnBatteries 屬性</span><span class="sxs-lookup"><span data-stu-id="dd799-106">TaskSettings.StopIfGoingOnBatteries property</span></span>

<span data-ttu-id="dd799-107">針對腳本，取得或設定布林值，這個值表示如果電腦正進入電池，工作將會停止。</span><span class="sxs-lookup"><span data-stu-id="dd799-107">For scripting, gets or sets a Boolean value that indicates that the task will be stopped if the computer is going onto batteries.</span></span>

<span data-ttu-id="dd799-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="dd799-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd799-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd799-109">Syntax</span></span>


```VB
TaskSettings.StopIfGoingOnBatteries As Boolean
```



## <a name="property-value"></a><span data-ttu-id="dd799-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="dd799-110">Property value</span></span>

<span data-ttu-id="dd799-111">此為布林值，指出如果電腦即將進入電池，將會停止該工作。</span><span class="sxs-lookup"><span data-stu-id="dd799-111">A Boolean value that indicates that the task will be stopped if the computer is going onto batteries.</span></span> <span data-ttu-id="dd799-112">若為 True，則屬性會指出如果電腦即將進入電池，將會停止該工作。</span><span class="sxs-lookup"><span data-stu-id="dd799-112">If True, the property indicates that the task will be stopped if the computer is going onto batteries.</span></span> <span data-ttu-id="dd799-113">如果為 False，屬性工作表示如果電腦正在進入電池，將不會停止該工作。</span><span class="sxs-lookup"><span data-stu-id="dd799-113">If False, the property indicates that the task will not be stopped if the computer is going onto batteries.</span></span> <span data-ttu-id="dd799-114">預設值為 True。</span><span class="sxs-lookup"><span data-stu-id="dd799-114">The default is True.</span></span> <span data-ttu-id="dd799-115">如需詳細資訊，請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="dd799-115">See Remarks for more details.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd799-116">備註</span><span class="sxs-lookup"><span data-stu-id="dd799-116">Remarks</span></span>

<span data-ttu-id="dd799-117">讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [**StopIfGoingOnBatteries**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) 元素中指定。</span><span class="sxs-lookup"><span data-stu-id="dd799-117">When reading or writing XML for a task, this setting is specified in the [**StopIfGoingOnBatteries**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd799-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="dd799-118">Requirements</span></span>



| <span data-ttu-id="dd799-119">需求</span><span class="sxs-lookup"><span data-stu-id="dd799-119">Requirement</span></span> | <span data-ttu-id="dd799-120">值</span><span class="sxs-lookup"><span data-stu-id="dd799-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd799-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dd799-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dd799-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dd799-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="dd799-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dd799-123">Minimum supported server</span></span><br/> | <span data-ttu-id="dd799-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dd799-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dd799-125">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="dd799-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="dd799-126"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dd799-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dd799-127">DLL</span><span class="sxs-lookup"><span data-stu-id="dd799-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd799-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd799-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd799-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dd799-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd799-130">工作排程器</span><span class="sxs-lookup"><span data-stu-id="dd799-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





