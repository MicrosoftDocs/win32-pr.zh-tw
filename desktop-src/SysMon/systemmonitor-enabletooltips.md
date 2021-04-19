---
title: SystemMonitor. EnableToolTips 屬性
description: 取得或設定值，這個值會決定當滑鼠停留在其中一個圖形視圖中的計數器上方時是否顯示工具提示 (不支援報表檢視) 。
ms.assetid: af9a78ea-a9de-4343-8978-4316769a5f30
keywords:
- EnableToolTips 屬性 SysMon
- EnableToolTips 屬性 SysMon，SystemMonitor 物件
- SystemMonitor 物件 SysMon，EnableToolTips 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.EnableToolTips
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 757cdd8a54bf6e5ae6e70b82dfc30865c796f944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967738"
---
# <a name="systemmonitorenabletooltips-property"></a><span data-ttu-id="13065-106">SystemMonitor. EnableToolTips 屬性</span><span class="sxs-lookup"><span data-stu-id="13065-106">SystemMonitor.EnableToolTips property</span></span>

<span data-ttu-id="13065-107">取得或設定值，這個值會決定當滑鼠停留在其中一個圖形視圖中的計數器上方時是否顯示工具提示 (不支援報表檢視) 。</span><span class="sxs-lookup"><span data-stu-id="13065-107">Retrieves or sets a value that determines if a tool tip is shown when the mouse hovers over a counter in one of the graph views (not supported for report view).</span></span>

## <a name="syntax"></a><span data-ttu-id="13065-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="13065-108">Syntax</span></span>


```VB
Property EnableToolTips As Boolean
```



## <a name="property-value"></a><span data-ttu-id="13065-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="13065-109">Property value</span></span>

<span data-ttu-id="13065-110">True 會顯示工具提示，其中包含其中的計數器資訊;否則為 False。</span><span class="sxs-lookup"><span data-stu-id="13065-110">True displays a tool tip with the counter information in it; otherwise, False.</span></span>

## <a name="remarks"></a><span data-ttu-id="13065-111">備註</span><span class="sxs-lookup"><span data-stu-id="13065-111">Remarks</span></span>

<span data-ttu-id="13065-112">針對折線圖，工具提示會錨定到最接近滑鼠的資料點。</span><span class="sxs-lookup"><span data-stu-id="13065-112">For line graphs, the tool tip is anchored to the data point that is closest to the mouse.</span></span> <span data-ttu-id="13065-113">針對橫條圖和長條圖，工具提示表示橫條圖的總數據值，而不是橫條圖內的點。</span><span class="sxs-lookup"><span data-stu-id="13065-113">For bar charts and histograms, the tool tip represents the total data value of the bar, not a point within the bar.</span></span>

<span data-ttu-id="13065-114">工具提示包含以資料來源為基礎的不同資訊。</span><span class="sxs-lookup"><span data-stu-id="13065-114">The tool tip contains different information based upon the data source.</span></span> <span data-ttu-id="13065-115">針對記錄檔，工具提示包含計數器路徑、計數器值、時間戳記、資料點中包含的資料樣本數目，以及最小和最大資料值。</span><span class="sxs-lookup"><span data-stu-id="13065-115">For log files, the tool tip contains the counter path, counter value, time stamp, number of data samples included in the data point, and the minimum and maximum data values.</span></span>

<span data-ttu-id="13065-116">針對即時活動，工具提示包含計數器路徑、計數器值和時間戳記。</span><span class="sxs-lookup"><span data-stu-id="13065-116">For real time activity, the tool tip contains the counter path, counter value, and time stamp.</span></span>

## <a name="requirements"></a><span data-ttu-id="13065-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="13065-117">Requirements</span></span>



| <span data-ttu-id="13065-118">需求</span><span class="sxs-lookup"><span data-stu-id="13065-118">Requirement</span></span> | <span data-ttu-id="13065-119">值</span><span class="sxs-lookup"><span data-stu-id="13065-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="13065-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="13065-120">Minimum supported client</span></span><br/> | <span data-ttu-id="13065-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13065-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="13065-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="13065-122">Minimum supported server</span></span><br/> | <span data-ttu-id="13065-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13065-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="13065-124">DLL</span><span class="sxs-lookup"><span data-stu-id="13065-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13065-125"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="13065-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





