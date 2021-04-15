---
title: SystemMonitor. LogFileName 屬性
description: 抓取或設定要做為系統監視器中顯示的計數器值來源之記錄檔的名稱。
ms.assetid: a93d1c98-4875-4d8e-940c-4443d1e585e6
keywords:
- LogFileName 屬性 SysMon
- LogFileName 屬性 SysMon、SystemMonitor 類別
- SystemMonitor 類別 SysMon，LogFileName 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.LogFileName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf9d6168f416d1bdab47a4c2952ac60ee7e67397
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384705"
---
# <a name="systemmonitorlogfilename-property"></a><span data-ttu-id="b0171-106">SystemMonitor. LogFileName 屬性</span><span class="sxs-lookup"><span data-stu-id="b0171-106">SystemMonitor.LogFileName property</span></span>

<span data-ttu-id="b0171-107">抓取或設定要做為系統監視器中顯示的計數器值來源之記錄檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="b0171-107">Retrieves or sets the name of a log file to use as the source of counter values displayed in the System Monitor.</span></span>

> [!Note]  
> <span data-ttu-id="b0171-108">記錄 [**檔屬性已使此屬性過時**](systemmonitor-logfiles.md) 。</span><span class="sxs-lookup"><span data-stu-id="b0171-108">This property has been made obsolete by the [**LogFiles**](systemmonitor-logfiles.md) property.</span></span>

 

<span data-ttu-id="b0171-109">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="b0171-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0171-110">語法</span><span class="sxs-lookup"><span data-stu-id="b0171-110">Syntax</span></span>


```VB
Property LogFileName As String
```



## <a name="property-value"></a><span data-ttu-id="b0171-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="b0171-111">Property value</span></span>

<span data-ttu-id="b0171-112">記錄檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="b0171-112">Path to the log file.</span></span> <span data-ttu-id="b0171-113">您可以指定絕對、相對或 UNC 路徑。</span><span class="sxs-lookup"><span data-stu-id="b0171-113">You can specify an absolute, relative, or UNC path.</span></span> <span data-ttu-id="b0171-114">記錄檔副檔名必須是 .csv、tsv 或 .blg。</span><span class="sxs-lookup"><span data-stu-id="b0171-114">The log file name extension must be either .csv, .tsv, or .blg.</span></span>

## <a name="exceptions"></a><span data-ttu-id="b0171-115">例外狀況</span><span class="sxs-lookup"><span data-stu-id="b0171-115">Exceptions</span></span>



| <span data-ttu-id="b0171-116">例外狀況類型</span><span class="sxs-lookup"><span data-stu-id="b0171-116">Exception type</span></span>                                  | <span data-ttu-id="b0171-117">條件</span><span class="sxs-lookup"><span data-stu-id="b0171-117">Condition</span></span>                                                              |
|-------------------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="b0171-118">**System.runtime.interopservices.outattribute. COMException**</span><span class="sxs-lookup"><span data-stu-id="b0171-118">**System.Runtime.InteropServices.COMException**</span></span> | <span data-ttu-id="b0171-119">找不到指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="b0171-119">Unable to find the specified file.</span></span> <span data-ttu-id="b0171-120">Err 值為0xC0000BD1。</span><span class="sxs-lookup"><span data-stu-id="b0171-120">The Err.Number value is 0xC0000BD1.</span></span> |
| <span data-ttu-id="b0171-121">**System. ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="b0171-121">**System.ArgumentException**</span></span>                    | <span data-ttu-id="b0171-122">您不能指定空字串。</span><span class="sxs-lookup"><span data-stu-id="b0171-122">You cannot specify an empty string.</span></span>                                    |



 

## <a name="remarks"></a><span data-ttu-id="b0171-123">備註</span><span class="sxs-lookup"><span data-stu-id="b0171-123">Remarks</span></span>

<span data-ttu-id="b0171-124">這個屬性會從記錄 [**檔集合的**](systemmonitor-logfiles.md) 第一個成員傳回記錄檔名稱。</span><span class="sxs-lookup"><span data-stu-id="b0171-124">This property returns the log file name from the first member of the [**LogFiles**](systemmonitor-logfiles.md) collection.</span></span>

<span data-ttu-id="b0171-125">如果記錄檔集合包含一或多個 [**成員，則**](systemmonitor-logfiles.md) 設定這個屬性將會失敗。</span><span class="sxs-lookup"><span data-stu-id="b0171-125">Setting this property will fail if the [**LogFiles**](systemmonitor-logfiles.md) collection contains one or more members.</span></span>

<span data-ttu-id="b0171-126">您必須使用 Logman.exe 工具或 Perfmon MMC 嵌入式管理單元來產生您新增至此集合的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="b0171-126">You must use the Logman.exe tool or the Perfmon.msc MMC snap-in to generate the log files that you add to this collection.</span></span> <span data-ttu-id="b0171-127">針對 Perfmon，計數器記錄檔位於 **效能記錄檔及警示** 下。</span><span class="sxs-lookup"><span data-stu-id="b0171-127">For Perfmon.msc, the counter logs are located under **Performance Logs and Alerts**.</span></span> <span data-ttu-id="b0171-128">如需有關使用 Logman.exe 或 Perfmon 的詳細資訊，請在 **說明及支援中心** 中分別搜尋 Logman 或使用效能。</span><span class="sxs-lookup"><span data-stu-id="b0171-128">For details on using Logman.exe or Perfmon.msc, search for Logman or Using Performance, respectively, in the **Help and Support Center**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0171-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0171-129">Requirements</span></span>



| <span data-ttu-id="b0171-130">需求</span><span class="sxs-lookup"><span data-stu-id="b0171-130">Requirement</span></span> | <span data-ttu-id="b0171-131">值</span><span class="sxs-lookup"><span data-stu-id="b0171-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b0171-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b0171-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b0171-133">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0171-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b0171-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b0171-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b0171-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0171-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b0171-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b0171-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0171-137"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="b0171-137"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0171-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b0171-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0171-139">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="b0171-139">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="b0171-140">**SystemMonitor. DataSourceType**</span><span class="sxs-lookup"><span data-stu-id="b0171-140">**SystemMonitor.DataSourceType**</span></span>](systemmonitor-datasourcetype.md)
</dt> </dl>

 

 





