---
title: SystemMonitor. ShowValueBar 屬性
description: 抓取或設定值，這個值會決定是否要在控制項上顯示值列 (圖形) 下方的統計值集。
ms.assetid: 320fbbbb-c4ea-4772-9b10-1e123849c255
keywords:
- ShowValueBar 屬性 SysMon
- ShowValueBar 屬性 SysMon、SystemMonitor 類別
- SystemMonitor 類別 SysMon，ShowValueBar 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.ShowValueBar
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f393b36162fae6aed996d2afaccd4749f22598f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685688"
---
# <a name="systemmonitorshowvaluebar-property"></a><span data-ttu-id="ef288-106">SystemMonitor. ShowValueBar 屬性</span><span class="sxs-lookup"><span data-stu-id="ef288-106">SystemMonitor.ShowValueBar property</span></span>

<span data-ttu-id="ef288-107">抓取或設定值，這個值會決定是否要在控制項上顯示值列 (圖形) 下方的統計值集。</span><span class="sxs-lookup"><span data-stu-id="ef288-107">Retrieves or sets a value that determines whether the value bar (the set of statistical values below the graph) is displayed on the control.</span></span>

<span data-ttu-id="ef288-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="ef288-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef288-109">語法</span><span class="sxs-lookup"><span data-stu-id="ef288-109">Syntax</span></span>


```VB
Property ShowValueBar As Boolean
```



## <a name="property-value"></a><span data-ttu-id="ef288-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="ef288-110">Property value</span></span>

<span data-ttu-id="ef288-111">True 表示顯示在控制項上的值列;否則為 false。</span><span class="sxs-lookup"><span data-stu-id="ef288-111">True indicates that the value bar is displayed on the control; otherwise false.</span></span> <span data-ttu-id="ef288-112">這個屬性的預設值是 True。</span><span class="sxs-lookup"><span data-stu-id="ef288-112">The default value for this property is true.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef288-113">備註</span><span class="sxs-lookup"><span data-stu-id="ef288-113">Remarks</span></span>

<span data-ttu-id="ef288-114">顯示的統計資料包含最後一個值、平均值，以及目前選取的計數器在顯示的時間間隔內的最小值和最大值。</span><span class="sxs-lookup"><span data-stu-id="ef288-114">The displayed statistics include the last value, the average value, and the minimum and maximum values of the currently selected counter over the displayed time interval.</span></span> <span data-ttu-id="ef288-115">若要選取要顯示的計數器值，使用者必須在控制項的 [圖例] 窗格中選取計數器。</span><span class="sxs-lookup"><span data-stu-id="ef288-115">To select the counter values to display, the user must select the counter in the Legend pane of the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef288-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="ef288-116">Requirements</span></span>



| <span data-ttu-id="ef288-117">需求</span><span class="sxs-lookup"><span data-stu-id="ef288-117">Requirement</span></span> | <span data-ttu-id="ef288-118">值</span><span class="sxs-lookup"><span data-stu-id="ef288-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef288-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ef288-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ef288-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef288-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ef288-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ef288-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ef288-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef288-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ef288-123">DLL</span><span class="sxs-lookup"><span data-stu-id="ef288-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef288-124"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="ef288-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef288-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ef288-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef288-126">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="ef288-126">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





