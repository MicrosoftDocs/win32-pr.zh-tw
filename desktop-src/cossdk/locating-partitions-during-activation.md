---
description: 在啟用期間尋找磁碟分割
ms.assetid: a5452ed6-ab0f-4d38-bc16-1de6cbf57486
title: 在啟用期間尋找磁碟分割
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e8912c8277d79c1a20300a1a880644801d0bcb
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "104555711"
---
# <a name="locating-partitions-during-activation"></a><span data-ttu-id="51a46-103">在啟用期間尋找磁碟分割</span><span class="sxs-lookup"><span data-stu-id="51a46-103">Locating Partitions During Activation</span></span>

<span data-ttu-id="51a46-104">找出要啟用元件的正確磁碟分割取決於下列各項：</span><span class="sxs-lookup"><span data-stu-id="51a46-104">Locating the correct partition in which to activate a component depends on the following:</span></span>

-   <span data-ttu-id="51a46-105">呼叫程式中用來啟動元件的函式呼叫和參數</span><span class="sxs-lookup"><span data-stu-id="51a46-105">The function call and parameters used in the calling program to activate the component</span></span>
-   <span data-ttu-id="51a46-106">要啟用的元件是本機或遠端</span><span class="sxs-lookup"><span data-stu-id="51a46-106">Whether the component being activated is local or remote</span></span>
-   <span data-ttu-id="51a46-107">資料分割快取的內部使用</span><span class="sxs-lookup"><span data-stu-id="51a46-107">The internal use of the partition cache</span></span>

## <a name="the-calling-program"></a><span data-ttu-id="51a46-108">呼叫程式</span><span class="sxs-lookup"><span data-stu-id="51a46-108">The Calling Program</span></span>

<span data-ttu-id="51a46-109">COM + 會根據呼叫程式啟動元件的方式，選取要啟用的資料分割。</span><span class="sxs-lookup"><span data-stu-id="51a46-109">COM+ selects the partition for component activation based on how the calling program activates the component.</span></span>

<span data-ttu-id="51a46-110">有三種不同的動作，可讓 COM + 在選取用於元件啟用的資料分割時採用。</span><span class="sxs-lookup"><span data-stu-id="51a46-110">There are three different actions that COM+ can take when selecting a partition for component activation.</span></span> <span data-ttu-id="51a46-111">採取的動作取決於呼叫程式如何將物件具現化，也就是函式呼叫是否包含分割區識別碼和 CLSID 所組成的資料分割標記，或是只包含 CLSID。</span><span class="sxs-lookup"><span data-stu-id="51a46-111">The action taken depends on how the calling program instantiates the object that is, whether the function call includes a partition moniker, which consists of a partition ID and a CLSID, or includes a CLSID only.</span></span>

<span data-ttu-id="51a46-112">下表顯示 COM + 可採用的各種動作（依優先順序）以找出資料分割。</span><span class="sxs-lookup"><span data-stu-id="51a46-112">The following table shows the various actions that COM+ can take, in order of precedence, to locate a partition.</span></span>



| <span data-ttu-id="51a46-113">函式呼叫</span><span class="sxs-lookup"><span data-stu-id="51a46-113">Function call</span></span>                                                  | <span data-ttu-id="51a46-114">參數</span><span class="sxs-lookup"><span data-stu-id="51a46-114">Parameter</span></span>                                                      | <span data-ttu-id="51a46-115">COM + 動作</span><span class="sxs-lookup"><span data-stu-id="51a46-115">COM+ action</span></span>                                                                                                                                                                                    |
|----------------------------------------------------------------|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51a46-116">[**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) 或 **GetObject**</span><span class="sxs-lookup"><span data-stu-id="51a46-116">[**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) or **GetObject**</span></span><br/> | <span data-ttu-id="51a46-117">分割區標記 (包括資料分割識別碼和 CLSID) </span><span class="sxs-lookup"><span data-stu-id="51a46-117">Partition moniker (includes partition ID and CLSID)</span></span><br/> | <span data-ttu-id="51a46-118">使用資料分割標記中指定的分割區識別碼。</span><span class="sxs-lookup"><span data-stu-id="51a46-118">Uses the partition ID specified in the partition moniker.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="51a46-119">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="51a46-119">**CoCreateInstance**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)<br/>        | <span data-ttu-id="51a46-120">CLSID</span><span class="sxs-lookup"><span data-stu-id="51a46-120">CLSID</span></span><br/>                                               | <span data-ttu-id="51a46-121">使用使用者識別之預設分割區的分割區識別碼，或在相同進程中先前元件啟用期間新增至內容的資料分割識別碼。</span><span class="sxs-lookup"><span data-stu-id="51a46-121">Uses either the partition ID of the user identity's default partition or the partition ID that was added to the context during a previous component activation in the same process.</span></span><br/> |



 

