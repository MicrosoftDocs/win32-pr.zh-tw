---
title: LogFiles 物件 (Isysmon.h)
description: 您可以使用這個類別來管理一個或多個包含效能計數器資料之記錄檔的集合。若要取出這個物件，請呼叫 SystemMonitor。
ms.assetid: 1af475c5-ed0c-49b4-a558-13eb8758a986
keywords:
- 記錄檔物件 SysMon
- 記錄檔物件 SysMon，描述
topic_type:
- apiref
api_name:
- LogFiles
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab30de5c371c012e1320950e4a491021bb0b15c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464197"
---
# <a name="logfiles-object"></a><span data-ttu-id="101df-105">記錄檔物件</span><span class="sxs-lookup"><span data-stu-id="101df-105">LogFiles object</span></span>

<span data-ttu-id="101df-106">您可以使用這個類別來管理一個或多個包含效能計數器資料之記錄檔的集合。</span><span class="sxs-lookup"><span data-stu-id="101df-106">Use this class to manage a collection of one or more log files that contain performance counter data.</span></span>

<span data-ttu-id="101df-107">若要取出這個物件，請呼叫 [**SystemMonitor。**](systemmonitor-logfiles.md)</span><span class="sxs-lookup"><span data-stu-id="101df-107">To retrieve this object, call [**SystemMonitor.LogFiles**](systemmonitor-logfiles.md).</span></span>

## <a name="members"></a><span data-ttu-id="101df-108">成員</span><span class="sxs-lookup"><span data-stu-id="101df-108">Members</span></span>

<span data-ttu-id="101df-109">記錄 **檔物件具有** 下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="101df-109">The **LogFiles** object has these types of members:</span></span>

-   [<span data-ttu-id="101df-110">方法</span><span class="sxs-lookup"><span data-stu-id="101df-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="101df-111">屬性</span><span class="sxs-lookup"><span data-stu-id="101df-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="101df-112">方法</span><span class="sxs-lookup"><span data-stu-id="101df-112">Methods</span></span>

<span data-ttu-id="101df-113">記錄 **檔物件有** 這些方法。</span><span class="sxs-lookup"><span data-stu-id="101df-113">The **LogFiles** object has these methods.</span></span>



| <span data-ttu-id="101df-114">方法</span><span class="sxs-lookup"><span data-stu-id="101df-114">Method</span></span>                                          | <span data-ttu-id="101df-115">描述</span><span class="sxs-lookup"><span data-stu-id="101df-115">Description</span></span>                                                                           |
|:------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="101df-116">**添加**</span><span class="sxs-lookup"><span data-stu-id="101df-116">**Add**</span></span>](systemmonitor-logfiles-add.md)       | <span data-ttu-id="101df-117">將 [**LogFileItem**](logfileitem.md) 實例加入至集合。</span><span class="sxs-lookup"><span data-stu-id="101df-117">Adds a [**LogFileItem**](logfileitem.md) instance to the collection.</span></span><br/>      |
| [<span data-ttu-id="101df-118">**移除**</span><span class="sxs-lookup"><span data-stu-id="101df-118">**Remove**</span></span>](systemmonitor-logfiles-remove.md) | <span data-ttu-id="101df-119">從集合中移除 [**LogFileItem**](logfileitem.md) 實例。</span><span class="sxs-lookup"><span data-stu-id="101df-119">Removes a [**LogFileItem**](logfileitem.md) instance from the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="101df-120">屬性</span><span class="sxs-lookup"><span data-stu-id="101df-120">Properties</span></span>

<span data-ttu-id="101df-121">記錄 **檔物件具有** 這些屬性。</span><span class="sxs-lookup"><span data-stu-id="101df-121">The **LogFiles** object has these properties.</span></span>



| <span data-ttu-id="101df-122">屬性</span><span class="sxs-lookup"><span data-stu-id="101df-122">Property</span></span>                                                 | <span data-ttu-id="101df-123">描述</span><span class="sxs-lookup"><span data-stu-id="101df-123">Description</span></span>                                                                                         |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="101df-124">**計數**</span><span class="sxs-lookup"><span data-stu-id="101df-124">**Count**</span></span>](systemmonitor-logfiles-count.md)<br/> | <span data-ttu-id="101df-125">抓取集合中 [**LogFileItem**](logfileitem.md) 實例的數目。</span><span class="sxs-lookup"><span data-stu-id="101df-125">Retrieves the number of [**LogFileItem**](logfileitem.md) instances in the collection.</span></span><br/>  |
| [<span data-ttu-id="101df-126">**項目**</span><span class="sxs-lookup"><span data-stu-id="101df-126">**Item**</span></span>](systemmonitor-logfiles-item.md)<br/>   | <span data-ttu-id="101df-127">從集合中抓取指定的 [**LogFileItem**](logfileitem.md) 實例。</span><span class="sxs-lookup"><span data-stu-id="101df-127">Retrieves the specified [**LogFileItem**](logfileitem.md) instance from the collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="101df-128">備註</span><span class="sxs-lookup"><span data-stu-id="101df-128">Remarks</span></span>

