---
title: SystemMonitor. MonitorDuplicateInstances 屬性
description: 抓取或設定值，這個值會決定是否可以監視計數器的多個實例。
ms.assetid: fe8d6074-eb29-4093-9f79-39e6171a3a3f
keywords:
- MonitorDuplicateInstances 屬性 SysMon
- MonitorDuplicateInstances 屬性 SysMon、SystemMonitor 類別
- SystemMonitor 類別 SysMon，MonitorDuplicateInstances 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.MonitorDuplicateInstances
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6ae53d0a1dcf3f67a43dab7959bb42619ace6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384454"
---
# <a name="systemmonitormonitorduplicateinstances-property"></a><span data-ttu-id="badf9-106">SystemMonitor. MonitorDuplicateInstances 屬性</span><span class="sxs-lookup"><span data-stu-id="badf9-106">SystemMonitor.MonitorDuplicateInstances property</span></span>

<span data-ttu-id="badf9-107">抓取或設定值，這個值會決定是否可以監視計數器的多個實例。</span><span class="sxs-lookup"><span data-stu-id="badf9-107">Retrieves or sets a value that determines whether multiple instances of a counter can be monitored.</span></span>

<span data-ttu-id="badf9-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="badf9-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="badf9-109">語法</span><span class="sxs-lookup"><span data-stu-id="badf9-109">Syntax</span></span>


```VB
Property MonitorDuplicateInstances As Boolean
```



## <a name="property-value"></a><span data-ttu-id="badf9-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="badf9-110">Property value</span></span>

<span data-ttu-id="badf9-111">True 表示可以監視計數器的多個實例， (True 是預設) 。</span><span class="sxs-lookup"><span data-stu-id="badf9-111">True indicates that multiple instances of a counter can be monitored (True is the default).</span></span> <span data-ttu-id="badf9-112">False 表示只能監視一個計數器的實例。</span><span class="sxs-lookup"><span data-stu-id="badf9-112">False indicates that only one instance of a counter can be monitored.</span></span>

## <a name="remarks"></a><span data-ttu-id="badf9-113">備註</span><span class="sxs-lookup"><span data-stu-id="badf9-113">Remarks</span></span>

<span data-ttu-id="badf9-114">\#如果有多個實例，則系統監視器會將 n 附加至每個實例名稱，但第一個名稱除外。</span><span class="sxs-lookup"><span data-stu-id="badf9-114">System Monitor appends \#n to every instance name, except the first, if multiple instances exist.</span></span> <span data-ttu-id="badf9-115">序號（n）會以1開始，並為每個新的實例遞增一。</span><span class="sxs-lookup"><span data-stu-id="badf9-115">The serial number, n, begins with one and is incremented by one for each new instance.</span></span> <span data-ttu-id="badf9-116">例如，如果您指定「 \\ 處理 (\*) \\ % 處理器時間」，則計數器集合應該包含 svchost 的多個實例。</span><span class="sxs-lookup"><span data-stu-id="badf9-116">For example, if you specify "\\Process(\*)\\% Processor Time", the counter collection should contain multiple instances of svchost.</span></span> <span data-ttu-id="badf9-117">第一次出現的是 svchost，下一次出現的是 svchost \# 1，依此類推。</span><span class="sxs-lookup"><span data-stu-id="badf9-117">The first occurrence will be svchost, the next occurrence will be svchost\#1, and so on.</span></span>

<span data-ttu-id="badf9-118">只有當您使用萬用字元 (\*) 作為實例名稱時，才會監視重複的實例。</span><span class="sxs-lookup"><span data-stu-id="badf9-118">Duplicate instances are monitored only if you use the wildcard character (\*) for the instance name.</span></span> <span data-ttu-id="badf9-119">如果您指定「 \\ 進程 (svchost) \\ % 處理器時間」，則只會監視找到的 svchost 第一個實例，而不是所有 svchost 實例。</span><span class="sxs-lookup"><span data-stu-id="badf9-119">If you specified "\\Process(svchost)\\% Processor Time" only the first instance found of svchost is monitored, not all instances of svchost.</span></span>

## <a name="requirements"></a><span data-ttu-id="badf9-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="badf9-120">Requirements</span></span>



| <span data-ttu-id="badf9-121">需求</span><span class="sxs-lookup"><span data-stu-id="badf9-121">Requirement</span></span> | <span data-ttu-id="badf9-122">值</span><span class="sxs-lookup"><span data-stu-id="badf9-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="badf9-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="badf9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="badf9-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="badf9-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="badf9-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="badf9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="badf9-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="badf9-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="badf9-127">DLL</span><span class="sxs-lookup"><span data-stu-id="badf9-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="badf9-128"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="badf9-128"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="badf9-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="badf9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="badf9-130">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="badf9-130">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





