---
title: SystemMonitor. OnCounterAdded 事件
description: 當計數器新增至計數器集合時通知您。
ms.assetid: f798443f-e2f1-4d25-b142-d88d6e4fe12c
keywords:
- OnCounterAdded 事件 SysMon
- OnCounterAdded 事件 SysMon、SystemMonitor 類別
- SystemMonitor 類別 SysMon，OnCounterAdded 事件
topic_type:
- apiref
api_name:
- SystemMonitor.OnCounterAdded
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f150709114ae25da89b107c7de85e3c5eca2551f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968963"
---
# <a name="systemmonitoroncounteradded-event"></a><span data-ttu-id="603ae-106">SystemMonitor. OnCounterAdded 事件</span><span class="sxs-lookup"><span data-stu-id="603ae-106">SystemMonitor.OnCounterAdded event</span></span>

<span data-ttu-id="603ae-107">當計數器新增至 [**計數器**](counters.md) 集合時通知您。</span><span class="sxs-lookup"><span data-stu-id="603ae-107">Notifies you when a counter is added to the [**Counters**](counters.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="603ae-108">語法</span><span class="sxs-lookup"><span data-stu-id="603ae-108">Syntax</span></span>


```VB
SystemMonitor.OnCounterAdded( _
  ByVal index As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="603ae-109">參數</span><span class="sxs-lookup"><span data-stu-id="603ae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="603ae-110">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="603ae-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="603ae-111">加入至 [**計數器**](counters.md) 集合物件之計數器的索引。</span><span class="sxs-lookup"><span data-stu-id="603ae-111">Index of the counter added to the [**Counters**](counters.md) collection object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="603ae-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="603ae-112">Return value</span></span>

<span data-ttu-id="603ae-113">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="603ae-113">This event does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="603ae-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="603ae-114">Requirements</span></span>



| <span data-ttu-id="603ae-115">需求</span><span class="sxs-lookup"><span data-stu-id="603ae-115">Requirement</span></span> | <span data-ttu-id="603ae-116">值</span><span class="sxs-lookup"><span data-stu-id="603ae-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="603ae-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="603ae-117">Minimum supported client</span></span><br/> | <span data-ttu-id="603ae-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="603ae-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="603ae-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="603ae-119">Minimum supported server</span></span><br/> | <span data-ttu-id="603ae-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="603ae-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="603ae-121">DLL</span><span class="sxs-lookup"><span data-stu-id="603ae-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="603ae-122"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="603ae-122"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="603ae-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="603ae-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="603ae-124">**SystemMonitor.OnCounterDeleted**</span><span class="sxs-lookup"><span data-stu-id="603ae-124">**SystemMonitor.OnCounterDeleted**</span></span>](-systemmonitor-oncounterdeleted.md)
</dt> <dt>

[<span data-ttu-id="603ae-125">**SystemMonitor.OnCounterSelected**</span><span class="sxs-lookup"><span data-stu-id="603ae-125">**SystemMonitor.OnCounterSelected**</span></span>](-systemmonitor-oncounterselected.md)
</dt> </dl>

 

 





