---
description: LINEADDRESSSTATE \_ 位旗標常數描述各種位址狀態專案。
ms.assetid: f06140d0-f41a-4228-93c5-21d609af5473
title: 'LINEADDRESSSTATE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 483ac665c41989c65b43419442601dfb70667dc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000984"
---
# <a name="lineaddressstate_-constants"></a><span data-ttu-id="e41ee-103">LINEADDRESSSTATE \_ 常數</span><span class="sxs-lookup"><span data-stu-id="e41ee-103">LINEADDRESSSTATE\_ Constants</span></span>

<span data-ttu-id="e41ee-104">**LINEADDRESSSTATE \_** 位旗標常數描述各種位址狀態專案。</span><span class="sxs-lookup"><span data-stu-id="e41ee-104">The **LINEADDRESSSTATE\_** bit-flag constants describe various address status items.</span></span>

<dl> <dt>

<span data-ttu-id="e41ee-105"><span id="LINEADDRESSSTATE_CAPSCHANGE"></span><span id="lineaddressstate_capschange"></span>**LINEADDRESSSTATE \_ CAPSCHANGE**</span><span class="sxs-lookup"><span data-stu-id="e41ee-105"><span id="LINEADDRESSSTATE_CAPSCHANGE"></span><span id="lineaddressstate_capschange"></span>**LINEADDRESSSTATE\_CAPSCHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e41ee-106">指出，由於使用者或其他情況所做的設定變更，位址的 [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) 結構中有一或多個成員已變更。</span><span class="sxs-lookup"><span data-stu-id="e41ee-106">Indicates that, due to configuration changes made by the user or other circumstances, one or more of the members in the [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) structure for the address have changed.</span></span> <span data-ttu-id="e41ee-107">應用程式應該使用 [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps) 來讀取更新的結構。</span><span class="sxs-lookup"><span data-stu-id="e41ee-107">The application should use [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps) to read the updated structure.</span></span> <span data-ttu-id="e41ee-108">如果服務提供者將包含此值的 [**行 \_ ADDRESSSTATE**](line-addressstate.md) 訊息傳送至 tapi，tapi 會將它傳遞至已協商 tapi 1.4 版或更新版本的應用程式; 協調先前 API 版本的應用程式將會收到指定 LINEDEVSTATE 重新初始化的 [**行 \_ LINEDEVSTATE**](line-linedevstate.md) 訊息 \_ ，要求使用者將其關機並重新初始化，以取得更新的資訊。</span><span class="sxs-lookup"><span data-stu-id="e41ee-108">If a service provider sends a [**LINE\_ADDRESSSTATE**](line-addressstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will receive [**LINE\_LINEDEVSTATE**](line-linedevstate.md) messages specifying LINEDEVSTATE\_REINIT, requiring them to shut down and reinitialize their connection to TAPI to obtain the updated information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e41ee-109"><span id="LINEADDRESSSTATE_DEVSPECIFIC"></span><span id="lineaddressstate_devspecific"></span>**LINEADDRESSSTATE \_ DEVSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="e41ee-109"><span id="LINEADDRESSSTATE_DEVSPECIFIC"></span><span id="lineaddressstate_devspecific"></span>**LINEADDRESSSTATE\_DEVSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e41ee-110">位址狀態的裝置特定專案已變更。</span><span class="sxs-lookup"><span data-stu-id="e41ee-110">The device-specific item of the address status has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e41ee-111"><span id="LINEADDRESSSTATE_FORWARD"></span><span id="lineaddressstate_forward"></span>**\_向前 LINEADDRESSSTATE**</span><span class="sxs-lookup"><span data-stu-id="e41ee-111"><span id="LINEADDRESSSTATE_FORWARD"></span><span id="lineaddressstate_forward"></span>**LINEADDRESSSTATE\_FORWARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e41ee-112">位址的轉送狀態已變更，包括判斷無回應條件的環形數。</span><span class="sxs-lookup"><span data-stu-id="e41ee-112">The forwarding status of the address has changed, including possibly the number of rings for determining a no-answer condition.</span></span> <span data-ttu-id="e41ee-113">應用程式應該檢查位址狀態，以判斷位址目前轉送狀態的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e41ee-113">The application should check the address status to determine details about the address's current forwarding status.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e41ee-114"><span id="LINEADDRESSSTATE_INUSEMANY"></span><span id="lineaddressstate_inusemany"></span>**LINEADDRESSSTATE \_ INUSEMANY**</span><span class="sxs-lookup"><span data-stu-id="e41ee-114"><span id="LINEADDRESSSTATE_INUSEMANY"></span><span id="lineaddressstate_inusemany"></span>**LINEADDRESSSTATE\_INUSEMANY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e41ee-115">受監視或橋接的位址已變更，而不是由一個工作站使用於一個以上的工作站。</span><span class="sxs-lookup"><span data-stu-id="e41ee-115">The monitored or bridged address has changed from being in use by one station to being in use by more than one station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e41ee-116"><span id="LINEADDRESSSTATE_INUSEONE"></span><span id="lineaddressstate_inuseone"></span>**LINEADDRESSSTATE \_ INUSEONE**</span><span class="sxs-lookup"><span data-stu-id="e41ee-116"><span id="LINEADDRESSSTATE_INUSEONE"></span><span id="lineaddressstate_inuseone"></span>**LINEADDRESSSTATE\_INUSEONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e41ee-117">位址已從閒置狀態變更，或由許多橋接的電臺使用，只供一個站使用。</span><span class="sxs-lookup"><span data-stu-id="e41ee-117">The address has changed from idle or in use by many bridged stations to being in use by just one station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e41ee-118"><span id="LINEADDRESSSTATE_INUSEZERO"></span><span id="lineaddressstate_inusezero"></span>**LINEADDRESSSTATE \_ INUSEZERO**</span><span class="sxs-lookup"><span data-stu-id="e41ee-118"><span id="LINEADDRESSSTATE_INUSEZERO"></span><span id="lineaddressstate_inusezero"></span>**LINEADDRESSSTATE\_INUSEZERO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e41ee-119">位址已變更為閒置 (它未由任何工作站) 使用中。</span><span class="sxs-lookup"><span data-stu-id="e41ee-119">The address has changed to idle (it is not in use by any stations).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e41ee-120"><span id="LINEADDRESSSTATE_NUMCALLS"></span><span id="lineaddressstate_numcalls"></span>**LINEADDRESSSTATE \_ NUMCALLS**</span><span class="sxs-lookup"><span data-stu-id="e41ee-120"><span id="LINEADDRESSSTATE_NUMCALLS"></span><span id="lineaddressstate_numcalls"></span>**LINEADDRESSSTATE\_NUMCALLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e41ee-121">位址上的呼叫數目已變更。</span><span class="sxs-lookup"><span data-stu-id="e41ee-121">The number of calls on the address has changed.</span></span> <span data-ttu-id="e41ee-122">這是事件的結果，例如新的來電、位址上的外寄呼叫，或變更其保存狀態的呼叫。</span><span class="sxs-lookup"><span data-stu-id="e41ee-122">This is the result of events such as a new incoming call, an outgoing call on the address, or a call changing its hold status.</span></span> <span data-ttu-id="e41ee-123">此旗標涵蓋 [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)結構中任何成員 **dwNumActiveCalls**、 **dwNumOnHoldCalls** 和 **dwNumOnHoldPendingCalls** 的變更。</span><span class="sxs-lookup"><span data-stu-id="e41ee-123">This flag covers changes in any of the members **dwNumActiveCalls**, **dwNumOnHoldCalls** and **dwNumOnHoldPendingCalls** in the [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) structure.</span></span> <span data-ttu-id="e41ee-124">當應用程式收到 [**一行 \_ ADDRESSSTATE**](line-addressstate.md) (numCalls) 訊息時，應用程式應該會檢查這三個成員。</span><span class="sxs-lookup"><span data-stu-id="e41ee-124">The application should check all three of these members when it receives a [**LINE\_ADDRESSSTATE**](line-addressstate.md) (numCalls) message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e41ee-125"><span id="LINEADDRESSSTATE_OTHER"></span><span id="lineaddressstate_other"></span>**LINEADDRESSSTATE \_ 其他**</span><span class="sxs-lookup"><span data-stu-id="e41ee-125"><span id="LINEADDRESSSTATE_OTHER"></span><span id="lineaddressstate_other"></span>**LINEADDRESSSTATE\_OTHER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e41ee-126">位址-下列以外的狀態專案已變更。</span><span class="sxs-lookup"><span data-stu-id="e41ee-126">Address-status items other than those listed below have changed.</span></span> <span data-ttu-id="e41ee-127">應用程式應該檢查目前的位址狀態，以判斷哪些專案已經變更。</span><span class="sxs-lookup"><span data-stu-id="e41ee-127">The application should check the current address status to determine which items have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e41ee-128"><span id="LINEADDRESSSTATE_TERMINALS"></span><span id="lineaddressstate_terminals"></span>**LINEADDRESSSTATE \_ 終端機**</span><span class="sxs-lookup"><span data-stu-id="e41ee-128"><span id="LINEADDRESSSTATE_TERMINALS"></span><span id="lineaddressstate_terminals"></span>**LINEADDRESSSTATE\_TERMINALS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e41ee-129">位址的終端機設定已變更。</span><span class="sxs-lookup"><span data-stu-id="e41ee-129">The terminal settings for the address have changed.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e41ee-130">備註</span><span class="sxs-lookup"><span data-stu-id="e41ee-130">Remarks</span></span>

