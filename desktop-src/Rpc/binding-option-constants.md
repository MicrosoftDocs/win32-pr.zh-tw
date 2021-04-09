---
title: '系結選項常數 (Rpcdce .h) '
description: 應用程式會設定系結選項常數，以控制 RPC 執行時間程式庫處理遠端程序呼叫的方式。 下表列出每個系結屬性，以及系結屬性的相關常數值。
ms.assetid: ff88e05d-b9f3-42ef-a44f-fee9261832c8
topic_type:
- apiref
api_name:
- RPC_C_OPT_BINDING_NONCAUSAL
- RPC_C_OPT_MAX_OPTIONS
- RPC_C_DONT_FAIL
- RPC_C_OPT_SESSION_ID
- RPC_C_OPT_COOKIE_AUTH
- RPC_C_OPT_RESOURCE_TYPE_UUID
- RPC_C_OPT_DONT_LINGER
- RPC_C_OPT_UNIQUE_BINDING
api_location:
- Rpcdce.h
- Rpcdcep.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52152b5ddcc17abe5c698697e30f1f1a512ee4f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934152"
---
# <a name="binding-option-constants"></a><span data-ttu-id="d7767-104">系結選項常數</span><span class="sxs-lookup"><span data-stu-id="d7767-104">Binding Option Constants</span></span>

<span data-ttu-id="d7767-105">應用程式會設定系結選項常數，以控制 RPC 執行時間程式庫處理遠端程序呼叫的方式。</span><span class="sxs-lookup"><span data-stu-id="d7767-105">Applications set the binding option constants to control how the RPC run-time library processes remote procedure calls.</span></span> <span data-ttu-id="d7767-106">下表列出每個系結屬性，以及系結屬性的相關常數值。</span><span class="sxs-lookup"><span data-stu-id="d7767-106">The following table lists each binding property, and the relevant constant values for the binding properties.</span></span>

> [!Note]  
> <span data-ttu-id="d7767-107">下表中 (MQ) 的所有訊息佇列選項僅適用于 Windows 2000。</span><span class="sxs-lookup"><span data-stu-id="d7767-107">All message queue options (MQ) in the following table are valid for Windows 2000 only.</span></span> <span data-ttu-id="d7767-108">Windows XP 和更新版本不支援訊息佇列。</span><span class="sxs-lookup"><span data-stu-id="d7767-108">Windows XP and later versions do not support message queuing.</span></span> <span data-ttu-id="d7767-109">開發人員不建議使用訊息佇列。</span><span class="sxs-lookup"><span data-stu-id="d7767-109">Developers are discouraged from using message queuing.</span></span>

 



