---
title: SystemMonitor. MaximumScale 屬性
description: 抓取或設定圖形垂直 (Y) 軸的最大值。
ms.assetid: 305886e3-2586-47c7-a888-6e393580c456
keywords:
- MaximumScale 屬性 SysMon
- MaximumScale 屬性 SysMon、SystemMonitor 類別
- SystemMonitor 類別 SysMon，MaximumScale 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.MaximumScale
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37740802fac4d89bbcbe9d5c105e357b55ab481
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934243"
---
# <a name="systemmonitormaximumscale-property"></a><span data-ttu-id="a35bd-106">SystemMonitor. MaximumScale 屬性</span><span class="sxs-lookup"><span data-stu-id="a35bd-106">SystemMonitor.MaximumScale property</span></span>

<span data-ttu-id="a35bd-107">抓取或設定圖形垂直 (Y) 軸的最大值。</span><span class="sxs-lookup"><span data-stu-id="a35bd-107">Retrieves or sets the maximum value of the vertical (Y) axis of the graph.</span></span>

<span data-ttu-id="a35bd-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="a35bd-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a35bd-109">語法</span><span class="sxs-lookup"><span data-stu-id="a35bd-109">Syntax</span></span>


```VB
Property MaximumScale As Long
```



## <a name="property-value"></a><span data-ttu-id="a35bd-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="a35bd-110">Property value</span></span>

<span data-ttu-id="a35bd-111">圖形垂直軸的正面最大值。</span><span class="sxs-lookup"><span data-stu-id="a35bd-111">Positive maximum value of the vertical axis of the graph.</span></span> <span data-ttu-id="a35bd-112">垂直尺規的預設最大值為100。</span><span class="sxs-lookup"><span data-stu-id="a35bd-112">The default maximum value of the vertical scale is 100.</span></span> <span data-ttu-id="a35bd-113">最小值，您可以將最大值設為一個以上的值，而不是 [**MinimumScale**](systemmonitor-minimumscale.md) 值。</span><span class="sxs-lookup"><span data-stu-id="a35bd-113">The lowest value that you can set the maximum value to is one more than the [**MinimumScale**](systemmonitor-minimumscale.md) value.</span></span> <span data-ttu-id="a35bd-114">您可以將最大值設定為999999999的最大值。</span><span class="sxs-lookup"><span data-stu-id="a35bd-114">The highest value that you can set the maximum value to is 999,999,999.</span></span>

## <a name="remarks"></a><span data-ttu-id="a35bd-115">備註</span><span class="sxs-lookup"><span data-stu-id="a35bd-115">Remarks</span></span>

<span data-ttu-id="a35bd-116">控制項會根據顯示控制項的大小，自動調整顯示在垂直尺規上的尺規數位位置。</span><span class="sxs-lookup"><span data-stu-id="a35bd-116">The control automatically adjusts the position of the scale numbers displayed on the vertical scale according to the size of the displayed control.</span></span>

## <a name="requirements"></a><span data-ttu-id="a35bd-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="a35bd-117">Requirements</span></span>



| <span data-ttu-id="a35bd-118">需求</span><span class="sxs-lookup"><span data-stu-id="a35bd-118">Requirement</span></span> | <span data-ttu-id="a35bd-119">值</span><span class="sxs-lookup"><span data-stu-id="a35bd-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a35bd-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a35bd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a35bd-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a35bd-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="a35bd-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a35bd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a35bd-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a35bd-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a35bd-124">DLL</span><span class="sxs-lookup"><span data-stu-id="a35bd-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a35bd-125"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="a35bd-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a35bd-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a35bd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a35bd-127">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="a35bd-127">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="a35bd-128">**SystemMonitor.MinimumScale**</span><span class="sxs-lookup"><span data-stu-id="a35bd-128">**SystemMonitor.MinimumScale**</span></span>](systemmonitor-minimumscale.md)
</dt> <dt>

[<span data-ttu-id="a35bd-129">**SystemMonitor.ShowScaleLabels**</span><span class="sxs-lookup"><span data-stu-id="a35bd-129">**SystemMonitor.ShowScaleLabels**</span></span>](systemmonitor-showscalelabels.md)
</dt> </dl>

 

 





