---
description: 完成提供者的 WMI 之後，它會從記憶體卸載提供者。
ms.assetid: 6116769f-3402-42b3-835d-9bdb0fc27ce0
ms.tgt_platform: multiple
title: 卸載提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 123d8c4f6b9d9155cdc22dc435635466956bdb0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512972"
---
# <a name="unloading-a-provider"></a><span data-ttu-id="9630b-103">卸載提供者</span><span class="sxs-lookup"><span data-stu-id="9630b-103">Unloading a Provider</span></span>

<span data-ttu-id="9630b-104">完成提供者的 WMI 之後，它會從記憶體卸載提供者。</span><span class="sxs-lookup"><span data-stu-id="9630b-104">After WMI is finished with a provider, it unloads the provider from memory.</span></span> <span data-ttu-id="9630b-105">WMI 卸載提供者的主要原因是要節省系統資源。</span><span class="sxs-lookup"><span data-stu-id="9630b-105">The primary reason WMI unloads a provider is to conserve system resources.</span></span> <span data-ttu-id="9630b-106">因此，您必須新增可讓 WMI 以有效率的方式卸載提供者的程式碼。</span><span class="sxs-lookup"><span data-stu-id="9630b-106">Therefore, you must add code that allows WMI to unload your provider in an efficient manner.</span></span> <span data-ttu-id="9630b-107">它會從快取控制項指定的間隔時間，到 WMI 要卸載提供者的間隔兩倍。</span><span class="sxs-lookup"><span data-stu-id="9630b-107">It takes anywhere from the interval specified in the cache control to twice that interval for WMI to unload a provider.</span></span>

<span data-ttu-id="9630b-108">WMI 會以下列其中一種方式卸載提供者：</span><span class="sxs-lookup"><span data-stu-id="9630b-108">WMI unloads a provider in one of the following ways:</span></span>

-   <span data-ttu-id="9630b-109">在提供者完成提供給它的工作之後，請將提供者卸載。</span><span class="sxs-lookup"><span data-stu-id="9630b-109">Unload a provider after the provider finishes the tasks given to it.</span></span>
-   <span data-ttu-id="9630b-110">當使用者關閉系統時，快速卸載所有提供者。</span><span class="sxs-lookup"><span data-stu-id="9630b-110">Quickly unload all providers when the user shuts down the system.</span></span> <span data-ttu-id="9630b-111">請注意，WMI 服務從命令列關閉時，WMI 會卸載同進程提供者。</span><span class="sxs-lookup"><span data-stu-id="9630b-111">Note that WMI unloads in-process providers when the WMI service is shut down from the command line.</span></span>

<span data-ttu-id="9630b-112">雖然第一個案例較常見，但您必須撰寫您的提供者以瞭解這兩種可能性。</span><span class="sxs-lookup"><span data-stu-id="9630b-112">While the first scenario is more common, you must write your provider for both possibilities.</span></span>

