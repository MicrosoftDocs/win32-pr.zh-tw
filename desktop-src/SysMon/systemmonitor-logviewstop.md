---
title: SystemMonitor. LogViewStop 屬性
description: 取得或設定用來從記錄檔抓取計數器值的結束日期。
ms.assetid: 5dabfb26-fa33-4fb5-a075-ed8955a56f1e
keywords:
- LogViewStop 屬性 SysMon
- LogViewStop 屬性 SysMon，SystemMonitor 物件
- SystemMonitor 物件 SysMon，LogViewStop 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.LogViewStop
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b725ee2efba22453d44f1e15fb9ce231b07cdb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934336"
---
# <a name="systemmonitorlogviewstop-property"></a><span data-ttu-id="e7e03-106">SystemMonitor. LogViewStop 屬性</span><span class="sxs-lookup"><span data-stu-id="e7e03-106">SystemMonitor.LogViewStop property</span></span>

<span data-ttu-id="e7e03-107">取得或設定用來從記錄檔抓取計數器值的結束日期。</span><span class="sxs-lookup"><span data-stu-id="e7e03-107">Retrieves or sets the ending date used to retrieve counter values from the log files.</span></span>

<span data-ttu-id="e7e03-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="e7e03-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7e03-109">語法</span><span class="sxs-lookup"><span data-stu-id="e7e03-109">Syntax</span></span>


```VB
Property LogViewStop As Date
```



## <a name="property-value"></a><span data-ttu-id="e7e03-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="e7e03-110">Property value</span></span>

<span data-ttu-id="e7e03-111">用來從記錄檔中取出計數器值的結束日期。</span><span class="sxs-lookup"><span data-stu-id="e7e03-111">Ending date used to retrieve counter values from the log files.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7e03-112">備註</span><span class="sxs-lookup"><span data-stu-id="e7e03-112">Remarks</span></span>

<span data-ttu-id="e7e03-113">SYSMON 會從 [**SystemMonitor LogViewStart**](systemmonitor-logviewstart.md) 和停止日期中的記錄檔抓取計數器值（含）。</span><span class="sxs-lookup"><span data-stu-id="e7e03-113">SYSMON retrieves counter values from the log files that falls within the [**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md) and stop dates, inclusively.</span></span>

<span data-ttu-id="e7e03-114">如果您未指定停止值，或將此屬性設定為晚于記錄檔中所包含之最後一個日期的日期值，則 SYSMON 會將此值變更為在記錄檔中找到的最新日期值。</span><span class="sxs-lookup"><span data-stu-id="e7e03-114">If you do not specify a stop value or you set this property to a date value that is later than the last date contained in the log file, SYSMON changes the value to the latest date value found in the log files.</span></span>

<span data-ttu-id="e7e03-115">如果這個屬性設定為小於 [**LogViewStart**](systemmonitor-logviewstart.md)的日期值，則 SYSMON 會將值變更為 **LogViewStart** 的值。</span><span class="sxs-lookup"><span data-stu-id="e7e03-115">If this property is set to a date value that is less than [**LogViewStart**](systemmonitor-logviewstart.md), SYSMON changes the value to the value of **LogViewStart**.</span></span>

<span data-ttu-id="e7e03-116">您必須在設定停止日期之前設定開始日期;否則，這兩個值會設定為 MinValue，如果您在設定 [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md)之後設定日期，則只會從記錄檔中取出第一個計數器值。</span><span class="sxs-lookup"><span data-stu-id="e7e03-116">You must set the start date before you set the stop date; otherwise, both values are set to Date.MinValue, and if you set the dates after setting [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md), then only the first counter value is retrieved from the log file.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7e03-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7e03-117">Requirements</span></span>



| <span data-ttu-id="e7e03-118">需求</span><span class="sxs-lookup"><span data-stu-id="e7e03-118">Requirement</span></span> | <span data-ttu-id="e7e03-119">值</span><span class="sxs-lookup"><span data-stu-id="e7e03-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7e03-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e7e03-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e7e03-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7e03-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e7e03-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e7e03-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e7e03-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7e03-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e7e03-124">DLL</span><span class="sxs-lookup"><span data-stu-id="e7e03-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7e03-125"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="e7e03-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7e03-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7e03-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7e03-127">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="e7e03-127">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="e7e03-128">**SystemMonitor.GetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="e7e03-128">**SystemMonitor.GetLogViewRange**</span></span>](systemmonitor-getlogviewrange.md)
</dt> <dt>

[<span data-ttu-id="e7e03-129">**SystemMonitor.LogSourceStopTime**</span><span class="sxs-lookup"><span data-stu-id="e7e03-129">**SystemMonitor.LogSourceStopTime**</span></span>](systemmonitor-logsourcestoptime.md)
</dt> <dt>

[<span data-ttu-id="e7e03-130">**SystemMonitor.LogViewStart**</span><span class="sxs-lookup"><span data-stu-id="e7e03-130">**SystemMonitor.LogViewStart**</span></span>](systemmonitor-logviewstart.md)
</dt> <dt>

[<span data-ttu-id="e7e03-131">**SystemMonitor.SetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="e7e03-131">**SystemMonitor.SetLogViewRange**</span></span>](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





