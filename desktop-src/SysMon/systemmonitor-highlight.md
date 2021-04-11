---
title: SystemMonitor：醒目提示屬性
description: 抓取或設定值，指出在圖形中是否反白顯示所選計數器的值。
ms.assetid: 5342b81f-71bb-4564-b520-1e91d3002c5b
keywords:
- 醒目提示屬性 SysMon
- 醒目提示屬性 SysMon，SystemMonitor 類別
- SystemMonitor 類別 SysMon，醒目提示屬性
topic_type:
- apiref
api_name:
- SystemMonitor.Highlight
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3009501123673175c64d88acd838f94aa7e332aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843616"
---
# <a name="systemmonitorhighlight-property"></a><span data-ttu-id="94f1a-106">SystemMonitor：醒目提示屬性</span><span class="sxs-lookup"><span data-stu-id="94f1a-106">SystemMonitor.Highlight property</span></span>

<span data-ttu-id="94f1a-107">抓取或設定值，指出在圖形中是否反白顯示所選計數器的值。</span><span class="sxs-lookup"><span data-stu-id="94f1a-107">Retrieves or sets a value indicating whether the values of the selected counters are highlighted in the graph.</span></span>

<span data-ttu-id="94f1a-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="94f1a-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="94f1a-109">語法</span><span class="sxs-lookup"><span data-stu-id="94f1a-109">Syntax</span></span>


```VB
Property Highlight As Boolean
```



## <a name="property-value"></a><span data-ttu-id="94f1a-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="94f1a-110">Property value</span></span>

<span data-ttu-id="94f1a-111">True 表示選取的計數器值在圖形中會反白顯示;否則為 False。</span><span class="sxs-lookup"><span data-stu-id="94f1a-111">True indicates that the values of the selected counters are highlighted in the graph; otherwise, False.</span></span> <span data-ttu-id="94f1a-112">預設值是 False。</span><span class="sxs-lookup"><span data-stu-id="94f1a-112">The default value is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="94f1a-113">備註</span><span class="sxs-lookup"><span data-stu-id="94f1a-113">Remarks</span></span>

<span data-ttu-id="94f1a-114">若要選取一或多個計數器，可以將 [**CounterItem**](counteritem-selected.md) 設為 True，或使用者可以從圖例中所顯示的計數器清單中選取計數器。</span><span class="sxs-lookup"><span data-stu-id="94f1a-114">To select one or more counters, you can set [**CounterItem.Selected**](counteritem-selected.md) to True, or the user can select the counters from the list of counters shown in the Legend.</span></span>

<span data-ttu-id="94f1a-115">**在 Windows Vista 之前：** 您無法以程式設計方式選取計數器，而且使用者只能從圖例所顯示的計數器清單中選取一個計數器。</span><span class="sxs-lookup"><span data-stu-id="94f1a-115">**Prior to Windows Vista:** You cannot programmatically select counters and the user can select only one counter from the list of counters shown in the Legend.</span></span>

<span data-ttu-id="94f1a-116">醒目提示可以是黑色或白色，視 [**背景**](systemmonitor-backcolor.md) 色彩屬性的值而定。</span><span class="sxs-lookup"><span data-stu-id="94f1a-116">Highlighting can be black or white, depending on the value of the [**BackColor**](systemmonitor-backcolor.md) property.</span></span> <span data-ttu-id="94f1a-117">醒目提示會自動設為色彩，以在反白顯示色彩和背景色彩之間提供足夠的對比。</span><span class="sxs-lookup"><span data-stu-id="94f1a-117">The highlighting is automatically set to the color that will provide sufficient contrast between highlight color and the background color.</span></span>

## <a name="requirements"></a><span data-ttu-id="94f1a-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="94f1a-118">Requirements</span></span>



| <span data-ttu-id="94f1a-119">需求</span><span class="sxs-lookup"><span data-stu-id="94f1a-119">Requirement</span></span> | <span data-ttu-id="94f1a-120">值</span><span class="sxs-lookup"><span data-stu-id="94f1a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="94f1a-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="94f1a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="94f1a-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="94f1a-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="94f1a-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="94f1a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="94f1a-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="94f1a-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="94f1a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="94f1a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94f1a-126"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="94f1a-126"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94f1a-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="94f1a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94f1a-128">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="94f1a-128">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="94f1a-129">**CounterItem。已選取**</span><span class="sxs-lookup"><span data-stu-id="94f1a-129">**CounterItem.Selected**</span></span>](counteritem-selected.md)
</dt> </dl>

 

 





