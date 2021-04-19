---
title: '計數器集合 (Isysmon .h) '
description: 您可以使用這個類別來管理 CounterItem 物件的集合。 若要取出這個物件，請呼叫 SystemMonitor。
ms.assetid: 01542569-3fee-440a-8722-db377380b73c
keywords:
- 計數器集合 SysMon
- 計數器集合 SysMon，描述
topic_type:
- apiref
api_name:
- Counters
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbcbf8da93f13dce2ce2a290adeab9394ee8addb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966944"
---
# <a name="counters-collection"></a><span data-ttu-id="222b7-106">計數器集合</span><span class="sxs-lookup"><span data-stu-id="222b7-106">Counters collection</span></span>

<span data-ttu-id="222b7-107">您可以使用這個類別來管理 [**CounterItem**](counteritem.md) 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="222b7-107">Use this class to manage the collection of [**CounterItem**](counteritem.md) objects.</span></span>

<span data-ttu-id="222b7-108">若要取出這個物件，請呼叫 [**SystemMonitor。**](systemmonitor-counters.md)</span><span class="sxs-lookup"><span data-stu-id="222b7-108">To retrieve this object, call [**SystemMonitor.Counters**](systemmonitor-counters.md).</span></span>

## <a name="members"></a><span data-ttu-id="222b7-109">成員</span><span class="sxs-lookup"><span data-stu-id="222b7-109">Members</span></span>

<span data-ttu-id="222b7-110">**計數器** 集合有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="222b7-110">The **Counters** collection has these types of members:</span></span>

-   [<span data-ttu-id="222b7-111">方法</span><span class="sxs-lookup"><span data-stu-id="222b7-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="222b7-112">屬性</span><span class="sxs-lookup"><span data-stu-id="222b7-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="222b7-113">方法</span><span class="sxs-lookup"><span data-stu-id="222b7-113">Methods</span></span>

<span data-ttu-id="222b7-114">**計數器** 集合具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="222b7-114">The **Counters** collection has these methods.</span></span>



| <span data-ttu-id="222b7-115">方法</span><span class="sxs-lookup"><span data-stu-id="222b7-115">Method</span></span>                            | <span data-ttu-id="222b7-116">描述</span><span class="sxs-lookup"><span data-stu-id="222b7-116">Description</span></span>                                                                           |
|:----------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="222b7-117">**添加**</span><span class="sxs-lookup"><span data-stu-id="222b7-117">**Add**</span></span>](counters-add.md)       | <span data-ttu-id="222b7-118">將 [**CounterItem**](counteritem.md) 實例加入至集合。</span><span class="sxs-lookup"><span data-stu-id="222b7-118">Adds a [**CounterItem**](counteritem.md) instance to the collection.</span></span><br/>      |
| [<span data-ttu-id="222b7-119">**移除**</span><span class="sxs-lookup"><span data-stu-id="222b7-119">**Remove**</span></span>](counters-remove.md) | <span data-ttu-id="222b7-120">從集合中移除 [**CounterItem**](counteritem.md) 實例。</span><span class="sxs-lookup"><span data-stu-id="222b7-120">Removes a [**CounterItem**](counteritem.md) instance from the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="222b7-121">屬性</span><span class="sxs-lookup"><span data-stu-id="222b7-121">Properties</span></span>

<span data-ttu-id="222b7-122">**計數器** 集合具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="222b7-122">The **Counters** collection has these properties.</span></span>



| <span data-ttu-id="222b7-123">屬性</span><span class="sxs-lookup"><span data-stu-id="222b7-123">Property</span></span>                                   | <span data-ttu-id="222b7-124">描述</span><span class="sxs-lookup"><span data-stu-id="222b7-124">Description</span></span>                                                                                         |
|:-------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="222b7-125">**計數**</span><span class="sxs-lookup"><span data-stu-id="222b7-125">**Count**</span></span>](counters-count.md)<br/> | <span data-ttu-id="222b7-126">抓取集合中 [**CounterItem**](counteritem.md) 實例的數目。</span><span class="sxs-lookup"><span data-stu-id="222b7-126">Retrieves the number of [**CounterItem**](counteritem.md) instances in the collection.</span></span><br/>  |
| [<span data-ttu-id="222b7-127">**項目**</span><span class="sxs-lookup"><span data-stu-id="222b7-127">**Item**</span></span>](counters-item.md)<br/>   | <span data-ttu-id="222b7-128">從集合中抓取指定的 [**CounterItem**](counteritem.md) 實例。</span><span class="sxs-lookup"><span data-stu-id="222b7-128">Retrieves the specified [**CounterItem**](counteritem.md) instance from the collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="222b7-129">備註</span><span class="sxs-lookup"><span data-stu-id="222b7-129">Remarks</span></span>

<span data-ttu-id="222b7-130">**計數器** 物件是 [**SystemMonitor**](systemmonitor.md)物件的預設屬性。</span><span class="sxs-lookup"><span data-stu-id="222b7-130">The **Counters** object is the default property of the [**SystemMonitor**](systemmonitor.md) object.</span></span>

<span data-ttu-id="222b7-131">將您想要繪製的計數器加入至此集合。</span><span class="sxs-lookup"><span data-stu-id="222b7-131">Add to this collection those counters that you want to graph.</span></span> <span data-ttu-id="222b7-132">SYSMON 會根據您指定的 [**資料來源**](systemmonitor-datasourcetype.md) ，從系統或記錄檔抓取計數器值。</span><span class="sxs-lookup"><span data-stu-id="222b7-132">SYSMON retrieves the counter values either from the system or from a log file depending on the [**data source**](systemmonitor-datasourcetype.md) that you specify.</span></span>

## <a name="requirements"></a><span data-ttu-id="222b7-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="222b7-133">Requirements</span></span>



| <span data-ttu-id="222b7-134">需求</span><span class="sxs-lookup"><span data-stu-id="222b7-134">Requirement</span></span> | <span data-ttu-id="222b7-135">值</span><span class="sxs-lookup"><span data-stu-id="222b7-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="222b7-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="222b7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="222b7-137">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="222b7-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="222b7-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="222b7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="222b7-139">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="222b7-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="222b7-140">標頭</span><span class="sxs-lookup"><span data-stu-id="222b7-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="222b7-141"><dt>Isysmon。h</dt></span><span class="sxs-lookup"><span data-stu-id="222b7-141"><dt>Isysmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="222b7-142">DLL</span><span class="sxs-lookup"><span data-stu-id="222b7-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="222b7-143"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="222b7-143"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





