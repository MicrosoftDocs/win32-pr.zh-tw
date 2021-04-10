---
title: TriggerCollection 專案屬性
description: 針對腳本，從集合取得指定的觸發程式。
ms.assetid: 517976df-b3fc-4f2e-8d37-262195c65182
keywords:
- Item 屬性工作排程器
- 專案屬性工作排程器，TriggerCollection 物件
- TriggerCollection 物件工作排程器，Item 屬性
topic_type:
- apiref
api_name:
- TriggerCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d600418d43459d6c4cbfcb0746a378633d096c24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685726"
---
# <a name="triggercollectionitem-property"></a><span data-ttu-id="6432d-106">TriggerCollection 專案屬性</span><span class="sxs-lookup"><span data-stu-id="6432d-106">TriggerCollection.Item property</span></span>

<span data-ttu-id="6432d-107">針對腳本，從集合取得指定的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="6432d-107">For scripting, gets the specified trigger from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6432d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6432d-108">Syntax</span></span>


```VB
TriggerCollection.Item( _
  ByVal index _
) As Trigger
```



## <a name="property-value"></a><span data-ttu-id="6432d-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="6432d-109">Property value</span></span>

<span data-ttu-id="6432d-110">代表所要求之觸發程式的 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="6432d-110">A [**Trigger**](trigger.md) object that represents the requested trigger.</span></span>

## <a name="remarks"></a><span data-ttu-id="6432d-111">備註</span><span class="sxs-lookup"><span data-stu-id="6432d-111">Remarks</span></span>

<span data-ttu-id="6432d-112">集合以1為基礎。</span><span class="sxs-lookup"><span data-stu-id="6432d-112">Collections are 1-based.</span></span> <span data-ttu-id="6432d-113">換句話說，集合中第一個專案的索引為1。</span><span class="sxs-lookup"><span data-stu-id="6432d-113">In other words, the index for the first item in the collection is 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="6432d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="6432d-114">Requirements</span></span>



| <span data-ttu-id="6432d-115">需求</span><span class="sxs-lookup"><span data-stu-id="6432d-115">Requirement</span></span> | <span data-ttu-id="6432d-116">值</span><span class="sxs-lookup"><span data-stu-id="6432d-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6432d-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6432d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6432d-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6432d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6432d-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6432d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6432d-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6432d-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6432d-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="6432d-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="6432d-122"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6432d-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6432d-123">DLL</span><span class="sxs-lookup"><span data-stu-id="6432d-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6432d-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6432d-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6432d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6432d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6432d-126">工作排程器</span><span class="sxs-lookup"><span data-stu-id="6432d-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





