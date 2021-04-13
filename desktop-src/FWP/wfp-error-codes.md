---
title: WFP 錯誤碼 (Winerror.h)
description: " (WFP) 特定錯誤碼。"
ms.assetid: 11f3085a-f044-4a78-b47a-59b9086562bf
topic_type:
- apiref
api_name:
- FWP_E_CALLOUT_NOT_FOUND
- FWP_E_CONDITION_NOT_FOUND
- FWP_E_FILTER_NOT_FOUND
- FWP_E_LAYER_NOT_FOUND
- FWP_E_PROVIDER_NOT_FOUND
- FWP_E_PROVIDER_CONTEXT_NOT_FOUND
- FWP_E_SUBLAYER_NOT_FOUND
- FWP_E_NOT_FOUND
- FWP_E_ALREADY_EXISTS
- FWP_E_IN_USE
- FWP_E_DYNAMIC_SESSION_IN_PROGRESS
- FWP_E_WRONG_SESSION
- FWP_E_NO_TXN_IN_PROGRESS
- FWP_E_TXN_IN_PROGRESS
- FWP_E_TXN_ABORTED
- FWP_E_SESSION_ABORTED
- FWP_E_INCOMPATIBLE_TXN
- FWP_E_TIMEOUT
- FWP_E_NET_EVENTS_DISABLED
- FWP_E_INCOMPATIBLE_LAYER
- FWP_E_KM_CLIENTS_ONLY
- FWP_E_LIFETIME_MISMATCH
- FWP_E_BUILTIN_OBJECT
- FWP_E_TOO_MANY_CALLOUTS
- FWP_E_NOTIFICATION_DROPPED
- FWP_E_TRAFFIC_MISMATCH
- FWP_E_INCOMPATIBLE_SA_STATE
- FWP_E_NULL_POINTER
- FWP_E_INVALID_ENUMERATOR
- FWP_E_INVALID_FLAGS
- FWP_E_INVALID_NET_MASK
- FWP_E_INVALID_RANGE
- FWP_E_INVALID_INTERVAL
- FWP_E_ZERO_LENGTH_ARRAY
- FWP_E_NULL_DISPLAY_NAME
- FWP_E_INVALID_ACTION_TYPE
- FWP_E_INVALID_WEIGHT
- FWP_E_MATCH_TYPE_MISMATCH
- FWP_E_TYPE_MISMATCH
- FWP_E_OUT_OF_BOUNDS
- FWP_E_RESERVED
- FWP_E_DUPLICATE_CONDITION
- FWP_E_DUPLICATE_KEYMOD
- FWP_E_ACTION_INCOMPATIBLE_WITH_LAYER
- FWP_E_ACTION_INCOMPATIBLE_WITH_SUBLAYER
- FWP_E_CONTEXT_INCOMPATIBLE_WITH_LAYER
- FWP_E_CONTEXT_INCOMPATIBLE_WITH_CALLOUT
- FWP_E_INCOMPATIBLE_AUTH_METHOD
- FWP_E_INCOMPATIBLE_DH_GROUP
- FWP_E_EM_NOT_SUPPORTED
- FWP_E_NEVER_MATCH
- FWP_E_PROVIDER_CONTEXT_MISMATCH
- FWP_E_INVALID_PARAMETER
- FWP_E_TOO_MANY_SUBLAYERS
- FWP_E_CALLOUT_NOTIFICATION_FAILED
- FWP_E_INVALID_AUTH_TRANSFORM
- FWP_E_INVALID_CIPHER_TRANSFORM
api_location:
- winerror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a0e7ee1ab0364a31f136f0c0cdbf87f459225b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466053"
---
# <a name="wfp-error-codes"></a><span data-ttu-id="fbbb4-103">WFP 錯誤碼</span><span class="sxs-lookup"><span data-stu-id="fbbb4-103">WFP Error Codes</span></span>

<span data-ttu-id="fbbb4-104">Windows 篩選平台 (WFP) 特定錯誤碼如下所示。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-104">Windows Filtering Platform (WFP) specific error codes are as follows.</span></span>

<dl> <dt>

