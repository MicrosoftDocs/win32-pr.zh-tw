---
title: SystemMonitor CollectSample 方法
description: 針對計數器物件中的每個計數器取樣一個值。
ms.assetid: 4c91c759-597f-4aa8-aa77-eb181616e8b0
keywords:
- CollectSample 方法 SysMon
- CollectSample 方法 SysMon、SystemMonitor 介面
- SystemMonitor 介面 SysMon，CollectSample 方法
topic_type:
- apiref
api_name:
- SystemMonitor.CollectSample
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e1c269d044c17a2ec1322fa969e0c86f468a901
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465561"
---
# <a name="systemmonitorcollectsample-method"></a><span data-ttu-id="d3a90-106">SystemMonitor：： CollectSample 方法</span><span class="sxs-lookup"><span data-stu-id="d3a90-106">SystemMonitor::CollectSample method</span></span>

<span data-ttu-id="d3a90-107">針對 [**計數器**](counters.md) 物件中的每個計數器取樣一個值。</span><span class="sxs-lookup"><span data-stu-id="d3a90-107">Samples a value for each counter in the [**Counters**](counters.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3a90-108">語法</span><span class="sxs-lookup"><span data-stu-id="d3a90-108">Syntax</span></span>


```VB
Sub CollectSample()
```



## <a name="parameters"></a><span data-ttu-id="d3a90-109">參數</span><span class="sxs-lookup"><span data-stu-id="d3a90-109">Parameters</span></span>

<span data-ttu-id="d3a90-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d3a90-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d3a90-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d3a90-111">Return value</span></span>

<span data-ttu-id="d3a90-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d3a90-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3a90-113">備註</span><span class="sxs-lookup"><span data-stu-id="d3a90-113">Remarks</span></span>

<span data-ttu-id="d3a90-114">只有當 [**ManualUpdate**](systemmonitor-manualupdate.md)為 True，且您要從電腦目前的活動取樣計數器值時，才會呼叫 **CollectSample** ，而不會在從記錄檔取樣時使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="d3a90-114">Call **CollectSample** only if [**ManualUpdate**](systemmonitor-manualupdate.md) is True and you are sampling counter values from the current activity of the computer do not use this method when sampling from a log file.</span></span> <span data-ttu-id="d3a90-115">圖形或報表會以新的值更新。</span><span class="sxs-lookup"><span data-stu-id="d3a90-115">The graph or report is updated with the new value.</span></span> <span data-ttu-id="d3a90-116">請注意，某些圖形類型需要兩個範例，才能繪製資料（例如折線圖）。</span><span class="sxs-lookup"><span data-stu-id="d3a90-116">Note that some types of graphs need two samples in order to graph the data, for example, the line graph.</span></span>

<span data-ttu-id="d3a90-117">若要在收集樣本時接收通知，請執行 [**OnSampleCollected**](-systemmonitor-onsamplecollected.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="d3a90-117">To receive notification when the sample has been collected, implement the [**OnSampleCollected**](-systemmonitor-onsamplecollected.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3a90-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3a90-118">Requirements</span></span>



| <span data-ttu-id="d3a90-119">需求</span><span class="sxs-lookup"><span data-stu-id="d3a90-119">Requirement</span></span> | <span data-ttu-id="d3a90-120">值</span><span class="sxs-lookup"><span data-stu-id="d3a90-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d3a90-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d3a90-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d3a90-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3a90-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="d3a90-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d3a90-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d3a90-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3a90-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d3a90-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d3a90-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3a90-126"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="d3a90-126"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3a90-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3a90-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3a90-128">**計數器**</span><span class="sxs-lookup"><span data-stu-id="d3a90-128">**Counters**</span></span>](counters.md)
</dt> <dt>

[<span data-ttu-id="d3a90-129">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="d3a90-129">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





