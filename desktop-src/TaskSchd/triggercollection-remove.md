---
title: TriggerCollection 方法
description: 針對腳本，從工作所用的觸發程式集合中移除指定的觸發程式。
ms.assetid: 30dccf16-2b4c-4776-9c19-f82ddd859d45
keywords:
- 觸發程式工作排程器，移除
- 移除方法工作排程器
- Remove 方法工作排程器，TriggerCollection 物件
- TriggerCollection 物件工作排程器、Remove 方法
topic_type:
- apiref
api_name:
- TriggerCollection.Remove
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401e84e57b28db9b08fd7e93e85fb7bc35f60647
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317220"
---
# <a name="triggercollectionremove-method"></a><span data-ttu-id="58dbb-107">TriggerCollection 方法</span><span class="sxs-lookup"><span data-stu-id="58dbb-107">TriggerCollection.Remove method</span></span>

<span data-ttu-id="58dbb-108">針對腳本，從工作所用的觸發程式集合中移除指定的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="58dbb-108">For scripting, removes the specified trigger from the collection of triggers used by the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="58dbb-109">語法</span><span class="sxs-lookup"><span data-stu-id="58dbb-109">Syntax</span></span>


```VB
TriggerCollection.Remove( _
  ByVal index _
)
```



## <a name="parameters"></a><span data-ttu-id="58dbb-110">參數</span><span class="sxs-lookup"><span data-stu-id="58dbb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58dbb-111">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="58dbb-111">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58dbb-112">要移除之觸發程式的索引。</span><span class="sxs-lookup"><span data-stu-id="58dbb-112">The index of the trigger to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58dbb-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="58dbb-113">Return value</span></span>

<span data-ttu-id="58dbb-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="58dbb-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="58dbb-115">備註</span><span class="sxs-lookup"><span data-stu-id="58dbb-115">Remarks</span></span>

<span data-ttu-id="58dbb-116">移除專案時，請注意集合中第一個專案的索引是1，而最後一個專案的索引是 [**TriggerCollection 計數**](triggercollection-count.md) 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="58dbb-116">When removing items, note that the index for the first item in the collection is 1 and the index for the last item is the value of the [**TriggerCollection.Count**](triggercollection-count.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="58dbb-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="58dbb-117">Requirements</span></span>



| <span data-ttu-id="58dbb-118">需求</span><span class="sxs-lookup"><span data-stu-id="58dbb-118">Requirement</span></span> | <span data-ttu-id="58dbb-119">值</span><span class="sxs-lookup"><span data-stu-id="58dbb-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58dbb-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="58dbb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="58dbb-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58dbb-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="58dbb-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="58dbb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="58dbb-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58dbb-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="58dbb-124">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="58dbb-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="58dbb-125"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="58dbb-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="58dbb-126">DLL</span><span class="sxs-lookup"><span data-stu-id="58dbb-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58dbb-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58dbb-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58dbb-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="58dbb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58dbb-129">工作排程器</span><span class="sxs-lookup"><span data-stu-id="58dbb-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