<span data-ttu-id="fbbb4-105"><span id="FWP_E_CALLOUT_NOT_FOUND"></span><span id="fwp_e_callout_not_found"></span>**\_ \_ \_ \_ 找不到 .FWP E 標注**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-105"><span id="FWP_E_CALLOUT_NOT_FOUND"></span><span id="fwp_e_callout_not_found"></span>**FWP\_E\_CALLOUT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-106">0x80320001</span><span class="sxs-lookup"><span data-stu-id="fbbb4-106">0x80320001</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-107">標注不存在。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-107">The callout does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-108"><span id="FWP_E_CONDITION_NOT_FOUND"></span><span id="fwp_e_condition_not_found"></span>**\_ \_ \_ \_ 找不到 .FWP E 條件**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-108"><span id="FWP_E_CONDITION_NOT_FOUND"></span><span id="fwp_e_condition_not_found"></span>**FWP\_E\_CONDITION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-109">0x80320002</span><span class="sxs-lookup"><span data-stu-id="fbbb4-109">0x80320002</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-110">篩選準則不存在。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-110">The filter condition does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-111"><span id="FWP_E_FILTER_NOT_FOUND"></span><span id="fwp_e_filter_not_found"></span>**\_ \_ \_ \_ 找不到 .FWP E 篩選**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-111"><span id="FWP_E_FILTER_NOT_FOUND"></span><span id="fwp_e_filter_not_found"></span>**FWP\_E\_FILTER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-112">0x80320003</span><span class="sxs-lookup"><span data-stu-id="fbbb4-112">0x80320003</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-113">篩選不存在。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-113">The filter does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-114"><span id="FWP_E_LAYER_NOT_FOUND"></span><span id="fwp_e_layer_not_found"></span>**\_ \_ \_ 找不到 .FWP E 圖層 \_**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-114"><span id="FWP_E_LAYER_NOT_FOUND"></span><span id="fwp_e_layer_not_found"></span>**FWP\_E\_LAYER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-115">0x80320004</span><span class="sxs-lookup"><span data-stu-id="fbbb4-115">0x80320004</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-116">圖層不存在。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-116">The layer does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-117"><span id="FWP_E_PROVIDER_NOT_FOUND"></span><span id="fwp_e_provider_not_found"></span>**\_ \_ \_ 找不到 .FWP E 提供者 \_**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-117"><span id="FWP_E_PROVIDER_NOT_FOUND"></span><span id="fwp_e_provider_not_found"></span>**FWP\_E\_PROVIDER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-118">0x80320005</span><span class="sxs-lookup"><span data-stu-id="fbbb4-118">0x80320005</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-119">提供者不存在。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-119">The provider does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-120"><span id="FWP_E_PROVIDER_CONTEXT_NOT_FOUND"></span><span id="fwp_e_provider_context_not_found"></span>**\_ \_ \_ \_ \_ 找不到 .FWP E 提供者內容**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-120"><span id="FWP_E_PROVIDER_CONTEXT_NOT_FOUND"></span><span id="fwp_e_provider_context_not_found"></span>**FWP\_E\_PROVIDER\_CONTEXT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-121">0x80320006</span><span class="sxs-lookup"><span data-stu-id="fbbb4-121">0x80320006</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-122">提供者內容不存在。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-122">The provider context does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-123"><span id="FWP_E_SUBLAYER_NOT_FOUND"></span><span id="fwp_e_sublayer_not_found"></span>**\_ \_ \_ \_ 找不到 .FWP E 子層**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-123"><span id="FWP_E_SUBLAYER_NOT_FOUND"></span><span id="fwp_e_sublayer_not_found"></span>**FWP\_E\_SUBLAYER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-124">0x80320007</span><span class="sxs-lookup"><span data-stu-id="fbbb4-124">0x80320007</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-125">子層不存在。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-125">The sub-layer does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-126"><span id="FWP_E_NOT_FOUND"></span><span id="fwp_e_not_found"></span>**\_ \_ 找不到 .FWP E \_**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-126"><span id="FWP_E_NOT_FOUND"></span><span id="fwp_e_not_found"></span>**FWP\_E\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-127">0x80320008</span><span class="sxs-lookup"><span data-stu-id="fbbb4-127">0x80320008</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-128">物件不存在。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-128">The object does not exist.</span></span>

<span data-ttu-id="fbbb4-129">如果找不到 SA 內容識別碼， [IPsecSaCoNtext \* ](fwp-ipsec-functions.md)函數會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-129">The [IPsecSaContext\*](fwp-ipsec-functions.md) functions return this error if the SA context ID is not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-130"><span id="FWP_E_ALREADY_EXISTS"></span><span id="fwp_e_already_exists"></span>**\_ \_ 已有 .FWP \_ E**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-130"><span id="FWP_E_ALREADY_EXISTS"></span><span id="fwp_e_already_exists"></span>**FWP\_E\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-131">0x80320009</span><span class="sxs-lookup"><span data-stu-id="fbbb4-131">0x80320009</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-132">具有 GUID 或 LUID 的物件已經存在。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-132">An object with that GUID or LUID already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-133"><span id="FWP_E_IN_USE"></span><span id="fwp_e_in_use"></span>**\_ \_ 使用中的 .FWP 電子 \_**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-133"><span id="FWP_E_IN_USE"></span><span id="fwp_e_in_use"></span>**FWP\_E\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-134">0x8032000A</span><span class="sxs-lookup"><span data-stu-id="fbbb4-134">0x8032000A</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-135">物件是由其他物件所參考，所以無法刪除。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-135">The object is referenced by other objects, so it cannot be deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-136"><span id="FWP_E_DYNAMIC_SESSION_IN_PROGRESS"></span><span id="fwp_e_dynamic_session_in_progress"></span>**\_ \_ \_ \_ 正在進行的 .FWP 電子動態會話 \_**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-136"><span id="FWP_E_DYNAMIC_SESSION_IN_PROGRESS"></span><span id="fwp_e_dynamic_session_in_progress"></span>**FWP\_E\_DYNAMIC\_SESSION\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-137">0x8032000B</span><span class="sxs-lookup"><span data-stu-id="fbbb4-137">0x8032000B</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-138">不允許從動態會話內呼叫。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-138">The call is not allowed from within a dynamic session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-139"><span id="FWP_E_WRONG_SESSION"></span><span id="fwp_e_wrong_session"></span>**.FWP 的 \_ 電子 \_ 錯誤 \_ 會話**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-139"><span id="FWP_E_WRONG_SESSION"></span><span id="fwp_e_wrong_session"></span>**FWP\_E\_WRONG\_SESSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-140">0x8032000C</span><span class="sxs-lookup"><span data-stu-id="fbbb4-140">0x8032000C</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-141">從錯誤的會話進行呼叫，因此無法完成。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-141">The call was made from the wrong session, so it cannot be completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-142"><span id="FWP_E_NO_TXN_IN_PROGRESS"></span><span id="fwp_e_no_txn_in_progress"></span>**\_ \_ 未 \_ \_ \_ 進行的 .FWP E TXN**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-142"><span id="FWP_E_NO_TXN_IN_PROGRESS"></span><span id="fwp_e_no_txn_in_progress"></span>**FWP\_E\_NO\_TXN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-143">0x8032000D</span><span class="sxs-lookup"><span data-stu-id="fbbb4-143">0x8032000D</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-144">呼叫必須從明確交易內進行。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-144">The call must be made from within an explicit transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-145"><span id="FWP_E_TXN_IN_PROGRESS"></span><span id="fwp_e_txn_in_progress"></span>**\_ \_ \_ 正在進行的 .FWP 電子 TXN \_**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-145"><span id="FWP_E_TXN_IN_PROGRESS"></span><span id="fwp_e_txn_in_progress"></span>**FWP\_E\_TXN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-146">0x8032000E</span><span class="sxs-lookup"><span data-stu-id="fbbb4-146">0x8032000E</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-147">不允許從明確交易內呼叫。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-147">The call is not allowed from within an explicit transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-148"><span id="FWP_E_TXN_ABORTED"></span><span id="fwp_e_txn_aborted"></span>**已 \_ 中止 .FWP E \_ TXN \_**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-148"><span id="FWP_E_TXN_ABORTED"></span><span id="fwp_e_txn_aborted"></span>**FWP\_E\_TXN\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-149">0x8032000F</span><span class="sxs-lookup"><span data-stu-id="fbbb4-149">0x8032000F</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-150">明確的交易已強制取消。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-150">The explicit transaction has been forcibly canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-151"><span id="FWP_E_SESSION_ABORTED"></span><span id="fwp_e_session_aborted"></span>**已 \_ 中止 .FWP E \_ 會話 \_**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-151"><span id="FWP_E_SESSION_ABORTED"></span><span id="fwp_e_session_aborted"></span>**FWP\_E\_SESSION\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-152">0x80320010</span><span class="sxs-lookup"><span data-stu-id="fbbb4-152">0x80320010</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-153">會話已取消。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-153">The session has been canceled.</span></span>