<span data-ttu-id="101df-129">若要讓 SYSMON 顯示記錄檔中的效能計數器，請將 [**SystemMonitor DataSourceType**](systemmonitor-datasourcetype.md) 為 [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants)。</span><span class="sxs-lookup"><span data-stu-id="101df-129">To have SYSMON display performance counters from a log file, set [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) to [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span></span> <span data-ttu-id="101df-130">將記錄檔加入至集合之後，請使用 [**計數器**](counters.md) 集合來指定您要從記錄檔讀取的計數器資料。</span><span class="sxs-lookup"><span data-stu-id="101df-130">After adding the log files to the collection, use the [**Counters**](counters.md) collection to specify the counters data that you want to read from the log files.</span></span> <span data-ttu-id="101df-131">請注意，如果 **SystemMonitor DataSourceType** 設定為 **DataSourceTypeConstants.sysmonLogFiles**，則每次您將記錄檔或計數器新增至各自的集合時，SYSMON 將會重新取樣記錄檔。</span><span class="sxs-lookup"><span data-stu-id="101df-131">Note that if **SystemMonitor.DataSourceType** is set to **DataSourceTypeConstants.sysmonLogFiles**, SYSMON will resample the log files each time you add a log file or counter to their respective collections.</span></span>

<span data-ttu-id="101df-132">**在 Windows Vista 之前：** 如果 [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md)的值設定為 [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants)，您就無法將記錄檔加入 [**記錄檔集合**](systemmonitor-logfiles.md)。</span><span class="sxs-lookup"><span data-stu-id="101df-132">**Prior to Windows Vista:** You cannot add log files to the [**log file collection**](systemmonitor-logfiles.md) if the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span></span> <span data-ttu-id="101df-133">首先，將 **SystemMonitor** 設定為 **DataSourceTypeConstants.sysmonNullDataSource**、新增您的記錄檔和計數器，然後將 **SystemMonitor DataSourceType** 設定為 **DataSourceTypeConstants.sysmonLogFiles**。</span><span class="sxs-lookup"><span data-stu-id="101df-133">First, set **SystemMonitor.DataSourceType** to **DataSourceTypeConstants.sysmonNullDataSource**, add your log files and counters, and then set **SystemMonitor.DataSourceType** to **DataSourceTypeConstants.sysmonLogFiles**.</span></span>

<span data-ttu-id="101df-134">[**SystemMonitor. LogViewStart**](systemmonitor-logviewstart.md)和 [**SystemMonitor. LogViewStop**](systemmonitor-logviewstop.md)屬性會指定從記錄檔到圖形的取樣值範圍。</span><span class="sxs-lookup"><span data-stu-id="101df-134">The [**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md) and [**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md) properties specify the range of sampled values from the log files to graph.</span></span> <span data-ttu-id="101df-135">SYSMON 圖形的記錄檔中只會有一個資料檢視 (圖表視圖不會像繪製電腦目前的活動) 一樣地滾動。</span><span class="sxs-lookup"><span data-stu-id="101df-135">SYSMON graphs only one view worth of data from the log file (the graph view does not scroll as it does when graphing the current activity of the computer).</span></span> <span data-ttu-id="101df-136">如果取樣的資料超過可在單一圖表上顯示的資料，SYSMON 會將取樣的資料壓縮 (每個圖形化點都代表多個取樣值的平均值，) 以符合圖形上記錄檔中的所有取樣資料。</span><span class="sxs-lookup"><span data-stu-id="101df-136">If the sampled data exceeds what can be shown on a single graph view, SYSMON compresses the sampled data (each graphed point represents the average of multiple sampled values) to fit all the sampled data from the log files on the graph.</span></span>

## <a name="requirements"></a><span data-ttu-id="101df-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="101df-137">Requirements</span></span>



| <span data-ttu-id="101df-138">需求</span><span class="sxs-lookup"><span data-stu-id="101df-138">Requirement</span></span> | <span data-ttu-id="101df-139">值</span><span class="sxs-lookup"><span data-stu-id="101df-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="101df-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="101df-140">Minimum supported client</span></span><br/> | <span data-ttu-id="101df-141">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="101df-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="101df-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="101df-142">Minimum supported server</span></span><br/> | <span data-ttu-id="101df-143">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="101df-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="101df-144">標頭</span><span class="sxs-lookup"><span data-stu-id="101df-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="101df-145"><dt>Isysmon。h</dt></span><span class="sxs-lookup"><span data-stu-id="101df-145"><dt>Isysmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="101df-146">DLL</span><span class="sxs-lookup"><span data-stu-id="101df-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="101df-147"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="101df-147"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