<span data-ttu-id="e41ee-131">無延伸。</span><span class="sxs-lookup"><span data-stu-id="e41ee-131">No extensibility.</span></span> <span data-ttu-id="e41ee-132">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="e41ee-132">All 32 bits are reserved.</span></span>

<span data-ttu-id="e41ee-133">在 [**\_ ADDRESSSTATE**](line-addressstate.md) 訊息中，會通知應用程式這些狀態專案的變更。</span><span class="sxs-lookup"><span data-stu-id="e41ee-133">An application is notified about changes to these status items in the [**LINE\_ADDRESSSTATE**](line-addressstate.md) message.</span></span> <span data-ttu-id="e41ee-134">位址的裝置功能指出可能為此位址報告的位址狀態變更。</span><span class="sxs-lookup"><span data-stu-id="e41ee-134">The address's device capabilities indicate which address state changes can possibly be reported for this address.</span></span>

## <a name="requirements"></a><span data-ttu-id="e41ee-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="e41ee-135">Requirements</span></span>



| <span data-ttu-id="e41ee-136">需求</span><span class="sxs-lookup"><span data-stu-id="e41ee-136">Requirement</span></span> | <span data-ttu-id="e41ee-137">值</span><span class="sxs-lookup"><span data-stu-id="e41ee-137">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e41ee-138">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="e41ee-138">TAPI version</span></span><br/> | <span data-ttu-id="e41ee-139">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="e41ee-139">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="e41ee-140">標頭</span><span class="sxs-lookup"><span data-stu-id="e41ee-140">Header</span></span><br/>       | <dl> <span data-ttu-id="e41ee-141"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="e41ee-141"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e41ee-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e41ee-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e41ee-143">**行 \_ ADDRESSSTATE**</span><span class="sxs-lookup"><span data-stu-id="e41ee-143">**LINE\_ADDRESSSTATE**</span></span>](line-addressstate.md)
</dt> <dt>

[<span data-ttu-id="e41ee-144">**行 \_ LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="e41ee-144">**LINE\_LINEDEVSTATE**</span></span>](line-linedevstate.md)
</dt> <dt>

[<span data-ttu-id="e41ee-145">**LINEADDRESSCAPS**</span><span class="sxs-lookup"><span data-stu-id="e41ee-145">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="e41ee-146">**LINEADDRESSSTATUS**</span><span class="sxs-lookup"><span data-stu-id="e41ee-146">**LINEADDRESSSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[<span data-ttu-id="e41ee-147">**lineGetAddressCaps**</span><span class="sxs-lookup"><span data-stu-id="e41ee-147">**lineGetAddressCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> </dl>

 

 




