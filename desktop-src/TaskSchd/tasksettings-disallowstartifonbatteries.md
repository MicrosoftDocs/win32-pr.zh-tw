---
title: TaskSettings. DisallowStartIfOnBatteries 屬性
description: 針對腳本，取得或設定布林值，指出如果電腦是以電池執行，將不會啟動工作。
ms.assetid: 5e13f168-a396-495f-a486-e64e8524c8cd
keywords:
- DisallowStartIfOnBatteries 屬性工作排程器
- DisallowStartIfOnBatteries 屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器、DisallowStartIfOnBatteries 屬性
topic_type:
- apiref
api_name:
- TaskSettings.DisallowStartIfOnBatteries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d35a7fde3012b25dfeab65e6e6088bb1d950892d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105347"
---
# <a name="tasksettingsdisallowstartifonbatteries-property"></a><span data-ttu-id="0470f-106">TaskSettings. DisallowStartIfOnBatteries 屬性</span><span class="sxs-lookup"><span data-stu-id="0470f-106">TaskSettings.DisallowStartIfOnBatteries property</span></span>

<span data-ttu-id="0470f-107">針對腳本，取得或設定布林值，指出如果電腦是以電池執行，將不會啟動工作。</span><span class="sxs-lookup"><span data-stu-id="0470f-107">For scripting, gets or sets a Boolean value that indicates that the task will not be started if the computer is running on batteries.</span></span>

<span data-ttu-id="0470f-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="0470f-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0470f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0470f-109">Syntax</span></span>


```VB
TaskSettings.DisallowStartIfOnBatteries As Boolean
```



## <a name="property-value"></a><span data-ttu-id="0470f-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="0470f-110">Property value</span></span>

<span data-ttu-id="0470f-111">指出當電腦以電池執行時，不會啟動工作的布林值。</span><span class="sxs-lookup"><span data-stu-id="0470f-111">A Boolean value that indicates that the task will not be started if the computer is running on batteries.</span></span> <span data-ttu-id="0470f-112">若為 True，則在電腦以電池執行時，不會啟動工作。</span><span class="sxs-lookup"><span data-stu-id="0470f-112">If True, the task will not be started if the computer is running on batteries.</span></span> <span data-ttu-id="0470f-113">如果為 False，則工作會在電腦以電池執行時啟動。</span><span class="sxs-lookup"><span data-stu-id="0470f-113">If False, the task will be started if the computer is running on batteries.</span></span> <span data-ttu-id="0470f-114">預設值為 True。</span><span class="sxs-lookup"><span data-stu-id="0470f-114">The default is True.</span></span>

## <a name="remarks"></a><span data-ttu-id="0470f-115">備註</span><span class="sxs-lookup"><span data-stu-id="0470f-115">Remarks</span></span>

<span data-ttu-id="0470f-116">讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [**DisallowStartIfOnBatteries**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md) 元素中指定。</span><span class="sxs-lookup"><span data-stu-id="0470f-116">When reading or writing XML for a task, this setting is specified in the [**DisallowStartIfOnBatteries**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="0470f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="0470f-117">Requirements</span></span>



| <span data-ttu-id="0470f-118">需求</span><span class="sxs-lookup"><span data-stu-id="0470f-118">Requirement</span></span> | <span data-ttu-id="0470f-119">值</span><span class="sxs-lookup"><span data-stu-id="0470f-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0470f-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0470f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0470f-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0470f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0470f-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0470f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0470f-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0470f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0470f-124">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="0470f-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="0470f-125"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0470f-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0470f-126">DLL</span><span class="sxs-lookup"><span data-stu-id="0470f-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0470f-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0470f-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0470f-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0470f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0470f-129">工作排程器</span><span class="sxs-lookup"><span data-stu-id="0470f-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





