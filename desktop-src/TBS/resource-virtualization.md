---
title: 資源虛擬化
description: 資源虛擬化
ms.assetid: ead0e99a-94da-4e80-bb68-d8f4b199173d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f340b1a1bddfb3fd591452e028c80403b9c7e02f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674079"
---
# <a name="resource-virtualization"></a><span data-ttu-id="622fe-103">資源虛擬化</span><span class="sxs-lookup"><span data-stu-id="622fe-103">Resource Virtualization</span></span>

<span data-ttu-id="622fe-104">TB 的主要功能是有效率地共用某些有限的 TPM 資源：金鑰、授權和傳輸會話。</span><span class="sxs-lookup"><span data-stu-id="622fe-104">The primary function of the TBS is to efficiently share certain limited TPM resources: keys, authorization, and transport sessions.</span></span>

<span data-ttu-id="622fe-105">建立其中一個資源的實例時，TBS 會建立資源的虛擬實例，並在結果命令資料流程中傳回這個虛擬實例的控制碼 (而非 TPM) 所傳回的實際控制碼實例。</span><span class="sxs-lookup"><span data-stu-id="622fe-105">When an instance of one of these resources is created, the TBS creates a virtual instance of the resource, and returns a handle to this virtual instance in the result command stream (rather than the actual handle instance returned by the TPM).</span></span> <span data-ttu-id="622fe-106">此 TB 會在內部維護虛擬控制碼與實際控制碼之間的對應。</span><span class="sxs-lookup"><span data-stu-id="622fe-106">The TBS maintains a mapping between the virtual handle and the actual handle internally.</span></span> <span data-ttu-id="622fe-107">如果 TPM 的空間不足以保存指定類型的更多資源，則會選擇性地儲存和收回資源的現有實例，直到 TPM 可保存新的資源為止。</span><span class="sxs-lookup"><span data-stu-id="622fe-107">If the TPM runs out of space to hold more resources of a given type, existing instances of the resource are selectively saved and evicted until the TPM can hold the new resource.</span></span> <span data-ttu-id="622fe-108">) 如果不再需要舊的資源，則會在提交命令之前，先將已儲存的內容載入 (儲存和收回其他資源。</span><span class="sxs-lookup"><span data-stu-id="622fe-108">When the old resources are required again, the TBS loads the saved contexts (saving and evicting other resources if necessary) before submitting the command.</span></span>

<span data-ttu-id="622fe-109">TB 中的所有虛擬化都會代表特定的內容執行。</span><span class="sxs-lookup"><span data-stu-id="622fe-109">All virtualization in the TBS is performed on behalf of a specific context.</span></span> <span data-ttu-id="622fe-110">每個內容都只允許存取專門建立的虛擬資源，以及 TPM 上對應于這些虛擬資源的實體資源。</span><span class="sxs-lookup"><span data-stu-id="622fe-110">Each context is only allowed to access virtual resources created specifically on its behalf, as well as the physical resources on the TPM that corresponds to those virtual resources.</span></span> <span data-ttu-id="622fe-111">依預設，所有虛擬資源的總數限制為500。</span><span class="sxs-lookup"><span data-stu-id="622fe-111">By default, the total number of all virtualized resources is limited to 500.</span></span> <span data-ttu-id="622fe-112">您可以藉由建立或修改 **HKEY \_ LOCAL \_ MACHINE**   \\ **Software** \\ **Microsoft** \\ **Tpm** 下名為 MaxResources 的 DWORD 登錄值來改變這個數位。</span><span class="sxs-lookup"><span data-stu-id="622fe-112">This number can be altered by creating or modifying a **DWORD** registry value named **MaxResources** under **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Tpm**.</span></span> <span data-ttu-id="622fe-113">您可以使用效能監視器工具來追蹤 TB 資源的數目，以觀察即時的 TB 資源使用方式。</span><span class="sxs-lookup"><span data-stu-id="622fe-113">Real-time TBS resource usage can be observed by using the Performance Monitor tool to track the number of TBS resources.</span></span> <span data-ttu-id="622fe-114">這種限制在 Windows 8 和 Windows Server 2012 中已過時。</span><span class="sxs-lookup"><span data-stu-id="622fe-114">This restriction became obsolete with Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="622fe-115">不是由 TB (（例如計數器和 NV 存放) 區）虛擬化的有限 TPM 資源，必須在軟體堆疊間以合作方式共用。</span><span class="sxs-lookup"><span data-stu-id="622fe-115">Limited TPM resources that are not virtualized by the TBS (such as counters and NV store) must be cooperatively shared among software stacks.</span></span>

> [!Note]  
> <span data-ttu-id="622fe-116">此處理虛擬化會導致在計算 HMAC 授權參數中包含金鑰控制碼的命令失敗。</span><span class="sxs-lookup"><span data-stu-id="622fe-116">This handle virtualization causes commands that include key handles in the calculation of HMAC authorization parameters to fail.</span></span> <span data-ttu-id="622fe-117">如此一來，在 TB 環境中，應用程式軟體就無法使用 TPM 1.2 版中已淘汰的許多命令。</span><span class="sxs-lookup"><span data-stu-id="622fe-117">As a result, many commands deprecated in TPM version 1.2 cannot be used by application software in the TBS environment.</span></span>

 

## <a name="resource-limits"></a><span data-ttu-id="622fe-118">資源限制</span><span class="sxs-lookup"><span data-stu-id="622fe-118">Resource Limits</span></span>

<span data-ttu-id="622fe-119">TPM 可讓呼叫端查詢其功能，以判斷哪些空間可用於特定類型的資源。</span><span class="sxs-lookup"><span data-stu-id="622fe-119">The TPM enables callers to query its capabilities to determine how much space is available for certain types of resources.</span></span> <span data-ttu-id="622fe-120">其中某些資源限制（例如金鑰的可用空間量、授權會話，以及傳輸會話）實際上是透過虛擬化來延長。</span><span class="sxs-lookup"><span data-stu-id="622fe-120">Some of these resource limits, such as the amount of space available for keys, authorization sessions, and transport sessions, are effectively extended by the TBS through virtualization.</span></span> <span data-ttu-id="622fe-121">**MaxResources** 登錄設定所控制的 TBS 限制通常遠高於基礎 TPM 硬體的實際限制。</span><span class="sxs-lookup"><span data-stu-id="622fe-121">TBS limitations, which are controlled by the **MaxResources** registry setting, are usually far larger than the actual limitations of the underlying TPM hardware.</span></span> <span data-ttu-id="622fe-122">不提供任何機制來與 TPM 硬體限制分開查詢 TBS 的限制。</span><span class="sxs-lookup"><span data-stu-id="622fe-122">No mechanism is supplied for querying TBS limitations separately from the TPM hardware limits.</span></span> <span data-ttu-id="622fe-123">Windows 8 和 Windows Server 2012 已淘汰此 TB 的限制。</span><span class="sxs-lookup"><span data-stu-id="622fe-123">This TBS limitation became obsolete with Windows 8 and Windows Server 2012.</span></span>

## <a name="keys"></a><span data-ttu-id="622fe-124">索引鍵</span><span class="sxs-lookup"><span data-stu-id="622fe-124">Keys</span></span>

<span data-ttu-id="622fe-125">TBS 會將金鑰控制碼虛擬化，如此一來，當金鑰不在使用時，可以從 TPM 透明地卸載金鑰，並在需要時將金鑰載入回 TPM。</span><span class="sxs-lookup"><span data-stu-id="622fe-125">The TBS virtualizes key handles so that keys can be transparently unloaded from the TPM when they are not being used and loaded back onto the TPM when they are needed.</span></span> <span data-ttu-id="622fe-126">建立金鑰時，TBS 會將虛擬控制碼與載入的金鑰產生關聯。</span><span class="sxs-lookup"><span data-stu-id="622fe-126">When a key is created, the TBS associates a virtual handle with the loaded key.</span></span> <span data-ttu-id="622fe-127">資源的存留期會使用相同的虛擬控制碼。</span><span class="sxs-lookup"><span data-stu-id="622fe-127">The same virtual handle is used for the lifetime of the resource.</span></span> <span data-ttu-id="622fe-128">虛擬金鑰控制碼只在建立它們的內容中有效，而相關聯的資源則不會保留到內容的存留期之外。</span><span class="sxs-lookup"><span data-stu-id="622fe-128">Virtual key handles are only valid in the context that created them, and the associated resources are not preserved beyond the life of the context.</span></span>

-   <span data-ttu-id="622fe-129">使用 TPM LoadKey2 建立金鑰 \_</span><span class="sxs-lookup"><span data-stu-id="622fe-129">Creating Keys with TPM\_LoadKey2</span></span>

    <span data-ttu-id="622fe-130">如果金鑰是使用 TPM \_ LoadKey2、TPM2 \_ CREATEPRIMARY、TPM2 \_ Load 或 TPM2 \_ LoadExternal 命令所建立，則 tb 會將傳回位元組資料流程中的控制碼取代為其選擇的虛擬金鑰控制碼。</span><span class="sxs-lookup"><span data-stu-id="622fe-130">If a key is created by using the TPM\_LoadKey2, TPM2\_CreatePrimary, TPM2\_Load, or TPM2\_LoadExternal command, the TBS replaces the handle in the return byte stream with a virtual key handle of its choosing.</span></span> <span data-ttu-id="622fe-131">如此一來，TBS 可確保每個虛擬控制碼都是唯一的。</span><span class="sxs-lookup"><span data-stu-id="622fe-131">As a result, the TBS ensures that each virtual handle is unique.</span></span> <span data-ttu-id="622fe-132">如果 TBS 偵測到衝突， (極不太可能的事件) ，則會從 TPM 卸載金鑰，並通知呼叫的軟體。</span><span class="sxs-lookup"><span data-stu-id="622fe-132">If the TBS detects a collision (an extremely unlikely event), the TBS unloads the key from the TPM and informs the calling software.</span></span> <span data-ttu-id="622fe-133">然後，軟體可以重新提交作業。</span><span class="sxs-lookup"><span data-stu-id="622fe-133">The software can then resubmit the operation.</span></span> <span data-ttu-id="622fe-134">您可以重複此程式，直到 TBS 取得唯一的索引鍵控制碼為止。</span><span class="sxs-lookup"><span data-stu-id="622fe-134">This process can be repeated until the TBS gets a unique key handle.</span></span>

-   <span data-ttu-id="622fe-135">清除索引鍵</span><span class="sxs-lookup"><span data-stu-id="622fe-135">Clearing Keys</span></span>

    <span data-ttu-id="622fe-136">當虛擬 \_ \_ 機從用戶端內容收到該虛擬控制碼的 TPM FLUSHSPECIFIC 或 TPM2 FlushCoNtext 訊息時，會使虛擬金鑰控制碼失效。</span><span class="sxs-lookup"><span data-stu-id="622fe-136">The TBS invalidates the virtual key handle when it receives a TPM\_FlushSpecific or TPM2\_FlushContext message for that virtual handle from the client context.</span></span> <span data-ttu-id="622fe-137">當收到清除訊息時，如果金鑰實際存在於 TPM 上，則會在該時間從 TPM 清除金鑰。</span><span class="sxs-lookup"><span data-stu-id="622fe-137">If the key is physically present on the TPM when the flush message is received, the TBS flushes the key from the TPM at that time.</span></span>

-   <span data-ttu-id="622fe-138">暫時移除金鑰</span><span class="sxs-lookup"><span data-stu-id="622fe-138">Temporarily Removing Keys</span></span>

    <span data-ttu-id="622fe-139">從 TPM 收回金鑰以騰出空間給新的專案時，TB \_ 之前會先執行 tpm SaveCoNtext 或 TPM2 \_ CoNtextSave 命令，再將它收回。</span><span class="sxs-lookup"><span data-stu-id="622fe-139">When evicting a key from the TPM to make room for a new item, the TBS executes a TPM\_SaveContext or TPM2\_ContextSave command on the key before evicting it.</span></span>

-   <span data-ttu-id="622fe-140">還原金鑰</span><span class="sxs-lookup"><span data-stu-id="622fe-140">Restoring Keys</span></span>

    <span data-ttu-id="622fe-141">當參考已載入金鑰的命令提交到 TB 時，它可確保金鑰實際上存在於 TPM 上。</span><span class="sxs-lookup"><span data-stu-id="622fe-141">When a command that references a loaded key is submitted to the TBS, it ensures that the key is physically present on the TPM.</span></span> <span data-ttu-id="622fe-142">如果機碼不存在，則會使用對 TPM \_ LoadCoNtext 或 TPM2 CoNtextLoad 的呼叫來還原 \_ 。</span><span class="sxs-lookup"><span data-stu-id="622fe-142">If the key is not present, the TBS restores it with a call to TPM\_LoadContext or TPM2\_ContextLoad.</span></span> <span data-ttu-id="622fe-143">如果無法將金鑰還原至 TPM，則 TBS 會傳回 TPM \_ E \_ 無效 \_ 的 KEYHANDLE 作為 tpm 結果。</span><span class="sxs-lookup"><span data-stu-id="622fe-143">If a key cannot be restored to the TPM, the TBS returns TPM\_E\_INVALID\_KEYHANDLE as the TPM result.</span></span>

<span data-ttu-id="622fe-144">TBS 會以 TPM 上所載入金鑰的實體控制碼，取代命令資料流程中與金鑰相關聯的每個虛擬控制碼。</span><span class="sxs-lookup"><span data-stu-id="622fe-144">The TBS replaces each virtual handle associated with a key in a command stream with the physical handle of the key loaded on the TPM.</span></span> <span data-ttu-id="622fe-145">如果在呼叫端的內容中，以 TBS 無法辨識的虛擬控制碼來提交命令，則 TBS 會為具有 TPM \_ E 無效 KEYHANDLE 的呼叫端格式化錯誤串流 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="622fe-145">If a command is submitted with a virtual handle that is not recognized by the TBS in the context of the caller, the TBS formats an error stream for the caller with TPM\_E\_INVALID\_KEYHANDLE.</span></span>

## <a name="authorization-sessions"></a><span data-ttu-id="622fe-146">授權會話</span><span class="sxs-lookup"><span data-stu-id="622fe-146">Authorization Sessions</span></span>

<span data-ttu-id="622fe-147">授權會話是藉由呼叫 TPM \_ OIAP、tpm \_ OSAP 或 tpm DSAP 所建立 \_ 。</span><span class="sxs-lookup"><span data-stu-id="622fe-147">Authorization sessions are created by calling TPM\_OIAP, TPM\_OSAP, or TPM\_DSAP.</span></span> <span data-ttu-id="622fe-148">在每個案例中，傳回位元組資料流程包含新建立之授權會話的實體 TPM 控制碼。</span><span class="sxs-lookup"><span data-stu-id="622fe-148">In each case, the return byte stream contains the physical TPM handle of the newly created authorization session.</span></span> <span data-ttu-id="622fe-149">TBS 以虛擬控制碼取代此情況。</span><span class="sxs-lookup"><span data-stu-id="622fe-149">The TBS replaces this with a virtual handle.</span></span> <span data-ttu-id="622fe-150">後續參考授權會話時，TB 會以授權會話的實體控制碼取代命令資料流程中的虛擬控制碼。</span><span class="sxs-lookup"><span data-stu-id="622fe-150">When the authorization session is subsequently referenced, the TBS replaces the virtual handle in the command stream with the physical handle of the authorization session.</span></span> <span data-ttu-id="622fe-151">TBS 可確保虛擬授權會話的存留期與實體授權會話的存留期相符。</span><span class="sxs-lookup"><span data-stu-id="622fe-151">The TBS ensures that the lifetime of the virtual authorization session matches that of the physical authorization session.</span></span> <span data-ttu-id="622fe-152">如果用戶端嘗試使用已過期的虛擬控制碼，則會使用錯誤 TPM INVALIDAUTHHANDLE 來格式化錯誤串流 \_ 。</span><span class="sxs-lookup"><span data-stu-id="622fe-152">If a client attempts to use an expired virtual handle, the TBS formats an error stream with error TPM\_INVALIDAUTHHANDLE.</span></span>

<span data-ttu-id="622fe-153">會話位置會受到限制，而且此 TB 可以用來儲存授權會話內容的外部位置。</span><span class="sxs-lookup"><span data-stu-id="622fe-153">Session slots are limited, and the TBS may run out of external slots in which to save authorization session contexts.</span></span> <span data-ttu-id="622fe-154">如果發生這種情況，TB 會選擇授權會話使其失效，以便能夠成功儲存新的內容。</span><span class="sxs-lookup"><span data-stu-id="622fe-154">If this happens, the TBS chooses an authorization session to invalidate so that the new context can be successfully saved.</span></span> <span data-ttu-id="622fe-155">嘗試使用舊內容的應用程式將需要重新建立授權會話。</span><span class="sxs-lookup"><span data-stu-id="622fe-155">An application that attempts to use the old context will need to re-create the authorization session.</span></span>

<span data-ttu-id="622fe-156">當發生下列任何一種情況時，TBS 會使虛擬授權會話失效：</span><span class="sxs-lookup"><span data-stu-id="622fe-156">The TBS invalidates the virtual authorization session when any of the following cases occur:</span></span>

-   <span data-ttu-id="622fe-157">從 TPM 傳回的命令資料流程中，與授權會話相關聯的繼續使用旗標為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="622fe-157">The continue-use flag associated with the authorization session in the returned command stream from the TPM is **FALSE**.</span></span>
-   <span data-ttu-id="622fe-158">使用授權會話的命令會失敗。</span><span class="sxs-lookup"><span data-stu-id="622fe-158">A command that uses an authorization session fails.</span></span>
-   <span data-ttu-id="622fe-159">執行的命令會使與命令 (（例如 TPM CreateWrapKey) ）相關聯的授權會話失效 \_ 。</span><span class="sxs-lookup"><span data-stu-id="622fe-159">A command is executed that invalidates the authorization session associated with the command (such as TPM\_CreateWrapKey).</span></span>
-   <span data-ttu-id="622fe-160">與 OSAP 或 DSAP 會話相關聯的金鑰，會透過呼叫 TPM \_ FlushSpecific 或 TPM2 FlushCoNtext 從 tpm 收回 \_ (而不考慮此命令是否源自于 tb 或更高層級的軟體) 。</span><span class="sxs-lookup"><span data-stu-id="622fe-160">A key associated with an OSAP or DSAP session is evicted from the TPM with a call to TPM\_FlushSpecific or TPM2\_FlushContext (without regard to whether this command originated with the TBS or with higher-level software).</span></span>

    <span data-ttu-id="622fe-161">在成功執行某些不具決定性的命令之後，將會自動重新同步處理授權會話，以確保此 TB 狀態與 TPM 狀態保持一致。</span><span class="sxs-lookup"><span data-stu-id="622fe-161">The TBS will automatically resynchronize the authorization sessions after successful execution of certain nondeterministic commands to ensure that the TBS state remains consistent with the TPM state.</span></span> <span data-ttu-id="622fe-162">受影響的命令如下：</span><span class="sxs-lookup"><span data-stu-id="622fe-162">The affected commands are:</span></span>

    -   <span data-ttu-id="622fe-163">TPM \_ ORD \_ 委派 \_ 管理</span><span class="sxs-lookup"><span data-stu-id="622fe-163">TPM\_ORD\_Delegate\_Manage</span></span>
    -   <span data-ttu-id="622fe-164">TPM \_ ORD \_ 委派 \_ CreateOwnerDelegation</span><span class="sxs-lookup"><span data-stu-id="622fe-164">TPM\_ORD\_Delegate\_CreateOwnerDelegation</span></span>
    -   <span data-ttu-id="622fe-165">TPM \_ ORD \_ 委派 \_ LoadOwnerDelegation</span><span class="sxs-lookup"><span data-stu-id="622fe-165">TPM\_ORD\_Delegate\_LoadOwnerDelegation</span></span>

<span data-ttu-id="622fe-166">在下列每個案例中，tpm 會自動清除 TPM 上的授權會話：</span><span class="sxs-lookup"><span data-stu-id="622fe-166">In each of the following cases the authorization session on the TPM is flushed automatically by the TPM:</span></span>

-   <span data-ttu-id="622fe-167">建立授權會話</span><span class="sxs-lookup"><span data-stu-id="622fe-167">Creating Authorization Sessions</span></span>

    <span data-ttu-id="622fe-168">虛擬授權會話控制碼只在建立它們的內容中有效，且相關聯的資源不會在相關聯內容的存留期間保留。</span><span class="sxs-lookup"><span data-stu-id="622fe-168">Virtual authorization session handles are only valid in the context that created them, and the associated resources are not preserved beyond the life of the associated context.</span></span>

-   <span data-ttu-id="622fe-169">清除授權會話</span><span class="sxs-lookup"><span data-stu-id="622fe-169">Clearing Authorization Sessions</span></span>

    <span data-ttu-id="622fe-170">如果虛擬授權會話收到 \_ \_ 用戶端內容中虛擬控制碼的 TPM FLUSHSPECIFIC 或 TPM2 FlushCoNtext 命令，則會使虛擬授權會話失效。</span><span class="sxs-lookup"><span data-stu-id="622fe-170">The TBS invalidates the virtual authorization session if it receives a TPM\_FlushSpecific or TPM2\_FlushContext command for the virtual handle from the client context.</span></span> <span data-ttu-id="622fe-171">如果接收到 flush 命令時，TPM 上實際有授權會話，則此 TB 會立即從 TPM 清除實體會話。</span><span class="sxs-lookup"><span data-stu-id="622fe-171">If the authorization session is physically present on the TPM when the flush command is received, the TBS flushes the physical session from the TPM immediately.</span></span>

-   <span data-ttu-id="622fe-172">暫時移除授權會話</span><span class="sxs-lookup"><span data-stu-id="622fe-172">Temporarily Removing Authorization Sessions</span></span>

    <span data-ttu-id="622fe-173">從 TPM 收回授權會話以騰出空間給新的實體時，TB \_ \_ 會在該授權會話上執行 TPM SAVECONTEXT 或 TPM2 CoNtextSave。</span><span class="sxs-lookup"><span data-stu-id="622fe-173">When evicting an authorization session from the TPM to make room for a new entity, the TBS executes TPM\_SaveContext or TPM2\_ContextSave on that authorization session.</span></span>

-   <span data-ttu-id="622fe-174">還原授權會話</span><span class="sxs-lookup"><span data-stu-id="622fe-174">Restoring Authorization Sessions</span></span>

    <span data-ttu-id="622fe-175">當授權 TPM 命令提交至 TB 時，此 TB 可確保命令中參考的所有虛擬授權會話實際上都存在於 TPM 中。</span><span class="sxs-lookup"><span data-stu-id="622fe-175">When an authorized TPM command is submitted to the TBS, the TBS ensures that all virtual authorization sessions referred to in the command are physically present on the TPM.</span></span> <span data-ttu-id="622fe-176">如果有任何授權會話不存在，則 TBS 會使用 TPM \_ LoadCoNtext 或 TPM2 CoNtextLoad 的呼叫來還原它們 \_ 。</span><span class="sxs-lookup"><span data-stu-id="622fe-176">If any of the authorization sessions are not present, the TBS restores them with a call to TPM\_LoadContext or TPM2\_ContextLoad.</span></span> <span data-ttu-id="622fe-177">如果授權會話無法還原至 TPM，則 TBS 會傳回 TPM \_ 電子 \_ 無效 \_ 的控制碼作為 tpm 結果。</span><span class="sxs-lookup"><span data-stu-id="622fe-177">If an authorization session cannot be restored to the TPM, the TBS returns TPM\_E\_INVALID\_HANDLE as the TPM result.</span></span>

<span data-ttu-id="622fe-178">TBS 會以 TPM 上載入之授權會話的實體控制碼，取代命令資料流程中與授權會話相關聯的每個虛擬控制碼。</span><span class="sxs-lookup"><span data-stu-id="622fe-178">The TBS replaces each virtual handle associated with an authorization session in a command stream with the physical handle of the authorization session loaded on the TPM.</span></span>

<span data-ttu-id="622fe-179">如果在呼叫端的內容中，以 TBS 無法辨識的虛擬控制碼來提交命令，則 TBS 會為具有錯誤 TPM \_ E \_ 無效控制碼的呼叫端格式化錯誤串流 \_ 。</span><span class="sxs-lookup"><span data-stu-id="622fe-179">If a command is submitted with a virtual handle that is not recognized by the TBS in the context of the caller, the TBS formats an error stream for the caller with the error TPM\_E\_INVALID\_HANDLE.</span></span>

## <a name="transport-sessions"></a><span data-ttu-id="622fe-180">傳輸會話</span><span class="sxs-lookup"><span data-stu-id="622fe-180">Transport Sessions</span></span>

> [!Note]  
> <span data-ttu-id="622fe-181">如這裡所述，傳輸會話的處理是 Windows Vista 和 Windows Server 2008 專用的。</span><span class="sxs-lookup"><span data-stu-id="622fe-181">The handling of transport sessions as described here is specific to Windows Vista and Windows Server 2008.</span></span>

 

<span data-ttu-id="622fe-182">傳輸會話是 TPM 所提供的一種機制，可讓軟體堆疊在軟體和 TPM 之間傳遞時，將命令中的資料加密。</span><span class="sxs-lookup"><span data-stu-id="622fe-182">Transport sessions are a mechanism provided by the TPM that enables a software stack to encrypt data in a command as it passes between the software and the TPM.</span></span> <span data-ttu-id="622fe-183">這可防止敵人在通過硬體匯流排時攔截資料。</span><span class="sxs-lookup"><span data-stu-id="622fe-183">This prevents an adversary from intercepting the data as it passes over the hardware bus.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="622fe-184">只有承載資料會加密。</span><span class="sxs-lookup"><span data-stu-id="622fe-184">Only the payload data is encrypted.</span></span> <span data-ttu-id="622fe-185">仍可以識別正在執行的命令。</span><span class="sxs-lookup"><span data-stu-id="622fe-185">The commands being executed can still be identified.</span></span>

 

<span data-ttu-id="622fe-186">可惜的是，這種機制也可防止 TB 檢查承載資料。</span><span class="sxs-lookup"><span data-stu-id="622fe-186">Unfortunately, this mechanism also prevents the TBS from examining payload data.</span></span> <span data-ttu-id="622fe-187">在大多數情況下，這不是問題，因為 TBS 只會修改控制碼，而不是承載資料。</span><span class="sxs-lookup"><span data-stu-id="622fe-187">In most cases this is not an issue because the TBS only modifies handles, not payload data.</span></span> <span data-ttu-id="622fe-188">不過，在 TPM LoadCoNtext 的情況下 \_ ，加密會涵蓋傳回的資源控制碼。</span><span class="sxs-lookup"><span data-stu-id="622fe-188">However, in the case of TPM\_LoadContext for instance, the returned resource handle is covered by the encryption.</span></span> <span data-ttu-id="622fe-189">因此，此 TB 可防止嘗試執行 \_ 傳輸會話所涵蓋的 TPM LoadCoNtext 操作。</span><span class="sxs-lookup"><span data-stu-id="622fe-189">Therefore, the TBS prevents attempts to perform a TPM\_LoadContext operation covered by a transport session.</span></span>

<span data-ttu-id="622fe-190">TBS 會在傳輸會話下封鎖下列命令：</span><span class="sxs-lookup"><span data-stu-id="622fe-190">The TBS blocks the following commands under transport session:</span></span>

-   <span data-ttu-id="622fe-191">TPM \_ EstablishTransport</span><span class="sxs-lookup"><span data-stu-id="622fe-191">TPM\_EstablishTransport</span></span>
-   <span data-ttu-id="622fe-192">TPM \_ ExecuteTransport</span><span class="sxs-lookup"><span data-stu-id="622fe-192">TPM\_ExecuteTransport</span></span>
-   <span data-ttu-id="622fe-193">TPM \_ 終止 \_ 控制碼</span><span class="sxs-lookup"><span data-stu-id="622fe-193">TPM\_Terminate\_Handle</span></span>
-   <span data-ttu-id="622fe-194">TPM \_ LoadKey</span><span class="sxs-lookup"><span data-stu-id="622fe-194">TPM\_LoadKey</span></span>
-   <span data-ttu-id="622fe-195">TPM \_ EvictKey</span><span class="sxs-lookup"><span data-stu-id="622fe-195">TPM\_EvictKey</span></span>
-   <span data-ttu-id="622fe-196">TPM \_ SaveKeyCoNtext</span><span class="sxs-lookup"><span data-stu-id="622fe-196">TPM\_SaveKeyContext</span></span>
-   <span data-ttu-id="622fe-197">TPM \_ LoadKeyCoNtext</span><span class="sxs-lookup"><span data-stu-id="622fe-197">TPM\_LoadKeyContext</span></span>
-   <span data-ttu-id="622fe-198">TPM \_ SaveAuthCoNtext</span><span class="sxs-lookup"><span data-stu-id="622fe-198">TPM\_SaveAuthContext</span></span>
-   <span data-ttu-id="622fe-199">TPM \_ LoadAuthCoNtext</span><span class="sxs-lookup"><span data-stu-id="622fe-199">TPM\_LoadAuthContext</span></span>
-   <span data-ttu-id="622fe-200">TPM \_ SaveCoNtext</span><span class="sxs-lookup"><span data-stu-id="622fe-200">TPM\_SaveContext</span></span>
-   <span data-ttu-id="622fe-201">TPM \_ LoadCoNtext</span><span class="sxs-lookup"><span data-stu-id="622fe-201">TPM\_LoadContext</span></span>
-   <span data-ttu-id="622fe-202">TPM \_ FlushSpecific</span><span class="sxs-lookup"><span data-stu-id="622fe-202">TPM\_FlushSpecific</span></span>

<span data-ttu-id="622fe-203">當傳輸會話涵蓋其中任何一個命令時，會傳回 \_ \_ \_ 不支援的 tpm E EMBEDDED 命令 \_ 作為 tpm 結果。</span><span class="sxs-lookup"><span data-stu-id="622fe-203">When any one of these commands is covered by a transport session, the TBS returns TPM\_E\_EMBEDDED\_COMMAND\_UNSUPPORTED as the TPM result.</span></span>

<span data-ttu-id="622fe-204">傳輸會話控制碼會以類似于金鑰控制碼和授權控制碼的方式進行虛擬化。</span><span class="sxs-lookup"><span data-stu-id="622fe-204">Transport session handles are virtualized in a manner similar to key handles and authorization handles.</span></span> <span data-ttu-id="622fe-205">TPM 上可用的已儲存傳輸會話內容位置數目有限。</span><span class="sxs-lookup"><span data-stu-id="622fe-205">There are a limited number of saved transport session context slots available on the TPM.</span></span>

<span data-ttu-id="622fe-206">如果發生下列任何一種情況，則 TBS 會使虛擬傳輸會話失效：</span><span class="sxs-lookup"><span data-stu-id="622fe-206">The TBS invalidates the virtual transport session if any of the following cases occurs:</span></span>

-   <span data-ttu-id="622fe-207">從 TPM 傳回命令資料流程中與傳輸會話相關聯的繼續使用旗標為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="622fe-207">The continue-use flag associated with the transport session in the return command stream from the TPM is **FALSE**.</span></span>

    <span data-ttu-id="622fe-208">如同上述的授權會話，在成功執行特定的非決定性命令之後，會自動重新同步處理傳輸會話，以確保 TB 狀態與 TPM 狀態保持一致。</span><span class="sxs-lookup"><span data-stu-id="622fe-208">As with authorization sessions above, the TBS will automatically resynchronize transport sessions after successful execution of certain nondeterministic commands to ensure that the TBS state remains consistent with the TPM state.</span></span> <span data-ttu-id="622fe-209">受影響的命令如下：</span><span class="sxs-lookup"><span data-stu-id="622fe-209">The affected commands are:</span></span>

    -   <span data-ttu-id="622fe-210">TPM \_ ORD \_ 委派 \_ 管理</span><span class="sxs-lookup"><span data-stu-id="622fe-210">TPM\_ORD\_Delegate\_Manage</span></span>
    -   <span data-ttu-id="622fe-211">TPM \_ ORD \_ 委派 \_ CreateOwnerDelegation</span><span class="sxs-lookup"><span data-stu-id="622fe-211">TPM\_ORD\_Delegate\_CreateOwnerDelegation</span></span>
    -   <span data-ttu-id="622fe-212">TPM \_ ORD \_ 委派 \_ LoadOwnerDelegation</span><span class="sxs-lookup"><span data-stu-id="622fe-212">TPM\_ORD\_Delegate\_LoadOwnerDelegation</span></span>

<span data-ttu-id="622fe-213">在上述每一種情況下，tpm 將會自動清除 TPM 上的傳輸會話：</span><span class="sxs-lookup"><span data-stu-id="622fe-213">In each of these cases, the transport session on the TPM will be flushed automatically by the TPM:</span></span>

-   <span data-ttu-id="622fe-214">建立傳輸會話</span><span class="sxs-lookup"><span data-stu-id="622fe-214">Creating Transport Sessions</span></span>

    <span data-ttu-id="622fe-215">TBS 會為用戶端所建立的每個傳輸會話建立虛擬控制碼。</span><span class="sxs-lookup"><span data-stu-id="622fe-215">The TBS creates a virtual handle for each transport session created by a client.</span></span> <span data-ttu-id="622fe-216">虛擬傳輸控制碼只在建立它們的內容中有效，且相關聯的資源不會在相關聯內容的存留期間保留。</span><span class="sxs-lookup"><span data-stu-id="622fe-216">Virtual transport handles are only valid in the context that created them, and the associated resources are not preserved beyond the life of the associated context.</span></span>

-   <span data-ttu-id="622fe-217">清除傳輸會話</span><span class="sxs-lookup"><span data-stu-id="622fe-217">Clearing Transport Sessions</span></span>

    <span data-ttu-id="622fe-218">如果虛擬傳輸會話 \_ 從用戶端內容收到虛擬控制碼的 TPM FlushSpecific 命令，則會使其失效。</span><span class="sxs-lookup"><span data-stu-id="622fe-218">The TBS invalidates the virtual transport session if it receives a TPM\_FlushSpecific command for the virtual handle from the client context.</span></span> <span data-ttu-id="622fe-219">如果接收到 flush 命令時，在 TPM 上實際存在傳輸會話，則會立即從 TPM 清除實體會話。</span><span class="sxs-lookup"><span data-stu-id="622fe-219">If the transport session is physically present on the TPM when the flush command is received, the TBS flushes the physical session from the TPM immediately.</span></span>

-   <span data-ttu-id="622fe-220">暫時移除傳輸會話</span><span class="sxs-lookup"><span data-stu-id="622fe-220">Temporarily Removing Transport Sessions</span></span>

    <span data-ttu-id="622fe-221">從 TPM 收回傳輸會話以騰出空間給新的實體時，TB \_ 會在該傳輸會話上執行 TPM SaveCoNtext。</span><span class="sxs-lookup"><span data-stu-id="622fe-221">When evicting a transport session from the TPM to make room for a new entity, the TBS executes TPM\_SaveContext on that transport session.</span></span>

-   <span data-ttu-id="622fe-222">還原傳輸會話</span><span class="sxs-lookup"><span data-stu-id="622fe-222">Restoring Transport Sessions</span></span>

    <span data-ttu-id="622fe-223">將 TPM \_ ExecuteTransport 命令提交到 tb 時，tb 可確保命令中所參考的傳輸會話實際上存在於 TPM 上。</span><span class="sxs-lookup"><span data-stu-id="622fe-223">When a TPM\_ExecuteTransport command is submitted to the TBS, the TBS ensures that the transport session referred to in the command is physically present on the TPM.</span></span> <span data-ttu-id="622fe-224">如果傳輸會話不存在，則會使用對 TPM LoadCoNtext 的呼叫來還原 \_ 。</span><span class="sxs-lookup"><span data-stu-id="622fe-224">If the transport session is not present, the TBS restores it with a call to TPM\_LoadContext.</span></span>

<span data-ttu-id="622fe-225">此 TB 會以 TPM 上載入之傳輸會話的實體控制碼，取代命令資料流程中與傳輸會話相關聯的虛擬控制碼。</span><span class="sxs-lookup"><span data-stu-id="622fe-225">The TBS replaces the virtual handle associated with the transport session in a command stream with the physical handle of the transport session loaded on the TPM.</span></span> <span data-ttu-id="622fe-226">如果在呼叫端的內容中，以 TBS 無法辨識的虛擬控制碼來提交命令，則會使用 TPM \_ E \_ 無效控制碼來格式化呼叫端的錯誤資料流程 \_ 。</span><span class="sxs-lookup"><span data-stu-id="622fe-226">If a command is submitted with a virtual handle that is not recognized by the TBS in the context of the caller, the TBS formats an error stream for the caller by using TPM\_E\_INVALID\_HANDLE.</span></span>

## <a name="exclusive-transport-sessions"></a><span data-ttu-id="622fe-227">專屬傳輸會話</span><span class="sxs-lookup"><span data-stu-id="622fe-227">Exclusive Transport Sessions</span></span>

<span data-ttu-id="622fe-228">專屬的包裝傳輸會話是最上層軟體的一種方式，可判斷是否有任何其他軟體在一連串命令期間存取 TPM。</span><span class="sxs-lookup"><span data-stu-id="622fe-228">Exclusive wrapped transport sessions are a way for top-level software to determine whether any other software has accessed the TPM during a chain of commands.</span></span> <span data-ttu-id="622fe-229">它們不會防止其他軟體存取 TPM，而只是讓傳輸會話的建立者有辦法判斷是否發生其他存取。</span><span class="sxs-lookup"><span data-stu-id="622fe-229">They do not prevent other software from accessing the TPM, they just give the creator of the transport session a means of determining that some other access occurred.</span></span> <span data-ttu-id="622fe-230">此 TB 不會執行任何特定的動作來阻礙專屬的傳輸會話，但它與它們有點不相容。</span><span class="sxs-lookup"><span data-stu-id="622fe-230">The TBS does not do anything specific to hinder exclusive transport sessions, but it is somewhat incompatible with them.</span></span> <span data-ttu-id="622fe-231">此 TB 會嘗試以透明的方式複製 TPM 的自然行為，因此不會優先于建立專屬傳輸會話的內容中使用命令。</span><span class="sxs-lookup"><span data-stu-id="622fe-231">The TBS attempts to duplicate the natural behavior of the TPM by being transparent, so it does not favor commands from contexts that establish an exclusive transport session.</span></span> <span data-ttu-id="622fe-232">例如，如果用戶端 B 在用戶端 A 位於獨佔傳輸會話時提交命令，則會使用戶端 A 的獨佔傳輸會話失效。</span><span class="sxs-lookup"><span data-stu-id="622fe-232">For example, if client B submits a command when client A is in an exclusive transport session, then it will invalidate the exclusive transport session of client A.</span></span>

<span data-ttu-id="622fe-233">以 TB 起始的命令也可以終止獨佔傳輸會話。</span><span class="sxs-lookup"><span data-stu-id="622fe-233">Commands initiated by TBS can also terminate the exclusive transport session.</span></span> <span data-ttu-id="622fe-234">當用戶端 A 在獨佔傳輸會話中，而且用戶端執行的命令呼叫不是實際存在於 TPM 中的資源時，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="622fe-234">This happens when client A is in an exclusive transport session, and a command executed by client A calls for a resource that is not physically present in the TPM.</span></span> <span data-ttu-id="622fe-235">這種情況會觸發 TBS 虛擬化管理員執行 TPM \_ LoadCoNtext 命令來提供該資源，以終止用戶端 a 的獨佔傳輸會話。</span><span class="sxs-lookup"><span data-stu-id="622fe-235">This situation triggers the TBS virtualization manager to execute a TPM\_LoadContext command to supply that resource, which terminates the exclusive transport session of client A.</span></span>

 

 




