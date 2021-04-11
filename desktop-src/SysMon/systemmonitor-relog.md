---
title: SystemMonitor 方法
description: 將計數器資料 Relogs 至新的檔案。 您也可以使用這個方法來指定新的檔案類型，並減少記錄檔中包含的樣本數目。
ms.assetid: 4439f9ef-99e0-47d4-8f6f-d08afcba672d
keywords:
- 重新 SysMon 方法
- 重新 SysMon，SystemMonitor 物件
- SystemMonitor 物件 SysMon，重新的方法
topic_type:
- apiref
api_name:
- SystemMonitor.Relog
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109d0a6e44ef73652bd563099929ce601670610b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094367"
---
# <a name="systemmonitorrelog-method"></a><span data-ttu-id="219cd-107">SystemMonitor 方法</span><span class="sxs-lookup"><span data-stu-id="219cd-107">SystemMonitor.Relog method</span></span>

<span data-ttu-id="219cd-108">將計數器資料 Relogs 至新的檔案。</span><span class="sxs-lookup"><span data-stu-id="219cd-108">Relogs the counter data to a new file.</span></span> <span data-ttu-id="219cd-109">您也可以使用這個方法來指定新的檔案類型，並減少記錄檔中包含的樣本數目。</span><span class="sxs-lookup"><span data-stu-id="219cd-109">You can also use this method to specify a new file type and to reduce the number of samples contained in the log file.</span></span>

## <a name="syntax"></a><span data-ttu-id="219cd-110">語法</span><span class="sxs-lookup"><span data-stu-id="219cd-110">Syntax</span></span>


```VB
SystemMonitor.Relog( _
  ByVal fileName As String, _
  ByVal fileType As SysmonFileType, _
  ByVal filter As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="219cd-111">參數</span><span class="sxs-lookup"><span data-stu-id="219cd-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="219cd-112">*檔案名* \[在\]</span><span class="sxs-lookup"><span data-stu-id="219cd-112">*fileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="219cd-113">記錄檔的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="219cd-113">File path of the log file.</span></span> <span data-ttu-id="219cd-114">您可以將路徑指定為絕對路徑、相對路徑或 UNC 路徑。</span><span class="sxs-lookup"><span data-stu-id="219cd-114">You can specify the path as an absolute, relative, or UNC path.</span></span> <span data-ttu-id="219cd-115">記錄檔副檔名必須是 .blg、tsv 或 .csv。</span><span class="sxs-lookup"><span data-stu-id="219cd-115">The log file name extension must be either .blg, .tsv, or .csv.</span></span> <span data-ttu-id="219cd-116">如果路徑中的資料夾不存在，SYSMON 會加以建立。</span><span class="sxs-lookup"><span data-stu-id="219cd-116">If a folder in the path does not exist, SYSMON will create it.</span></span> <span data-ttu-id="219cd-117">如果檔案存在，則會覆寫檔案。</span><span class="sxs-lookup"><span data-stu-id="219cd-117">If the file exists, the file is overwritten.</span></span> <span data-ttu-id="219cd-118">SYSMON 會從父目錄套用預設 Acl。</span><span class="sxs-lookup"><span data-stu-id="219cd-118">SYSMON applies the default ACLs from the parent directory.</span></span>

</dd> <dt>

<span data-ttu-id="219cd-119">*類型類型* \[在\]</span><span class="sxs-lookup"><span data-stu-id="219cd-119">*fileType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="219cd-120">儲存至記錄檔的計數器資料格式。</span><span class="sxs-lookup"><span data-stu-id="219cd-120">Format of the counter data saved to the log file.</span></span> <span data-ttu-id="219cd-121">您可以指定 [**SysmonFileType.sysmonFileBlg**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype)、 **SysmonFileType.sysMonFileCsv** 或 **SysmonFileType.sysmonFileTsv**。</span><span class="sxs-lookup"><span data-stu-id="219cd-121">You can specify either [**SysmonFileType.sysmonFileBlg**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype), **SysmonFileType.sysmonFileCsv**, or **SysmonFileType.sysmonFileTsv**.</span></span>

</dd> <dt>

<span data-ttu-id="219cd-122">*篩選* \[在\]</span><span class="sxs-lookup"><span data-stu-id="219cd-122">*filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="219cd-123">舊記錄檔中要儲存至新記錄檔的樣本數。</span><span class="sxs-lookup"><span data-stu-id="219cd-123">Number of samples from the old log files to save in the new log file.</span></span> <span data-ttu-id="219cd-124">指定1，將舊檔案中的每個範例儲存至新檔案。</span><span class="sxs-lookup"><span data-stu-id="219cd-124">Specify 1 to save every sample from the old files to the new files.</span></span> <span data-ttu-id="219cd-125">指定2以從舊檔案的每個範例中儲存一個。</span><span class="sxs-lookup"><span data-stu-id="219cd-125">Specify 2 to save one out of every two samples from the old file.</span></span> <span data-ttu-id="219cd-126">指定3以從舊檔案的每三個樣本中儲存一份。</span><span class="sxs-lookup"><span data-stu-id="219cd-126">Specify 3 to save one out of every three samples from the old file.</span></span> <span data-ttu-id="219cd-127">依此類推。</span><span class="sxs-lookup"><span data-stu-id="219cd-127">And so on.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="219cd-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="219cd-128">Return value</span></span>

<span data-ttu-id="219cd-129">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="219cd-129">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="219cd-130">備註</span><span class="sxs-lookup"><span data-stu-id="219cd-130">Remarks</span></span>

<span data-ttu-id="219cd-131">這個方法會使用 [**SystemMonitor**](systemmonitor-logfiles.md) .log 集合中包含的記錄檔來重新記錄計數器資料。</span><span class="sxs-lookup"><span data-stu-id="219cd-131">This method uses the log files contained in the [**SystemMonitor.LogFiles**](systemmonitor-logfiles.md) collection to relog the counter data.</span></span>

## <a name="requirements"></a><span data-ttu-id="219cd-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="219cd-132">Requirements</span></span>



| <span data-ttu-id="219cd-133">需求</span><span class="sxs-lookup"><span data-stu-id="219cd-133">Requirement</span></span> | <span data-ttu-id="219cd-134">值</span><span class="sxs-lookup"><span data-stu-id="219cd-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="219cd-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="219cd-135">Minimum supported client</span></span><br/> | <span data-ttu-id="219cd-136">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="219cd-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="219cd-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="219cd-137">Minimum supported server</span></span><br/> | <span data-ttu-id="219cd-138">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="219cd-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="219cd-139">DLL</span><span class="sxs-lookup"><span data-stu-id="219cd-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="219cd-140"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="219cd-140"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="219cd-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="219cd-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="219cd-142">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="219cd-142">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="219cd-143">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="219cd-143">**SystemMonitor.SaveAs**</span></span>](systemmonitor-saveas.md)
</dt> </dl>

 

 





