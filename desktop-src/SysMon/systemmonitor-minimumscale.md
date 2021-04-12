---
title: SystemMonitor. MinimumScale 屬性
description: 抓取或設定圖形垂直 (Y) 軸的最小值。
ms.assetid: 22dacfbf-27bb-48fe-b646-4cf17645a131
keywords:
- MinimumScale 屬性 SysMon
- MinimumScale 屬性 SysMon、SystemMonitor 類別
- SystemMonitor 類別 SysMon，MinimumScale 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.MinimumScale
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f675e96ecdd4e547ca4a93b248556fd8c0539a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465213"
---
# <a name="systemmonitorminimumscale-property"></a><span data-ttu-id="effa9-106">SystemMonitor. MinimumScale 屬性</span><span class="sxs-lookup"><span data-stu-id="effa9-106">SystemMonitor.MinimumScale property</span></span>

<span data-ttu-id="effa9-107">抓取或設定圖形垂直 (Y) 軸的最小值。</span><span class="sxs-lookup"><span data-stu-id="effa9-107">Retrieves or sets the minimum value of the vertical (Y) axis of the graph.</span></span>

<span data-ttu-id="effa9-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="effa9-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="effa9-109">語法</span><span class="sxs-lookup"><span data-stu-id="effa9-109">Syntax</span></span>


```VB
Property MinimumScale As Long
```



## <a name="property-value"></a><span data-ttu-id="effa9-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="effa9-110">Property value</span></span>

<span data-ttu-id="effa9-111">圖形垂直軸的正面最小值。</span><span class="sxs-lookup"><span data-stu-id="effa9-111">Positive minimum value of the vertical axis of the graph.</span></span> <span data-ttu-id="effa9-112">垂直尺規的預設最小值是0。</span><span class="sxs-lookup"><span data-stu-id="effa9-112">The default minimum value of the vertical scale is 0.</span></span> <span data-ttu-id="effa9-113">您可以將最小值設為一個小於 [**MaximumScale**](systemmonitor-maximumscale.md) 值的最大值。</span><span class="sxs-lookup"><span data-stu-id="effa9-113">The highest value that you can set the minimum value to is one less than [**MaximumScale**](systemmonitor-maximumscale.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="effa9-114">備註</span><span class="sxs-lookup"><span data-stu-id="effa9-114">Remarks</span></span>

<span data-ttu-id="effa9-115">控制項會根據顯示控制項的大小，自動調整顯示在垂直尺規上的尺規數位位置。</span><span class="sxs-lookup"><span data-stu-id="effa9-115">The control automatically adjusts the position of the scale numbers displayed on the vertical scale according to the size of the displayed control.</span></span>

## <a name="requirements"></a><span data-ttu-id="effa9-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="effa9-116">Requirements</span></span>



| <span data-ttu-id="effa9-117">需求</span><span class="sxs-lookup"><span data-stu-id="effa9-117">Requirement</span></span> | <span data-ttu-id="effa9-118">值</span><span class="sxs-lookup"><span data-stu-id="effa9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="effa9-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="effa9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="effa9-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="effa9-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="effa9-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="effa9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="effa9-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="effa9-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="effa9-123">DLL</span><span class="sxs-lookup"><span data-stu-id="effa9-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="effa9-124"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="effa9-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="effa9-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="effa9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="effa9-126">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="effa9-126">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="effa9-127">**SystemMonitor.MaximumScale**</span><span class="sxs-lookup"><span data-stu-id="effa9-127">**SystemMonitor.MaximumScale**</span></span>](systemmonitor-maximumscale.md)
</dt> <dt>

[<span data-ttu-id="effa9-128">**SystemMonitor.ShowScaleLabels**</span><span class="sxs-lookup"><span data-stu-id="effa9-128">**SystemMonitor.ShowScaleLabels**</span></span>](systemmonitor-showscalelabels.md)
</dt> </dl>

 

 