| <span data-ttu-id="d7767-110">常數/值</span><span class="sxs-lookup"><span data-stu-id="d7767-110">Constant/value</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="d7767-111">Description</span><span class="sxs-lookup"><span data-stu-id="d7767-111">Description</span></span>                                                                                                                                                                                                                                                                                           |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_OPT_BINDING_NONCAUSAL"></span><span id="rpc_c_opt_binding_noncausal"></span><dl> <span data-ttu-id="d7767-112"><dt>**RPC \_C \_ OPT \_ \_**</dt>系結 NONCAUSAL <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="d7767-112"><dt>**RPC\_C\_OPT\_BINDING\_NONCAUSAL**</dt> <dt>9</dt></span></span> </dl>     | <span data-ttu-id="d7767-113">預設值。</span><span class="sxs-lookup"><span data-stu-id="d7767-113">Default.</span></span> <span data-ttu-id="d7767-114">如果 **為 FALSE**，則為因果呼叫順序。</span><span class="sxs-lookup"><span data-stu-id="d7767-114">If **FALSE**, causal call ordering.</span></span> <span data-ttu-id="d7767-115">RPC 呼叫會以嚴格的提交順序來執行。</span><span class="sxs-lookup"><span data-stu-id="d7767-115">RPC calls are executed in strict order of submission.</span></span> <span data-ttu-id="d7767-116">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="d7767-116">See Remarks.</span></span><br/> <span data-ttu-id="d7767-117">若 **為 TRUE**，則 noncausal 呼叫順序。</span><span class="sxs-lookup"><span data-stu-id="d7767-117">If **TRUE**, noncausal call ordering.</span></span> <span data-ttu-id="d7767-118">RPC 呼叫會獨立執行。</span><span class="sxs-lookup"><span data-stu-id="d7767-118">RPC calls are executed independently.</span></span> <span data-ttu-id="d7767-119">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="d7767-119">See Remarks.</span></span><br/>                                                                        |
| <span id="RPC_C_OPT_MAX_OPTIONS"></span><span id="rpc_c_opt_max_options"></span><dl> <span data-ttu-id="d7767-120"><dt>**RPC \_C \_ OPT \_ 最大 \_ 選項**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="d7767-120"><dt>**RPC\_C\_OPT\_MAX\_OPTIONS**</dt> <dt>17</dt></span></span> </dl>                      | <span data-ttu-id="d7767-121">應用程式不需要。</span><span class="sxs-lookup"><span data-stu-id="d7767-121">Not needed for application programs.</span></span> <span data-ttu-id="d7767-122">由 Microsoft 在內部使用。</span><span class="sxs-lookup"><span data-stu-id="d7767-122">Used internally by Microsoft.</span></span><br/>                                                                                                                                                                                                                         |
| <span id="RPC_C_DONT_FAIL"></span><span id="rpc_c_dont_fail"></span><dl> <span data-ttu-id="d7767-123"><dt>**RPC \_C \_ 不 \_ 會失敗**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="d7767-123"><dt>**RPC\_C\_DONT\_FAIL**</dt> <dt>4</dt></span></span> </dl>                                          | <span data-ttu-id="d7767-124">應用程式不需要。</span><span class="sxs-lookup"><span data-stu-id="d7767-124">Not needed for application programs.</span></span> <span data-ttu-id="d7767-125">由 Microsoft 在內部使用。</span><span class="sxs-lookup"><span data-stu-id="d7767-125">Used internally by Microsoft.</span></span><br/>                                                                                                                                                                                                                         |
| <span id="RPC_C_OPT_SESSION_ID"></span><span id="rpc_c_opt_session_id"></span><dl> <span data-ttu-id="d7767-126"><dt>**RPC \_C \_ OPT \_ 會話 \_ 識別碼**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="d7767-126"><dt>**RPC\_C\_OPT\_SESSION\_ID**</dt> <dt>6</dt></span></span> </dl>                          | <span data-ttu-id="d7767-127">若 **為 TRUE**，則會為每個連接產生會話識別碼。</span><span class="sxs-lookup"><span data-stu-id="d7767-127">If **TRUE**, a session ID is generated for each connection.</span></span><br/>                                                                                                                                                                                                                                |
| <span id="RPC_C_OPT_COOKIE_AUTH"></span><span id="rpc_c_opt_cookie_auth"></span><dl> <span data-ttu-id="d7767-128"><dt>**RPC \_C \_ OPT \_ COOKIE \_ 驗證**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="d7767-128"><dt>**RPC\_C\_OPT\_COOKIE\_AUTH**</dt> <dt>7</dt></span></span> </dl>                       | <span data-ttu-id="d7767-129">若為 **TRUE**，則會使用以用戶端 cookie 為基礎的驗證來進行連接。</span><span class="sxs-lookup"><span data-stu-id="d7767-129">If **TRUE**, client-side cookie-based authentication is used for connections.</span></span> <span data-ttu-id="d7767-130">[**RPC \_ C \_ OPT \_ COOKIE \_ 驗證 \_ 描述**](/windows/desktop/api/Rpcdcep/ns-rpcdcep-rpc_c_opt_cookie_auth_descriptor)元結構的指標會在 [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption)中做為 *OptionValue* 參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="d7767-130">A pointer to the [**RPC\_C\_OPT\_COOKIE\_AUTH\_DESCRIPTOR**](/windows/desktop/api/Rpcdcep/ns-rpcdcep-rpc_c_opt_cookie_auth_descriptor) structure is passed as the *OptionValue* parameter in [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption).</span></span><br/> |
| <span id="RPC_C_OPT_RESOURCE_TYPE_UUID"></span><span id="rpc_c_opt_resource_type_uuid"></span><dl> <span data-ttu-id="d7767-131"><dt>**RPC \_C \_ OPT \_ 資源 \_ 類型 \_ UUID**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="d7767-131"><dt>**RPC\_C\_OPT\_RESOURCE\_TYPE\_UUID**</dt> <dt>8</dt></span></span> </dl> | <span data-ttu-id="d7767-132">應用程式不需要。</span><span class="sxs-lookup"><span data-stu-id="d7767-132">Not needed for application programs.</span></span> <span data-ttu-id="d7767-133">由 Microsoft 在內部使用。</span><span class="sxs-lookup"><span data-stu-id="d7767-133">Used internally by Microsoft.</span></span><br/>                                                                                                                                                                                                                         |
| <span id="RPC_C_OPT_DONT_LINGER"></span><span id="rpc_c_opt_dont_linger"></span><dl> <span data-ttu-id="d7767-134"><dt>**RPC \_C \_ OPT \_ \_**</dt>不會逗留 <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="d7767-134"><dt>**RPC\_C\_OPT\_DONT\_LINGER**</dt> <dt>13</dt></span></span> </dl>                      | <span data-ttu-id="d7767-135">若 **為 TRUE**，則會在釋放關聯的最後一個系結控制碼/內容控制碼之後，強制關閉該關聯。</span><span class="sxs-lookup"><span data-stu-id="d7767-135">If **TRUE**, force shutdown of the association after the last binding handle/context handle on it is freed.</span></span><br/>                                                                                                                                                                                |
| <span id="RPC_C_OPT_UNIQUE_BINDING"></span><span id="rpc_c_opt_unique_binding"></span><dl> <span data-ttu-id="d7767-136"><dt>**RPC \_C \_ OPT \_ 唯一 \_**</dt>系結 <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="d7767-136"><dt>**RPC\_C\_OPT\_UNIQUE\_BINDING**</dt> <dt>11</dt></span></span> </dl>             | <span data-ttu-id="d7767-137">當設為 **true** 時，RPC 不會重複使用現有的連接。</span><span class="sxs-lookup"><span data-stu-id="d7767-137">When set to **true**, RPC does not reuse existing connections.</span></span> <span data-ttu-id="d7767-138">針對每個連接開啟唯一的系結控制碼，並為每個唯一的系結控制碼維護狀態。</span><span class="sxs-lookup"><span data-stu-id="d7767-138">A unique binding handle is opened for each connection and state is maintained for each unique binding handle.</span></span><br/>                                                                                                               |



