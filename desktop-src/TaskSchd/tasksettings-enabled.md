---
title: TaskSettings 已啟用屬性
description: 針對腳本，取得或設定布林值，表示已啟用工作。 只有當這項設定為 True 時，才能執行此工作。
ms.assetid: af8aa237-3402-4a82-b6ef-b713e1757d3a
keywords:
- Enabled 屬性工作排程器
- Enabled 屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器，Enabled 屬性
topic_type:
- apiref
api_name:
- TaskSettings.Enabled
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6805d7b754ac2c3553d5fde91826ffa192b91d97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384906"
---
# <a name="tasksettingsenabled-property"></a><span data-ttu-id="f5e44-107">TaskSettings 已啟用屬性</span><span class="sxs-lookup"><span data-stu-id="f5e44-107">TaskSettings.Enabled property</span></span>

<span data-ttu-id="f5e44-108">針對腳本，取得或設定布林值，表示已啟用工作。</span><span class="sxs-lookup"><span data-stu-id="f5e44-108">For scripting, gets or sets a Boolean value that indicates that the task is enabled.</span></span> <span data-ttu-id="f5e44-109">只有當這項設定為 True 時，才能執行此工作。</span><span class="sxs-lookup"><span data-stu-id="f5e44-109">The task can be performed only when this setting is True.</span></span>

<span data-ttu-id="f5e44-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="f5e44-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5e44-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5e44-111">Syntax</span></span>


```VB
TaskSettings.Enabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="f5e44-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="f5e44-112">Property value</span></span>

<span data-ttu-id="f5e44-113">若為 True，則會啟用工作。</span><span class="sxs-lookup"><span data-stu-id="f5e44-113">If True, the task is enabled.</span></span> <span data-ttu-id="f5e44-114">如果為 False，則不會啟用工作。</span><span class="sxs-lookup"><span data-stu-id="f5e44-114">If False, the task is not enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5e44-115">備註</span><span class="sxs-lookup"><span data-stu-id="f5e44-115">Remarks</span></span>

<span data-ttu-id="f5e44-116">讀取或寫入工作的 XML 時，此設定會指定在工作排程器架構的 [**Enabled (settingsType)**](taskschedulerschema-enabled-settingstype-element.md) 元素中。</span><span class="sxs-lookup"><span data-stu-id="f5e44-116">When reading or writing XML for a task, this setting is specified in the [**Enabled (settingsType)**](taskschedulerschema-enabled-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5e44-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="f5e44-117">Requirements</span></span>



| <span data-ttu-id="f5e44-118">需求</span><span class="sxs-lookup"><span data-stu-id="f5e44-118">Requirement</span></span> | <span data-ttu-id="f5e44-119">值</span><span class="sxs-lookup"><span data-stu-id="f5e44-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5e44-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f5e44-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f5e44-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f5e44-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f5e44-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f5e44-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f5e44-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f5e44-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f5e44-124">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="f5e44-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="f5e44-125"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f5e44-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f5e44-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f5e44-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5e44-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5e44-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5e44-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f5e44-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5e44-129">工作排程器</span><span class="sxs-lookup"><span data-stu-id="f5e44-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





