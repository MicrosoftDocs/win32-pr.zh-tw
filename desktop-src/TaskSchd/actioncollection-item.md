---
title: Actioncollection 動作專案屬性
description: 針對腳本，從集合取得指定的動作。
ms.assetid: a5567c82-2d56-4c3e-894c-ca6d432a3358
keywords:
- Item 屬性工作排程器
- 專案屬性工作排程器，Actioncollection 動作物件
- Actioncollection 動作物件工作排程器，Item 屬性
topic_type:
- apiref
api_name:
- ActionCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4853009c547f3bdfbb269e512ce5d39273726095
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385013"
---
# <a name="actioncollectionitem-property"></a><span data-ttu-id="bf54a-106">Actioncollection 動作專案屬性</span><span class="sxs-lookup"><span data-stu-id="bf54a-106">ActionCollection.Item property</span></span>

<span data-ttu-id="bf54a-107">針對腳本，從集合取得指定的動作。</span><span class="sxs-lookup"><span data-stu-id="bf54a-107">For scripting, gets a specified action from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf54a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf54a-108">Syntax</span></span>


```VB
ActionCollection.Item( _
  ByVal Index _
) As Action
```



## <a name="property-value"></a><span data-ttu-id="bf54a-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="bf54a-109">Property value</span></span>

<span data-ttu-id="bf54a-110">代表所要求之動作的 [**動作**](action.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="bf54a-110">An [**Action**](action.md) object that represents the requested action.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf54a-111">備註</span><span class="sxs-lookup"><span data-stu-id="bf54a-111">Remarks</span></span>

<span data-ttu-id="bf54a-112">集合以1為基礎。</span><span class="sxs-lookup"><span data-stu-id="bf54a-112">Collections are 1-based.</span></span> <span data-ttu-id="bf54a-113">換句話說，集合中第一個專案的索引為1。</span><span class="sxs-lookup"><span data-stu-id="bf54a-113">In other words, the index for the first item in the collection is 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf54a-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="bf54a-114">Requirements</span></span>



| <span data-ttu-id="bf54a-115">需求</span><span class="sxs-lookup"><span data-stu-id="bf54a-115">Requirement</span></span> | <span data-ttu-id="bf54a-116">值</span><span class="sxs-lookup"><span data-stu-id="bf54a-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf54a-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bf54a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bf54a-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf54a-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="bf54a-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bf54a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bf54a-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf54a-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bf54a-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="bf54a-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="bf54a-122"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bf54a-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bf54a-123">DLL</span><span class="sxs-lookup"><span data-stu-id="bf54a-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf54a-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf54a-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf54a-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bf54a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf54a-126">工作排程器</span><span class="sxs-lookup"><span data-stu-id="bf54a-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="bf54a-127">**Actioncollection 動作**</span><span class="sxs-lookup"><span data-stu-id="bf54a-127">**ActionCollection**</span></span>](actioncollection.md)
</dt> </dl>

 

 





