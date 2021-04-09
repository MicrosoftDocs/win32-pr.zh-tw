---
title: SystemMonitor. ChartScroll 屬性
description: 抓取或設定值，這個值會決定折線圖是否會在視圖中滾動。
ms.assetid: df4806be-dfd3-4ff7-985d-b46c00bb19f8
keywords:
- ChartScroll 屬性 SysMon
- ChartScroll 屬性 SysMon，SystemMonitor 物件
- SystemMonitor 物件 SysMon，ChartScroll 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.ChartScroll
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51288af710e5ae94baf46acf0d2ed91732a1d310
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934478"
---
# <a name="systemmonitorchartscroll-property"></a><span data-ttu-id="448f7-106">SystemMonitor. ChartScroll 屬性</span><span class="sxs-lookup"><span data-stu-id="448f7-106">SystemMonitor.ChartScroll property</span></span>

<span data-ttu-id="448f7-107">抓取或設定值，這個值會決定折線圖是否會在視圖中滾動。</span><span class="sxs-lookup"><span data-stu-id="448f7-107">Retrieves or sets a value that determines if the line graph scrolls in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="448f7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="448f7-108">Syntax</span></span>


```VB
Property ChartScroll As Boolean
```



## <a name="property-value"></a><span data-ttu-id="448f7-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="448f7-109">Property value</span></span>

<span data-ttu-id="448f7-110">如果折線圖會從右至左連續滾動，則為 True;否則，如果折線圖是由左至右繪製，並在視圖中換行，則為 False。</span><span class="sxs-lookup"><span data-stu-id="448f7-110">True if the line graph scrolls continuously from right to left; otherwise, False if the line graph is drawn from left to right and wraps around on itself in the view.</span></span> <span data-ttu-id="448f7-111">預設值為 False。</span><span class="sxs-lookup"><span data-stu-id="448f7-111">False is the default.</span></span>

## <a name="remarks"></a><span data-ttu-id="448f7-112">備註</span><span class="sxs-lookup"><span data-stu-id="448f7-112">Remarks</span></span>

<span data-ttu-id="448f7-113">如果 [**SystemMonitor**](systemmonitor-displaytype.md) 不是 [**DisplayTypeConstants.sysmonLineGraph**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants)，則會忽略此值。</span><span class="sxs-lookup"><span data-stu-id="448f7-113">This value is ignored if the [**SystemMonitor.DisplayType**](systemmonitor-displaytype.md) is not [**DisplayTypeConstants.sysmonLineGraph**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).</span></span>

## <a name="requirements"></a><span data-ttu-id="448f7-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="448f7-114">Requirements</span></span>



| <span data-ttu-id="448f7-115">需求</span><span class="sxs-lookup"><span data-stu-id="448f7-115">Requirement</span></span> | <span data-ttu-id="448f7-116">值</span><span class="sxs-lookup"><span data-stu-id="448f7-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="448f7-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="448f7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="448f7-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="448f7-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="448f7-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="448f7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="448f7-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="448f7-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="448f7-121">DLL</span><span class="sxs-lookup"><span data-stu-id="448f7-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="448f7-122"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="448f7-122"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





