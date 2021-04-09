---
title: Actioncollection 動作方法
description: 針對腳本，會從集合中移除指定的動作。
ms.assetid: ae1da6a9-5851-4ccb-80dc-75d7a99e7c6a
keywords:
- 移除方法工作排程器
- Remove 方法工作排程器，Actioncollection 動作物件
- Actioncollection 動作物件工作排程器、Remove 方法
topic_type:
- apiref
api_name:
- ActionCollection.Remove
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e110f870f4f192051b47cb3b65f0ebb41a490708
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686148"
---
# <a name="actioncollectionremove-method"></a><span data-ttu-id="72343-106">Actioncollection 動作方法</span><span class="sxs-lookup"><span data-stu-id="72343-106">ActionCollection.Remove method</span></span>

<span data-ttu-id="72343-107">針對腳本，會從集合中移除指定的動作。</span><span class="sxs-lookup"><span data-stu-id="72343-107">For scripting, removes the specified action from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="72343-108">語法</span><span class="sxs-lookup"><span data-stu-id="72343-108">Syntax</span></span>


```VB
ActionCollection.Remove( _
  ByVal index _
)
```



## <a name="parameters"></a><span data-ttu-id="72343-109">參數</span><span class="sxs-lookup"><span data-stu-id="72343-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72343-110">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="72343-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72343-111">要移除之動作的索引。</span><span class="sxs-lookup"><span data-stu-id="72343-111">The index of the action to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72343-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="72343-112">Return value</span></span>

<span data-ttu-id="72343-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="72343-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="72343-114">備註</span><span class="sxs-lookup"><span data-stu-id="72343-114">Remarks</span></span>

<span data-ttu-id="72343-115">移除專案時，請注意集合中第一個專案的索引是1，而最後一個專案的索引是 [**Actioncollection 動作計數**](actioncollection-count.md) 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="72343-115">When removing items, note that the index for the first item in the collection is 1 and the index for the last item is the value of the [**ActionCollection.Count**](actioncollection-count.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="72343-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="72343-116">Requirements</span></span>



| <span data-ttu-id="72343-117">需求</span><span class="sxs-lookup"><span data-stu-id="72343-117">Requirement</span></span> | <span data-ttu-id="72343-118">值</span><span class="sxs-lookup"><span data-stu-id="72343-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72343-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="72343-119">Minimum supported client</span></span><br/> | <span data-ttu-id="72343-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72343-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="72343-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="72343-121">Minimum supported server</span></span><br/> | <span data-ttu-id="72343-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72343-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="72343-123">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="72343-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="72343-124"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="72343-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="72343-125">DLL</span><span class="sxs-lookup"><span data-stu-id="72343-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72343-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72343-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72343-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="72343-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72343-128">工作排程器</span><span class="sxs-lookup"><span data-stu-id="72343-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="72343-129">**Actioncollection 動作**</span><span class="sxs-lookup"><span data-stu-id="72343-129">**ActionCollection**</span></span>](actioncollection.md)
</dt> </dl>

 

 