<span data-ttu-id="51a46-122">下列各節將說明上表所列的 COM + 動作。</span><span class="sxs-lookup"><span data-stu-id="51a46-122">The COM+ actions listed in the preceding table are explained in the following sections.</span></span>

## <a name="use-of-partition-monikers"></a><span data-ttu-id="51a46-123">使用分割區的名字</span><span class="sxs-lookup"><span data-stu-id="51a46-123">Use of Partition Monikers</span></span>

<span data-ttu-id="51a46-124">您可以使用資料 *分割標記*，在函式呼叫內明確選取資料分割。</span><span class="sxs-lookup"><span data-stu-id="51a46-124">A partition can be selected explicitly within a function call by using a *partition moniker*.</span></span> <span data-ttu-id="51a46-125">在程式碼中，會使用資料分割標記來明確指定已啟動元件的資料分割。</span><span class="sxs-lookup"><span data-stu-id="51a46-125">A partition moniker is used within code to explicitly specify the partition of the activated component.</span></span> <span data-ttu-id="51a46-126">如果使用資料分割標記來找出分割區，則會從該分割區進行啟用。</span><span class="sxs-lookup"><span data-stu-id="51a46-126">If a partition moniker is used to locate the partition, the activation occurs from that partition.</span></span> <span data-ttu-id="51a46-127">也就是說，在標記中包含的資料分割識別碼會優先于使用者的預設分割區，或是存在於呼叫端內容中的資料分割識別碼。</span><span class="sxs-lookup"><span data-stu-id="51a46-127">That is, the partition ID included in the moniker takes precedence over the user's default partition or over a partition ID that exists in the caller's context.</span></span>

<span data-ttu-id="51a46-128">在 c + + 程式碼中，使用資料分割標記的語法如下所示：</span><span class="sxs-lookup"><span data-stu-id="51a46-128">In C++ code, the syntax for the use of a partition moniker is as follows:</span></span>


```C++
HRESULT CoGetObject(
  L"partition:partitionGUID/new:clsid",
  pBindOptions,
  IID_IUnknown,
  (void**)&pIUnknown);
```



<span data-ttu-id="51a46-129">下列範例顯示 c + + 程式碼的程式碼片段，其中會使用分割區的標記做為 [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) 函數的引數：</span><span class="sxs-lookup"><span data-stu-id="51a46-129">The following example shows a snippet of C++ code, in which a partition moniker is being used as an argument to the [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) function:</span></span>


```C++
// Create CLSID1 configured in the Production partition.
HRESULT hr = CoGetObject(
  L"partition:{35056070-D5B7-4b59-9FBF-0D23417F6937}/new:CLSID1",
  pBindOptions, IID_IUnknown, (void**)&pIUnknown);
```



<span data-ttu-id="51a46-130">在 Visual Basic 程式碼中，資料分割標記的語法如下所示：</span><span class="sxs-lookup"><span data-stu-id="51a46-130">In Visual Basic code, the syntax for a partition moniker is as follows:</span></span>


```VB
GetObject("partition:partitionGUID/new:CLSID") As Object
```



<span data-ttu-id="51a46-131">下列範例會顯示 Visual Basic 程式碼的程式碼片段，其中資料分割標記會當做 **GetObject** 函數的引數使用：</span><span class="sxs-lookup"><span data-stu-id="51a46-131">The following example shows a snippet of Visual Basic code, in which a partition moniker is being used as an argument to the **GetObject** function:</span></span>


```VB
Dim objCLSID1 As Object
Set objCLSID1 = GetObject( _
   "partition:{35056070-D5B7-4b59-9FBF-0D23417F6937}/new:CLSID1")
```



## <a name="use-of-default-mapping"></a><span data-ttu-id="51a46-132">使用預設對應</span><span class="sxs-lookup"><span data-stu-id="51a46-132">Use of Default Mapping</span></span>

