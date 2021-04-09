---
title: IdleSettings. StopOnIdleEnd 屬性
description: 針對腳本，取得或設定布林值，指出如果閒置條件在工作完成之前結束，工作排程器將終止工作。
ms.assetid: 5908bf6b-227a-4234-a741-82cf38163171
keywords:
- StopOnIdleEnd 屬性工作排程器
- StopOnIdleEnd 屬性工作排程器，IdleSettings 物件
- IdleSettings 物件工作排程器、StopOnIdleEnd 屬性
topic_type:
- apiref
api_name:
- IdleSettings.StopOnIdleEnd
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3f475c0a05d43cf0fbdd7097c1ee083f9040b07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843264"
---
# <a name="idlesettingsstoponidleend-property"></a><span data-ttu-id="21825-106">IdleSettings. StopOnIdleEnd 屬性</span><span class="sxs-lookup"><span data-stu-id="21825-106">IdleSettings.StopOnIdleEnd property</span></span>

<span data-ttu-id="21825-107">針對腳本，取得或設定布林值，指出如果閒置條件在工作完成之前結束，工作排程器將終止工作。</span><span class="sxs-lookup"><span data-stu-id="21825-107">For scripting, gets or sets a Boolean value that indicates that the Task Scheduler will terminate the task if the idle condition ends before the task is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="21825-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="21825-108">Syntax</span></span>


```VB
IdleSettings.StopOnIdleEnd As Boolean
```



## <a name="property-value"></a><span data-ttu-id="21825-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="21825-109">Property value</span></span>

<span data-ttu-id="21825-110">布林值，指出如果閒置條件在工作完成之前結束，工作排程器將終止工作。</span><span class="sxs-lookup"><span data-stu-id="21825-110">A Boolean value that indicates that the Task Scheduler will terminate the task if the idle condition ends before the task is completed.</span></span>

## <a name="remarks"></a><span data-ttu-id="21825-111">備註</span><span class="sxs-lookup"><span data-stu-id="21825-111">Remarks</span></span>

<span data-ttu-id="21825-112">讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) 元素中指定。</span><span class="sxs-lookup"><span data-stu-id="21825-112">When reading or writing XML for a task, this setting is specified in the [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="21825-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="21825-113">Requirements</span></span>



| <span data-ttu-id="21825-114">需求</span><span class="sxs-lookup"><span data-stu-id="21825-114">Requirement</span></span> | <span data-ttu-id="21825-115">值</span><span class="sxs-lookup"><span data-stu-id="21825-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21825-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="21825-116">Minimum supported client</span></span><br/> | <span data-ttu-id="21825-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="21825-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="21825-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="21825-118">Minimum supported server</span></span><br/> | <span data-ttu-id="21825-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="21825-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="21825-120">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="21825-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="21825-121"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="21825-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="21825-122">DLL</span><span class="sxs-lookup"><span data-stu-id="21825-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21825-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21825-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21825-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21825-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21825-125">工作排程器</span><span class="sxs-lookup"><span data-stu-id="21825-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="21825-126">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="21825-126">**IdleSettings**</span></span>](idlesettings.md)
</dt> </dl>

 

 





