---
title: TaskSettings. AllowDemandStart 屬性
description: 針對腳本，取得或設定布林值，這個值表示可以使用 [執行] 命令或內容功能表來啟動工作。
ms.assetid: 1eae19ae-3b4d-4eb2-82d0-685ef2729f36
keywords:
- AllowDemandStart 屬性工作排程器
- AllowDemandStart 屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器、AllowDemandStart 屬性
topic_type:
- apiref
api_name:
- TaskSettings.AllowDemandStart
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 657ba45e0809b74803e27de70fae52576fcf2a26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384090"
---
# <a name="tasksettingsallowdemandstart-property"></a><span data-ttu-id="047f8-106">TaskSettings. AllowDemandStart 屬性</span><span class="sxs-lookup"><span data-stu-id="047f8-106">TaskSettings.AllowDemandStart property</span></span>

<span data-ttu-id="047f8-107">針對腳本，取得或設定布林值，這個值表示可以使用 [執行] 命令或內容功能表來啟動工作。</span><span class="sxs-lookup"><span data-stu-id="047f8-107">For scripting, gets or sets a Boolean value that indicates that the task can be started by using either the Run command or the Context menu.</span></span>

<span data-ttu-id="047f8-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="047f8-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="047f8-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="047f8-109">Syntax</span></span>


```VB
TaskSettings.AllowDemandStart As Boolean
```



## <a name="property-value"></a><span data-ttu-id="047f8-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="047f8-110">Property value</span></span>

<span data-ttu-id="047f8-111">若為 True，則可以使用 [執行] 命令或內容功能表來執行工作。</span><span class="sxs-lookup"><span data-stu-id="047f8-111">If True, the task can be run by using the Run command or the Context menu.</span></span> <span data-ttu-id="047f8-112">如果為 False，則無法使用 [執行] 命令或內容功能表來執行工作。</span><span class="sxs-lookup"><span data-stu-id="047f8-112">If False, the task cannot be run using the Run command or the Context menu.</span></span> <span data-ttu-id="047f8-113">預設值為 True。</span><span class="sxs-lookup"><span data-stu-id="047f8-113">The default is True.</span></span>

## <a name="remarks"></a><span data-ttu-id="047f8-114">備註</span><span class="sxs-lookup"><span data-stu-id="047f8-114">Remarks</span></span>

<span data-ttu-id="047f8-115">當這個屬性設定為 True 時，可以在任何觸發程式啟動工作時獨立啟動工作。</span><span class="sxs-lookup"><span data-stu-id="047f8-115">When this property is set to True, the task can be started independent of when any triggers start the task.</span></span>

<span data-ttu-id="047f8-116">讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [AllowStartOnDemand](taskschedulerschema-allowstartondemand-settingstype-element.md) 元素中指定。</span><span class="sxs-lookup"><span data-stu-id="047f8-116">When reading or writing XML for a task, this setting is specified in the [AllowStartOnDemand](taskschedulerschema-allowstartondemand-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="047f8-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="047f8-117">Requirements</span></span>



| <span data-ttu-id="047f8-118">需求</span><span class="sxs-lookup"><span data-stu-id="047f8-118">Requirement</span></span> | <span data-ttu-id="047f8-119">值</span><span class="sxs-lookup"><span data-stu-id="047f8-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="047f8-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="047f8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="047f8-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="047f8-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="047f8-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="047f8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="047f8-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="047f8-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="047f8-124">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="047f8-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="047f8-125"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="047f8-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="047f8-126">DLL</span><span class="sxs-lookup"><span data-stu-id="047f8-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="047f8-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="047f8-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="047f8-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="047f8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="047f8-129">工作排程器</span><span class="sxs-lookup"><span data-stu-id="047f8-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