<span data-ttu-id="51a46-133">當 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 函數用來啟動元件時，使用元件的 CLSID 時，com + 會使用預設的使用者識別對應，也就是使用者在 Active Directory 內對應的資料分割集。</span><span class="sxs-lookup"><span data-stu-id="51a46-133">When the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function is used to activate a component, using the component's CLSID, COM+ uses the default user-identity mapping that is, the partition set that the user is mapped to within Active Directory.</span></span> <span data-ttu-id="51a46-134">但是，如果使用者未對應到 Active Directory 內的資料分割集，則會選取全域資料分割。</span><span class="sxs-lookup"><span data-stu-id="51a46-134">However, if the user is not mapped to a partition set within Active Directory, the Global Partition is selected.</span></span>

## <a name="use-of-partition-ids-and-object-context"></a><span data-ttu-id="51a46-135">使用資料分割識別碼和物件內容</span><span class="sxs-lookup"><span data-stu-id="51a46-135">Use of Partition IDs and Object Context</span></span>

<span data-ttu-id="51a46-136">指派給新分割區的五個屬性之一是分割區識別碼。</span><span class="sxs-lookup"><span data-stu-id="51a46-136">One of the five properties assigned to a new partition is the partition ID.</span></span> <span data-ttu-id="51a46-137">當用戶端程式呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 函數來具現化物件時，會將資料分割識別碼加入至內容。</span><span class="sxs-lookup"><span data-stu-id="51a46-137">When the client program calls the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to instantiate an object, the partition ID is added to the context.</span></span> <span data-ttu-id="51a46-138">使用來自內容的資料分割識別碼來找出分割區是很重要的，因為它可確保在開始執行鏈之後，資料分割識別碼會維持不變，除非它透過分割區標記明確變更。</span><span class="sxs-lookup"><span data-stu-id="51a46-138">Using the partition ID from the context to locate the partition is important because it ensures that after a chain of activations has begun, the partition ID remains the same unless it is changed explicitly through a partition moniker.</span></span>

<span data-ttu-id="51a46-139">如需在啟用期間尋找資料分割的詳細資訊，請參閱 [Com + 佇列元件和](com--queued-components-and-partitions.md)分割區。</span><span class="sxs-lookup"><span data-stu-id="51a46-139">For additional information on locating partitions during activation, see [COM+ Queued Components and Partitions](com--queued-components-and-partitions.md).</span></span>

## <a name="local-and-remote-activation"></a><span data-ttu-id="51a46-140">本機和遠端啟用</span><span class="sxs-lookup"><span data-stu-id="51a46-140">Local and Remote Activation</span></span>

-   <span data-ttu-id="51a46-141">如果所呼叫的元件存在於另一部電腦上，磁碟分割屬性 (包括分割區識別碼) 會封送處理至另一部電腦，而且該元件會從已封送處理的分割區啟用。</span><span class="sxs-lookup"><span data-stu-id="51a46-141">If the component being called exists on another computer, the partition properties (including the partition ID) are marshaled to the other computer and the component is activated from the marshaled partition.</span></span> <span data-ttu-id="51a46-142">如果未封送處理資料分割識別碼，COM + 會使用對應至 Active Directory 內使用者識別的預設資料分割集。</span><span class="sxs-lookup"><span data-stu-id="51a46-142">If no partition ID was marshaled, COM+ uses the default partition set mapped to the user identity within Active Directory.</span></span>

## <a name="the-partition-cache"></a><span data-ttu-id="51a46-143">分割區快取</span><span class="sxs-lookup"><span data-stu-id="51a46-143">The Partition Cache</span></span>

<span data-ttu-id="51a46-144">在網域環境中，COM + 會使用 Active Directory 中的對應，找出正確的資料分割以進行元件啟用。</span><span class="sxs-lookup"><span data-stu-id="51a46-144">In a domain environment, COM+ uses the mappings in Active Directory to locate the correct partition for component activation.</span></span> <span data-ttu-id="51a46-145">不過，在 Active Directory 中頻繁地查閱可能會導致網路流量過高。</span><span class="sxs-lookup"><span data-stu-id="51a46-145">However, frequent lookups in Active Directory can result in excessive network traffic.</span></span> <span data-ttu-id="51a46-146">為了將在 Active Directory 中頻繁查閱使用者對分割集對應所產生的網路流量降至最低，COM + 會使用 *分割* 區快取。</span><span class="sxs-lookup"><span data-stu-id="51a46-146">To minimize network traffic resulting from frequent lookups of user-to-partition-set mapping in Active Directory, COM+ uses a *partition cache*.</span></span>