## <a name="remarks"></a><span data-ttu-id="d7767-139">備註</span><span class="sxs-lookup"><span data-stu-id="d7767-139">Remarks</span></span>

<span data-ttu-id="d7767-140">根據預設，RPC 執行時間程式庫會以嚴格的提交順序，從應用程式的每個執行緒在給定的系結控制碼上執行呼叫。</span><span class="sxs-lookup"><span data-stu-id="d7767-140">By default, the RPC run-time library executes the calls on a given binding handle from each thread of an application in strict order of submission.</span></span> <span data-ttu-id="d7767-141">這並不保證會序列化相同系結控制碼上不同執行緒的呼叫。</span><span class="sxs-lookup"><span data-stu-id="d7767-141">This does not guarantee that calls from different threads on the same binding handle are serialized.</span></span> <span data-ttu-id="d7767-142">多執行緒應用程式必須序列化其 RPC 呼叫。</span><span class="sxs-lookup"><span data-stu-id="d7767-142">Multithreaded applications must serialize their RPC calls.</span></span> <span data-ttu-id="d7767-143">如果此行為過於嚴格，您可以啟用 noncausal 順序。</span><span class="sxs-lookup"><span data-stu-id="d7767-143">If this behavior is too restrictive, you can enable noncausal ordering.</span></span> <span data-ttu-id="d7767-144">當您這樣做時，RPC 執行時間程式庫會獨立執行呼叫。</span><span class="sxs-lookup"><span data-stu-id="d7767-144">When you do, the RPC run-time library executes calls independently.</span></span> <span data-ttu-id="d7767-145">它不會在提交時進行排序。</span><span class="sxs-lookup"><span data-stu-id="d7767-145">It imposes no ordering on their submission.</span></span>

<span data-ttu-id="d7767-146">可能會發現 noncausal 順序的應用程式範例之一，就是執行緒在相同系結控制碼上進行呼叫的多執行緒程式。</span><span class="sxs-lookup"><span data-stu-id="d7767-146">One example of an application that might find noncausal ordering useful is a multithreaded program whose threads make calls on the same binding handle.</span></span> <span data-ttu-id="d7767-147">同樣地，在系結控制碼上使用多個非同步呼叫的程式，會發現 noncausal 順序是一個方便的選項。</span><span class="sxs-lookup"><span data-stu-id="d7767-147">Similarly, a program that uses multiple asynchronous calls on a binding handle will find noncausal ordering a convenient option.</span></span> <span data-ttu-id="d7767-148">另一個範例可能是使用單一線程處理數個用戶端要求的網際網路 proxy 程式。</span><span class="sxs-lookup"><span data-stu-id="d7767-148">Another example might be an Internet proxy program that uses a single thread to handle requests for several clients.</span></span> <span data-ttu-id="d7767-149">在上述每一種情況下，嘗試序列化遠端程序呼叫是非常嚴格的。</span><span class="sxs-lookup"><span data-stu-id="d7767-149">In each of these cases, it would be extremely restrictive to try to serialize the remote procedure calls.</span></span>

