---
title: 計數器。 Remove 方法
description: 從集合中移除 CounterItem 實例。
ms.assetid: 88e5907a-8c8f-4a24-9c5d-0c592f61dac0
keywords:
- 移除方法 SysMon
- Remove 方法 SysMon，計數器類別
- 計數器類別 SysMon，Remove 方法
topic_type:
- apiref
api_name:
- Counters.Remove
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa82a1a988be3554c265c097ba2a582035547391
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934245"
---
# <a name="countersremove-method"></a><span data-ttu-id="12ae6-106">計數器。 Remove 方法</span><span class="sxs-lookup"><span data-stu-id="12ae6-106">Counters.Remove method</span></span>

<span data-ttu-id="12ae6-107">從集合中移除 [**CounterItem**](counteritem.md) 實例。</span><span class="sxs-lookup"><span data-stu-id="12ae6-107">Removes a [**CounterItem**](counteritem.md) instance from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="12ae6-108">語法</span><span class="sxs-lookup"><span data-stu-id="12ae6-108">Syntax</span></span>


```VB
Counters.Remove( _
  ByVal index As Object _
)
```



## <a name="parameters"></a><span data-ttu-id="12ae6-109">參數</span><span class="sxs-lookup"><span data-stu-id="12ae6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12ae6-110">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="12ae6-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12ae6-111">要從集合中移除之 [**CounterItem**](counteritem.md) 物件的索引。</span><span class="sxs-lookup"><span data-stu-id="12ae6-111">Index of the [**CounterItem**](counteritem.md) object to remove from the collection.</span></span> <span data-ttu-id="12ae6-112">索引是以一為基礎。</span><span class="sxs-lookup"><span data-stu-id="12ae6-112">The index is one-based.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12ae6-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="12ae6-113">Return value</span></span>

<span data-ttu-id="12ae6-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="12ae6-114">This method does not return a value.</span></span>

## <a name="exceptions"></a><span data-ttu-id="12ae6-115">例外狀況</span><span class="sxs-lookup"><span data-stu-id="12ae6-115">Exceptions</span></span>



| <span data-ttu-id="12ae6-116">例外狀況類型</span><span class="sxs-lookup"><span data-stu-id="12ae6-116">Exception type</span></span>                                  | <span data-ttu-id="12ae6-117">條件</span><span class="sxs-lookup"><span data-stu-id="12ae6-117">Condition</span></span>                                                      |
|-------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="12ae6-118">**System.runtime.interopservices.outattribute. COMException**</span><span class="sxs-lookup"><span data-stu-id="12ae6-118">**System.Runtime.InteropServices.COMException**</span></span> | <span data-ttu-id="12ae6-119">指定的索引無效。</span><span class="sxs-lookup"><span data-stu-id="12ae6-119">The specified index is not valid.</span></span> <span data-ttu-id="12ae6-120">Err 值為???。</span><span class="sxs-lookup"><span data-stu-id="12ae6-120">The Err.Number value is ???.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="12ae6-121">備註</span><span class="sxs-lookup"><span data-stu-id="12ae6-121">Remarks</span></span>

<span data-ttu-id="12ae6-122">若要從集合中移除所有計數器，您可以呼叫 [**SystemMonitor。**](systemmonitor-reset.md)</span><span class="sxs-lookup"><span data-stu-id="12ae6-122">To remove all counters from the collection, you can call [**SystemMonitor.Reset**](systemmonitor-reset.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="12ae6-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="12ae6-123">Requirements</span></span>



| <span data-ttu-id="12ae6-124">需求</span><span class="sxs-lookup"><span data-stu-id="12ae6-124">Requirement</span></span> | <span data-ttu-id="12ae6-125">值</span><span class="sxs-lookup"><span data-stu-id="12ae6-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12ae6-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="12ae6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="12ae6-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12ae6-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="12ae6-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="12ae6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="12ae6-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12ae6-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="12ae6-130">DLL</span><span class="sxs-lookup"><span data-stu-id="12ae6-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12ae6-131"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="12ae6-131"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12ae6-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12ae6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12ae6-133">**計數器**</span><span class="sxs-lookup"><span data-stu-id="12ae6-133">**Counters**</span></span>](counters.md)
</dt> <dt>

[<span data-ttu-id="12ae6-134">**SystemMonitor 重設**</span><span class="sxs-lookup"><span data-stu-id="12ae6-134">**SystemMonitor.Reset**</span></span>](systemmonitor-reset.md)
</dt> </dl>

 

 