<span data-ttu-id="fbbb4-154">會話控制碼必須藉由呼叫 [**FwpmEngineClose0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineclose0)來關閉，即使它已不再有效也是一樣。否則，用戶端狀態將會流失。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-154">The session handle needs to be closed by calling [**FwpmEngineClose0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineclose0), even though it is no longer valid; otherwise, the client-side state will be leaked.</span></span> <span data-ttu-id="fbbb4-155">您應呼叫 [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)來建立新的會話。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-155">A new session should be created by calling [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-156"><span id="FWP_E_INCOMPATIBLE_TXN"></span><span id="fwp_e_incompatible_txn"></span>**.FWP 的 \_ 電子 \_ 不相容 \_ TXN**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-156"><span id="FWP_E_INCOMPATIBLE_TXN"></span><span id="fwp_e_incompatible_txn"></span>**FWP\_E\_INCOMPATIBLE\_TXN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-157">0x80320011</span><span class="sxs-lookup"><span data-stu-id="fbbb4-157">0x80320011</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-158">不允許在唯讀交易內進行呼叫。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-158">The call is not allowed from within a read-only transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-159"><span id="FWP_E_TIMEOUT"></span><span id="fwp_e_timeout"></span>**.FWP \_ E \_ TIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-159"><span id="FWP_E_TIMEOUT"></span><span id="fwp_e_timeout"></span>**FWP\_E\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-160">0x80320012</span><span class="sxs-lookup"><span data-stu-id="fbbb4-160">0x80320012</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-161">呼叫會在等候取得交易鎖定的時候超時。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-161">The call timed out while waiting to acquire the transaction lock.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-162"><span id="FWP_E_NET_EVENTS_DISABLED"></span><span id="fwp_e_net_events_disabled"></span>**\_ \_ \_ \_ 已停用 .FWP 的電子網路**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-162"><span id="FWP_E_NET_EVENTS_DISABLED"></span><span id="fwp_e_net_events_disabled"></span>**FWP\_E\_NET\_EVENTS\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-163">0x80320013</span><span class="sxs-lookup"><span data-stu-id="fbbb4-163">0x80320013</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-164">已停用網路診斷事件的收集。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-164">The collection of network diagnostic events is disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-165"><span id="FWP_E_INCOMPATIBLE_LAYER"></span><span id="fwp_e_incompatible_layer"></span>**.FWP \_ E \_ 不相容的 \_ 圖層**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-165"><span id="FWP_E_INCOMPATIBLE_LAYER"></span><span id="fwp_e_incompatible_layer"></span>**FWP\_E\_INCOMPATIBLE\_LAYER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-166">0x80320014</span><span class="sxs-lookup"><span data-stu-id="fbbb4-166">0x80320014</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-167">指定的層級不支援此作業。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-167">The operation is not supported by the specified layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-168"><span id="FWP_E_KM_CLIENTS_ONLY"></span><span id="fwp_e_km_clients_only"></span>**\_僅限 .FWP 的 E \_ KM \_ 用戶端 \_**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-168"><span id="FWP_E_KM_CLIENTS_ONLY"></span><span id="fwp_e_km_clients_only"></span>**FWP\_E\_KM\_CLIENTS\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-169">0x80320015</span><span class="sxs-lookup"><span data-stu-id="fbbb4-169">0x80320015</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-170">只有核心模式呼叫端可以呼叫。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-170">The call is allowed for kernel-mode callers only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-171"><span id="FWP_E_LIFETIME_MISMATCH"></span><span id="fwp_e_lifetime_mismatch"></span>**.FWP \_ E \_ 存留期 \_ 不符**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-171"><span id="FWP_E_LIFETIME_MISMATCH"></span><span id="fwp_e_lifetime_mismatch"></span>**FWP\_E\_LIFETIME\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-172">0x80320016</span><span class="sxs-lookup"><span data-stu-id="fbbb4-172">0x80320016</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-173">呼叫嘗試將兩個物件與不相容的存留期產生關聯。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-173">The call tried to associate two objects with incompatible lifetimes.</span></span>

<span data-ttu-id="fbbb4-174">如需物件存留期和物件關聯的詳細資訊，請參閱 [物件管理](object-management.md) 。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-174">See [Object Management](object-management.md) for more information on object lifetime and object association.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-175"><span id="FWP_E_BUILTIN_OBJECT"></span><span id="fwp_e_builtin_object"></span>**.FWP \_ E 內 \_ 建 \_ 物件**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-175"><span id="FWP_E_BUILTIN_OBJECT"></span><span id="fwp_e_builtin_object"></span>**FWP\_E\_BUILTIN\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-176">0x80320017</span><span class="sxs-lookup"><span data-stu-id="fbbb4-176">0x80320017</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-177">物件是內建的，因此無法刪除。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-177">The object is built-in, so it cannot be deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-178"><span id="FWP_E_TOO_MANY_CALLOUTS"></span><span id="fwp_e_too_many_callouts"></span>**.FWP 的 \_ 電子 \_ 太 \_ 多 \_ 標注**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-178"><span id="FWP_E_TOO_MANY_CALLOUTS"></span><span id="fwp_e_too_many_callouts"></span>**FWP\_E\_TOO\_MANY\_CALLOUTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-179">0x80320018</span><span class="sxs-lookup"><span data-stu-id="fbbb4-179">0x80320018</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-180">已達到最大的標注數目。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-180">The maximum number of callouts has been reached.</span></span>

<span data-ttu-id="fbbb4-181">最多可以同時註冊100000個標注。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-181">At most, 100,000 callouts can be registered at the same time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-182"><span id="FWP_E_NOTIFICATION_DROPPED"></span><span id="fwp_e_notification_dropped"></span>**已捨棄的 .FWP \_ E \_ 通知 \_**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-182"><span id="FWP_E_NOTIFICATION_DROPPED"></span><span id="fwp_e_notification_dropped"></span>**FWP\_E\_NOTIFICATION\_DROPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-183">0x80320019</span><span class="sxs-lookup"><span data-stu-id="fbbb4-183">0x80320019</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-184">因為訊息佇列的最大容量，所以無法傳遞通知。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-184">A notification could not be delivered because a message queue is at its maximum capacity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-185"><span id="FWP_E_TRAFFIC_MISMATCH"></span><span id="fwp_e_traffic_mismatch"></span>**.FWP 的 \_ 電子 \_ 流量 \_ 不符**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-185"><span id="FWP_E_TRAFFIC_MISMATCH"></span><span id="fwp_e_traffic_mismatch"></span>**FWP\_E\_TRAFFIC\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-186">0x8032001A</span><span class="sxs-lookup"><span data-stu-id="fbbb4-186">0x8032001A</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-187">網路流量參數不符合安全性關聯內容的參數。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-187">The network traffic parameters do not match those for the security association context.</span></span>

<span data-ttu-id="fbbb4-188">您可以多次呼叫 [**IPsecSaCoNtextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0) ，但呼叫端必須每次都指定相同的 [**IPSEC \_ TRAFFIC0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic0) 。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-188">[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0) can be called multiple times, but the caller must specify the same [**IPSEC\_TRAFFIC0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic0) each time.</span></span> <span data-ttu-id="fbbb4-189">如果後續的呼叫提供不同的 **IPSEC \_ TRAFFIC0**，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-189">This error is returned if a subsequent call supplies a different **IPSEC\_TRAFFIC0**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-190"><span id="FWP_E_INCOMPATIBLE_SA_STATE"></span><span id="fwp_e_incompatible_sa_state"></span>**.FWP \_ E \_ 不相容的 \_ SA \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-190"><span id="FWP_E_INCOMPATIBLE_SA_STATE"></span><span id="fwp_e_incompatible_sa_state"></span>**FWP\_E\_INCOMPATIBLE\_SA\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-191">0x8032001B</span><span class="sxs-lookup"><span data-stu-id="fbbb4-191">0x8032001B</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-192"> (SA) 狀態的目前安全性關聯不允許此呼叫。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-192">The call is not allowed for the current security association (SA) state.</span></span>

<span data-ttu-id="fbbb4-193">SA 內容函式必須以特定順序呼叫：</span><span class="sxs-lookup"><span data-stu-id="fbbb4-193">The SA context functions must be called in a specific order:</span></span>

-   [<span data-ttu-id="fbbb4-194">**IPsecSaCoNtextCreate0**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-194">**IPsecSaContextCreate0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)
-   [<span data-ttu-id="fbbb4-195">**IPsecSaCoNtextGetSpi0**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-195">**IPsecSaContextGetSpi0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)
-   [<span data-ttu-id="fbbb4-196">**IPsecSaCoNtextAddInbound0**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-196">**IPsecSaContextAddInbound0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)
-   [<span data-ttu-id="fbbb4-197">**IPsecSaCoNtextAddOutbound0**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-197">**IPsecSaContextAddOutbound0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)

<span data-ttu-id="fbbb4-198">如果以順序呼叫此錯誤，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-198">This error is returned if they are called out of order.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-199"><span id="FWP_E_NULL_POINTER"></span><span id="fwp_e_null_pointer"></span>**.FWP \_ E \_ Null \_ 指標**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-199"><span id="FWP_E_NULL_POINTER"></span><span id="fwp_e_null_pointer"></span>**FWP\_E\_NULL\_POINTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-200">0x8032001C</span><span class="sxs-lookup"><span data-stu-id="fbbb4-200">0x8032001C</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-201">必要的指標為 null。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-201">A required pointer is null.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-202"><span id="FWP_E_INVALID_ENUMERATOR"></span><span id="fwp_e_invalid_enumerator"></span>**.FWP \_ E \_ 不正確 \_ 枚舉器**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-202"><span id="FWP_E_INVALID_ENUMERATOR"></span><span id="fwp_e_invalid_enumerator"></span>**FWP\_E\_INVALID\_ENUMERATOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-203">0x8032001D</span><span class="sxs-lookup"><span data-stu-id="fbbb4-203">0x8032001D</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-204">結構中的列舉值超出範圍。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-204">An enumerator value in a structure is out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-205"><span id="FWP_E_INVALID_FLAGS"></span><span id="fwp_e_invalid_flags"></span>**.FWP \_ E \_ 不正確 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-205"><span id="FWP_E_INVALID_FLAGS"></span><span id="fwp_e_invalid_flags"></span>**FWP\_E\_INVALID\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-206">0x8032001E</span><span class="sxs-lookup"><span data-stu-id="fbbb4-206">0x8032001E</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-207">[旗標] 欄位包含不正確值。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-207">The flags field contains an invalid value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-208"><span id="FWP_E_INVALID_NET_MASK"></span><span id="fwp_e_invalid_net_mask"></span>**.FWP \_ E \_ 不正確 \_ 淨 \_ 遮罩**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-208"><span id="FWP_E_INVALID_NET_MASK"></span><span id="fwp_e_invalid_net_mask"></span>**FWP\_E\_INVALID\_NET\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-209">0x8032001F</span><span class="sxs-lookup"><span data-stu-id="fbbb4-209">0x8032001F</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-210">網路遮罩無效。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-210">A network mask is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-211"><span id="FWP_E_INVALID_RANGE"></span><span id="fwp_e_invalid_range"></span>**.FWP \_ E \_ 無效 \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-211"><span id="FWP_E_INVALID_RANGE"></span><span id="fwp_e_invalid_range"></span>**FWP\_E\_INVALID\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-212">0x80320020</span><span class="sxs-lookup"><span data-stu-id="fbbb4-212">0x80320020</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-213">[**.Fwp \_ RANGE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_range0)結構無效。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-213">An [**FWP\_RANGE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_range0) structure is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-214"><span id="FWP_E_INVALID_INTERVAL"></span><span id="fwp_e_invalid_interval"></span>**.FWP \_ E \_ 無效 \_ 間隔**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-214"><span id="FWP_E_INVALID_INTERVAL"></span><span id="fwp_e_invalid_interval"></span>**FWP\_E\_INVALID\_INTERVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-215">0x80320021</span><span class="sxs-lookup"><span data-stu-id="fbbb4-215">0x80320021</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-216">時間間隔無效。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-216">The time interval is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-217"><span id="FWP_E_ZERO_LENGTH_ARRAY"></span><span id="fwp_e_zero_length_array"></span>**.FWP \_ E \_ 零 \_ 長度 \_ 陣列**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-217"><span id="FWP_E_ZERO_LENGTH_ARRAY"></span><span id="fwp_e_zero_length_array"></span>**FWP\_E\_ZERO\_LENGTH\_ARRAY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-218">0x80320022</span><span class="sxs-lookup"><span data-stu-id="fbbb4-218">0x80320022</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-219">必須包含至少一個元素的陣列長度為零。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-219">An array that must contain at least one element has zero length.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-220"><span id="FWP_E_NULL_DISPLAY_NAME"></span><span id="fwp_e_null_display_name"></span>**.FWP \_ E \_ Null \_ 顯示 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-220"><span id="FWP_E_NULL_DISPLAY_NAME"></span><span id="fwp_e_null_display_name"></span>**FWP\_E\_NULL\_DISPLAY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-221">0x80320023</span><span class="sxs-lookup"><span data-stu-id="fbbb4-221">0x80320023</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-222">**DisplayData.name** 欄位不可以是 null。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-222">The **displayData.name** field cannot be null.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-223"><span id="FWP_E_INVALID_ACTION_TYPE"></span><span id="fwp_e_invalid_action_type"></span>**.FWP \_ E \_ 不正確 \_ 動作 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-223"><span id="FWP_E_INVALID_ACTION_TYPE"></span><span id="fwp_e_invalid_action_type"></span>**FWP\_E\_INVALID\_ACTION\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-224">0x80320024</span><span class="sxs-lookup"><span data-stu-id="fbbb4-224">0x80320024</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-225">動作類型不是篩選準則的其中一個允許動作類型。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-225">The action type is not one of the allowed action types for a filter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-226"><span id="FWP_E_INVALID_WEIGHT"></span><span id="fwp_e_invalid_weight"></span>**.FWP \_ E \_ 不正確 \_ 權數**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-226"><span id="FWP_E_INVALID_WEIGHT"></span><span id="fwp_e_invalid_weight"></span>**FWP\_E\_INVALID\_WEIGHT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-227">0x80320025</span><span class="sxs-lookup"><span data-stu-id="fbbb4-227">0x80320025</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-228">篩選權數無效。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-228">The filter weight is not valid.</span></span>

<span data-ttu-id="fbbb4-229">如需詳細資訊，請參閱 [篩選權數指派](filter-weight-assignment.md) 。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-229">See [Filter Weight Assignment](filter-weight-assignment.md) for more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-230"><span id="FWP_E_MATCH_TYPE_MISMATCH"></span><span id="fwp_e_match_type_mismatch"></span>**.FWP \_ E \_ 符合 \_ 類型 \_ 不符**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-230"><span id="FWP_E_MATCH_TYPE_MISMATCH"></span><span id="fwp_e_match_type_mismatch"></span>**FWP\_E\_MATCH\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-231">0x80320026</span><span class="sxs-lookup"><span data-stu-id="fbbb4-231">0x80320026</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-232">篩選準則包含與運算元不相容的比對類型。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-232">A filter condition contains a match type that is not compatible with the operands.</span></span>

<span data-ttu-id="fbbb4-233">如需詳細資訊，請參閱 [**.Fwp \_ 相符 \_ 類型**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type) 。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-233">See [**FWP\_MATCH\_TYPE**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type) for more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-234"><span id="FWP_E_TYPE_MISMATCH"></span><span id="fwp_e_type_mismatch"></span>**.FWP \_ E \_ 類型 \_ 不符**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-234"><span id="FWP_E_TYPE_MISMATCH"></span><span id="fwp_e_type_mismatch"></span>**FWP\_E\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-235">0x80320027</span><span class="sxs-lookup"><span data-stu-id="fbbb4-235">0x80320027</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-236">[**.Fwp \_ VALUE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_value0)結構或 [**FWPM \_ 條件 \_ VALUE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_condition_value0)結構的型別錯誤。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-236">An [**FWP\_VALUE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_value0) structure or an [**FWPM\_CONDITION\_VALUE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_condition_value0) structure is of the wrong type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-237"><span id="FWP_E_OUT_OF_BOUNDS"></span><span id="fwp_e_out_of_bounds"></span>**已 \_ \_ 超出 \_ 範圍的 \_ .FWP E**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-237"><span id="FWP_E_OUT_OF_BOUNDS"></span><span id="fwp_e_out_of_bounds"></span>**FWP\_E\_OUT\_OF\_BOUNDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-238">0x80320028</span><span class="sxs-lookup"><span data-stu-id="fbbb4-238">0x80320028</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-239">整數值超出允許的範圍。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-239">An integer value is outside the allowed range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-240"><span id="FWP_E_RESERVED"></span><span id="fwp_e_reserved"></span>**.FWP \_ E \_ 保留**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-240"><span id="FWP_E_RESERVED"></span><span id="fwp_e_reserved"></span>**FWP\_E\_RESERVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-241">0x80320029</span><span class="sxs-lookup"><span data-stu-id="fbbb4-241">0x80320029</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-242">保留的欄位不是零。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-242">A reserved field is nonzero.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-243"><span id="FWP_E_DUPLICATE_CONDITION"></span><span id="fwp_e_duplicate_condition"></span>**.FWP \_ E \_ 重複 \_ 條件**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-243"><span id="FWP_E_DUPLICATE_CONDITION"></span><span id="fwp_e_duplicate_condition"></span>**FWP\_E\_DUPLICATE\_CONDITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-244">0x8032002A</span><span class="sxs-lookup"><span data-stu-id="fbbb4-244">0x8032002A</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-245">篩選準則不能包含多個在單一欄位上運作的條件。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-245">A filter cannot contain multiple conditions operating on a single field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-246"><span id="FWP_E_DUPLICATE_KEYMOD"></span><span id="fwp_e_duplicate_keymod"></span>**.FWP \_ E \_ 重複的 \_ KEYMOD**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-246"><span id="FWP_E_DUPLICATE_KEYMOD"></span><span id="fwp_e_duplicate_keymod"></span>**FWP\_E\_DUPLICATE\_KEYMOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-247">0x8032002B</span><span class="sxs-lookup"><span data-stu-id="fbbb4-247">0x8032002B</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-248">原則不能包含相同的加密模組一次以上。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-248">A policy cannot contain the same keying module more than once.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-249"><span id="FWP_E_ACTION_INCOMPATIBLE_WITH_LAYER"></span><span id="fwp_e_action_incompatible_with_layer"></span>**\_ \_ \_ \_ 與圖層不相容的 \_ .FWP E 動作**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-249"><span id="FWP_E_ACTION_INCOMPATIBLE_WITH_LAYER"></span><span id="fwp_e_action_incompatible_with_layer"></span>**FWP\_E\_ACTION\_INCOMPATIBLE\_WITH\_LAYER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-250">0x8032002C</span><span class="sxs-lookup"><span data-stu-id="fbbb4-250">0x8032002C</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-251">動作類型與圖層不相容。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-251">The action type is not compatible with the layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-252"><span id="FWP_E_ACTION_INCOMPATIBLE_WITH_SUBLAYER"></span><span id="fwp_e_action_incompatible_with_sublayer"></span>**\_ \_ \_ \_ 具有子層的 .FWP E 動作不相容 \_**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-252"><span id="FWP_E_ACTION_INCOMPATIBLE_WITH_SUBLAYER"></span><span id="fwp_e_action_incompatible_with_sublayer"></span>**FWP\_E\_ACTION\_INCOMPATIBLE\_WITH\_SUBLAYER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-253">0x8032002D</span><span class="sxs-lookup"><span data-stu-id="fbbb4-253">0x8032002D</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-254">動作類型與子層不相容。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-254">The action type is not compatible with the sub-layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-255"><span id="FWP_E_CONTEXT_INCOMPATIBLE_WITH_LAYER"></span><span id="fwp_e_context_incompatible_with_layer"></span>**.FWP \_ E \_ 內容 \_ \_ 與 \_ 圖層不相容**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-255"><span id="FWP_E_CONTEXT_INCOMPATIBLE_WITH_LAYER"></span><span id="fwp_e_context_incompatible_with_layer"></span>**FWP\_E\_CONTEXT\_INCOMPATIBLE\_WITH\_LAYER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-256">0x8032002E</span><span class="sxs-lookup"><span data-stu-id="fbbb4-256">0x8032002E</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-257">原始內容或提供者內容與圖層不相容。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-257">The raw context or the provider context is not compatible with the layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-258"><span id="FWP_E_CONTEXT_INCOMPATIBLE_WITH_CALLOUT"></span><span id="fwp_e_context_incompatible_with_callout"></span>**.FWP \_ E \_ 內容 \_ \_ 與 \_ 標注不相容**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-258"><span id="FWP_E_CONTEXT_INCOMPATIBLE_WITH_CALLOUT"></span><span id="fwp_e_context_incompatible_with_callout"></span>**FWP\_E\_CONTEXT\_INCOMPATIBLE\_WITH\_CALLOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-259">0x8032002F</span><span class="sxs-lookup"><span data-stu-id="fbbb4-259">0x8032002F</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-260">原始內容或提供者內容與標注不相容。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-260">The raw context or the provider context is not compatible with the callout.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-261"><span id="FWP_E_INCOMPATIBLE_AUTH_METHOD"></span><span id="fwp_e_incompatible_auth_method"></span>**.FWP 的 \_ 電子 \_ 不相容 \_ AUTH \_ 方法**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-261"><span id="FWP_E_INCOMPATIBLE_AUTH_METHOD"></span><span id="fwp_e_incompatible_auth_method"></span>**FWP\_E\_INCOMPATIBLE\_AUTH\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-262">0x80320030</span><span class="sxs-lookup"><span data-stu-id="fbbb4-262">0x80320030</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-263">驗證方法與原則類型不相容。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-263">The authentication method is not compatible with the policy type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-264"><span id="FWP_E_INCOMPATIBLE_DH_GROUP"></span><span id="fwp_e_incompatible_dh_group"></span>**.FWP 的 \_ 電子 \_ 不相容 \_ DH \_ 群組**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-264"><span id="FWP_E_INCOMPATIBLE_DH_GROUP"></span><span id="fwp_e_incompatible_dh_group"></span>**FWP\_E\_INCOMPATIBLE\_DH\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-265">0x80320031L</span><span class="sxs-lookup"><span data-stu-id="fbbb4-265">0x80320031L</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-266">Diffie-Hellman 群組與原則類型不相容。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-266">The Diffie-Hellman group is not compatible with the policy type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-267"><span id="FWP_E_EM_NOT_SUPPORTED"></span><span id="fwp_e_em_not_supported"></span>**\_ \_ \_ 不支援 .FWP E \_ EM**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-267"><span id="FWP_E_EM_NOT_SUPPORTED"></span><span id="fwp_e_em_not_supported"></span>**FWP\_E\_EM\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-268">0x80320032</span><span class="sxs-lookup"><span data-stu-id="fbbb4-268">0x80320032</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-269">IKE 原則不能包含擴充模式原則。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-269">An IKE policy cannot contain an Extended Mode policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-270"><span id="FWP_E_NEVER_MATCH"></span><span id="fwp_e_never_match"></span>**.FWP \_ E \_ 永不 \_ 相符**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-270"><span id="FWP_E_NEVER_MATCH"></span><span id="fwp_e_never_match"></span>**FWP\_E\_NEVER\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-271">0x80320033</span><span class="sxs-lookup"><span data-stu-id="fbbb4-271">0x80320033</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-272">列舉範本或訂閱永遠不會與任何物件相符。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-272">The enumeration template or subscription will never match any objects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-273"><span id="FWP_E_PROVIDER_CONTEXT_MISMATCH"></span><span id="fwp_e_provider_context_mismatch"></span>**.FWP \_ E \_ 提供者 \_ 內容 \_ 不符**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-273"><span id="FWP_E_PROVIDER_CONTEXT_MISMATCH"></span><span id="fwp_e_provider_context_mismatch"></span>**FWP\_E\_PROVIDER\_CONTEXT\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-274">0x80320034</span><span class="sxs-lookup"><span data-stu-id="fbbb4-274">0x80320034</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-275">提供者內容的類型錯誤。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-275">The provider context is of the wrong type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-276"><span id="FWP_E_INVALID_PARAMETER"></span><span id="fwp_e_invalid_parameter"></span>**.FWP \_ E \_ 不正確 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-276"><span id="FWP_E_INVALID_PARAMETER"></span><span id="fwp_e_invalid_parameter"></span>**FWP\_E\_INVALID\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-277">0x80320035</span><span class="sxs-lookup"><span data-stu-id="fbbb4-277">0x80320035</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-278">參數錯誤。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-278">The parameter is incorrect.</span></span>

<span data-ttu-id="fbbb4-279">此錯誤的可能原因：</span><span class="sxs-lookup"><span data-stu-id="fbbb4-279">Possible reasons for this error:</span></span>

-   <span data-ttu-id="fbbb4-280">呼叫 [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0)時，不需將旗標 **FWPM 通道旗標指向 [ \_ \_ \_ \_ \_ 點**] 和 [本機/遠端位址以外的條件]。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-280">[**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) was called without setting the flag **FWPM\_TUNNEL\_FLAG\_POINT\_TO\_POINT** and with conditions other than local/remote address.</span></span>
-   <span data-ttu-id="fbbb4-281">不正確 Unicode 字串，或包含不可列印字元的 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-281">An invalid Unicode string, or a Unicode string that contains unprintable characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-282"><span id="FWP_E_TOO_MANY_SUBLAYERS"></span><span id="fwp_e_too_many_sublayers"></span>**.FWP 的 \_ 電子郵件 \_ 太 \_ 多 \_ 子層**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-282"><span id="FWP_E_TOO_MANY_SUBLAYERS"></span><span id="fwp_e_too_many_sublayers"></span>**FWP\_E\_TOO\_MANY\_SUBLAYERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-283">0x80320036</span><span class="sxs-lookup"><span data-stu-id="fbbb4-283">0x80320036</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-284">已達到子層的最大數目。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-284">The maximum number of sublayers has been reached.</span></span>

<span data-ttu-id="fbbb4-285">WFP 最多可支援 2 6 個子層。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-285">WFP supports at most 2 6 sublayers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-286"><span id="FWP_E_CALLOUT_NOTIFICATION_FAILED"></span><span id="fwp_e_callout_notification_failed"></span>**.FWP \_ E \_ 標注 \_ 通知 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-286"><span id="FWP_E_CALLOUT_NOTIFICATION_FAILED"></span><span id="fwp_e_callout_notification_failed"></span>**FWP\_E\_CALLOUT\_NOTIFICATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-287">0x80320037</span><span class="sxs-lookup"><span data-stu-id="fbbb4-287">0x80320037</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-288">標注的通知函數傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-288">The notification function for a callout returned an error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-289"><span id="FWP_E_INVALID_AUTH_TRANSFORM"></span><span id="fwp_e_invalid_auth_transform"></span>**.FWP \_ 電子 \_ 不正確 \_ 驗證 \_ 轉換**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-289"><span id="FWP_E_INVALID_AUTH_TRANSFORM"></span><span id="fwp_e_invalid_auth_transform"></span>**FWP\_E\_INVALID\_AUTH\_TRANSFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-290">0x80320038</span><span class="sxs-lookup"><span data-stu-id="fbbb4-290">0x80320038</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-291">IPsec 驗證轉換無效。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-291">The IPsec authentication transform is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbbb4-292"><span id="FWP_E_INVALID_CIPHER_TRANSFORM"></span><span id="fwp_e_invalid_cipher_transform"></span>**.FWP \_ E \_ 不正確 \_ 密碼 \_ 轉換**</span><span class="sxs-lookup"><span data-stu-id="fbbb4-292"><span id="FWP_E_INVALID_CIPHER_TRANSFORM"></span><span id="fwp_e_invalid_cipher_transform"></span>**FWP\_E\_INVALID\_CIPHER\_TRANSFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbbb4-293">0x80320039</span><span class="sxs-lookup"><span data-stu-id="fbbb4-293">0x80320039</span></span>
</dt> <dt>



<span data-ttu-id="fbbb4-294">IPsec 加密轉換無效。</span><span class="sxs-lookup"><span data-stu-id="fbbb4-294">The IPsec cipher transform is not valid.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fbbb4-295">規格需求</span><span class="sxs-lookup"><span data-stu-id="fbbb4-295">Requirements</span></span>



| <span data-ttu-id="fbbb4-296">需求</span><span class="sxs-lookup"><span data-stu-id="fbbb4-296">Requirement</span></span> | <span data-ttu-id="fbbb4-297">值</span><span class="sxs-lookup"><span data-stu-id="fbbb4-297">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fbbb4-298">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fbbb4-298">Minimum supported client</span></span><br/> | <span data-ttu-id="fbbb4-299">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fbbb4-299">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fbbb4-300">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fbbb4-300">Minimum supported server</span></span><br/> | <span data-ttu-id="fbbb4-301">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fbbb4-301">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fbbb4-302">標頭</span><span class="sxs-lookup"><span data-stu-id="fbbb4-302">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbbb4-303"><dt>Winerror.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="fbbb4-303"><dt>Winerror.h</dt></span></span> </dl> |



 

 





