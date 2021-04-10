---
title: CounterItem 選取的屬性
description: 抓取或設定值，這個值會指出是否已選取計數器。
ms.assetid: 293cc2ea-728c-4364-be2b-080bd188fe1c
keywords:
- 選取的屬性 SysMon
- 選取的屬性 SysMon，CounterItem 物件
- CounterItem 物件 SysMon，選取的屬性
topic_type:
- apiref
api_name:
- CounterItem.Selected
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac707dfaf2ed379884395a08128ddaeda771fa00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934479"
---
# <a name="counteritemselected-property"></a><span data-ttu-id="e4fd7-106">CounterItem 選取的屬性</span><span class="sxs-lookup"><span data-stu-id="e4fd7-106">CounterItem.Selected property</span></span>

<span data-ttu-id="e4fd7-107">抓取或設定值，這個值會指出是否已選取計數器。</span><span class="sxs-lookup"><span data-stu-id="e4fd7-107">Retrieves or sets a value that indicates if the counter is selected.</span></span>

<span data-ttu-id="e4fd7-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="e4fd7-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4fd7-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4fd7-109">Syntax</span></span>


```VB
Property Selected As Boolean
```



## <a name="property-value"></a><span data-ttu-id="e4fd7-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="e4fd7-110">Property value</span></span>

<span data-ttu-id="e4fd7-111">如果已選取計數器，則為 True;否則為 false。</span><span class="sxs-lookup"><span data-stu-id="e4fd7-111">True if the counter is selected; otherwise, false.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4fd7-112">備註</span><span class="sxs-lookup"><span data-stu-id="e4fd7-112">Remarks</span></span>

<span data-ttu-id="e4fd7-113">您可以從計數器集合中選取一個或多個計數器。</span><span class="sxs-lookup"><span data-stu-id="e4fd7-113">You can select one or more counters from the collection of counters.</span></span> <span data-ttu-id="e4fd7-114">選取計數器、選取圖例中的計數器、讓計數器顯示于圖例中，然後產生 [**OnCounterSelected**](-systemmonitor-oncounterselected.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="e4fd7-114">Selecting a counter, selects the counter in the Legend, makes the counter visible in the Legend, and generates an [**OnCounterSelected**](-systemmonitor-oncounterselected.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4fd7-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="e4fd7-115">Requirements</span></span>



| <span data-ttu-id="e4fd7-116">需求</span><span class="sxs-lookup"><span data-stu-id="e4fd7-116">Requirement</span></span> | <span data-ttu-id="e4fd7-117">值</span><span class="sxs-lookup"><span data-stu-id="e4fd7-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4fd7-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e4fd7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e4fd7-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e4fd7-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e4fd7-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e4fd7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e4fd7-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e4fd7-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e4fd7-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e4fd7-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4fd7-123"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="e4fd7-123"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4fd7-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e4fd7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4fd7-125">**CounterItem**</span><span class="sxs-lookup"><span data-stu-id="e4fd7-125">**CounterItem**</span></span>](counteritem.md)
</dt> </dl>

 

 





