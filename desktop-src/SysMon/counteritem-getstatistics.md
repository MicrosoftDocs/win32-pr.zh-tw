---
title: CounterItem. GetStatistics 方法
description: 抓取計數器的平均值、最大值和最小值。
ms.assetid: fb55d68b-1dbe-48b1-88c8-51f33048ec24
keywords:
- GetStatistics 方法 SysMon
- GetStatistics 方法 SysMon、CounterItem 類別
- CounterItem 類別 SysMon，GetStatistics 方法
topic_type:
- apiref
api_name:
- CounterItem.GetStatistics
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c993ed8b9bb39a4d8bb3ff18663f2d884ece156
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934504"
---
# <a name="counteritemgetstatistics-method"></a><span data-ttu-id="1cda7-106">CounterItem. GetStatistics 方法</span><span class="sxs-lookup"><span data-stu-id="1cda7-106">CounterItem.GetStatistics method</span></span>

<span data-ttu-id="1cda7-107">抓取計數器的平均值、最大值和最小值。</span><span class="sxs-lookup"><span data-stu-id="1cda7-107">Retrieves the average, maximum, and minimum values for the counter.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cda7-108">語法</span><span class="sxs-lookup"><span data-stu-id="1cda7-108">Syntax</span></span>


```VB
CounterItem.GetStatistics( _
  ByRef max As Double, _
  ByRef min As Double, _
  ByRef average As Double, _
  ByRef status As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="1cda7-109">參數</span><span class="sxs-lookup"><span data-stu-id="1cda7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cda7-110">*最大值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1cda7-110">*max* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1cda7-111">計數器的最大值。</span><span class="sxs-lookup"><span data-stu-id="1cda7-111">Maximum value of the counter.</span></span>

</dd> <dt>

<span data-ttu-id="1cda7-112">*最小值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1cda7-112">*min* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1cda7-113">計數器的最小值。</span><span class="sxs-lookup"><span data-stu-id="1cda7-113">Minimum value of the counter.</span></span>

</dd> <dt>

<span data-ttu-id="1cda7-114">*平均* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1cda7-114">*average* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1cda7-115">計數器的平均值。</span><span class="sxs-lookup"><span data-stu-id="1cda7-115">Average value of the counter.</span></span>

</dd> <dt>

<span data-ttu-id="1cda7-116">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1cda7-116">*status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1cda7-117">指出值是否有效。</span><span class="sxs-lookup"><span data-stu-id="1cda7-117">Indicates if the values are valid.</span></span>



| <span data-ttu-id="1cda7-118">值</span><span class="sxs-lookup"><span data-stu-id="1cda7-118">Value</span></span>                                                                                              | <span data-ttu-id="1cda7-119">意義</span><span class="sxs-lookup"><span data-stu-id="1cda7-119">Meaning</span></span>                              |
|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="1cda7-120"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1cda7-120"><dt>0</dt></span></span> </dl>                       | <span data-ttu-id="1cda7-121">值有效。</span><span class="sxs-lookup"><span data-stu-id="1cda7-121">The values are valid.</span></span><br/>     |
| <dl> <span data-ttu-id="1cda7-122"><dt>0xC0000BBA (3221228474) </dt></span><span class="sxs-lookup"><span data-stu-id="1cda7-122"><dt>0xC0000BBA (3221228474)</dt></span></span> </dl> | <span data-ttu-id="1cda7-123">值無效。</span><span class="sxs-lookup"><span data-stu-id="1cda7-123">The values are not valid.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cda7-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="1cda7-124">Return value</span></span>

<span data-ttu-id="1cda7-125">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="1cda7-125">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cda7-126">備註</span><span class="sxs-lookup"><span data-stu-id="1cda7-126">Remarks</span></span>

<span data-ttu-id="1cda7-127">只有在圖形視窗中顯示的計數器值會用來計算統計值。</span><span class="sxs-lookup"><span data-stu-id="1cda7-127">Only those counter values that are visible in the graph window are used to calculate the statistical values.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cda7-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="1cda7-128">Requirements</span></span>



| <span data-ttu-id="1cda7-129">需求</span><span class="sxs-lookup"><span data-stu-id="1cda7-129">Requirement</span></span> | <span data-ttu-id="1cda7-130">值</span><span class="sxs-lookup"><span data-stu-id="1cda7-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1cda7-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1cda7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1cda7-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1cda7-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="1cda7-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1cda7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1cda7-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1cda7-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1cda7-135">DLL</span><span class="sxs-lookup"><span data-stu-id="1cda7-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1cda7-136"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="1cda7-136"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cda7-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1cda7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cda7-138">**CounterItem**</span><span class="sxs-lookup"><span data-stu-id="1cda7-138">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="1cda7-139">**CounterItem.GetDataAt**</span><span class="sxs-lookup"><span data-stu-id="1cda7-139">**CounterItem.GetDataAt**</span></span>](counteritem-getdataat.md)
</dt> <dt>

[<span data-ttu-id="1cda7-140">**CounterItem**</span><span class="sxs-lookup"><span data-stu-id="1cda7-140">**CounterItem.GetValue**</span></span>](counteritem-getvalue.md)
</dt> </dl>

 

 