<span data-ttu-id="51a46-147">分割區快取包含在使用者身分識別或 Ou 與其分割集之間的 Active Directory 中進行的對應。</span><span class="sxs-lookup"><span data-stu-id="51a46-147">The partition cache contains the mappings that were made in Active Directory between user identities or OUs and their partition sets.</span></span> <span data-ttu-id="51a46-148">此分割區快取位於 COM + 應用程式所在的應用程式伺服器上。</span><span class="sxs-lookup"><span data-stu-id="51a46-148">This partition cache is located on the application server on which the COM+ applications reside.</span></span>

<span data-ttu-id="51a46-149">當 COM + 需要判斷使用者的預設分割區，或驗證使用者對資料分割的存取權限時，它會在本機檢查資料分割快取以查詢使用者的對應，而不是從遠端檢查 Active Directory。</span><span class="sxs-lookup"><span data-stu-id="51a46-149">When COM+ needs to determine a user's default partition or validate a user's access rights to a partition, it checks the partition cache locally to look up the user's mapping, instead of checking Active Directory remotely.</span></span>

<span data-ttu-id="51a46-150">如果分割區快取中的查閱失敗，COM + 就會檢查 Active Directory。</span><span class="sxs-lookup"><span data-stu-id="51a46-150">If the lookup in the partition cache fails, COM+ then checks Active Directory.</span></span> <span data-ttu-id="51a46-151">如果 Active Directory 中的查閱成功，COM + 會將該對應儲存在分割區快取中。</span><span class="sxs-lookup"><span data-stu-id="51a46-151">If the lookup is successful in Active Directory, COM+ stores that mapping in the partition cache.</span></span> <span data-ttu-id="51a46-152">下次對該使用者對分割區對應進行查閱時，COM + 會在分割區快取中找到它。</span><span class="sxs-lookup"><span data-stu-id="51a46-152">The next time a lookup is done for that user-to-partition mapping, COM+ will find it in the partition cache.</span></span>

<span data-ttu-id="51a46-153">下圖顯示 COM + 用來尋找元件啟用之分割區的進程。</span><span class="sxs-lookup"><span data-stu-id="51a46-153">The following illustration shows the process that COM+ uses to locate a partition for component activation.</span></span>

![此圖顯示 COM + 用來尋找元件啟用之分割區之進程的疑難排解樹狀結構。](images/5d00eb4e-4572-491c-85e9-33ceed2cd753.png)

<span data-ttu-id="51a46-155">快取的大小和快取專案的到期時間是透過登錄機碼設定。</span><span class="sxs-lookup"><span data-stu-id="51a46-155">The size of the cache and the expiration time for the cache entries are set via registry keys.</span></span> <span data-ttu-id="51a46-156">如需設定這些登錄機碼的詳細資訊，請參閱 [建立和設定 COM +](creating-and-configuring-com--partitions.md)分割。</span><span class="sxs-lookup"><span data-stu-id="51a46-156">For information on configuring these registry keys, see [Creating and Configuring COM+ Partitions](creating-and-configuring-com--partitions.md).</span></span>

> [!Note]  
> <span data-ttu-id="51a46-157">如果伺服器電腦與網路中斷連線，而伺服器中斷連線時，使用者對分割區的對應會變更，則磁碟分割快取可能會包含過期的使用者對分割區對應。</span><span class="sxs-lookup"><span data-stu-id="51a46-157">If a server computer is disconnected from the network and the user-to-partition mapping is changed while the server is disconnected, the partition cache might contain outdated user-to-partition mapping.</span></span> <span data-ttu-id="51a46-158">如果使用者對分割區對應是用來啟動元件的機制，這可能會導致啟用錯誤。</span><span class="sxs-lookup"><span data-stu-id="51a46-158">This could result in an activation error if user-to-partition mapping is the mechanism used to activate a component.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="51a46-159">相關主題</span><span class="sxs-lookup"><span data-stu-id="51a46-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51a46-160">找出要啟用的元件</span><span class="sxs-lookup"><span data-stu-id="51a46-160">Locating a Component for Activation</span></span>](locating-a-component-for-activation.md)
</dt> </dl>

 

