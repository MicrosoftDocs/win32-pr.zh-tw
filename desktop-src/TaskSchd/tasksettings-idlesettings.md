---
title: TaskSettings. IdleSettings 屬性
description: 針對腳本，取得或設定指定當電腦處於閒置狀態時，工作排程器如何執行工作的資訊。
ms.assetid: 5205db6d-668e-498a-bbd5-edfcf66eec7f
keywords:
- IdleSettings 屬性工作排程器
- IdleSettings 屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器、IdleSettings 屬性
topic_type:
- apiref
api_name:
- TaskSettings.IdleSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 972d341d205ff5719f94a9c0a3b44f64c5678495
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965505"
---
# <a name="tasksettingsidlesettings-property"></a><span data-ttu-id="aa5fe-106">TaskSettings. IdleSettings 屬性</span><span class="sxs-lookup"><span data-stu-id="aa5fe-106">TaskSettings.IdleSettings property</span></span>

<span data-ttu-id="aa5fe-107">針對腳本，取得或設定指定當電腦處於閒置狀態時，工作排程器如何執行工作的資訊。</span><span class="sxs-lookup"><span data-stu-id="aa5fe-107">For scripting, gets or sets the information that specifies how the Task Scheduler performs tasks when the computer is in an idle condition.</span></span> <span data-ttu-id="aa5fe-108">如需有關閒置條件的詳細資訊，請參閱工作 [閒置條件](task-idle-conditions.md)。</span><span class="sxs-lookup"><span data-stu-id="aa5fe-108">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

<span data-ttu-id="aa5fe-109">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="aa5fe-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa5fe-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa5fe-110">Syntax</span></span>


```VB
TaskSettings.IdleSettings As IdleSettings
```



## <a name="property-value"></a><span data-ttu-id="aa5fe-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="aa5fe-111">Property value</span></span>

<span data-ttu-id="aa5fe-112">[**IdleSettings**](idlesettings.md)物件，指定當電腦進入閒置狀態時，工作排程器如何處理工作。</span><span class="sxs-lookup"><span data-stu-id="aa5fe-112">An [**IdleSettings**](idlesettings.md) object that specifies how the Task Scheduler handles the task when the computer goes into an idle condition.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa5fe-113">備註</span><span class="sxs-lookup"><span data-stu-id="aa5fe-113">Remarks</span></span>

<span data-ttu-id="aa5fe-114">讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) 元素中指定。</span><span class="sxs-lookup"><span data-stu-id="aa5fe-114">When reading or writing XML for a task, this setting is specified in the [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa5fe-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa5fe-115">Requirements</span></span>



| <span data-ttu-id="aa5fe-116">需求</span><span class="sxs-lookup"><span data-stu-id="aa5fe-116">Requirement</span></span> | <span data-ttu-id="aa5fe-117">值</span><span class="sxs-lookup"><span data-stu-id="aa5fe-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa5fe-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aa5fe-118">Minimum supported client</span></span><br/> | <span data-ttu-id="aa5fe-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aa5fe-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="aa5fe-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aa5fe-120">Minimum supported server</span></span><br/> | <span data-ttu-id="aa5fe-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aa5fe-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="aa5fe-122">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="aa5fe-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="aa5fe-123"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="aa5fe-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="aa5fe-124">DLL</span><span class="sxs-lookup"><span data-stu-id="aa5fe-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa5fe-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa5fe-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa5fe-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aa5fe-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa5fe-127">工作排程器</span><span class="sxs-lookup"><span data-stu-id="aa5fe-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





