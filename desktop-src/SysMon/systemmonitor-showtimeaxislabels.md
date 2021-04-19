---
title: SystemMonitor. ShowTimeAxisLabels 屬性
description: 抓取或設定值，這個值會判斷圖形視圖的水準 (X) 軸是否包含標籤。
ms.assetid: 9e9d2d2c-f053-4afe-85de-25242842498f
keywords:
- ShowTimeAxisLabels 屬性 SysMon
- ShowTimeAxisLabels 屬性 SysMon，SystemMonitor 物件
- SystemMonitor 物件 SysMon，ShowTimeAxisLabels 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.ShowTimeAxisLabels
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06569dcd4702ae687b09bfae88c84482a49afb71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965891"
---
# <a name="systemmonitorshowtimeaxislabels-property"></a><span data-ttu-id="c9a4d-106">SystemMonitor. ShowTimeAxisLabels 屬性</span><span class="sxs-lookup"><span data-stu-id="c9a4d-106">SystemMonitor.ShowTimeAxisLabels property</span></span>

<span data-ttu-id="c9a4d-107">抓取或設定值，這個值會判斷圖形視圖的水準 (X) 軸是否包含標籤。</span><span class="sxs-lookup"><span data-stu-id="c9a4d-107">Retrieves or sets a value that determines if the horizontal (X) axis of the graph view contains labels.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9a4d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9a4d-108">Syntax</span></span>


```VB
Property ShowTimeAxisLabels As Boolean
```



## <a name="property-value"></a><span data-ttu-id="c9a4d-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="c9a4d-109">Property value</span></span>

<span data-ttu-id="c9a4d-110">True 值會將標籤套用至 X 軸。</span><span class="sxs-lookup"><span data-stu-id="c9a4d-110">A value of True will apply labels to the x-axis.</span></span> <span data-ttu-id="c9a4d-111">False 的值將不會。</span><span class="sxs-lookup"><span data-stu-id="c9a4d-111">A value of False will not.</span></span> <span data-ttu-id="c9a4d-112">預設值是 False。</span><span class="sxs-lookup"><span data-stu-id="c9a4d-112">The default is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9a4d-113">備註</span><span class="sxs-lookup"><span data-stu-id="c9a4d-113">Remarks</span></span>

<span data-ttu-id="c9a4d-114">SYSMON 會忽略橫條圖、報表和長條圖的這個屬性。</span><span class="sxs-lookup"><span data-stu-id="c9a4d-114">SYSMON ignores this property for bar graphs, reports and histograms.</span></span>

<span data-ttu-id="c9a4d-115">針對折線圖，SYSMON 會使用取樣計數器值作為標籤的時間。</span><span class="sxs-lookup"><span data-stu-id="c9a4d-115">For line graphs, SYSMON uses the time that the counter value was sampled as the label.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9a4d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9a4d-116">Requirements</span></span>



| <span data-ttu-id="c9a4d-117">需求</span><span class="sxs-lookup"><span data-stu-id="c9a4d-117">Requirement</span></span> | <span data-ttu-id="c9a4d-118">值</span><span class="sxs-lookup"><span data-stu-id="c9a4d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c9a4d-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c9a4d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c9a4d-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9a4d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c9a4d-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c9a4d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c9a4d-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9a4d-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c9a4d-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c9a4d-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9a4d-124"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="c9a4d-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





