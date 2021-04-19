---
title: SystemMonitor. ManualUpdate 屬性
description: 抓取或設定值，指出系統監視器的內容將會以手動方式更新，還是在指定的間隔自動更新。
ms.assetid: e068a955-ec1d-4f93-9261-25ba87773913
keywords:
- ManualUpdate 屬性 SysMon
- ManualUpdate 屬性 SysMon、SystemMonitor 類別
- SystemMonitor 類別 SysMon，ManualUpdate 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.ManualUpdate
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d1ecb426b47ba9cb7ec50b737f4f32d5ce274eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968964"
---
# <a name="systemmonitormanualupdate-property"></a><span data-ttu-id="74264-106">SystemMonitor. ManualUpdate 屬性</span><span class="sxs-lookup"><span data-stu-id="74264-106">SystemMonitor.ManualUpdate property</span></span>

<span data-ttu-id="74264-107">抓取或設定值，指出系統監視器的內容將會以手動方式更新，還是在指定的間隔自動更新。</span><span class="sxs-lookup"><span data-stu-id="74264-107">Retrieves or sets a value indicating whether the contents of the System Monitor will be updated manually, or automatically at specified intervals.</span></span>

<span data-ttu-id="74264-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="74264-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="74264-109">語法</span><span class="sxs-lookup"><span data-stu-id="74264-109">Syntax</span></span>


```VB
Property ManualUpdate As Boolean
```



## <a name="property-value"></a><span data-ttu-id="74264-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="74264-110">Property value</span></span>

<span data-ttu-id="74264-111">True 表示圖形會以手動方式更新。</span><span class="sxs-lookup"><span data-stu-id="74264-111">True indicates that graph is updated manually.</span></span> <span data-ttu-id="74264-112">False 表示會根據 [**SystemMonitor. UpdateInterval**](systemmonitor-updateinterval.md)中指定的更新間隔自動更新圖形。</span><span class="sxs-lookup"><span data-stu-id="74264-112">False indicates that the graph is updated automatically based on the update interval specified in [**SystemMonitor.UpdateInterval**](systemmonitor-updateinterval.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="74264-113">備註</span><span class="sxs-lookup"><span data-stu-id="74264-113">Remarks</span></span>

<span data-ttu-id="74264-114">依預設，圖表會自動更新。</span><span class="sxs-lookup"><span data-stu-id="74264-114">By default, the graph is updated automatically.</span></span>

<span data-ttu-id="74264-115">若要手動更新圖形，請呼叫 [**SystemMonitor. CollectSample**](systemmonitor-collectsample.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="74264-115">To update the graph manually, call the [**SystemMonitor.CollectSample**](systemmonitor-collectsample.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="74264-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="74264-116">Requirements</span></span>



| <span data-ttu-id="74264-117">需求</span><span class="sxs-lookup"><span data-stu-id="74264-117">Requirement</span></span> | <span data-ttu-id="74264-118">值</span><span class="sxs-lookup"><span data-stu-id="74264-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="74264-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="74264-119">Minimum supported client</span></span><br/> | <span data-ttu-id="74264-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74264-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="74264-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="74264-121">Minimum supported server</span></span><br/> | <span data-ttu-id="74264-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74264-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="74264-123">DLL</span><span class="sxs-lookup"><span data-stu-id="74264-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74264-124"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="74264-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74264-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74264-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74264-126">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="74264-126">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="74264-127">**SystemMonitor.CollectSample**</span><span class="sxs-lookup"><span data-stu-id="74264-127">**SystemMonitor.CollectSample**</span></span>](systemmonitor-collectsample.md)
</dt> <dt>

[<span data-ttu-id="74264-128">**SystemMonitor.UpdateGraph**</span><span class="sxs-lookup"><span data-stu-id="74264-128">**SystemMonitor.UpdateGraph**</span></span>](systemmonitor-updategraph.md)
</dt> </dl>

 

 





