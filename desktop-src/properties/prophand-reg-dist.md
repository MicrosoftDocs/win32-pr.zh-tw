---
description: 本文說明如何註冊和散發屬性處理常式，以便與 Windows 屬性系統搭配使用。
ms.assetid: E6E81E04-9CC1-4df5-9A87-DE0CBD177356
title: 註冊和散發屬性處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cffd6169ecbf371e49e27c555f468cdc03e2c3fc
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408341"
---
# <a name="registering-and-distributing-property-handlers"></a><span data-ttu-id="70293-103">註冊和散發屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="70293-103">Registering and Distributing Property Handlers</span></span>

<span data-ttu-id="70293-104">本主題說明如何建立及註冊屬性處理常式，以便與 Windows 屬性系統搭配使用。</span><span class="sxs-lookup"><span data-stu-id="70293-104">This topic explains how to create and register property handlers to work with the Windows property system.</span></span>

<span data-ttu-id="70293-105">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="70293-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="70293-106">註冊和散發屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="70293-106">Registering and Distributing Property Handlers</span></span>](#registering-and-distributing-property-handlers)
-   [<span data-ttu-id="70293-107">屬性處理常式的效能和可靠性考慮</span><span class="sxs-lookup"><span data-stu-id="70293-107">Performance and Reliability Considerations for Property Handlers</span></span>](#performance-and-reliability-considerations-for-property-handlers)
    -   [<span data-ttu-id="70293-108">效能和可靠性的指導方針</span><span class="sxs-lookup"><span data-stu-id="70293-108">Guidelines for Performance and Reliability</span></span>](#guidelines-for-performance-and-reliability)
-   [<span data-ttu-id="70293-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="70293-109">Related topics</span></span>](#related-topics)

## <a name="registering-and-distributing-property-handlers"></a><span data-ttu-id="70293-110">註冊和散發屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="70293-110">Registering and Distributing Property Handlers</span></span>

<span data-ttu-id="70293-111">在執行屬性處理常式之後，它必須註冊，而且其副檔名必須與處理常式相關聯。</span><span class="sxs-lookup"><span data-stu-id="70293-111">After the property handler is implemented, it must be registered and its file name extension must be associated with the handler.</span></span> <span data-ttu-id="70293-112">下列使用配方副檔名的範例說明所需的登錄專案。</span><span class="sxs-lookup"><span data-stu-id="70293-112">The following example using the .recipe extension illustrates the required registry entries to do so.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {50d9450f-2a80-4f08-93b9-2eb526477d1a}
         (Default) = Recipe Property Handler
         ManualSafeSave [REG_DWORD] = 00000001
         InProcServer32
            (Default) = C:\\SDK\\PropertyHandlerSample\\bin\\RecipeHandlers.dll
            ThreadingModel = Apartment
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PropertySystem
                  PropertyHandlers
                     .recipe
                        (Default) = {50d9450f-2a80-4f08-93b9-2eb526477d1a}
```

<span data-ttu-id="70293-113">特定檔案類型的屬性處理常式通常會與應用程式 () ，以建立或操作該類型的檔案。</span><span class="sxs-lookup"><span data-stu-id="70293-113">Property handlers for a particular file type are commonly distributed with the application(s) that create or manipulate files of that type.</span></span> <span data-ttu-id="70293-114">不過，您也應該考慮讓您的屬性處理常式可獨立于這些應用程式中使用，以支援在伺服器案例中，索引子會使用屬性處理常式來編制檔案類型的索引，但不需要這些應用程式的隨附應用程式。</span><span class="sxs-lookup"><span data-stu-id="70293-114">However, you should also consider making your property handlers available independently of these applications to support indexing of your file type in server scenarios where property handlers are used by the indexer, but their accompanying applications are not required.</span></span> <span data-ttu-id="70293-115">如果您為屬性處理常式建立獨立的安裝套件，請確定它包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="70293-115">If you create a stand-alone installation package for your property handler, be sure that it includes the following:</span></span>

-   <span data-ttu-id="70293-116">在 [註冊和散發屬性處理常式]()的主題中指定的屬性處理常式註冊詳細資料。</span><span class="sxs-lookup"><span data-stu-id="70293-116">The property handler registration details specified in the topic [Registering and Distributing Property Handlers]().</span></span>
-   <span data-ttu-id="70293-117">註冊您的檔案類型以及任何必須安裝的架構檔案，以便讓用戶端存取屬性處理常式的所有功能。</span><span class="sxs-lookup"><span data-stu-id="70293-117">Registration for your file type and any schema files that must be installed, to enable clients to access all the features of your property handler.</span></span>

## <a name="performance-and-reliability-considerations-for-property-handlers"></a><span data-ttu-id="70293-118">屬性處理常式的效能和可靠性考慮</span><span class="sxs-lookup"><span data-stu-id="70293-118">Performance and Reliability Considerations for Property Handlers</span></span>

<span data-ttu-id="70293-119">系統會針對特定電腦上的每個檔案叫用屬性處理常式。</span><span class="sxs-lookup"><span data-stu-id="70293-119">Property handlers are invoked for each file on a particular computer.</span></span> <span data-ttu-id="70293-120">通常會在下列情況下呼叫它們：</span><span class="sxs-lookup"><span data-stu-id="70293-120">They are usually called under the following circumstances:</span></span>

-   <span data-ttu-id="70293-121">在編制檔案的索引期間。</span><span class="sxs-lookup"><span data-stu-id="70293-121">During indexing of the file.</span></span> <span data-ttu-id="70293-122">這是跨進程完成，在具有限制許可權的隔離進程中。</span><span class="sxs-lookup"><span data-stu-id="70293-122">This is done out-of-process, in an isolated process with restricted rights.</span></span>
-   <span data-ttu-id="70293-123">在 Windows 檔案總管中存取檔案的目的是為了讀取和寫入屬性值。</span><span class="sxs-lookup"><span data-stu-id="70293-123">When files are accessed in Windows Explorer for the purpose of reading and writing property values.</span></span> <span data-ttu-id="70293-124">這是在同進程中完成。</span><span class="sxs-lookup"><span data-stu-id="70293-124">This is done in-process.</span></span>

### <a name="guidelines-for-performance-and-reliability"></a><span data-ttu-id="70293-125">效能和可靠性的指導方針</span><span class="sxs-lookup"><span data-stu-id="70293-125">Guidelines for Performance and Reliability</span></span>

<span data-ttu-id="70293-126">使用者在任何時候都可能有數十個特定類型的檔案 (包括您在電腦上) ，而且隨時都可以存取或修改任何或所有檔案。</span><span class="sxs-lookup"><span data-stu-id="70293-126">At any time, a user might have tens of thousands of files of any specific type (including yours) on his or her computers, and could access or modify any or all of these files at any time.</span></span> <span data-ttu-id="70293-127">因為通常會叫用屬性處理常式來支援這些存取和修改作業，所以您的屬性處理常式的效能和可靠性特性在忙碌中，高度並行的環境相當重要。</span><span class="sxs-lookup"><span data-stu-id="70293-127">Because property handlers are frequently invoked to support these access and modify operations, the performance and reliability characteristics of your property handler in busy, highly concurrent environments is of critical importance.</span></span>

<span data-ttu-id="70293-128">當您開發和測試屬性處理常式時，請記住下列指導方針。</span><span class="sxs-lookup"><span data-stu-id="70293-128">Keep in mind the following guidelines as you are developing and testing your property handler.</span></span>

-   <span data-ttu-id="70293-129">**屬性列舉**</span><span class="sxs-lookup"><span data-stu-id="70293-129">**Property enumeration**</span></span>

    <span data-ttu-id="70293-130">在列舉屬性時，屬性處理常式應該會有非常快速的回應時間。</span><span class="sxs-lookup"><span data-stu-id="70293-130">Property handlers should have a very fast response time in enumerating their properties.</span></span> <span data-ttu-id="70293-131">應避免對屬性值、網路查閱或搜尋資源以外的資源進行記憶體密集的計算，以確保回應時間快速。</span><span class="sxs-lookup"><span data-stu-id="70293-131">Memory-intensive calculations of property values, network lookups, or the search for resources other than the file itself should be avoided to ensure fast response times.</span></span>

-   <span data-ttu-id="70293-132">**就地寫入屬性**</span><span class="sxs-lookup"><span data-stu-id="70293-132">**In-place property writing**</span></span>

    <span data-ttu-id="70293-133">如果可能的話，處理中型或大型檔案 (數百 KB 或更大的) 時，應排列檔案格式，以便讀取或寫入屬性值，而不需要從磁片讀取整個檔案。</span><span class="sxs-lookup"><span data-stu-id="70293-133">If possible, when dealing with medium-sized or large files (several hundred KB or larger), the file format should be arranged so that reading or writing property values does not require reading the whole file from disk.</span></span> <span data-ttu-id="70293-134">即使需要搜尋檔案，也不應該將它完整讀入記憶體，因為這樣會還更膨脹 Windows 檔案總管的工作集或 Windows Search 索引子，因為它們會嘗試存取或為這些檔案編制索引。</span><span class="sxs-lookup"><span data-stu-id="70293-134">Even if the file needs to be sought, it should not be read into memory in its entirety because that bloats the working set of Windows Explorer or the Windows Search indexer as they try to access or index these files.</span></span> <span data-ttu-id="70293-135">如需詳細資訊，請參閱 [初始化屬性處理常式](./building-property-handlers-property-handlers.md)。</span><span class="sxs-lookup"><span data-stu-id="70293-135">For more information, see [Initializing Property Handlers](./building-property-handlers-property-handlers.md).</span></span>

    <span data-ttu-id="70293-136">完成這項工作的一項實用技巧是以額外的空間填補檔案的標頭，如此一來，下次需要寫入屬性值時，就可以就地寫入該值，而不需要重寫整個檔案。</span><span class="sxs-lookup"><span data-stu-id="70293-136">One useful technique to accomplish this is to pad the header of the file with extra space so that the next time a property value needs to be written, the value can be written in place without needing to rewrite the entire file.</span></span> <span data-ttu-id="70293-137">這需要 ManualSafeSave 功能。</span><span class="sxs-lookup"><span data-stu-id="70293-137">This requires the ManualSafeSave functionality.</span></span> <span data-ttu-id="70293-138">這種方法需要額外的風險，因為寫入進行中時可能會中斷檔案寫入作業 (因為) 的系統損毀或電源中斷，但由於屬性大小通常很小，因此這類中斷的機率也相當小，而且可透過就地屬性寫入來實現的效能提升，會被視為足以證明這項額外的風險。</span><span class="sxs-lookup"><span data-stu-id="70293-138">This approach involves some extra risk that the file write operation might be interrupted while the write is in progress (due to a system crash or power loss), but because property sizes are generally small, the probability of such an interruption is similarly small, and the performance gains that can be realized through in-place property writing are considered significant enough to justify this additional risk.</span></span> <span data-ttu-id="70293-139">即便如此，您也應該小心測試您的實作，以確保在寫入作業期間發生失敗時，您的檔案不會損毀。</span><span class="sxs-lookup"><span data-stu-id="70293-139">Even so, you should take care to test your implementation extensively to ensure that your files are not corrupted in the event that a failure does arise in the course of a write operation.</span></span>

    <span data-ttu-id="70293-140">最後，當您執行以 ManualSafeSave 撰寫的就地屬性時，有時無法就地執行作業，而且必須改為重寫整個資料流程。</span><span class="sxs-lookup"><span data-stu-id="70293-140">Finally, when implementing in-place property writing with ManualSafeSave, sometimes the operation cannot be performed in-place, and the whole stream must be rewritten anyway.</span></span> <span data-ttu-id="70293-141">為了方便重寫，處理常式初始化期間提供的資料流程支援 [**IDestinationStreamFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory) 介面。</span><span class="sxs-lookup"><span data-stu-id="70293-141">To facilitate the rewrite, the stream provided during handler initialization supports the [**IDestinationStreamFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory) interface.</span></span> <span data-ttu-id="70293-142">**IDestinationStreamFactory** 介面讓處理常式得以取得要寫入的暫存資料流程;當所有寫入都已完成並呼叫 [**IDestinationStreamFactory：： GetDestinationStream**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream)方法時，此資料流程會用來完全取代原始檔案資料流程。</span><span class="sxs-lookup"><span data-stu-id="70293-142">The **IDestinationStreamFactory** interface enables handler implementations to obtain a temporary stream for writing; when all writes are completed and the [**IDestinationStreamFactory::GetDestinationStream**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream) method is called, this stream is used to fully replace the original file stream.</span></span> <span data-ttu-id="70293-143">使用目的資料流程時，原始檔案資料流程應視為唯讀，因為它會在呼叫 **IDestinationStreamFactory：： GetDestinationStream** 方法之後，由目的地資料流程取代。</span><span class="sxs-lookup"><span data-stu-id="70293-143">When the destination stream is used, the original file stream should be treated as read-only, because it will be replaced by the destination stream after the **IDestinationStreamFactory::GetDestinationStream** method has been called.</span></span>

-   <span data-ttu-id="70293-144">**選擇您的 COM 執行緒模型**</span><span class="sxs-lookup"><span data-stu-id="70293-144">**Choosing your COM threading model**</span></span>

    <span data-ttu-id="70293-145">若要最大化您的屬性處理常式效率，您應該指定它使用 COM 執行緒模型 `Both` 。</span><span class="sxs-lookup"><span data-stu-id="70293-145">To maximize the efficiency of your property handler, you should specify that it uses the COM threading model `Both`.</span></span> <span data-ttu-id="70293-146">這可讓您直接從 STA 公寓 (Windows 檔案總管存取，例如) 和郵件傳輸代理程式 (MTA) 單元 (Windows Search 中的 SearchProtocolHost 程式，例如) ，避免在這些環境中進行封送處理的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="70293-146">This enables direct access from STA apartments (Windows Explorer, for example) and message transfer agent (MTA) apartments (the SearchProtocolHost process in Windows Search, for example), avoiding the overhead of marshaling in those environments.</span></span> <span data-ttu-id="70293-147">若要達成執行緒模型的完整優點 `Both` ，您的處理常式所相依的任何服務都應該也指定為， `Both` 以避免呼叫這些元件時進行任何封送處理。</span><span class="sxs-lookup"><span data-stu-id="70293-147">To achieve the full benefit of the `Both` threading model, any services on which your handler depends should also be designated as `Both` to avoid any marshaling in calls to those components.</span></span> <span data-ttu-id="70293-148">請查看這些特定服務的檔，確認它們是否使用此執行緒模型。</span><span class="sxs-lookup"><span data-stu-id="70293-148">Check the documentation of these particular services to verify whether they use this threading model.</span></span>

-   <span data-ttu-id="70293-149">**屬性處理常式並行**</span><span class="sxs-lookup"><span data-stu-id="70293-149">**Property handler concurrency**</span></span>

    <span data-ttu-id="70293-150">屬性處理常式和 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面是針對序列而非平行存取所設計。</span><span class="sxs-lookup"><span data-stu-id="70293-150">Property handlers and the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface are designed for serial rather than concurrent access.</span></span> <span data-ttu-id="70293-151">從 Windows 程式碼基底的 Windows 檔案總管、Windows Search 索引子和其他所有屬性處理常式調用都保證此使用方式。</span><span class="sxs-lookup"><span data-stu-id="70293-151">Windows Explorer, the Windows Search indexer, and all other property handler invocations from the Windows codebase guarantee this usage.</span></span> <span data-ttu-id="70293-152">協力廠商不應該同時使用屬性處理常式，但無法保證此行為。</span><span class="sxs-lookup"><span data-stu-id="70293-152">There should be no reason for third parties to use a property handler concurrently, but this behavior cannot be guaranteed.</span></span> <span data-ttu-id="70293-153">此外，即使呼叫模式必須是序列，呼叫也可能會在不同的執行緒 (例如，當透過 COM RPC 從遠端呼叫物件時，會發生在索引子) 中。</span><span class="sxs-lookup"><span data-stu-id="70293-153">Also, even though the calling pattern is expected to be serial, the calls may come on different threads (for instance, when the object is being called remotely via COM RPC, as occurs in the indexer).</span></span> <span data-ttu-id="70293-154">因此，屬性處理常式的執行必須支援在不同的執行緒上呼叫，而在此情況下，如果同時呼叫，則應該不會影響任何不良的效果</span><span class="sxs-lookup"><span data-stu-id="70293-154">Therefore, property handler implementations must support being called on different threads, and ideally should not suffer any ill effects when called concurrently.</span></span> <span data-ttu-id="70293-155">因為預定的呼叫模式是序列，所以使用重要區段的簡單執行應該足以滿足大部分情況下的這些需求。</span><span class="sxs-lookup"><span data-stu-id="70293-155">Because the intended calling pattern is serial, a trivial implementation using a critical section should be sufficient to meet these requirements in most cases.</span></span> <span data-ttu-id="70293-156">您可以使用 [**TryEnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-tryentercriticalsection) 函式偵測和失敗並行呼叫，以避免封鎖並行呼叫。</span><span class="sxs-lookup"><span data-stu-id="70293-156">It is acceptable to avoid blocking on concurrent calls by using the [**TryEnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-tryentercriticalsection) function to detect and fail concurrent calls.</span></span>

-   <span data-ttu-id="70293-157">**檔案並行**</span><span class="sxs-lookup"><span data-stu-id="70293-157">**File concurrency**</span></span>

    <span data-ttu-id="70293-158">屬性處理常式通常用於多個應用程式同時存取檔案的案例中。</span><span class="sxs-lookup"><span data-stu-id="70293-158">Property handlers are often used in scenarios where multiple applications access a file concurrently.</span></span> <span data-ttu-id="70293-159">因此，處理常式和應用程式需要在開啟檔案時指定適當的共用模式來管理並行。</span><span class="sxs-lookup"><span data-stu-id="70293-159">Hence, the handler and the applications need to manage the concurrency by specifying appropriate sharing modes when opening the file.</span></span> <span data-ttu-id="70293-160">他們也必須留意其他應用程式所指定的存取權，以及管理不允許存取的情況。</span><span class="sxs-lookup"><span data-stu-id="70293-160">They also need to be aware of the access that the other applications specify and to manage cases where access is not allowed.</span></span> <span data-ttu-id="70293-161">如果所有取用者都指定了適當的共用模式，讓其他人能夠同時存取該檔案，但在這麼做時，必須管理一致性問題。</span><span class="sxs-lookup"><span data-stu-id="70293-161">It is best if all consumers specify liberal sharing modes to enable others to access the file concurrently, but when doing this, consistency issues need to be managed.</span></span> <span data-ttu-id="70293-162">若要使用最適當的共用模式，必須在存取檔案的應用程式之應用程式的內容中進行決策。</span><span class="sxs-lookup"><span data-stu-id="70293-162">Decisions on the most appropriate sharing modes to be used need to be made in the context of the community of applications that access the file.</span></span>

    <span data-ttu-id="70293-163">檔案系統可讓應用程式以一種方式開啟檔案，讓它們能夠控制其他應用程式是否可以開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="70293-163">File systems enable applications to open files in a way that gives them control over whether and how other applications can open the file.</span></span> <span data-ttu-id="70293-164">共用模式可啟用讀取、寫入和刪除存取。</span><span class="sxs-lookup"><span data-stu-id="70293-164">Sharing modes enable read, write, and delete access.</span></span> <span data-ttu-id="70293-165">屬性系統支援這些共用模式的子集，如下表所述。</span><span class="sxs-lookup"><span data-stu-id="70293-165">The property system supports a subset of these sharing modes, outlined in the following table.</span></span>

    

    | <span data-ttu-id="70293-166">存取模式</span><span class="sxs-lookup"><span data-stu-id="70293-166">Access mode</span></span>                     | <span data-ttu-id="70293-167">共用模式</span><span class="sxs-lookup"><span data-stu-id="70293-167">Sharing mode</span></span>                             |
    |---------------------------------|------------------------------------------|
    | <span data-ttu-id="70293-168">寫入</span><span class="sxs-lookup"><span data-stu-id="70293-168">Write</span></span>                           | <span data-ttu-id="70293-169">拒絕其他讀者和寫入器</span><span class="sxs-lookup"><span data-stu-id="70293-169">Deny other readers and writers</span></span>           |
    | <span data-ttu-id="70293-170">撰寫 (EnableShareDenyWrite) </span><span class="sxs-lookup"><span data-stu-id="70293-170">Write (EnableShareDenyWrite)</span></span>    | <span data-ttu-id="70293-171">啟用其他讀取器，拒絕其他寫入器</span><span class="sxs-lookup"><span data-stu-id="70293-171">Enable other readers, deny other writers</span></span> |
    | <span data-ttu-id="70293-172">唯讀 (預設) </span><span class="sxs-lookup"><span data-stu-id="70293-172">Read-only (default)</span></span>             | <span data-ttu-id="70293-173">啟用其他讀取器，拒絕其他寫入器</span><span class="sxs-lookup"><span data-stu-id="70293-173">Enable other readers, deny other writers</span></span> |
    | <span data-ttu-id="70293-174">唯讀 (EnableShareDenyNone) </span><span class="sxs-lookup"><span data-stu-id="70293-174">Read-only (EnableShareDenyNone)</span></span> | <span data-ttu-id="70293-175">啟用其他讀取器和寫入器</span><span class="sxs-lookup"><span data-stu-id="70293-175">Enable other readers and writers</span></span>         |

    

     

    <span data-ttu-id="70293-176">開啟以供 **寫入** (GPS READWRITE 的屬性處理常式 \_) 將會拒絕其他讀取器和寫入器。</span><span class="sxs-lookup"><span data-stu-id="70293-176">Property handlers open for **write** (GPS\_READWRITE) will deny other readers and writers.</span></span> <span data-ttu-id="70293-177">處理常式可以選擇允許讀取器，方法是指定 `EnableShareDenyWrite` 旗標 (表示在其註冊中啟用讀取) 。</span><span class="sxs-lookup"><span data-stu-id="70293-177">Handlers can opt into behavior that enables readers by specifying the `EnableShareDenyWrite` flag (implying enable Read) in its registration.</span></span>

    <span data-ttu-id="70293-178">屬性處理常式會開啟以供 **讀取** (GPS \_ 預設) ，預設會啟用其他讀取器，但拒絕其他寫入器。</span><span class="sxs-lookup"><span data-stu-id="70293-178">Property handlers open for **read** (GPS\_DEFAULT), by default enable other readers but deny other writers.</span></span> <span data-ttu-id="70293-179">處理常式可以選擇啟用其他寫入器，方法是 `EnableShareDenyNone` 在其註冊中指定旗標。</span><span class="sxs-lookup"><span data-stu-id="70293-179">Handlers can opt into enabling other writers by specifying the `EnableShareDenyNone` flag in its registration.</span></span> <span data-ttu-id="70293-180">這表示處理常式可以成功處理在處理常式讀取檔案時，檔案內容變更的情況。</span><span class="sxs-lookup"><span data-stu-id="70293-180">This means that a handler can successfully handle a situation in which the content of a file changes while the handler is reading the file.</span></span>

    <span data-ttu-id="70293-181">如需旗標定義，請參閱 [**GETPROPERTYSTOREFLAGS**](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags)。</span><span class="sxs-lookup"><span data-stu-id="70293-181">For flag definitions, see [**GETPROPERTYSTOREFLAGS**](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags).</span></span>

## <a name="related-topics"></a><span data-ttu-id="70293-182">相關主題</span><span class="sxs-lookup"><span data-stu-id="70293-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70293-183">瞭解屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="70293-183">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
</dt> <dt>

[<span data-ttu-id="70293-184">使用種類名稱</span><span class="sxs-lookup"><span data-stu-id="70293-184">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[<span data-ttu-id="70293-185">使用屬性清單</span><span class="sxs-lookup"><span data-stu-id="70293-185">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
</dt> <dt>

[<span data-ttu-id="70293-186">初始化屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="70293-186">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
</dt> <dt>

[<span data-ttu-id="70293-187">屬性處理常式的最佳作法和常見問題</span><span class="sxs-lookup"><span data-stu-id="70293-187">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
