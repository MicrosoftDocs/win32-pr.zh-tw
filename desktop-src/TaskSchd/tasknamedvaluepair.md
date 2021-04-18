---
title: TaskNamedValuePair 物件
description: 用來建立名稱/值組的腳本物件，其名稱與值相關聯。
ms.assetid: def679b1-28d5-4c52-9dca-42a6de06a1ec
keywords:
- TaskNamedValuePair 物件工作排程器
- TaskNamedValuePair 物件工作排程器，說明
topic_type:
- apiref
api_name:
- TaskNamedValuePair
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95229b5714d2cdcc43a071f2e51a50e04706429
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965477"
---
# <a name="tasknamedvaluepair-object"></a><span data-ttu-id="e93d3-105">TaskNamedValuePair 物件</span><span class="sxs-lookup"><span data-stu-id="e93d3-105">TaskNamedValuePair object</span></span>

<span data-ttu-id="e93d3-106">用來建立名稱/值組的腳本物件，其名稱與值相關聯。</span><span class="sxs-lookup"><span data-stu-id="e93d3-106">Scripting object that is used to create a name-value pair in which the name is associated with the value.</span></span>

## <a name="members"></a><span data-ttu-id="e93d3-107">成員</span><span class="sxs-lookup"><span data-stu-id="e93d3-107">Members</span></span>

<span data-ttu-id="e93d3-108">**TaskNamedValuePair** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e93d3-108">The **TaskNamedValuePair** object has these types of members:</span></span>

-   [<span data-ttu-id="e93d3-109">屬性</span><span class="sxs-lookup"><span data-stu-id="e93d3-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e93d3-110">屬性</span><span class="sxs-lookup"><span data-stu-id="e93d3-110">Properties</span></span>

<span data-ttu-id="e93d3-111">**TaskNamedValuePair** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e93d3-111">The **TaskNamedValuePair** object has these properties.</span></span>



| <span data-ttu-id="e93d3-112">屬性</span><span class="sxs-lookup"><span data-stu-id="e93d3-112">Property</span></span>                                             | <span data-ttu-id="e93d3-113">描述</span><span class="sxs-lookup"><span data-stu-id="e93d3-113">Description</span></span>                                                                            |
|:-----------------------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="e93d3-114">**Name**</span><span class="sxs-lookup"><span data-stu-id="e93d3-114">**Name**</span></span>](tasknamedvaluepair-name.md)<br/>   | <span data-ttu-id="e93d3-115">取得或設定與名稱/值配對中的值相關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="e93d3-115">Gets or sets the name that is associated with a value in a name-value pair.</span></span><br/> |
| [<span data-ttu-id="e93d3-116">**值**</span><span class="sxs-lookup"><span data-stu-id="e93d3-116">**Value**</span></span>](tasknamedvaluepair-value.md)<br/> | <span data-ttu-id="e93d3-117">取得或設定與名稱/值配對中的名稱相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="e93d3-117">Gets or sets the value that is associated with a name in a name-value pair.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e93d3-118">備註</span><span class="sxs-lookup"><span data-stu-id="e93d3-118">Remarks</span></span>

<span data-ttu-id="e93d3-119">針對工作讀取或撰寫您自己的 XML 時，會使用工作排程器架構的 [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) 元素來指定名稱/值組。</span><span class="sxs-lookup"><span data-stu-id="e93d3-119">When reading or writing your own XML for a task, a name-value pair is specified using the [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="e93d3-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="e93d3-120">Requirements</span></span>



| <span data-ttu-id="e93d3-121">需求</span><span class="sxs-lookup"><span data-stu-id="e93d3-121">Requirement</span></span> | <span data-ttu-id="e93d3-122">值</span><span class="sxs-lookup"><span data-stu-id="e93d3-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e93d3-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e93d3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e93d3-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e93d3-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e93d3-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e93d3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e93d3-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e93d3-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e93d3-127">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e93d3-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="e93d3-128"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e93d3-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e93d3-129">DLL</span><span class="sxs-lookup"><span data-stu-id="e93d3-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e93d3-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e93d3-130"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e93d3-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e93d3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e93d3-132">**TaskNamedValueCollection**</span><span class="sxs-lookup"><span data-stu-id="e93d3-132">**TaskNamedValueCollection**</span></span>](tasknamedvaluecollection.md)
</dt> </dl>

 

 





