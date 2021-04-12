---
title: SystemMonitor. SetLogViewRange 方法
description: 設定用來從記錄檔中取出計數器值的開始日期。
ms.assetid: ced641d0-cf71-4826-8ff0-c05f20a71aaa
keywords:
- SetLogViewRange 方法 SysMon
- SetLogViewRange 方法 SysMon，SystemMonitor 物件
- SystemMonitor 物件 SysMon，SetLogViewRange 方法
topic_type:
- apiref
api_name:
- SystemMonitor.SetLogViewRange
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 534a7dc3bf711832ec99e4202f4f56cc347f336b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384241"
---
# <a name="systemmonitorsetlogviewrange-method"></a><span data-ttu-id="83eb7-106">SystemMonitor. SetLogViewRange 方法</span><span class="sxs-lookup"><span data-stu-id="83eb7-106">SystemMonitor.SetLogViewRange method</span></span>

<span data-ttu-id="83eb7-107">設定用來從記錄檔中取出計數器值的開始日期。</span><span class="sxs-lookup"><span data-stu-id="83eb7-107">Sets the starting date used to retrieve counter values from the log files.</span></span>

## <a name="syntax"></a><span data-ttu-id="83eb7-108">語法</span><span class="sxs-lookup"><span data-stu-id="83eb7-108">Syntax</span></span>


```VB
SystemMonitor.SetLogViewRange( _
  ByVal StartTime As Date, _
  ByVal StopTime As Date _
)
```



## <a name="parameters"></a><span data-ttu-id="83eb7-109">參數</span><span class="sxs-lookup"><span data-stu-id="83eb7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83eb7-110">*StartTime* \[在\]</span><span class="sxs-lookup"><span data-stu-id="83eb7-110">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83eb7-111">用來從記錄檔中取出計數器值的開始日期。</span><span class="sxs-lookup"><span data-stu-id="83eb7-111">Starting date used to retrieve counter values from the log files.</span></span>

</dd> <dt>

<span data-ttu-id="83eb7-112">*StopTime* \[在\]</span><span class="sxs-lookup"><span data-stu-id="83eb7-112">*StopTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83eb7-113">用來從記錄檔中取出計數器值的結束日期。</span><span class="sxs-lookup"><span data-stu-id="83eb7-113">Ending date used to retrieve counter values from the log files.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83eb7-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="83eb7-114">Return value</span></span>

<span data-ttu-id="83eb7-115">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="83eb7-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="83eb7-116">備註</span><span class="sxs-lookup"><span data-stu-id="83eb7-116">Remarks</span></span>

<span data-ttu-id="83eb7-117">SYSMON 會從開始和停止日期內的記錄檔抓取計數器值（含）。</span><span class="sxs-lookup"><span data-stu-id="83eb7-117">SYSMON retrieves counter values from the log files that falls within the start and stop dates, inclusively.</span></span>

<span data-ttu-id="83eb7-118">如果您未指定開始日期，或是將開始日期設定為在記錄檔中找到的日期值範圍之外的日期值，SYSMON 會將值變更為記錄檔中找到的最早日期值。</span><span class="sxs-lookup"><span data-stu-id="83eb7-118">If you do not specify a start date or if you set the start date to a date value that is outside the range of date values found in the log files, SYSMON changes the value to the earliest date value found in the log files.</span></span> <span data-ttu-id="83eb7-119">如果開始值大於停止值，SYSMON 會將開始值變更為與停止值相同的值。</span><span class="sxs-lookup"><span data-stu-id="83eb7-119">If the start value is greater than the stop value, SYSMON changes the start value to be the same value as the stop value.</span></span>

<span data-ttu-id="83eb7-120">如果您未指定停止值，或將 [停用] 值設定為晚于記錄檔中所包含之最後一個日期的日期值，則 SYSMON 會將此值變更為記錄檔中找到的最新日期值。</span><span class="sxs-lookup"><span data-stu-id="83eb7-120">If you do not specify a stop value or you set the stop value to a date value that is later than the last date contained in the log file, SYSMON changes the value to the latest date value found in the log files.</span></span> <span data-ttu-id="83eb7-121">如果停止值小於停止值，SYSMON 會將停止值變更為與開始值相同的值。</span><span class="sxs-lookup"><span data-stu-id="83eb7-121">If the stop value is less than the stop value, SYSMON changes the stop value to be the same value as the start value.</span></span>

<span data-ttu-id="83eb7-122">如果您指定開始和停止日期，則應該在設定 [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md)之前指定日期。</span><span class="sxs-lookup"><span data-stu-id="83eb7-122">If you specify a start and stop date, you should specify the dates before setting [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md).</span></span> <span data-ttu-id="83eb7-123">如果您在設定 **SystemMonitor. DataSourceType** 之後設定日期，則只會從記錄檔中取出第一個計數器值。</span><span class="sxs-lookup"><span data-stu-id="83eb7-123">If you set the dates after setting **SystemMonitor.DataSourceType**, then only the first counter value is retrieved from the log file.</span></span>

## <a name="requirements"></a><span data-ttu-id="83eb7-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="83eb7-124">Requirements</span></span>



| <span data-ttu-id="83eb7-125">需求</span><span class="sxs-lookup"><span data-stu-id="83eb7-125">Requirement</span></span> | <span data-ttu-id="83eb7-126">值</span><span class="sxs-lookup"><span data-stu-id="83eb7-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83eb7-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="83eb7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="83eb7-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="83eb7-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="83eb7-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="83eb7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="83eb7-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="83eb7-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="83eb7-131">DLL</span><span class="sxs-lookup"><span data-stu-id="83eb7-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83eb7-132"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="83eb7-132"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83eb7-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="83eb7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83eb7-134">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="83eb7-134">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="83eb7-135">**SystemMonitor.GetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="83eb7-135">**SystemMonitor.GetLogViewRange**</span></span>](systemmonitor-getlogviewrange.md)
</dt> </dl>

 

 