<span data-ttu-id="9630b-113">本主題將討論下列各節：</span><span class="sxs-lookup"><span data-stu-id="9630b-113">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="9630b-114">卸載閒置提供者</span><span class="sxs-lookup"><span data-stu-id="9630b-114">Unloading an Idle Provider</span></span>](#unloading-an-idle-provider)
-   [<span data-ttu-id="9630b-115">存取提供者的閒置時間</span><span class="sxs-lookup"><span data-stu-id="9630b-115">Accessing the Idle Time for a Provider</span></span>](#accessing-the-idle-time-for-a-provider)
-   [<span data-ttu-id="9630b-116">卸載也是 WMI 用戶端的提供者</span><span class="sxs-lookup"><span data-stu-id="9630b-116">Unloading a Provider That Is Also a WMI Client</span></span>](#unloading-a-provider-that-is-also-a-wmi-client)
-   [<span data-ttu-id="9630b-117">在關機期間卸載提供者</span><span class="sxs-lookup"><span data-stu-id="9630b-117">Unloading a Provider During Shutdown</span></span>](#unloading-a-provider-during-shutdown)
-   [<span data-ttu-id="9630b-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="9630b-118">Related topics</span></span>](#related-topics)

## <a name="unloading-an-idle-provider"></a><span data-ttu-id="9630b-119">卸載閒置提供者</span><span class="sxs-lookup"><span data-stu-id="9630b-119">Unloading an Idle Provider</span></span>

<span data-ttu-id="9630b-120">WMI 卸載閒置提供者時，會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="9630b-120">WMI performs the following actions when it unloads an idle provider:</span></span>

-   <span data-ttu-id="9630b-121">判斷提供者是否閒置。</span><span class="sxs-lookup"><span data-stu-id="9630b-121">Determines if the provider is idle.</span></span>

    <span data-ttu-id="9630b-122">WMI 會使用 **ClearAfter** 屬性來決定提供者在卸載該提供者之前，可保持閒置的時間長度。</span><span class="sxs-lookup"><span data-stu-id="9630b-122">WMI uses the **ClearAfter** property to determine how long a provider may stay idle before unloading that provider.</span></span> <span data-ttu-id="9630b-123">如需詳細資訊，請參閱 [存取提供者的閒置時間](#accessing-the-idle-time-for-a-provider)。</span><span class="sxs-lookup"><span data-stu-id="9630b-123">For more information, see [Accessing the Idle Time for a Provider](#accessing-the-idle-time-for-a-provider).</span></span>

-   <span data-ttu-id="9630b-124">呼叫提供者的 [**發行**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 方法。</span><span class="sxs-lookup"><span data-stu-id="9630b-124">Calls the [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method of the provider.</span></span>

    <span data-ttu-id="9630b-125">如果提供者是純服務提供者，則 [**發行**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 會從使用中的記憶體中完全移除提供者。</span><span class="sxs-lookup"><span data-stu-id="9630b-125">If the provider was a pure provider, then [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) completely removes the provider from active memory.</span></span> <span data-ttu-id="9630b-126">不過，nonpure 提供者可能會在 WMI 呼叫 **發行** 之後繼續執行。</span><span class="sxs-lookup"><span data-stu-id="9630b-126">However, a nonpure provider may continue to run after WMI calls **Release**.</span></span>

## <a name="accessing-the-idle-time-for-a-provider"></a><span data-ttu-id="9630b-127">存取提供者的閒置時間</span><span class="sxs-lookup"><span data-stu-id="9630b-127">Accessing the Idle Time for a Provider</span></span>

<span data-ttu-id="9630b-128">提供者保持作用中的最小時間量是由 **ClearAfter** 屬性所決定。</span><span class="sxs-lookup"><span data-stu-id="9630b-128">The minimum amount of time a provider remains active is determined by the **ClearAfter** property.</span></span> <span data-ttu-id="9630b-129">您可以在根命名空間中衍生自 WMI 系統類別 [**\_ \_ CacheControl**](--cachecontrol.md)的類別實例中，找到 **ClearAfter** \\ 。</span><span class="sxs-lookup"><span data-stu-id="9630b-129">You can find **ClearAfter** in instances of classes derived from the WMI system class [**\_\_CacheControl**](--cachecontrol.md) in the \\root namespace.</span></span>

<span data-ttu-id="9630b-130">下列清單描述衍生自 [**\_ \_ CacheControl**](--cachecontrol.md)的類別，此類別會控制提供者卸載：</span><span class="sxs-lookup"><span data-stu-id="9630b-130">The following list describes the classes that are derived from [**\_\_CacheControl**](--cachecontrol.md), which controls provider unloading:</span></span>

-   [<span data-ttu-id="9630b-131">**\_\_EventConsumerProviderCacheControl**</span><span class="sxs-lookup"><span data-stu-id="9630b-131">**\_\_EventConsumerProviderCacheControl**</span></span>](--eventconsumerprovidercachecontrol.md)
-   [<span data-ttu-id="9630b-132">**\_\_EventProviderCacheControl**</span><span class="sxs-lookup"><span data-stu-id="9630b-132">**\_\_EventProviderCacheControl**</span></span>](--eventprovidercachecontrol.md)
-   [<span data-ttu-id="9630b-133">**\_\_EventSinkCacheControl**</span><span class="sxs-lookup"><span data-stu-id="9630b-133">**\_\_EventSinkCacheControl**</span></span>](--eventsinkcachecontrol.md)
-   [<span data-ttu-id="9630b-134">**\_\_ObjectProviderCacheControl**</span><span class="sxs-lookup"><span data-stu-id="9630b-134">**\_\_ObjectProviderCacheControl**</span></span>](--objectprovidercachecontrol.md)
-   [<span data-ttu-id="9630b-135">**\_\_PropertyProviderCacheControl**</span><span class="sxs-lookup"><span data-stu-id="9630b-135">**\_\_PropertyProviderCacheControl**</span></span>](--propertyprovidercachecontrol.md)

<span data-ttu-id="9630b-136">您可以針對特定類型的提供者，在快取控制項實例中編輯 **ClearAfter** 屬性，以變更 WMI 允許提供者保持非使用中的最小時間量。</span><span class="sxs-lookup"><span data-stu-id="9630b-136">You can change the minimum amount of time that WMI allows a provider to remain inactive by editing the **ClearAfter** property in the cache control instance for a specific type of provider.</span></span> <span data-ttu-id="9630b-137">例如，若要限制屬性提供者可以維持閒置的時間量，您可以在根命名空間中編輯 [**\_ \_ PropertyProviderCacheControl**](--propertyprovidercachecontrol.md)實例的 **ClearAfter** 屬性 \\ 。</span><span class="sxs-lookup"><span data-stu-id="9630b-137">For example, to limit the amount of time a property provider can remain idle, you would edit the **ClearAfter** property of a [**\_\_PropertyProviderCacheControl**](--propertyprovidercachecontrol.md) instance in the \\root namespace.</span></span>

## <a name="unloading-a-provider-that-is-also-a-wmi-client"></a><span data-ttu-id="9630b-138">卸載也是 WMI 用戶端的提供者</span><span class="sxs-lookup"><span data-stu-id="9630b-138">Unloading a Provider That Is Also a WMI Client</span></span>

<span data-ttu-id="9630b-139">當您的提供者完成呼叫的提供者函式之後，可能需要保持 WMI 的用戶端。</span><span class="sxs-lookup"><span data-stu-id="9630b-139">Your provider may need to remain a client of WMI after it has completed the provider functions it was called to perform.</span></span> <span data-ttu-id="9630b-140">例如，推送提供者可能需要向 WMI 發出查詢。</span><span class="sxs-lookup"><span data-stu-id="9630b-140">For example, a push provider may need to issue queries to WMI.</span></span> <span data-ttu-id="9630b-141">如需詳細資訊，請參閱 [判斷推播或提取狀態](determining-push-or-pull-status.md)。</span><span class="sxs-lookup"><span data-stu-id="9630b-141">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span> <span data-ttu-id="9630b-142">在此情況下，表示提供者之 [**\_ \_ Win32Provider**](--win32provider.md)實例的 **純** 屬性應該設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="9630b-142">In this case, the **Pure** property of the [**\_\_Win32Provider**](--win32provider.md) instance that represents the provider should be set to **TRUE**.</span></span> <span data-ttu-id="9630b-143">如果 **純** 屬性設為 **FALSE**，則當 WMI 呼叫其主要介面的發行方法時，提供者會在所有未完成的介面點上呼叫 [**IUnknown：： Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) ，藉以準備卸載。</span><span class="sxs-lookup"><span data-stu-id="9630b-143">If the **Pure** property is set to **FALSE**, the provider prepares to unload by calling [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on all outstanding interface points when WMI calls the Release method of its primary interface.</span></span> <span data-ttu-id="9630b-144">如需詳細資訊，請參閱 [**\_ \_ Win32Provider**](--win32provider.md)中的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="9630b-144">For more information, see the Remarks section in [**\_\_Win32Provider**](--win32provider.md).</span></span>

<span data-ttu-id="9630b-145">下列程式描述如何針對提供者的主要介面來執行發行方法。</span><span class="sxs-lookup"><span data-stu-id="9630b-145">The following procedure describes how to implement a release method for the primary interface of your provider.</span></span>

<span data-ttu-id="9630b-146">**若要卸載提供者**</span><span class="sxs-lookup"><span data-stu-id="9630b-146">**To unload a provider**</span></span>

1.  <span data-ttu-id="9630b-147">當 WMI 呼叫您提供者主要介面的 [**發行**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 方法時，釋放針對 wmi 所持有的所有介面指標。</span><span class="sxs-lookup"><span data-stu-id="9630b-147">Release all interface pointers held against WMI when WMI calls the [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method of the primary interface of your provider.</span></span>

    <span data-ttu-id="9630b-148">一般而言，提供者會保留 [**IWbemProviderInit：： Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize)中提供的 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)和 [**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="9630b-148">Typically, a provider holds pointers to the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) and [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) interfaces supplied in [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize).</span></span>

2.  <span data-ttu-id="9630b-149">如果相關聯的 [**\_ \_ Win32Provider**](--win32provider.md)實例中的 **Pure** 屬性設定為 **FALSE**，則提供者可以在 WMI 呼叫 [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)之後轉換至用戶端應用程式的角色。</span><span class="sxs-lookup"><span data-stu-id="9630b-149">If the **Pure** property in the associated [**\_\_Win32Provider**](--win32provider.md) instance is set to **FALSE**, the provider can transition to the role of client application after WMI calls [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="9630b-150">不過，WMI 無法卸載以用戶端系統的形式運作的提供者，這會增加系統的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="9630b-150">However, WMI cannot unload a provider that is operating as a client system, which increases the system overhead.</span></span>

    <span data-ttu-id="9630b-151">**純** 設為 **TRUE** 的提供者只存在於服務要求。</span><span class="sxs-lookup"><span data-stu-id="9630b-151">A provider with **Pure** set to **TRUE** exists only to service requests.</span></span> <span data-ttu-id="9630b-152">因此，這種類型的提供者無法採用用戶端應用程式的角色，而且 WMI 可以將它卸載。</span><span class="sxs-lookup"><span data-stu-id="9630b-152">Therefore, this type of provider cannot take on the role of a client application and WMI can unload it.</span></span>

## <a name="unloading-a-provider-during-shutdown"></a><span data-ttu-id="9630b-153">在關機期間卸載提供者</span><span class="sxs-lookup"><span data-stu-id="9630b-153">Unloading a Provider During Shutdown</span></span>

<span data-ttu-id="9630b-154">在一般情況下，使用卸載 [也是 Wmi 用戶端的提供者](#unloading-a-provider-that-is-also-a-wmi-client) 的指導方針，可讓 wmi 適當地卸載您的提供者。</span><span class="sxs-lookup"><span data-stu-id="9630b-154">Under normal circumstances, using the guidelines in [Unloading a Provider That is Also a WMI Client](#unloading-a-provider-that-is-also-a-wmi-client) allows WMI to unload your provider properly.</span></span> <span data-ttu-id="9630b-155">不過，您可能會遇到 WMI 無法 instigate 一般卸載程式的情況，例如，當使用者選擇關閉系統時。</span><span class="sxs-lookup"><span data-stu-id="9630b-155">However, you may run into situations where WMI is unable to instigate the normal unloading procedures, such as when the user chooses to shut the system down.</span></span> <span data-ttu-id="9630b-156">藉由使用資料儲存體的交易模型，除了執行良好的清除策略之外，您還可以確定您的提供者已正確卸載。</span><span class="sxs-lookup"><span data-stu-id="9630b-156">By using a transaction model of data storage, in addition to implementing a good cleanup strategy, you can ensure that your provider is properly unloaded.</span></span>

<span data-ttu-id="9630b-157">使用者可以隨時停止 WMI。</span><span class="sxs-lookup"><span data-stu-id="9630b-157">The user may stop WMI at any time.</span></span> <span data-ttu-id="9630b-158">在這種情況下，WMI 不會卸載任何提供者，也不會在任何同進程提供者上呼叫 [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) 進入點。</span><span class="sxs-lookup"><span data-stu-id="9630b-158">In such a situation, WMI does not unload any providers or call the [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) entry point on any in-process provider.</span></span> <span data-ttu-id="9630b-159">此外，如果同進程提供者是在關機時的方法呼叫中間，WMI 可能會在呼叫的中間終止執行中的執行緒。</span><span class="sxs-lookup"><span data-stu-id="9630b-159">Moreover, if an in-process provider is in the middle of a method call at the time of the shutdown, WMI can possibly terminate the executing thread in the middle of the call.</span></span> <span data-ttu-id="9630b-160">在此情況下，WMI 不會呼叫通常會處理清除的常式，例如物件的函式。</span><span class="sxs-lookup"><span data-stu-id="9630b-160">In this circumstance, WMI does not call routines that normally handle cleanup, such as an object destructor.</span></span> <span data-ttu-id="9630b-161">WMI 最多隻會呼叫 [**DllMain**](/windows/desktop/Dlls/dllmain) 。</span><span class="sxs-lookup"><span data-stu-id="9630b-161">At most, WMI will call [**DllMain**](/windows/desktop/Dlls/dllmain) only.</span></span>

<span data-ttu-id="9630b-162">當作業系統關閉 WMI 時，系統會自動釋放配置給同進程提供者的所有記憶體。</span><span class="sxs-lookup"><span data-stu-id="9630b-162">When the operating system shuts down WMI, the system automatically releases all memory allocated to an in-process provider.</span></span> <span data-ttu-id="9630b-163">作業系統也會關閉提供者所持有的大部分資源，例如檔案控制代碼、視窗控制碼等等。</span><span class="sxs-lookup"><span data-stu-id="9630b-163">The operating system also closes most resources held by the provider, such as file handles, window handles, and so on.</span></span> <span data-ttu-id="9630b-164">提供者不需要採取任何特定動作來進行這種動作。</span><span class="sxs-lookup"><span data-stu-id="9630b-164">The provider does not need to take any specific action to make this happen.</span></span>

<span data-ttu-id="9630b-165">因為 WMI 可能會在呼叫中間關機，所以提供者不應讓資料來源處於不一致的狀態。</span><span class="sxs-lookup"><span data-stu-id="9630b-165">Because WMI may shut down in the middle of a call, a provider should not leave data sources in an inconsistent state.</span></span> <span data-ttu-id="9630b-166">讓您的資料處於不一致的狀態，並不是唯讀提供者的問題。</span><span class="sxs-lookup"><span data-stu-id="9630b-166">Leaving your data in an inconsistent state is not a problem for read-only providers.</span></span> <span data-ttu-id="9630b-167">不過，具有寫入功能的提供者可能會想要在突然終止之後，執行某種類型的交易模型，以允許安全的回復。</span><span class="sxs-lookup"><span data-stu-id="9630b-167">However, providers with write capabilities may want to implement some sort of transaction model to allow a safe rollback after an abrupt termination.</span></span>

<span data-ttu-id="9630b-168">雖然作業系統可能會釋放一些一般系統資源，但系統並不會自動釋放所有資源。</span><span class="sxs-lookup"><span data-stu-id="9630b-168">While the operating system may release some general system resources, the system does not automatically release all resources.</span></span> <span data-ttu-id="9630b-169">例如，作業系統可能無法釋放通訊端或資料庫連接。</span><span class="sxs-lookup"><span data-stu-id="9630b-169">For example, the operating system may not release a socket or a database connection.</span></span> <span data-ttu-id="9630b-170">相反地，提供者可能需要手動清除這類資源。</span><span class="sxs-lookup"><span data-stu-id="9630b-170">Instead, the provider may need to manually clean up such resources.</span></span> <span data-ttu-id="9630b-171">若要避免這些問題，您可以跨進程執行您的提供者，也可以加入清除程式碼。</span><span class="sxs-lookup"><span data-stu-id="9630b-171">To avoid these problems, you can either implement your provider out-of-process, or you can add cleanup code.</span></span>

<span data-ttu-id="9630b-172">最簡單的解決方案是跨進程執行您的提供者。</span><span class="sxs-lookup"><span data-stu-id="9630b-172">The simplest solution is to implement your provider out-of-process.</span></span> <span data-ttu-id="9630b-173">當 WMI 關機時，不會終止跨進程提供者，雖然 WMI 將在 COM timeout 之後釋放該提供者。</span><span class="sxs-lookup"><span data-stu-id="9630b-173">An out-of-process provider is not killed when WMI shuts down, although WMI will release the provider after a COM timeout.</span></span> <span data-ttu-id="9630b-174">清除和終止強大問題的提供者，比效能可能跨進程更重要。</span><span class="sxs-lookup"><span data-stu-id="9630b-174">Providers for whom cleanup and termination robustness issues are more important than performance may be out-of-process.</span></span>

<span data-ttu-id="9630b-175">如果您必須將清除程式碼放在您的提供者中，您有兩個選項。</span><span class="sxs-lookup"><span data-stu-id="9630b-175">If you must place cleanup code in your provider, you have two options.</span></span> <span data-ttu-id="9630b-176">執行這類清除的一個地方就是 [**DllMain**](/windows/desktop/Dlls/dllmain)，在卸載 dll 時，作業系統會呼叫 dll 進入點函數。</span><span class="sxs-lookup"><span data-stu-id="9630b-176">One place to perform this sort of cleanup is [**DllMain**](/windows/desktop/Dlls/dllmain), the DLL entry point function the operating system calls when unloading the DLL.</span></span> <span data-ttu-id="9630b-177">清除程式碼可以直接加入 **DllMain** 中，執行它以回應 **DLL 進程 \_ 卸 \_ 離**。</span><span class="sxs-lookup"><span data-stu-id="9630b-177">Cleanup code can be added directly into **DllMain**, executing it in response to **DLL\_PROCESS\_DETACH**.</span></span> <span data-ttu-id="9630b-178">在 **DllMain** 中執行清除程式碼可能有點困難，尤其是在 MFC 或 ATL 之類的程式設計環境中。</span><span class="sxs-lookup"><span data-stu-id="9630b-178">Implementing cleanup code in **DllMain** can be somewhat difficult to arrange, especially in programming environments such as MFC or ATL.</span></span> <span data-ttu-id="9630b-179">For more information, see the Microsoft Knowledge Base article Q148791, "*How to Provide Your Own DllMain in an MFC Regular DLL.*"</span><span class="sxs-lookup"><span data-stu-id="9630b-179">For more information, see the Microsoft Knowledge Base article Q148791, "*How to Provide Your Own DllMain in an MFC Regular DLL.*"</span></span> <span data-ttu-id="9630b-180"> (此資源可能無法在某些語言及國家或地區使用。 ) </span><span class="sxs-lookup"><span data-stu-id="9630b-180">(This resource may not be available in some languages and countries or regions.)</span></span>

<span data-ttu-id="9630b-181">或者，您也可以將清除程式碼放在全域類別的函式中。</span><span class="sxs-lookup"><span data-stu-id="9630b-181">Alternately, you could also place the cleanup code in the destructor of a global class.</span></span> <span data-ttu-id="9630b-182">如需詳細資訊，請參閱卸載提供者。</span><span class="sxs-lookup"><span data-stu-id="9630b-182">For more information, see Unloading a Provider.</span></span> <span data-ttu-id="9630b-183">Windows 作業系統不會在堆積上配置全域物件。</span><span class="sxs-lookup"><span data-stu-id="9630b-183">The Windows operating system does not allocate global objects on the heap.</span></span> <span data-ttu-id="9630b-184">相反地，作業系統會在 DLL 卸載期間呼叫析構函數。</span><span class="sxs-lookup"><span data-stu-id="9630b-184">Instead, the operating system calls the destructors during DLL unload.</span></span>

<span data-ttu-id="9630b-185">以下是一個簡單的清除程式，可容納于 WMI 的全域物件內。</span><span class="sxs-lookup"><span data-stu-id="9630b-185">The following is a simple cleanup procedure that could fit inside a global object for WMI.</span></span>


```C++
class CMyCleanup
{
    ~CMyCleanup()
    {
        CloseHandle(m_hOpenFile);
        CloseDatabaseConnection(g_hDatabase);
    }
} g_Cleanup;
```



<span data-ttu-id="9630b-186">使用任一種方法可在清除程式碼中完成的工作有許多限制。</span><span class="sxs-lookup"><span data-stu-id="9630b-186">There are many restrictions as to what can be done in the cleanup code with either approach.</span></span> <span data-ttu-id="9630b-187">例如，不會以任何方式存取未隱含連結的執行緒和任何 Dll。</span><span class="sxs-lookup"><span data-stu-id="9630b-187">For example, neither threads nor any DLLs that are not implicitly linked may be accessed in any way.</span></span> <span data-ttu-id="9630b-188">此外，您無法在任何情況下進行 COM 呼叫。</span><span class="sxs-lookup"><span data-stu-id="9630b-188">Further, you cannot make COM calls under any circumstances.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9630b-189">相關主題</span><span class="sxs-lookup"><span data-stu-id="9630b-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9630b-190">設定命名空間安全描述項</span><span class="sxs-lookup"><span data-stu-id="9630b-190">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="9630b-191">保護您的提供者</span><span class="sxs-lookup"><span data-stu-id="9630b-191">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> <dt>

[<span data-ttu-id="9630b-192">開發 WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="9630b-192">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> </dl>

 

 
