---
title: SystemMonitor. SaveAs 方法
description: 將圖形視圖中的計數器值儲存至記錄檔。
ms.assetid: 34824c54-d8f4-4c2b-b417-aa0914c7164b
keywords:
- SaveAs 方法 SysMon
- SaveAs 方法 SysMon、SystemMonitor 物件
- SystemMonitor 物件 SysMon，SaveAs 方法
topic_type:
- apiref
api_name:
- SystemMonitor.SaveAs
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29c6eee811a27ba295f9c6bc5c2adb20d7b715e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965900"
---
# <a name="systemmonitorsaveas-method"></a><span data-ttu-id="85221-106">SystemMonitor. SaveAs 方法</span><span class="sxs-lookup"><span data-stu-id="85221-106">SystemMonitor.SaveAs method</span></span>

<span data-ttu-id="85221-107">將圖形視圖中的計數器值儲存至記錄檔。</span><span class="sxs-lookup"><span data-stu-id="85221-107">Saves the counter values in the graph view to a log file.</span></span>

## <a name="syntax"></a><span data-ttu-id="85221-108">語法</span><span class="sxs-lookup"><span data-stu-id="85221-108">Syntax</span></span>


```VB
SystemMonitor.SaveAs( _
  ByVal fileName As String, _
  ByVal fileType As SysmonFileType _
)
```



## <a name="parameters"></a><span data-ttu-id="85221-109">參數</span><span class="sxs-lookup"><span data-stu-id="85221-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85221-110">*檔案名* \[在\]</span><span class="sxs-lookup"><span data-stu-id="85221-110">*fileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85221-111">記錄檔的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="85221-111">File path of the log file.</span></span> <span data-ttu-id="85221-112">您可以將路徑指定為絕對路徑、相對路徑或 UNC 路徑。</span><span class="sxs-lookup"><span data-stu-id="85221-112">You can specify the path as an absolute, relative, or UNC path.</span></span> <span data-ttu-id="85221-113">記錄檔的副檔名必須是 tsv 或 .htm。</span><span class="sxs-lookup"><span data-stu-id="85221-113">The log file name extension must be either .tsv or .htm.</span></span> <span data-ttu-id="85221-114">如果路徑中的資料夾不存在，SYSMON 會加以建立。</span><span class="sxs-lookup"><span data-stu-id="85221-114">If a folder in the path does not exist, SYSMON will create it.</span></span> <span data-ttu-id="85221-115">如果檔案存在，則會覆寫檔案。</span><span class="sxs-lookup"><span data-stu-id="85221-115">If the file exists, the file is overwritten.</span></span> <span data-ttu-id="85221-116">SYSMON 會從父目錄套用預設 Acl。</span><span class="sxs-lookup"><span data-stu-id="85221-116">SYSMON applies the default ACLs from the parent directory.</span></span>

</dd> <dt>

<span data-ttu-id="85221-117">*類型類型* \[在\]</span><span class="sxs-lookup"><span data-stu-id="85221-117">*fileType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85221-118">儲存至記錄檔的計數器資料格式。</span><span class="sxs-lookup"><span data-stu-id="85221-118">Format of the counter data saved to the log file.</span></span> <span data-ttu-id="85221-119">您可以指定 [**SysmonFileType.sysmonFileHtml**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype) 或 **SysmonFileType.sysmonFileTsv**。</span><span class="sxs-lookup"><span data-stu-id="85221-119">You can specify either [**SysmonFileType.sysmonFileHtml**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype) or **SysmonFileType.sysmonFileTsv**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85221-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="85221-120">Return value</span></span>

<span data-ttu-id="85221-121">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="85221-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="85221-122">備註</span><span class="sxs-lookup"><span data-stu-id="85221-122">Remarks</span></span>

<span data-ttu-id="85221-123">只有儲存的資料點實際數目 (儲存在圖形視圖中可見的計數器資料，請參閱 [**SystemMonitor DataPointCount**](systemmonitor-datapointcount.md)) 。</span><span class="sxs-lookup"><span data-stu-id="85221-123">Only the counter data visible in the graph view is saved (for the actual number of data points saved, see [**SystemMonitor.DataPointCount**](systemmonitor-datapointcount.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="85221-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="85221-124">Requirements</span></span>



| <span data-ttu-id="85221-125">需求</span><span class="sxs-lookup"><span data-stu-id="85221-125">Requirement</span></span> | <span data-ttu-id="85221-126">值</span><span class="sxs-lookup"><span data-stu-id="85221-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="85221-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="85221-127">Minimum supported client</span></span><br/> | <span data-ttu-id="85221-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85221-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="85221-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="85221-129">Minimum supported server</span></span><br/> | <span data-ttu-id="85221-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85221-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="85221-131">DLL</span><span class="sxs-lookup"><span data-stu-id="85221-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85221-132"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="85221-132"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85221-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="85221-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85221-134">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="85221-134">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="85221-135">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="85221-135">**SystemMonitor.Relog**</span></span>](systemmonitor-relog.md)
</dt> </dl>

 

 





