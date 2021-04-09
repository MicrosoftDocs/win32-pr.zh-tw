---
title: 'CounterItem 物件 (Isysmon) '
description: 您可以使用這個類別來抓取計數器的路徑和值，並指定用來繪製計數器的色彩。 若要取得這個物件，請呼叫計數器。 Item。
ms.assetid: 76b69395-efd8-4321-b7ed-63daa46e2636
keywords:
- CounterItem 物件 SysMon
- CounterItem 物件 SysMon，描述
topic_type:
- apiref
api_name:
- CounterItem
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df999e327591309f015d8720f61643625eced4d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686011"
---
# <a name="counteritem-object"></a><span data-ttu-id="1dfd0-106">CounterItem 物件</span><span class="sxs-lookup"><span data-stu-id="1dfd0-106">CounterItem object</span></span>

<span data-ttu-id="1dfd0-107">您可以使用這個類別來抓取計數器的路徑和值，並指定用來繪製計數器的色彩。</span><span class="sxs-lookup"><span data-stu-id="1dfd0-107">Use this class to retrieve the path and value of a counter and to specify the color used to graph the counter.</span></span>

<span data-ttu-id="1dfd0-108">若要取得這個物件，請呼叫 [**計數器。 Item**](counters-item.md)。</span><span class="sxs-lookup"><span data-stu-id="1dfd0-108">To retrieve this object, call [**Counters.Item**](counters-item.md).</span></span>

## <a name="members"></a><span data-ttu-id="1dfd0-109">成員</span><span class="sxs-lookup"><span data-stu-id="1dfd0-109">Members</span></span>

<span data-ttu-id="1dfd0-110">**CounterItem** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1dfd0-110">The **CounterItem** object has these types of members:</span></span>

-   [<span data-ttu-id="1dfd0-111">方法</span><span class="sxs-lookup"><span data-stu-id="1dfd0-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="1dfd0-112">屬性</span><span class="sxs-lookup"><span data-stu-id="1dfd0-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1dfd0-113">方法</span><span class="sxs-lookup"><span data-stu-id="1dfd0-113">Methods</span></span>

<span data-ttu-id="1dfd0-114">**CounterItem** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="1dfd0-114">The **CounterItem** object has these methods.</span></span>



| <span data-ttu-id="1dfd0-115">方法</span><span class="sxs-lookup"><span data-stu-id="1dfd0-115">Method</span></span>                                             | <span data-ttu-id="1dfd0-116">描述</span><span class="sxs-lookup"><span data-stu-id="1dfd0-116">Description</span></span>                                                                    |
|:---------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="1dfd0-117">**GetDataAt**</span><span class="sxs-lookup"><span data-stu-id="1dfd0-117">**GetDataAt**</span></span>](counteritem-getdataat.md)         | <span data-ttu-id="1dfd0-118">從折線圖中的特定點抓取計數器資料。</span><span class="sxs-lookup"><span data-stu-id="1dfd0-118">Retrieves the counter data from a specific point in the line graph.</span></span><br/> |
| [<span data-ttu-id="1dfd0-119">**GetStatistics**</span><span class="sxs-lookup"><span data-stu-id="1dfd0-119">**GetStatistics**</span></span>](counteritem-getstatistics.md) | <span data-ttu-id="1dfd0-120">抓取計數器的平均值、最大值和最小值。</span><span class="sxs-lookup"><span data-stu-id="1dfd0-120">Retrieves the average, maximum, and minimum values for the counter.</span></span><br/> |
| [<span data-ttu-id="1dfd0-121">**GetValue**</span><span class="sxs-lookup"><span data-stu-id="1dfd0-121">**GetValue**</span></span>](counteritem-getvalue.md)           | <span data-ttu-id="1dfd0-122">抓取計數器的最後一個值。</span><span class="sxs-lookup"><span data-stu-id="1dfd0-122">Retrieves the last value of the counter.</span></span><br/>                            |



 

### <a name="properties"></a><span data-ttu-id="1dfd0-123">屬性</span><span class="sxs-lookup"><span data-stu-id="1dfd0-123">Properties</span></span>

<span data-ttu-id="1dfd0-124">**CounterItem** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1dfd0-124">The **CounterItem** object has these properties.</span></span>



