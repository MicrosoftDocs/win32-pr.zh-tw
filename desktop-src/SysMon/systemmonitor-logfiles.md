---
title: SystemMonitor 記錄檔屬性
description: 收集一或多個要作為系統監視器中顯示的計數器值來源的記錄檔。
ms.assetid: 6e9e7205-3516-404d-b67d-777e484900da
keywords:
- 記錄檔屬性 SysMon
- 記錄檔屬性 SysMon，SystemMonitor 物件
- SystemMonitor 物件 SysMon，記錄檔屬性
topic_type:
- apiref
api_name:
- SystemMonitor.LogFiles
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8127433319290b44498b272834923784b714052
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967336"
---
# <a name="systemmonitorlogfiles-property"></a><span data-ttu-id="178b8-106">SystemMonitor 記錄檔屬性</span><span class="sxs-lookup"><span data-stu-id="178b8-106">SystemMonitor.LogFiles property</span></span>

<span data-ttu-id="178b8-107">收集一或多個要作為系統監視器中顯示的計數器值來源的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="178b8-107">Collection of one or more log files to use as the source of counter values displayed in the System Monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="178b8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="178b8-108">Syntax</span></span>


```VB
Property LogFiles As ILogFiles
```



## <a name="property-value"></a><span data-ttu-id="178b8-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="178b8-109">Property value</span></span>

<span data-ttu-id="178b8-110">[**LogFileItem**](logfileitem.md)物件的集合，這些物件會指定當做圖形之資料來源使用的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="178b8-110">Collection of [**LogFileItem**](logfileitem.md) objects that specify the log files used as the data source for the graph.</span></span>

## <a name="remarks"></a><span data-ttu-id="178b8-111">備註</span><span class="sxs-lookup"><span data-stu-id="178b8-111">Remarks</span></span>

<span data-ttu-id="178b8-112">若要從記錄檔集合加入或移除記錄檔， [**SystemMonitor**](systemmonitor-datasourcetype.md) 的值不得設定為 sysmonLogFiles。</span><span class="sxs-lookup"><span data-stu-id="178b8-112">To add or remove a log file from the log file collection, the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) must not be set to sysmonLogFiles.</span></span>

## <a name="requirements"></a><span data-ttu-id="178b8-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="178b8-113">Requirements</span></span>



| <span data-ttu-id="178b8-114">需求</span><span class="sxs-lookup"><span data-stu-id="178b8-114">Requirement</span></span> | <span data-ttu-id="178b8-115">值</span><span class="sxs-lookup"><span data-stu-id="178b8-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="178b8-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="178b8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="178b8-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="178b8-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="178b8-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="178b8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="178b8-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="178b8-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="178b8-120">DLL</span><span class="sxs-lookup"><span data-stu-id="178b8-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="178b8-121"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="178b8-121"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="178b8-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="178b8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="178b8-123">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="178b8-123">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="178b8-124">**SystemMonitor. DataSourceType**</span><span class="sxs-lookup"><span data-stu-id="178b8-124">**SystemMonitor.DataSourceType**</span></span>](systemmonitor-datasourcetype.md)
</dt> <dt>

[<span data-ttu-id="178b8-125">**SystemMonitor.LogViewStart**</span><span class="sxs-lookup"><span data-stu-id="178b8-125">**SystemMonitor.LogViewStart**</span></span>](systemmonitor-logviewstart.md)
</dt> <dt>

[<span data-ttu-id="178b8-126">**SystemMonitor.LogViewStop**</span><span class="sxs-lookup"><span data-stu-id="178b8-126">**SystemMonitor.LogViewStop**</span></span>](systemmonitor-logviewstop.md)
</dt> <dt>

[<span data-ttu-id="178b8-127">**SystemMonitor.SqlLogSetName**</span><span class="sxs-lookup"><span data-stu-id="178b8-127">**SystemMonitor.SqlLogSetName**</span></span>](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





