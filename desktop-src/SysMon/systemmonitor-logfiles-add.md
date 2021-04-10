---
title: 記錄檔。新增方法
description: 將記錄檔加入至集合。
ms.assetid: f6b671ea-9620-49a7-8b0c-0c8e1d9819b0
keywords:
- 新增方法 SysMon
- 新增方法 SysMon，記錄檔類別
- 記錄檔類別 SysMon，加入方法
topic_type:
- apiref
api_name:
- LogFiles.Add
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f690670606cd7ee307ba945fc2daabe92953e81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103829"
---
# <a name="logfilesadd-method"></a><span data-ttu-id="b1b25-106">記錄檔。新增方法</span><span class="sxs-lookup"><span data-stu-id="b1b25-106">LogFiles.Add method</span></span>

<span data-ttu-id="b1b25-107">將記錄檔加入至集合。</span><span class="sxs-lookup"><span data-stu-id="b1b25-107">Adds a log file to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1b25-108">語法</span><span class="sxs-lookup"><span data-stu-id="b1b25-108">Syntax</span></span>


```VB
LogFiles.Add( _
  ByVal pathname As String _
) As LogFileItem
```



## <a name="parameters"></a><span data-ttu-id="b1b25-109">參數</span><span class="sxs-lookup"><span data-stu-id="b1b25-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1b25-110">*路徑名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b1b25-110">*pathname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1b25-111">記錄檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="b1b25-111">Path to the log file.</span></span> <span data-ttu-id="b1b25-112">您可以將路徑指定為絕對路徑、相對路徑或 UNC 路徑。</span><span class="sxs-lookup"><span data-stu-id="b1b25-112">You can specify the path as an absolute, relative, or UNC path.</span></span> <span data-ttu-id="b1b25-113">記錄檔副檔名必須是 .csv、tsv 或 .blg。</span><span class="sxs-lookup"><span data-stu-id="b1b25-113">The log file name extension must be either .csv, .tsv, or .blg.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b1b25-114">備註</span><span class="sxs-lookup"><span data-stu-id="b1b25-114">Remarks</span></span>

<span data-ttu-id="b1b25-115">您必須使用 Logman.exe 工具或 Perfmon MMC 嵌入式管理單元來產生您新增至此集合的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="b1b25-115">You must use the Logman.exe tool or the Perfmon.msc MMC snap-in to generate the log files that you add to this collection.</span></span> <span data-ttu-id="b1b25-116">針對 Perfmon，計數器記錄檔位於 **效能記錄檔及警示** 下。</span><span class="sxs-lookup"><span data-stu-id="b1b25-116">For Perfmon.msc, the counter logs are located under **Performance Logs and Alerts**.</span></span> <span data-ttu-id="b1b25-117">如需有關使用 Logman.exe 或 Perfmon 的詳細資訊，請在 **說明及支援中心** 中分別搜尋 Logman 或使用效能。</span><span class="sxs-lookup"><span data-stu-id="b1b25-117">For details on using Logman.exe or Perfmon.msc, search for Logman or Using Performance, respectively, in the **Help and Support Center**.</span></span>

<span data-ttu-id="b1b25-118">**在 Windows Vista 之前：** 如果 [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md)的值設定為 [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants)，您就無法將記錄檔加入 [**記錄檔集合**](systemmonitor-logfiles.md)。</span><span class="sxs-lookup"><span data-stu-id="b1b25-118">**Prior to Windows Vista:** You cannot add log files to the [**log file collection**](systemmonitor-logfiles.md) if the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span></span> <span data-ttu-id="b1b25-119">首先，將 **SystemMonitor** 設定為 **DataSourceTypeConstants.sysmonNullDataSource**、新增您的記錄檔和計數器，然後將 **SystemMonitor DataSourceType** 設定為 **DataSourceTypeConstants.sysmonLogFiles**。</span><span class="sxs-lookup"><span data-stu-id="b1b25-119">First, set **SystemMonitor.DataSourceType** to **DataSourceTypeConstants.sysmonNullDataSource**, add your log files and counters, and then set **SystemMonitor.DataSourceType** to **DataSourceTypeConstants.sysmonLogFiles**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1b25-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1b25-120">Requirements</span></span>



| <span data-ttu-id="b1b25-121">需求</span><span class="sxs-lookup"><span data-stu-id="b1b25-121">Requirement</span></span> | <span data-ttu-id="b1b25-122">值</span><span class="sxs-lookup"><span data-stu-id="b1b25-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b1b25-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b1b25-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b1b25-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b1b25-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b1b25-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b1b25-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b1b25-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b1b25-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b1b25-127">DLL</span><span class="sxs-lookup"><span data-stu-id="b1b25-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1b25-128"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="b1b25-128"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1b25-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b1b25-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1b25-130">LogFiles</span><span class="sxs-lookup"><span data-stu-id="b1b25-130">LogFiles</span></span>](logfiles.md)
</dt> <dt>

[<span data-ttu-id="b1b25-131">**LogFileItem**</span><span class="sxs-lookup"><span data-stu-id="b1b25-131">**LogFileItem**</span></span>](logfileitem.md)
</dt> <dt>

[<span data-ttu-id="b1b25-132">**LogFiles**</span><span class="sxs-lookup"><span data-stu-id="b1b25-132">**LogFiles**</span></span>](systemmonitor-logfiles.md)
</dt> </dl>

 

 