| <span data-ttu-id="1dfd0-125">屬性</span><span class="sxs-lookup"><span data-stu-id="1dfd0-125">Property</span></span>                                                  | <span data-ttu-id="1dfd0-126">描述</span><span class="sxs-lookup"><span data-stu-id="1dfd0-126">Description</span></span>                                                                     |
|:----------------------------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="1dfd0-127">**色彩**</span><span class="sxs-lookup"><span data-stu-id="1dfd0-127">**Color**</span></span>](counteritem-color.md)<br/>             | <span data-ttu-id="1dfd0-128">抓取或設定用來繪製計數器值的色彩。</span><span class="sxs-lookup"><span data-stu-id="1dfd0-128">Retrieves or sets the color used to graph the counter value.</span></span><br/>         |
| [<span data-ttu-id="1dfd0-129">**線條樣式**</span><span class="sxs-lookup"><span data-stu-id="1dfd0-129">**LineStyle**</span></span>](counteritem-linestyle.md)<br/>     | <span data-ttu-id="1dfd0-130">抓取或設定用來繪製計數器值的線條樣式。</span><span class="sxs-lookup"><span data-stu-id="1dfd0-130">Retrieves or sets the line style used to graph the counter value.</span></span><br/>    |
| [<span data-ttu-id="1dfd0-131">**路徑**</span><span class="sxs-lookup"><span data-stu-id="1dfd0-131">**Path**</span></span>](counteritem-path.md)<br/>               | <span data-ttu-id="1dfd0-132">抓取計數器的路徑。</span><span class="sxs-lookup"><span data-stu-id="1dfd0-132">Retrieves the path of the counter.</span></span><br/>                                   |
| [<span data-ttu-id="1dfd0-133">**ScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="1dfd0-133">**ScaleFactor**</span></span>](counteritem-scalefactor.md)<br/> | <span data-ttu-id="1dfd0-134">抓取或設定用來繪製計數器值的比例因數。</span><span class="sxs-lookup"><span data-stu-id="1dfd0-134">Retrieves or sets the scale factor used to graph the counter value.</span></span><br/>  |
| [<span data-ttu-id="1dfd0-135">**已選取**</span><span class="sxs-lookup"><span data-stu-id="1dfd0-135">**Selected**</span></span>](counteritem-selected.md)<br/>       | <span data-ttu-id="1dfd0-136">抓取或設定值，這個值會指出是否已選取計數器。</span><span class="sxs-lookup"><span data-stu-id="1dfd0-136">Retrieves or sets a value that indicates if the counter is selected.</span></span><br/> |
| [<span data-ttu-id="1dfd0-137">**值**</span><span class="sxs-lookup"><span data-stu-id="1dfd0-137">**Value**</span></span>](counteritem-value.md)<br/>             | <span data-ttu-id="1dfd0-138">抓取計數器的目前值。</span><span class="sxs-lookup"><span data-stu-id="1dfd0-138">Retrieves the current value of the counter.</span></span><br/>                          |
| [<span data-ttu-id="1dfd0-139">**可見**</span><span class="sxs-lookup"><span data-stu-id="1dfd0-139">**Visible**</span></span>](counteritem-visible.md)<br/>         | <span data-ttu-id="1dfd0-140">抓取或設定值，這個值會指出計數器是否為繪圖。</span><span class="sxs-lookup"><span data-stu-id="1dfd0-140">Retrieves or sets a value that indicates if the counter is graphed.</span></span><br/>  |
| [<span data-ttu-id="1dfd0-141">**寬度**</span><span class="sxs-lookup"><span data-stu-id="1dfd0-141">**Width**</span></span>](counteritem-width.md)<br/>             | <span data-ttu-id="1dfd0-142">抓取或設定用來繪製計數器值的線條寬度。</span><span class="sxs-lookup"><span data-stu-id="1dfd0-142">Retrieves or sets the line width used to graph the counter value.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="1dfd0-143">備註</span><span class="sxs-lookup"><span data-stu-id="1dfd0-143">Remarks</span></span>

<span data-ttu-id="1dfd0-144">[**值**](counteritem-value.md) 是 **CounterItem** 的預設屬性。</span><span class="sxs-lookup"><span data-stu-id="1dfd0-144">[**Value**](counteritem-value.md) is the default property of **CounterItem**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1dfd0-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="1dfd0-145">Requirements</span></span>



| <span data-ttu-id="1dfd0-146">需求</span><span class="sxs-lookup"><span data-stu-id="1dfd0-146">Requirement</span></span> | <span data-ttu-id="1dfd0-147">值</span><span class="sxs-lookup"><span data-stu-id="1dfd0-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1dfd0-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1dfd0-148">Minimum supported client</span></span><br/> | <span data-ttu-id="1dfd0-149">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1dfd0-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="1dfd0-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1dfd0-150">Minimum supported server</span></span><br/> | <span data-ttu-id="1dfd0-151">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1dfd0-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1dfd0-152">標頭</span><span class="sxs-lookup"><span data-stu-id="1dfd0-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="1dfd0-153"><dt>Isysmon。h</dt></span><span class="sxs-lookup"><span data-stu-id="1dfd0-153"><dt>Isysmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="1dfd0-154">DLL</span><span class="sxs-lookup"><span data-stu-id="1dfd0-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1dfd0-155"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="1dfd0-155"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dfd0-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1dfd0-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dfd0-157">SYSMON 類別</span><span class="sxs-lookup"><span data-stu-id="1dfd0-157">SYSMON Classes</span></span>](sysmon-classes.md)
</dt> </dl>

 

 





