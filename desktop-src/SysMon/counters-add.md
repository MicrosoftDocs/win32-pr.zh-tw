---
title: 計數器。 Add 方法
description: 將 CounterItem 實例加入至集合。
ms.assetid: 9daecfe6-c2a9-48af-8b59-4f81f0325535
keywords:
- 新增方法 SysMon
- Add 方法 SysMon，計數器類別
- 計數器類別 SysMon，Add 方法
topic_type:
- apiref
api_name:
- Counters.Add
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e6c974c5df6f531cd75292290c61534a923e5be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464716"
---
# <a name="countersadd-method"></a><span data-ttu-id="20629-106">計數器。 Add 方法</span><span class="sxs-lookup"><span data-stu-id="20629-106">Counters.Add method</span></span>

<span data-ttu-id="20629-107">將 [**CounterItem**](counteritem.md) 實例加入至集合。</span><span class="sxs-lookup"><span data-stu-id="20629-107">Adds a [**CounterItem**](counteritem.md) instance to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="20629-108">語法</span><span class="sxs-lookup"><span data-stu-id="20629-108">Syntax</span></span>


```VB
Counters.Add( _
  ByVal pathname As String _
) As CounterItem
```



## <a name="parameters"></a><span data-ttu-id="20629-109">參數</span><span class="sxs-lookup"><span data-stu-id="20629-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20629-110">*路徑名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="20629-110">*pathname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20629-111">計數器的路徑。</span><span class="sxs-lookup"><span data-stu-id="20629-111">Path to the counter.</span></span> <span data-ttu-id="20629-112">路徑可以包含電腦名稱稱，且必須包含效能物件名稱、物件實例名稱（如果指定的效能物件支援多個實例）和計數器名稱。</span><span class="sxs-lookup"><span data-stu-id="20629-112">The path can include a machine name, and must include a performance object name, an object instance name if the specified performance object supports multiple instances, and a counter name.</span></span> <span data-ttu-id="20629-113">此路徑規格不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="20629-113">This path specification is not case-sensitive.</span></span>

<span data-ttu-id="20629-114">如需指定計數器路徑的詳細資訊，請參閱 [指定計數器路徑](/windows/desktop/PerfCtrs/specifying-a-counter-path)。</span><span class="sxs-lookup"><span data-stu-id="20629-114">For details on specifying a counter path, see [Specifying a Counter Path](/windows/desktop/PerfCtrs/specifying-a-counter-path).</span></span>

</dd> </dl>

## <a name="exceptions"></a><span data-ttu-id="20629-115">例外狀況</span><span class="sxs-lookup"><span data-stu-id="20629-115">Exceptions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="20629-116">例外狀況類型</span><span class="sxs-lookup"><span data-stu-id="20629-116">Exception type</span></span></th>
<th><span data-ttu-id="20629-117">條件</span><span class="sxs-lookup"><span data-stu-id="20629-117">Condition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="20629-118"><strong>System.runtime.interopservices.outattribute. COMException</strong></span><span class="sxs-lookup"><span data-stu-id="20629-118"><strong>System.Runtime.InteropServices.COMException</strong></span></span></td>
<td><span data-ttu-id="20629-119">您可能會因為下列其中一個原因而收到此例外狀況：</span><span class="sxs-lookup"><span data-stu-id="20629-119">You can receive this exception for one of the following reasons:</span></span>
<ul>
<li><span data-ttu-id="20629-120">在電腦上找不到指定的效能物件。</span><span class="sxs-lookup"><span data-stu-id="20629-120">The specified performance object was not found on the computer.</span></span> <span data-ttu-id="20629-121">Err 值為0xC0000BB8。</span><span class="sxs-lookup"><span data-stu-id="20629-121">The Err.Number value is 0xC0000BB8.</span></span></li>
<li><span data-ttu-id="20629-122">找不到指定的計數器。</span><span class="sxs-lookup"><span data-stu-id="20629-122">The specified counter could not be found.</span></span> <span data-ttu-id="20629-123">Err 值為0xC0000BB9。</span><span class="sxs-lookup"><span data-stu-id="20629-123">The Err.Number value is 0xC0000BB9.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="20629-124">備註</span><span class="sxs-lookup"><span data-stu-id="20629-124">Remarks</span></span>

<span data-ttu-id="20629-125">如果您在 *pathname* 參數中指定萬用字元計數器， **Add** 方法會為每個展開的路徑建立一個 [**CounterItem**](counteritem.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="20629-125">If you specify a wildcard counter in the *pathname* parameter, the **Add** method creates one [**CounterItem**](counteritem.md) object for each expanded path.</span></span> <span data-ttu-id="20629-126">然後， **Add** 方法會傳回第一個加入之 **CounterItem** 的指標。</span><span class="sxs-lookup"><span data-stu-id="20629-126">The **Add** method then returns a pointer to the first added **CounterItem**.</span></span>

<span data-ttu-id="20629-127">如果萬用字元會產生重複的計數器，就不會報告錯誤，也不會建立重複的結果。</span><span class="sxs-lookup"><span data-stu-id="20629-127">If the wildcard would result in a duplicate counter, the error is not reported and no duplicate is created.</span></span> <span data-ttu-id="20629-128">如果在建立所有計數器之前發生錯誤狀況，則會報告錯誤，並不會建立剩餘的計數器。</span><span class="sxs-lookup"><span data-stu-id="20629-128">If an error condition occurs before all counters are created, the error is reported and the remaining counters are not created.</span></span>

<span data-ttu-id="20629-129">您可以新增的計數器數目沒有任何限制;不過，SYSMON 只會圖表集合中的第一個1024計數器。</span><span class="sxs-lookup"><span data-stu-id="20629-129">There is no limit to the number of counters that you can add; however, SYSMON will graph only the first 1,024 counters in the collection.</span></span> <span data-ttu-id="20629-130">SYSMON 將在報表中顯示的計數器數目沒有任何限制。</span><span class="sxs-lookup"><span data-stu-id="20629-130">There is no limit on the number of counters that SYSMON will display in a report.</span></span>

<span data-ttu-id="20629-131">若要在加入計數器時接收通知，請執行 [OnCounterAdded](systemmonitor-oncounteradded.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="20629-131">To receive notification when a counter is added, implement the [OnCounterAdded](systemmonitor-oncounteradded.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="20629-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="20629-132">Requirements</span></span>



| <span data-ttu-id="20629-133">需求</span><span class="sxs-lookup"><span data-stu-id="20629-133">Requirement</span></span> | <span data-ttu-id="20629-134">值</span><span class="sxs-lookup"><span data-stu-id="20629-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="20629-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="20629-135">Minimum supported client</span></span><br/> | <span data-ttu-id="20629-136">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="20629-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="20629-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="20629-137">Minimum supported server</span></span><br/> | <span data-ttu-id="20629-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="20629-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="20629-139">DLL</span><span class="sxs-lookup"><span data-stu-id="20629-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20629-140"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="20629-140"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20629-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="20629-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20629-142">**CounterItem**</span><span class="sxs-lookup"><span data-stu-id="20629-142">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="20629-143">**計數器**</span><span class="sxs-lookup"><span data-stu-id="20629-143">**Counters**</span></span>](counters.md)
</dt> <dt>

[<span data-ttu-id="20629-144">**SystemMonitor.BrowseCounters**</span><span class="sxs-lookup"><span data-stu-id="20629-144">**SystemMonitor.BrowseCounters**</span></span>](systemmonitor-browsecounters.md)
</dt> </dl>

 

