---
title: SystemMonitor. OnCounterDeleted 事件
description: 從計數器集合刪除計數器之前通知您。
ms.assetid: ab6bc1ba-20cd-4774-853e-b6adb765fae3
keywords:
- OnCounterDeleted 事件 SysMon
- OnCounterDeleted 事件 SysMon、SystemMonitor 類別
- SystemMonitor 類別 SysMon，OnCounterDeleted 事件
topic_type:
- apiref
api_name:
- SystemMonitor.OnCounterDeleted
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceafcc73f38e5413e312d00bf8aa8eba4eaf2c35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934429"
---
# <a name="systemmonitoroncounterdeleted-event"></a><span data-ttu-id="d345f-106">SystemMonitor. OnCounterDeleted 事件</span><span class="sxs-lookup"><span data-stu-id="d345f-106">SystemMonitor.OnCounterDeleted event</span></span>

<span data-ttu-id="d345f-107">從 [**計數器**](counters.md) 集合刪除計數器之前通知您。</span><span class="sxs-lookup"><span data-stu-id="d345f-107">Notifies you before a counter is deleted from the [**Counters**](counters.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d345f-108">語法</span><span class="sxs-lookup"><span data-stu-id="d345f-108">Syntax</span></span>


```VB
SystemMonitor.OnCounterDeleted( _
  ByVal index As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="d345f-109">參數</span><span class="sxs-lookup"><span data-stu-id="d345f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d345f-110">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d345f-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d345f-111">要從 [**計數器**](counters.md) 集合物件中刪除之計數器的索引。</span><span class="sxs-lookup"><span data-stu-id="d345f-111">Index of the counter to be deleted from the [**Counters**](counters.md) collection object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d345f-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d345f-112">Return value</span></span>

<span data-ttu-id="d345f-113">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d345f-113">This event does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d345f-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="d345f-114">Requirements</span></span>



| <span data-ttu-id="d345f-115">需求</span><span class="sxs-lookup"><span data-stu-id="d345f-115">Requirement</span></span> | <span data-ttu-id="d345f-116">值</span><span class="sxs-lookup"><span data-stu-id="d345f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d345f-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d345f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d345f-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d345f-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="d345f-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d345f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d345f-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d345f-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d345f-121">DLL</span><span class="sxs-lookup"><span data-stu-id="d345f-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d345f-122"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="d345f-122"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d345f-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d345f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d345f-124">**SystemMonitor.OnCounterAdded**</span><span class="sxs-lookup"><span data-stu-id="d345f-124">**SystemMonitor.OnCounterAdded**</span></span>](systemmonitor-oncounteradded.md)
</dt> <dt>

[<span data-ttu-id="d345f-125">**SystemMonitor.OnCounterSelected**</span><span class="sxs-lookup"><span data-stu-id="d345f-125">**SystemMonitor.OnCounterSelected**</span></span>](-systemmonitor-oncounterselected.md)
</dt> </dl>

 

 





