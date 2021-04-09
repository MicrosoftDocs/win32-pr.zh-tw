---
title: SystemMonitor BrowseCounters 方法
description: 顯示 [新增計數器] 對話方塊。
ms.assetid: 7edc4a80-4a04-49fd-b383-b892e1e16215
keywords:
- BrowseCounters 方法 SysMon
- BrowseCounters 方法 SysMon、SystemMonitor 介面
- SystemMonitor 介面 SysMon，BrowseCounters 方法
topic_type:
- apiref
api_name:
- SystemMonitor.BrowseCounters
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96df5d50ab9fc89963f9d09f4c0cb92479b4ecac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024552"
---
# <a name="systemmonitorbrowsecounters-method"></a><span data-ttu-id="bddcb-106">SystemMonitor：： BrowseCounters 方法</span><span class="sxs-lookup"><span data-stu-id="bddcb-106">SystemMonitor::BrowseCounters method</span></span>

<span data-ttu-id="bddcb-107">顯示 [ **新增計數器** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="bddcb-107">Displays the **Add Counters** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="bddcb-108">語法</span><span class="sxs-lookup"><span data-stu-id="bddcb-108">Syntax</span></span>


```VB
Sub BrowseCounters()
```



## <a name="parameters"></a><span data-ttu-id="bddcb-109">參數</span><span class="sxs-lookup"><span data-stu-id="bddcb-109">Parameters</span></span>

<span data-ttu-id="bddcb-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="bddcb-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bddcb-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="bddcb-111">Return value</span></span>

<span data-ttu-id="bddcb-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="bddcb-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bddcb-113">備註</span><span class="sxs-lookup"><span data-stu-id="bddcb-113">Remarks</span></span>

<span data-ttu-id="bddcb-114">此對話方塊可讓使用者從效能物件清單中選取本機或遠端效能計數器。</span><span class="sxs-lookup"><span data-stu-id="bddcb-114">This dialog box lets the user select local or remote performance counters from a list of performance objects.</span></span> <span data-ttu-id="bddcb-115">選取的計數器會新增至 [**計數器**](counters.md) 集合，並顯示于圖形或報表中。</span><span class="sxs-lookup"><span data-stu-id="bddcb-115">The selected counters are added to the [**Counters**](counters.md) collection and displayed in the graph or report.</span></span>

<span data-ttu-id="bddcb-116">若要在加入計數器時接收通知，請執行 [**OnCounterAdded**](systemmonitor-oncounteradded.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="bddcb-116">To receive notification when a counter is added, implement the [**OnCounterAdded**](systemmonitor-oncounteradded.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="bddcb-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="bddcb-117">Requirements</span></span>



| <span data-ttu-id="bddcb-118">需求</span><span class="sxs-lookup"><span data-stu-id="bddcb-118">Requirement</span></span> | <span data-ttu-id="bddcb-119">值</span><span class="sxs-lookup"><span data-stu-id="bddcb-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bddcb-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bddcb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bddcb-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bddcb-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="bddcb-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bddcb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bddcb-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bddcb-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bddcb-124">DLL</span><span class="sxs-lookup"><span data-stu-id="bddcb-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bddcb-125"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="bddcb-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bddcb-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bddcb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bddcb-127">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="bddcb-127">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="bddcb-128">**計數器。新增**</span><span class="sxs-lookup"><span data-stu-id="bddcb-128">**Counters.Add**</span></span>](counters-add.md)
</dt> </dl>

 

 





