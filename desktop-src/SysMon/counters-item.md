---
title: 計數器。 Item 屬性
description: 從集合中抓取指定的 CounterItem 實例。
ms.assetid: bf503371-c8bd-4e0d-ab8d-58de3f8fac5f
keywords:
- 專案屬性 SysMon
- Item 屬性 SysMon，計數器類別
- 計數器類別 SysMon，Item 屬性
topic_type:
- apiref
api_name:
- Counters.Item
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 251a645f0a4ceacdbfb4e2ab7e650f41e44dd508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464713"
---
# <a name="countersitem-property"></a><span data-ttu-id="bcf95-106">計數器。 Item 屬性</span><span class="sxs-lookup"><span data-stu-id="bcf95-106">Counters.Item property</span></span>

<span data-ttu-id="bcf95-107">從集合中抓取指定的 [**CounterItem**](counteritem.md) 實例。</span><span class="sxs-lookup"><span data-stu-id="bcf95-107">Retrieves the specified [**CounterItem**](counteritem.md) instance from the collection.</span></span>

<span data-ttu-id="bcf95-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="bcf95-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcf95-109">語法</span><span class="sxs-lookup"><span data-stu-id="bcf95-109">Syntax</span></span>


```VB
Property Item( _
  ByVal index As Object _
) As CounterItem
```



## <a name="property-value"></a><span data-ttu-id="bcf95-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="bcf95-110">Property value</span></span>

<span data-ttu-id="bcf95-111">對應至指定之索引值的 [**CounterItem**](counteritem.md)實例。</span><span class="sxs-lookup"><span data-stu-id="bcf95-111">[**CounterItem**](counteritem.md) instance that corresponds to the specified index value.</span></span>

## <a name="exceptions"></a><span data-ttu-id="bcf95-112">例外狀況</span><span class="sxs-lookup"><span data-stu-id="bcf95-112">Exceptions</span></span>



| <span data-ttu-id="bcf95-113">例外狀況類型</span><span class="sxs-lookup"><span data-stu-id="bcf95-113">Exception type</span></span>                                  | <span data-ttu-id="bcf95-114">條件</span><span class="sxs-lookup"><span data-stu-id="bcf95-114">Condition</span></span>                         |
|-------------------------------------------------|-----------------------------------|
| <span data-ttu-id="bcf95-115">**System.runtime.interopservices.outattribute. COMException**</span><span class="sxs-lookup"><span data-stu-id="bcf95-115">**System.Runtime.InteropServices.COMException**</span></span> | <span data-ttu-id="bcf95-116">指定的索引無效。</span><span class="sxs-lookup"><span data-stu-id="bcf95-116">The specified index is not valid.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="bcf95-117">備註</span><span class="sxs-lookup"><span data-stu-id="bcf95-117">Remarks</span></span>

<span data-ttu-id="bcf95-118">這是 [**計數器**](counters.md) 物件的預設屬性。</span><span class="sxs-lookup"><span data-stu-id="bcf95-118">This is the default property of the [**Counters**](counters.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcf95-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="bcf95-119">Requirements</span></span>



| <span data-ttu-id="bcf95-120">需求</span><span class="sxs-lookup"><span data-stu-id="bcf95-120">Requirement</span></span> | <span data-ttu-id="bcf95-121">值</span><span class="sxs-lookup"><span data-stu-id="bcf95-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bcf95-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bcf95-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bcf95-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bcf95-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="bcf95-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bcf95-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bcf95-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bcf95-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bcf95-126">DLL</span><span class="sxs-lookup"><span data-stu-id="bcf95-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcf95-127"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="bcf95-127"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcf95-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bcf95-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcf95-129">**CounterItem**</span><span class="sxs-lookup"><span data-stu-id="bcf95-129">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="bcf95-130">**計數器**</span><span class="sxs-lookup"><span data-stu-id="bcf95-130">**Counters**</span></span>](counters.md)
</dt> </dl>

 

 





