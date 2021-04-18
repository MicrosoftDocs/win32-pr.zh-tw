---
title: SystemMonitor. OnCounterSelected 事件
description: 在選取計數器時通知您。
ms.assetid: 788a95a7-47ec-41f9-bf46-324ad3cc8a4e
keywords:
- OnCounterSelected 事件 SysMon
- OnCounterSelected 事件 SysMon、SystemMonitor 類別
- SystemMonitor 類別 SysMon，OnCounterSelected 事件
topic_type:
- apiref
api_name:
- SystemMonitor.OnCounterSelected
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0174ab2f896a27e44df592ec28b7cb12a03198f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965496"
---
# <a name="systemmonitoroncounterselected-event"></a><span data-ttu-id="74c93-106">SystemMonitor. OnCounterSelected 事件</span><span class="sxs-lookup"><span data-stu-id="74c93-106">SystemMonitor.OnCounterSelected event</span></span>

<span data-ttu-id="74c93-107">在選取計數器時通知您。</span><span class="sxs-lookup"><span data-stu-id="74c93-107">Notifies you when a counter is selected.</span></span>

## <a name="syntax"></a><span data-ttu-id="74c93-108">語法</span><span class="sxs-lookup"><span data-stu-id="74c93-108">Syntax</span></span>


```VB
SystemMonitor.OnCounterSelected( _
  ByVal index As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="74c93-109">參數</span><span class="sxs-lookup"><span data-stu-id="74c93-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74c93-110">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="74c93-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74c93-111">[**計數器**](counters.md)集合物件中所選取計數器的索引。</span><span class="sxs-lookup"><span data-stu-id="74c93-111">Index of the selected counter in the [**Counters**](counters.md) collection object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74c93-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="74c93-112">Return value</span></span>

<span data-ttu-id="74c93-113">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="74c93-113">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="74c93-114">備註</span><span class="sxs-lookup"><span data-stu-id="74c93-114">Remarks</span></span>

<span data-ttu-id="74c93-115">您可以在下列情況收到此事件</span><span class="sxs-lookup"><span data-stu-id="74c93-115">You can receive this event when</span></span>

-   <span data-ttu-id="74c93-116">您將 [**CounterItem**](counteritem-selected.md) 設為 True</span><span class="sxs-lookup"><span data-stu-id="74c93-116">You set [**CounterItem.Selected**](counteritem-selected.md) to True</span></span>
-   <span data-ttu-id="74c93-117">使用者選取圖例中的計數器</span><span class="sxs-lookup"><span data-stu-id="74c93-117">The user selects a counter in the Legend</span></span>
-   <span data-ttu-id="74c93-118">使用者按兩下圖例中的計數器</span><span class="sxs-lookup"><span data-stu-id="74c93-118">The user double-clicks on a counter in the Legend</span></span>

## <a name="requirements"></a><span data-ttu-id="74c93-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="74c93-119">Requirements</span></span>



| <span data-ttu-id="74c93-120">需求</span><span class="sxs-lookup"><span data-stu-id="74c93-120">Requirement</span></span> | <span data-ttu-id="74c93-121">值</span><span class="sxs-lookup"><span data-stu-id="74c93-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="74c93-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="74c93-122">Minimum supported client</span></span><br/> | <span data-ttu-id="74c93-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74c93-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="74c93-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="74c93-124">Minimum supported server</span></span><br/> | <span data-ttu-id="74c93-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74c93-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="74c93-126">DLL</span><span class="sxs-lookup"><span data-stu-id="74c93-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74c93-127"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="74c93-127"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74c93-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74c93-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74c93-129">**SystemMonitor.OnCounterAdded**</span><span class="sxs-lookup"><span data-stu-id="74c93-129">**SystemMonitor.OnCounterAdded**</span></span>](systemmonitor-oncounteradded.md)
</dt> <dt>

[<span data-ttu-id="74c93-130">**SystemMonitor.OnCounterDeleted**</span><span class="sxs-lookup"><span data-stu-id="74c93-130">**SystemMonitor.OnCounterDeleted**</span></span>](-systemmonitor-oncounterdeleted.md)
</dt> </dl>

 

 





