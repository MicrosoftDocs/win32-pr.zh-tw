---
title: SystemMonitor. LogViewStart 屬性
description: 取得或設定用來從記錄檔抓取計數器值的開始日期。
ms.assetid: f9fdef17-e8b1-4efb-86db-40ca0c499194
keywords:
- LogViewStart 屬性 SysMon
- LogViewStart 屬性 SysMon、SystemMonitor 類別
- SystemMonitor 類別 SysMon，LogViewStart 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.LogViewStart
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 967c44940b195c4d8ddd3028e1d4f307827bbbfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934244"
---
# <a name="systemmonitorlogviewstart-property"></a><span data-ttu-id="ab87a-106">SystemMonitor. LogViewStart 屬性</span><span class="sxs-lookup"><span data-stu-id="ab87a-106">SystemMonitor.LogViewStart property</span></span>

<span data-ttu-id="ab87a-107">取得或設定用來從記錄檔抓取計數器值的開始日期。</span><span class="sxs-lookup"><span data-stu-id="ab87a-107">Retrieves or sets the starting date used to retrieve counter values from the log files.</span></span>

<span data-ttu-id="ab87a-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="ab87a-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab87a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab87a-109">Syntax</span></span>


```VB
Property LogViewStart As Date
```



## <a name="property-value"></a><span data-ttu-id="ab87a-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="ab87a-110">Property value</span></span>

<span data-ttu-id="ab87a-111">用來從記錄檔中取出計數器值的開始日期。</span><span class="sxs-lookup"><span data-stu-id="ab87a-111">Starting date used to retrieve counter values from the log files.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab87a-112">備註</span><span class="sxs-lookup"><span data-stu-id="ab87a-112">Remarks</span></span>

<span data-ttu-id="ab87a-113">SYSMON 會從開始和 SystemMonitor 中的記錄檔抓取計數器值（含） [**。**](systemmonitor-logviewstop.md)</span><span class="sxs-lookup"><span data-stu-id="ab87a-113">SYSMON retrieves counter values from the log files that falls within the start and [**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md) dates, inclusively.</span></span>

<span data-ttu-id="ab87a-114">如果您沒有指定開始日期，或是將這個屬性設定為在記錄檔中找到之日期值範圍以外的日期值，SYSMON 會將值變更為記錄檔中找到的最早日期值。</span><span class="sxs-lookup"><span data-stu-id="ab87a-114">If you do not specify a start date or if you set this property to a date value that is outside the range of date values found in the log files, SYSMON changes the value to the earliest date value found in the log files.</span></span>

<span data-ttu-id="ab87a-115">如果這個屬性設定為大於 [**LogViewStop**](systemmonitor-logviewstop.md)的日期值，則 SYSMON 會將值變更為 **LogViewStop** 的值。</span><span class="sxs-lookup"><span data-stu-id="ab87a-115">If this property is set to a date value that is greater than [**LogViewStop**](systemmonitor-logviewstop.md), SYSMON changes the value to the value of **LogViewStop**.</span></span>

<span data-ttu-id="ab87a-116">如果您指定開始和停止日期，則應該在設定 [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md)之前指定日期。</span><span class="sxs-lookup"><span data-stu-id="ab87a-116">If you specify a start and stop date, you should specify the dates before setting [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab87a-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab87a-117">Requirements</span></span>



| <span data-ttu-id="ab87a-118">需求</span><span class="sxs-lookup"><span data-stu-id="ab87a-118">Requirement</span></span> | <span data-ttu-id="ab87a-119">值</span><span class="sxs-lookup"><span data-stu-id="ab87a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ab87a-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ab87a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ab87a-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab87a-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ab87a-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ab87a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ab87a-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab87a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ab87a-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ab87a-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab87a-125"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="ab87a-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab87a-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab87a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab87a-127">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="ab87a-127">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="ab87a-128">**SystemMonitor.GetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="ab87a-128">**SystemMonitor.GetLogViewRange**</span></span>](systemmonitor-getlogviewrange.md)
</dt> <dt>

[<span data-ttu-id="ab87a-129">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="ab87a-129">**SystemMonitor.LogFiles**</span></span>](systemmonitor-logfiles.md)
</dt> <dt>

[<span data-ttu-id="ab87a-130">**SystemMonitor.LogViewStop**</span><span class="sxs-lookup"><span data-stu-id="ab87a-130">**SystemMonitor.LogViewStop**</span></span>](systemmonitor-logviewstop.md)
</dt> <dt>

[<span data-ttu-id="ab87a-131">**SystemMonitor.LogSourceStartTime**</span><span class="sxs-lookup"><span data-stu-id="ab87a-131">**SystemMonitor.LogSourceStartTime**</span></span>](systemmonitor-logsourcestarttime.md)
</dt> <dt>

[<span data-ttu-id="ab87a-132">**SystemMonitor.SetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="ab87a-132">**SystemMonitor.SetLogViewRange**</span></span>](systemmonitor-setlogviewrange.md)
</dt> </dl>

 

 





