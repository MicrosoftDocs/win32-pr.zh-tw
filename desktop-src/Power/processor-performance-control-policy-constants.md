---
description: 處理器效能控制原則常數指出適用于電源配置的處理器效能控制演算法。
ms.assetid: 928ba485-f767-47df-8b57-7630c68068a7
title: '處理器效能控制原則常數 (WinNT. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9597750f37d9efda80d4bb2bfff7bc121982e7d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513400"
---
# <a name="processor-performance-control-policy-constants"></a><span data-ttu-id="68ec6-103">處理器效能控制原則常數</span><span class="sxs-lookup"><span data-stu-id="68ec6-103">Processor Performance Control Policy Constants</span></span>

<span data-ttu-id="68ec6-104">處理器效能控制原則常數指出適用于電源配置的處理器效能控制演算法。</span><span class="sxs-lookup"><span data-stu-id="68ec6-104">The processor performance control policy constants indicate the processor performance control algorithm applied to a power scheme.</span></span>



| <span data-ttu-id="68ec6-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="68ec6-105">Constant/value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="68ec6-106">Description</span><span class="sxs-lookup"><span data-stu-id="68ec6-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PO_THROTTLE_ADAPTIVE"></span><span id="po_throttle_adaptive"></span><dl> <span data-ttu-id="68ec6-107"><dt>**PO \_節流 \_**</dt>調整 <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="68ec6-107"><dt>**PO\_THROTTLE\_ADAPTIVE**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="68ec6-108">嘗試使處理器效能符合目前的需求。</span><span class="sxs-lookup"><span data-stu-id="68ec6-108">Attempts to match the performance of the processor to the current demand.</span></span> <span data-ttu-id="68ec6-109">這項原則會使用高和低的電壓和頻率狀態。</span><span class="sxs-lookup"><span data-stu-id="68ec6-109">This policy will use both high and low voltage and frequency states.</span></span> <span data-ttu-id="68ec6-110">這項原則會將處理器的效能降至最低，只要沒有足夠的需求，就可以證明較高的電壓。</span><span class="sxs-lookup"><span data-stu-id="68ec6-110">This policy will lower the performance of the processor to the lowest voltage available whenever there is insufficient demand to justify a higher voltage.</span></span> <span data-ttu-id="68ec6-111">如果未使用 C3 狀態，並回應熱事件，此原則將會觸及處理器時鐘節流。</span><span class="sxs-lookup"><span data-stu-id="68ec6-111">This policy will engage processor clock throttling if the C3 state is not being utilized, and in response to thermal events.</span></span><br/> |
| <span id="PO_THROTTLE_CONSTANT"></span><span id="po_throttle_constant"></span><dl> <span data-ttu-id="68ec6-112"><dt>**PO \_節流 \_ 常數**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="68ec6-112"><dt>**PO\_THROTTLE\_CONSTANT**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="68ec6-113">不允許處理器使用任何高電壓的效能狀態。</span><span class="sxs-lookup"><span data-stu-id="68ec6-113">Does not allow the processor to use any high voltage performance states.</span></span> <span data-ttu-id="68ec6-114">除了回應熱事件之外，此原則不會與處理器時鐘節流互動。</span><span class="sxs-lookup"><span data-stu-id="68ec6-114">This policy will not engage processor clock throttling, except in response to thermal events.</span></span><br/>                                                                                                                                                                                                                                                                 |
| <span id="PO_THROTTLE_DEGRADE"></span><span id="po_throttle_degrade"></span><dl> <span data-ttu-id="68ec6-115"><dt>**PO \_節流 \_ 降級**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="68ec6-115"><dt>**PO\_THROTTLE\_DEGRADE**</dt> <dt>2</dt></span></span> </dl>    | <span data-ttu-id="68ec6-116">不允許處理器使用任何高電壓的效能狀態。</span><span class="sxs-lookup"><span data-stu-id="68ec6-116">Does not allow the processor to use any high voltage performance states.</span></span> <span data-ttu-id="68ec6-117">當電池低於特定閾值、未使用 C3 狀態，或回應熱事件時，此原則將會觸及處理器時鐘節流。</span><span class="sxs-lookup"><span data-stu-id="68ec6-117">This policy will engage processor clock throttling when the battery is below a certain threshold, if the C3 state is not being utilized, or in response to thermal events.</span></span><br/>                                                                                                                                                                                    |
| <span id="PO_THROTTLE_NONE"></span><span id="po_throttle_none"></span><dl> <span data-ttu-id="68ec6-118"><dt>**PO \_節流 \_ 無**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="68ec6-118"><dt>**PO\_THROTTLE\_NONE**</dt> <dt>0</dt></span></span> </dl>             | <span data-ttu-id="68ec6-119">未套用任何處理器效能控制。</span><span class="sxs-lookup"><span data-stu-id="68ec6-119">No processor performance control is applied.</span></span> <span data-ttu-id="68ec6-120">此原則一律會以最高的可能效能層級執行處理器。</span><span class="sxs-lookup"><span data-stu-id="68ec6-120">This policy always runs the processor at its highest possible performance level.</span></span> <span data-ttu-id="68ec6-121">除了回應熱事件之外，此原則不會與處理器時鐘節流互動。</span><span class="sxs-lookup"><span data-stu-id="68ec6-121">This policy will not engage processor clock throttling, except in response to thermal events.</span></span><br/>                                                                                                                                                                                                            |



## <a name="requirements"></a><span data-ttu-id="68ec6-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="68ec6-122">Requirements</span></span>



| <span data-ttu-id="68ec6-123">需求</span><span class="sxs-lookup"><span data-stu-id="68ec6-123">Requirement</span></span> | <span data-ttu-id="68ec6-124">值</span><span class="sxs-lookup"><span data-stu-id="68ec6-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68ec6-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="68ec6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="68ec6-126">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="68ec6-126">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="68ec6-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="68ec6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="68ec6-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="68ec6-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="68ec6-129">標頭</span><span class="sxs-lookup"><span data-stu-id="68ec6-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="68ec6-130"><dt>WinNT (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="68ec6-130"><dt>WinNT.h (include Windows.h)</dt></span></span> </dl> |



 

 




