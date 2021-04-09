---
title: 觸發程式。已啟用屬性
description: 針對腳本，取得或設定布林值，指出是否已啟用觸發程式。
ms.assetid: 8fb5a0cc-ddd4-430d-9593-95a4cb311f18
keywords:
- Enabled 屬性工作排程器
- 已啟用屬性工作排程器，觸發程式物件
- 觸發物件工作排程器，已啟用屬性
topic_type:
- apiref
api_name:
- Trigger.Enabled
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 411bc36dcf03933e2b4cee2f575aaec3b8133846
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934136"
---
# <a name="triggerenabled-property"></a><span data-ttu-id="c8f99-106">觸發程式。已啟用屬性</span><span class="sxs-lookup"><span data-stu-id="c8f99-106">Trigger.Enabled property</span></span>

<span data-ttu-id="c8f99-107">針對腳本，取得或設定布林值，指出是否已啟用觸發程式。</span><span class="sxs-lookup"><span data-stu-id="c8f99-107">For scripting, gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8f99-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8f99-108">Syntax</span></span>


```VB
Trigger.Enabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="c8f99-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="c8f99-109">Property value</span></span>

<span data-ttu-id="c8f99-110">如果觸發程式已啟用，則為 True;否則為 false。</span><span class="sxs-lookup"><span data-stu-id="c8f99-110">True if the trigger is enabled; otherwise, false.</span></span> <span data-ttu-id="c8f99-111">預設值是 true。</span><span class="sxs-lookup"><span data-stu-id="c8f99-111">The default is true.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8f99-112">備註</span><span class="sxs-lookup"><span data-stu-id="c8f99-112">Remarks</span></span>

<span data-ttu-id="c8f99-113">讀取或寫入工作的 XML 時，已啟用的屬性會使用工作排程器架構的 [**enabled**](taskschedulerschema-enabled-triggerbasetype-element.md) 元素來指定。</span><span class="sxs-lookup"><span data-stu-id="c8f99-113">When reading or writing XML for a task, the enabled property is specified using the [**Enabled**](taskschedulerschema-enabled-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8f99-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8f99-114">Requirements</span></span>



| <span data-ttu-id="c8f99-115">需求</span><span class="sxs-lookup"><span data-stu-id="c8f99-115">Requirement</span></span> | <span data-ttu-id="c8f99-116">值</span><span class="sxs-lookup"><span data-stu-id="c8f99-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8f99-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c8f99-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c8f99-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8f99-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c8f99-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c8f99-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c8f99-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8f99-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c8f99-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="c8f99-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="c8f99-122"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c8f99-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c8f99-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c8f99-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8f99-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8f99-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8f99-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8f99-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8f99-126">工作排程器</span><span class="sxs-lookup"><span data-stu-id="c8f99-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





