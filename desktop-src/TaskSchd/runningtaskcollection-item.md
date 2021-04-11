---
title: RunningTaskCollection 專案屬性
description: 針對腳本，從集合取得指定的工作。
ms.assetid: 8b0745da-a11f-426c-9d52-f59d188e0e86
keywords:
- Item 屬性工作排程器
- 專案屬性工作排程器，RunningTaskCollection 物件
- RunningTaskCollection 物件工作排程器，Item 屬性
topic_type:
- apiref
api_name:
- RunningTaskCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49d28da7a3f5348ff9f5d6171a1a698d95b646f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104651"
---
# <a name="runningtaskcollectionitem-property"></a><span data-ttu-id="d98d1-106">RunningTaskCollection 專案屬性</span><span class="sxs-lookup"><span data-stu-id="d98d1-106">RunningTaskCollection.Item property</span></span>

<span data-ttu-id="d98d1-107">針對腳本，從集合取得指定的工作。</span><span class="sxs-lookup"><span data-stu-id="d98d1-107">For scripting, gets the specified task from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d98d1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d98d1-108">Syntax</span></span>


```VB
RunningTaskCollection.Item( _
  ByVal Index _
) As RunningTask
```



## <a name="property-value"></a><span data-ttu-id="d98d1-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="d98d1-109">Property value</span></span>

<span data-ttu-id="d98d1-110">[**RunningTask**](runningtask.md)物件，其中包含要求的內容。</span><span class="sxs-lookup"><span data-stu-id="d98d1-110">A [**RunningTask**](runningtask.md) object that contains the requested context.</span></span>

## <a name="remarks"></a><span data-ttu-id="d98d1-111">備註</span><span class="sxs-lookup"><span data-stu-id="d98d1-111">Remarks</span></span>

<span data-ttu-id="d98d1-112">集合以1為基礎。</span><span class="sxs-lookup"><span data-stu-id="d98d1-112">Collections are 1-based.</span></span> <span data-ttu-id="d98d1-113">換句話說，集合中第一個專案的索引為1。</span><span class="sxs-lookup"><span data-stu-id="d98d1-113">In other words, the index for the first item in the collection is 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="d98d1-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="d98d1-114">Requirements</span></span>



| <span data-ttu-id="d98d1-115">需求</span><span class="sxs-lookup"><span data-stu-id="d98d1-115">Requirement</span></span> | <span data-ttu-id="d98d1-116">值</span><span class="sxs-lookup"><span data-stu-id="d98d1-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d98d1-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d98d1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d98d1-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d98d1-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d98d1-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d98d1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d98d1-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d98d1-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d98d1-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d98d1-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="d98d1-122"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d98d1-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d98d1-123">DLL</span><span class="sxs-lookup"><span data-stu-id="d98d1-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d98d1-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d98d1-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d98d1-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d98d1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d98d1-126">工作排程器</span><span class="sxs-lookup"><span data-stu-id="d98d1-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





