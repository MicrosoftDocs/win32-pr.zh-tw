---
title: CounterItem。 Value 屬性
description: 抓取計數器的最後取樣值。
ms.assetid: c5aeaa00-e185-484d-8a7a-d45a21690e20
keywords:
- 值屬性 SysMon
- Value 屬性 SysMon，CounterItem 類別
- CounterItem 類別 SysMon，Value 屬性
topic_type:
- apiref
api_name:
- CounterItem.Value
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62c0d6bd9e1751e34c980bc95f790314017eeb49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968167"
---
# <a name="counteritemvalue-property"></a><span data-ttu-id="e765f-106">CounterItem。 Value 屬性</span><span class="sxs-lookup"><span data-stu-id="e765f-106">CounterItem.Value property</span></span>

<span data-ttu-id="e765f-107">抓取計數器的最後取樣值。</span><span class="sxs-lookup"><span data-stu-id="e765f-107">Retrieves the last sampled value of the counter.</span></span>

<span data-ttu-id="e765f-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="e765f-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e765f-109">語法</span><span class="sxs-lookup"><span data-stu-id="e765f-109">Syntax</span></span>


```VB
Property Value As Double
```



## <a name="property-value"></a><span data-ttu-id="e765f-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="e765f-110">Property value</span></span>

<span data-ttu-id="e765f-111">計數器的上次取樣值。</span><span class="sxs-lookup"><span data-stu-id="e765f-111">Last sampled value of the counter.</span></span> <span data-ttu-id="e765f-112">如果發生錯誤，此值為-1。</span><span class="sxs-lookup"><span data-stu-id="e765f-112">The value is -1 if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="e765f-113">備註</span><span class="sxs-lookup"><span data-stu-id="e765f-113">Remarks</span></span>

<span data-ttu-id="e765f-114">這是 [**CounterItem**](counteritem.md) 物件的預設屬性。</span><span class="sxs-lookup"><span data-stu-id="e765f-114">This is the default property of the [**CounterItem**](counteritem.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="e765f-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="e765f-115">Requirements</span></span>



| <span data-ttu-id="e765f-116">需求</span><span class="sxs-lookup"><span data-stu-id="e765f-116">Requirement</span></span> | <span data-ttu-id="e765f-117">值</span><span class="sxs-lookup"><span data-stu-id="e765f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e765f-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e765f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e765f-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e765f-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e765f-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e765f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e765f-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e765f-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e765f-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e765f-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e765f-123"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="e765f-123"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e765f-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e765f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e765f-125">**CounterItem**</span><span class="sxs-lookup"><span data-stu-id="e765f-125">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="e765f-126">**CounterItem**</span><span class="sxs-lookup"><span data-stu-id="e765f-126">**CounterItem.GetValue**</span></span>](counteritem-getvalue.md)
</dt> </dl>

 

 