<span data-ttu-id="d7767-150">您只能在使用 **ncalrpc** 或 \**\_ \* ncacn* _ 通訊協定序列的系結控制碼上設定「 **RPC \_ C \_ OPT 未 \_ \_ 逗留**」選項。</span><span class="sxs-lookup"><span data-stu-id="d7767-150">The **RPC\_C\_OPT\_DONT\_LINGER** option can be set only on binding handles that use the **ncalrpc** or \**ncacn\_\** _ protocol sequences.</span></span> <span data-ttu-id="d7767-151">它不能用在 _*ncadg \_ \**_ 通訊協定序列上。</span><span class="sxs-lookup"><span data-stu-id="d7767-151">It cannot be used on _*ncadg\_\**_ protocol sequences.</span></span> <span data-ttu-id="d7767-152">具有此選項的 [_ *RpcBindingSetOption* \*](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption)函式必須在至少進行一個 RPC 呼叫的系結控制碼上呼叫。</span><span class="sxs-lookup"><span data-stu-id="d7767-152">The [_ *RpcBindingSetOption*\*](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) function with this option must be called on a binding handle on which at least one RPC call has been made.</span></span> <span data-ttu-id="d7767-153">如果未在系結控制碼上進行 RPC 呼叫，則會從 **RpcBindingSetOption** 函式呼叫傳回 **rpc \_ S \_ 錯誤 \_ \_ 的 \_** 系結類型。</span><span class="sxs-lookup"><span data-stu-id="d7767-153">If no RPC call have been made on the binding handle, **RPC\_S\_WRONG\_KIND\_OF\_BINDING** is returned from the **RpcBindingSetOption** function call.</span></span> <span data-ttu-id="d7767-154">不論附加至關聯的系結控制碼有多少，此選項都會對整個關聯生效。</span><span class="sxs-lookup"><span data-stu-id="d7767-154">The option takes effect for the entire association, regardless of how many binding handles are attached to the association.</span></span> <span data-ttu-id="d7767-155">由於在關聯終結之前會先進行檢查，因此可以在系結控制碼關閉之前隨時進行設定。</span><span class="sxs-lookup"><span data-stu-id="d7767-155">Since it is checked before the association is destroyed, it can be set at any time before the binding handle is closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7767-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7767-156">Requirements</span></span>



| <span data-ttu-id="d7767-157">需求</span><span class="sxs-lookup"><span data-stu-id="d7767-157">Requirement</span></span> | <span data-ttu-id="d7767-158">值</span><span class="sxs-lookup"><span data-stu-id="d7767-158">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7767-159">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d7767-159">Minimum supported client</span></span><br/> | <span data-ttu-id="d7767-160">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7767-160">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                           |
| <span data-ttu-id="d7767-161">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d7767-161">Minimum supported server</span></span><br/> | <span data-ttu-id="d7767-162">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7767-162">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                 |
| <span data-ttu-id="d7767-163">標頭</span><span class="sxs-lookup"><span data-stu-id="d7767-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7767-164"><dt>Rpcdce .h;</dt><dt>Rpcdcep .h</dt></span><span class="sxs-lookup"><span data-stu-id="d7767-164"><dt>Rpcdce.h; </dt> <dt>Rpcdcep.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7767-165">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7767-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7767-166">**RpcBindingSetOption**</span><span class="sxs-lookup"><span data-stu-id="d7767-166">**RpcBindingSetOption**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption)
</dt> <dt>

[<span data-ttu-id="d7767-167">**RpcBindingInqOption**</span><span class="sxs-lookup"><span data-stu-id="d7767-167">**RpcBindingInqOption**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqoption)
</dt> <dt>

[<span data-ttu-id="d7767-168">管理 (關聯) 的網路連接集 </span><span class="sxs-lookup"><span data-stu-id="d7767-168">Managing Network Connection Sets (Associations)</span></span>](managing-network-connection-sets-associations-.md)
</dt> </dl>

 

 





