---
title: SystemMonitor 的 OnDblClick 事件
description: 當使用者以滑鼠左鍵按兩下圖形線條、長條圖列或報表專案時，就會通知您。
ms.assetid: 06ad86ff-fcc0-4be5-a54c-7a6aa1147cf9
keywords:
- OnDblClick 事件 SysMon
- OnDblClick 事件 SysMon、SystemMonitor 類別
- SystemMonitor 類別 SysMon，OnDblClick 事件
topic_type:
- apiref
api_name:
- SystemMonitor.OnDblClick
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f21c6d67468ecb07bbe0fe83bec7b48a086571
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103836"
---
# <a name="systemmonitorondblclick-event"></a><span data-ttu-id="59018-106">SystemMonitor 的 OnDblClick 事件</span><span class="sxs-lookup"><span data-stu-id="59018-106">SystemMonitor.OnDblClick event</span></span>

<span data-ttu-id="59018-107">當使用者以滑鼠左鍵按兩下圖形線條、長條圖列或報表專案時，就會通知您。</span><span class="sxs-lookup"><span data-stu-id="59018-107">Notifies you when a user double-clicks the graph line, histogram bar, or report item with the left mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="59018-108">語法</span><span class="sxs-lookup"><span data-stu-id="59018-108">Syntax</span></span>


```VB
SystemMonitor.OnDblClick( _
  ByRef index As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="59018-109">參數</span><span class="sxs-lookup"><span data-stu-id="59018-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59018-110">*索引* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="59018-110">*index* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="59018-111">[**計數器**](counters.md)集合物件中所選取計數器的索引。</span><span class="sxs-lookup"><span data-stu-id="59018-111">Index of the selected counter in the [**Counters**](counters.md) collection object.</span></span> <span data-ttu-id="59018-112">如果未選取任何計數器，則會傳回索引值 0;否則，會傳回所選計數器的索引。</span><span class="sxs-lookup"><span data-stu-id="59018-112">An index value of 0 is returned if no counter was selected; otherwise, the index of the selected counter is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59018-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="59018-113">Return value</span></span>

<span data-ttu-id="59018-114">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="59018-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="59018-115">備註</span><span class="sxs-lookup"><span data-stu-id="59018-115">Remarks</span></span>

<span data-ttu-id="59018-116">觸發這個事件時，也會在 [圖例] 窗格中選取使用者在折線圖和長條圖中選取的計數器。</span><span class="sxs-lookup"><span data-stu-id="59018-116">When this event is triggered, the counter that the user selected in the line graph and histogram is also selected in the Legend pane.</span></span> <span data-ttu-id="59018-117">這可讓系統監視器的使用者更輕鬆地查看當顯示多個計數器值時所選取的計數器。</span><span class="sxs-lookup"><span data-stu-id="59018-117">This makes it easier for the user of the System Monitor to see which counter is selected when several counter values are displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="59018-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="59018-118">Requirements</span></span>



| <span data-ttu-id="59018-119">需求</span><span class="sxs-lookup"><span data-stu-id="59018-119">Requirement</span></span> | <span data-ttu-id="59018-120">值</span><span class="sxs-lookup"><span data-stu-id="59018-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="59018-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="59018-121">Minimum supported client</span></span><br/> | <span data-ttu-id="59018-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59018-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="59018-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="59018-123">Minimum supported server</span></span><br/> | <span data-ttu-id="59018-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59018-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="59018-125">DLL</span><span class="sxs-lookup"><span data-stu-id="59018-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59018-126"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="59018-126"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





