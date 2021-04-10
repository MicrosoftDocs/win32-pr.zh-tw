---
title: SystemMonitor. UpdateInterval 屬性
description: 抓取或設定 SYSMON 在下一次收集計數器資料並更新圖表或報表之前等候的時間長度。
ms.assetid: 297931e4-23ae-4384-a04a-9c1fa8aa1239
keywords:
- UpdateInterval 屬性 SysMon
- UpdateInterval 屬性 SysMon、SystemMonitor 類別
- SystemMonitor 類別 SysMon，UpdateInterval 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.UpdateInterval
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5872f870e831896ff37157a4a0f47584e77d93c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934299"
---
# <a name="systemmonitorupdateinterval-property"></a><span data-ttu-id="e7f53-106">SystemMonitor. UpdateInterval 屬性</span><span class="sxs-lookup"><span data-stu-id="e7f53-106">SystemMonitor.UpdateInterval property</span></span>

<span data-ttu-id="e7f53-107">抓取或設定 SYSMON 在下一次收集計數器資料並更新圖表或報表之前等候的時間長度。</span><span class="sxs-lookup"><span data-stu-id="e7f53-107">Retrieves or sets the length of time that SYSMON waits before the next time it collects counter data and updates the graph or report.</span></span>

<span data-ttu-id="e7f53-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="e7f53-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7f53-109">語法</span><span class="sxs-lookup"><span data-stu-id="e7f53-109">Syntax</span></span>


```VB
Property UpdateInterval As Single
```



## <a name="property-value"></a><span data-ttu-id="e7f53-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="e7f53-110">Property value</span></span>

<span data-ttu-id="e7f53-111">SYSMON 時間長度（以秒為單位），這是在下一次收集計數器資料並更新圖表或報表之前等候的時間長度。</span><span class="sxs-lookup"><span data-stu-id="e7f53-111">Length of time, in seconds, that SYSMON waits before the next time it collects counter data and updates the graph or report.</span></span> <span data-ttu-id="e7f53-112">最小間隔為1秒 (這也是) 的預設值。</span><span class="sxs-lookup"><span data-stu-id="e7f53-112">The minimum interval is 1 second (this is also the default value).</span></span> <span data-ttu-id="e7f53-113">最大值為1000000。</span><span class="sxs-lookup"><span data-stu-id="e7f53-113">The maximum value is 1,000,000.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7f53-114">備註</span><span class="sxs-lookup"><span data-stu-id="e7f53-114">Remarks</span></span>

<span data-ttu-id="e7f53-115">只有當 [**SystemMonitor. ManualUpdate**](systemmonitor-manualupdate.md) 設定為 False 時，這個屬性才會相關。</span><span class="sxs-lookup"><span data-stu-id="e7f53-115">This property is relevant only when [**SystemMonitor.ManualUpdate**](systemmonitor-manualupdate.md) is set to False.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7f53-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7f53-116">Requirements</span></span>



| <span data-ttu-id="e7f53-117">需求</span><span class="sxs-lookup"><span data-stu-id="e7f53-117">Requirement</span></span> | <span data-ttu-id="e7f53-118">值</span><span class="sxs-lookup"><span data-stu-id="e7f53-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7f53-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e7f53-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e7f53-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7f53-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e7f53-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e7f53-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e7f53-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7f53-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e7f53-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e7f53-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7f53-124"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="e7f53-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7f53-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7f53-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7f53-126">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="e7f53-126">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





