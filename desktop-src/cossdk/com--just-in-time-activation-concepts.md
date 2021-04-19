---
description: 及時 (JIT) 啟動服務可讓 COM + 在用戶端仍保留該物件的作用中參考時，停用物件。
ms.assetid: dbc7b257-8506-42c8-8a78-3474c6d4f4b6
title: COM + 即時啟用概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c942bfeb342ea305083e0c7d7ebdea2fe96bf24
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988057"
---
# <a name="com-just-in-time-activation-concepts"></a><span data-ttu-id="27a25-103">COM + 即時啟用概念</span><span class="sxs-lookup"><span data-stu-id="27a25-103">COM+ Just-in-Time Activation Concepts</span></span>

<span data-ttu-id="27a25-104">及時 (JIT) 啟動服務可讓 COM + 在用戶端仍保留該物件的作用中參考時，停用物件。</span><span class="sxs-lookup"><span data-stu-id="27a25-104">The just-in-time (JIT) activation service enables COM+ to deactivate an object while a client still holds an active reference to that object.</span></span> <span data-ttu-id="27a25-105">下次用戶端在物件上呼叫方法時（用戶端認為仍在使用中），COM + JIT 啟動服務會將物件透明地重新開機至用戶端（及時）。</span><span class="sxs-lookup"><span data-stu-id="27a25-105">The next time the client calls a method on the object, which the client believes to be still active, the COM+ JIT activation service reactivates the object transparently to the client, just in time.</span></span>

<span data-ttu-id="27a25-106">使用 COM + JIT 啟用的主要優點是，您可以讓用戶端在需要的情況下保留物件的參考，而不一定會佔用重要的伺服器資源（例如記憶體）。</span><span class="sxs-lookup"><span data-stu-id="27a25-106">The main advantage of using COM + JIT activation is that you can enable clients to hold references to objects for as long as they need them, without necessarily tying up valuable server resources such as memory.</span></span> <span data-ttu-id="27a25-107">其他重要的優點包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="27a25-107">Other important benefits include the following:</span></span>

-   <span data-ttu-id="27a25-108">使用 COM + JIT 啟用服務可大幅簡化用戶端的程式設計模型，因為用戶端不需要思考它如何使用昂貴的伺服器物件和伺服器資源。</span><span class="sxs-lookup"><span data-stu-id="27a25-108">Using the COM+ JIT activation service greatly simplifies the programming model for the client because the client doesn't have to think about how it uses expensive server objects and server resources.</span></span> <span data-ttu-id="27a25-109">如果沒有 JIT 啟用，當用戶端經常需要呼叫和釋放物件時，可能會產生重大的負面影響。</span><span class="sxs-lookup"><span data-stu-id="27a25-109">Without JIT activation, clients can incur a significant penalty when they frequently need to call and release objects.</span></span>
    > [!Note]  
    > <span data-ttu-id="27a25-110">您可以使用 [Com + 物件](com--object-pooling.md) 共用服務，進一步改善此效能優勢。</span><span class="sxs-lookup"><span data-stu-id="27a25-110">You can refine this performance benefit further by using the [COM+ Object Pooling](com--object-pooling.md) service.</span></span> <span data-ttu-id="27a25-111">藉由共用 JIT 啟動的物件，您可以大幅加速用戶端的物件重新開機，同時重複使用它們可能保留的資源，讓您更精確地控制伺服器上的指定物件所使用的記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="27a25-111">By pooling JIT-activated objects, you can greatly speed object reactivation for clients while reusing whatever resources they might be holding, giving you more precise control over how much memory is used by a given object on the server.</span></span> <span data-ttu-id="27a25-112">如需詳細資訊，請參閱 [物件共用和 COM + JIT 啟用](object-pooling-and-com--jit-activation.md)。</span><span class="sxs-lookup"><span data-stu-id="27a25-112">For more detail, see [Object Pooling and COM+ JIT Activation](object-pooling-and-com--jit-activation.md).</span></span>

     

-   <span data-ttu-id="27a25-113">使用分散式應用程式時，需要昂貴的網路來回行程才能建立每個物件，而用戶端從伺服器越多，啟動和封送處理伺服器物件、開啟通道，以及設定 proxy 和存根的成本就愈大。</span><span class="sxs-lookup"><span data-stu-id="27a25-113">With distributed applications, an expensive network round-trip is required for the creation of every object, and the farther the client is from the server, the greater the costs of activating and marshaling the server object, opening the channel, and setting up the proxy and stub.</span></span> <span data-ttu-id="27a25-114">藉由使用 COM + JIT 啟用服務，您可以將建立物件的頻率降到最低，以大幅提升應用程式的效能。</span><span class="sxs-lookup"><span data-stu-id="27a25-114">By using the COM+ JIT activation service, you can minimize the frequency of object creation to significantly improve the performance of your application.</span></span>
-   <span data-ttu-id="27a25-115">當您使用 COM + JIT 啟用來啟動這些物件，而這些物件是用戶端保存長時間存留的參考，但不一定都在使用時，伺服器記憶體不一定會讓這些物件保持運作。</span><span class="sxs-lookup"><span data-stu-id="27a25-115">When you use COM+ JIT activation to activate those objects to which clients hold long-lived references but which they aren't necessarily using all the time, server memory is not always tied up keeping those objects alive.</span></span> <span data-ttu-id="27a25-116">這可能會大幅增加應用程式的擴充性。</span><span class="sxs-lookup"><span data-stu-id="27a25-116">This can significantly increase the scalability of your application.</span></span> <span data-ttu-id="27a25-117">用戶端看到的唯一效能衝擊，就是 COM + 重新啟始物件所花費的時間，通常比為物件配置記憶體所花的時間還要多，而且明顯小於網路往返以進行遠端物件建立。</span><span class="sxs-lookup"><span data-stu-id="27a25-117">The only performance hit that clients see is the time it takes COM+ to reactivate the object, usually just marginally more time than it takes to allocate memory for the object and substantially less than the network round-trip for remote object creation.</span></span>

## <a name="enabling-com-jit-activation"></a><span data-ttu-id="27a25-118">啟用 COM + JIT 啟用</span><span class="sxs-lookup"><span data-stu-id="27a25-118">Enabling COM+ JIT Activation</span></span>

<span data-ttu-id="27a25-119">您可以使用 [元件服務] 系統管理工具或系統管理功能，為元件啟用 COM + JIT 啟用服務。</span><span class="sxs-lookup"><span data-stu-id="27a25-119">You can enable the COM+ JIT activation service for a component by using either the Component Services administrative tool or the Administrative functions.</span></span> <span data-ttu-id="27a25-120">如需如何進行此作業的詳細資訊，請參閱 [啟用元件的 JIT](enabling-jit-activation-for-a-component.md)啟用。</span><span class="sxs-lookup"><span data-stu-id="27a25-120">For details about how to do this, see [Enabling JIT Activation for a Component](enabling-jit-activation-for-a-component.md).</span></span>

<span data-ttu-id="27a25-121">COM + JIT 啟用可以與其他 COM + 服務互動，如下所示：</span><span class="sxs-lookup"><span data-stu-id="27a25-121">COM+ JIT activation can interact with other COM+ services, such as the following:</span></span>

-   <span data-ttu-id="27a25-122">當您的元件需要交易時，系統會自動為它啟用 JIT 啟用。</span><span class="sxs-lookup"><span data-stu-id="27a25-122">When your component requires transactions, JIT activation is automatically enabled for it.</span></span> <span data-ttu-id="27a25-123">如需更詳細的資訊，請參閱 [交易和 COM + JIT 啟用](transactions-and-com--jit-activation.md)。</span><span class="sxs-lookup"><span data-stu-id="27a25-123">For greater detail, see [Transactions and COM+ JIT Activation](transactions-and-com--jit-activation.md).</span></span>
-   <span data-ttu-id="27a25-124">當您的元件啟用 JIT 啟用時，同步處理會自動設為 [必要]。</span><span class="sxs-lookup"><span data-stu-id="27a25-124">When your component is enabled for JIT activation, synchronization is automatically set to required.</span></span> <span data-ttu-id="27a25-125">這表示，如果兩個用戶端同時呼叫 JIT 啟動的元件，而其中一個的方法呼叫傳回時，會造成物件被停用，而另一個則不會留下擱置。</span><span class="sxs-lookup"><span data-stu-id="27a25-125">This means that if two clients simultaneously call a JIT-activated component and a method call for one of them returns, causing the object to be deactivated, the other is not left stranded.</span></span>

## <a name="how-deactivation-is-triggered"></a><span data-ttu-id="27a25-126">觸發停用的方式</span><span class="sxs-lookup"><span data-stu-id="27a25-126">How Deactivation Is Triggered</span></span>

<span data-ttu-id="27a25-127">COM + 會根據物件內容上的 doneness 位狀態來停用物件。</span><span class="sxs-lookup"><span data-stu-id="27a25-127">COM+ deactivates an object based on the status of the doneness bit on the object context.</span></span> <span data-ttu-id="27a25-128">您的物件可以使用此位來表示在指定的方法呼叫期間，是否已完成（也就是已準備好停用）。</span><span class="sxs-lookup"><span data-stu-id="27a25-128">Your object can use this bit to signal whether it is done—that is, ready to be deactivated—during a given method call.</span></span> <span data-ttu-id="27a25-129">如需詳細資訊，請參閱 [設定完成位](setting-the-done-bit.md)。</span><span class="sxs-lookup"><span data-stu-id="27a25-129">For more information, see [Setting the Done Bit](setting-the-done-bit.md).</span></span>

## <a name="using-the-auto-done-property"></a><span data-ttu-id="27a25-130">使用自動完成屬性</span><span class="sxs-lookup"><span data-stu-id="27a25-130">Using the Auto-Done Property</span></span>

<span data-ttu-id="27a25-131">您可以使用 [元件服務] 系統管理工具來設定方法，使物件在方法傳回時自動停用。</span><span class="sxs-lookup"><span data-stu-id="27a25-131">Using the Component Services administrative tool, you can configure a method such that the object is automatically deactivated on method return.</span></span> <span data-ttu-id="27a25-132"> (如需有關如何設定此屬性的指示，請參閱為 [方法啟用自動完成](enabling-auto-done-for-a-method.md) ) 。您可以選取此選項，在交易中排除重複的方法呼叫來投票。</span><span class="sxs-lookup"><span data-stu-id="27a25-132">(See [Enabling Auto-Done for a Method](enabling-auto-done-for-a-method.md) for instructions about how to set this property.) By selecting this option, you can eliminate the repetitive method calls for voting in transactions.</span></span> <span data-ttu-id="27a25-133">因為一致性位的預設設定為 True，所以如果您也將完成的位變更為 True，而且不採取任何動作來變更這些設定，則在方法傳回之後，會自動呼叫 [**IObjectCoNtext：： SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) 。</span><span class="sxs-lookup"><span data-stu-id="27a25-133">Because the default setting for the consistency bit is True, if you have changed the done bit to True as well and you take no action to change these settings, [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) is called automatically after the method returns.</span></span>

<span data-ttu-id="27a25-134">不過，這種行為有一點要注意： COM + 將檢查方法傳回的 HRESULT。</span><span class="sxs-lookup"><span data-stu-id="27a25-134">However, there is one caveat to this behavior: COM+ will examine the HRESULT that the method returns.</span></span> <span data-ttu-id="27a25-135">如果該 HRESULT 指出失敗，一致性位會設為 False，而結果會與您呼叫 [**IObjectCoNtext：： SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)相同。</span><span class="sxs-lookup"><span data-stu-id="27a25-135">If that HRESULT indicates failure, the consistency bit is set to False and the result is the same as if you had called [**IObjectContext::SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort).</span></span>

<span data-ttu-id="27a25-136">總而言之，如果您針對方法選取 [自動完成]，而不採取任何動作來設定任何位，而且如果系統傳回 HRESULT (hr) ，則適用下列情況：</span><span class="sxs-lookup"><span data-stu-id="27a25-136">To summarize, if you select auto-done for a method and don't take any action to set any bits, and if an HRESULT(hr) is returned, the following applies:</span></span>

-   <span data-ttu-id="27a25-137">如果成功 (hr) ，就如同您呼叫 [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)一樣。</span><span class="sxs-lookup"><span data-stu-id="27a25-137">If SUCCEEDS(hr), it is as though you called [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete).</span></span>
-   <span data-ttu-id="27a25-138">如果 (hr) 失敗，就如同您呼叫 [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)一樣。</span><span class="sxs-lookup"><span data-stu-id="27a25-138">If FAILED(hr), it is as though you called [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort).</span></span>

## <a name="using-iobjectcontrol-to-manage-object-activation-and-deactivation"></a><span data-ttu-id="27a25-139">使用 IObjectControl 管理物件啟用和停用</span><span class="sxs-lookup"><span data-stu-id="27a25-139">Using IObjectControl to Manage Object Activation and Deactivation</span></span>

<span data-ttu-id="27a25-140">您可以執行 [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) 介面，讓 com + 執行時間自動管理物件的停用和重新啟用。</span><span class="sxs-lookup"><span data-stu-id="27a25-140">You can implement the [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) interface so that the COM+ runtime automatically manages deactivation and reactivation for your objects.</span></span> <span data-ttu-id="27a25-141">當物件執行這個介面時，COM + 會在停用物件時呼叫 [**IObjectControl：:D eactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) ，並在重新啟始物件時呼叫 [**IObjectControl：： Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) 。</span><span class="sxs-lookup"><span data-stu-id="27a25-141">When an object implements this interface, COM+ calls [**IObjectControl::Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) when it deactivates the object and [**IObjectControl::Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) when it reactivates it.</span></span> <span data-ttu-id="27a25-142">這些方法會在物件啟用時啟用自動內容初始化，並在停用時清除狀態。</span><span class="sxs-lookup"><span data-stu-id="27a25-142">These methods enable automatic context initialization on object activation and cleanup of state on deactivation.</span></span>

<span data-ttu-id="27a25-143">如果您要共用使用 COM + JIT 啟用的物件，強烈建議您執行 [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol)。</span><span class="sxs-lookup"><span data-stu-id="27a25-143">If you are pooling objects that use COM+ JIT activation, it is highly recommended that you implement [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol).</span></span> <span data-ttu-id="27a25-144">如需詳細資訊，請參閱 [物件共用和 COM + JIT 啟用](object-pooling-and-com--jit-activation.md)。</span><span class="sxs-lookup"><span data-stu-id="27a25-144">For more detail, see [Object Pooling and COM+ JIT Activation](object-pooling-and-com--jit-activation.md).</span></span>

## <a name="statelessness-and-jit-activation"></a><span data-ttu-id="27a25-145">無狀態和 JIT 啟用</span><span class="sxs-lookup"><span data-stu-id="27a25-145">Statelessness and JIT Activation</span></span>

<span data-ttu-id="27a25-146">交易對象一定是無狀態的，因為您無法跨交易界限共用狀態。</span><span class="sxs-lookup"><span data-stu-id="27a25-146">Transactional objects are necessarily stateless because you cannot share state across a transaction boundary.</span></span> <span data-ttu-id="27a25-147">因此，只有當您的物件沒有在停用時遺失的狀態時，才會使用 JIT 啟用;否則，您會違反交易的隔離。</span><span class="sxs-lookup"><span data-stu-id="27a25-147">Therefore, you would use JIT activation only when your object holds no state that would be lost on deactivation; otherwise, you violate the isolation of the transactions.</span></span> <span data-ttu-id="27a25-148">由於交易對象的自然使用模式，它們會執行一些工作單位，並在交易認可或中止時釋出物件，也就是 JIT 啟用和自動交易密切相關。</span><span class="sxs-lookup"><span data-stu-id="27a25-148">Due to the natural use patterns of transactional objects—they do some unit of work and release the object when the transaction commits or aborts—JIT activation and automatic transactions are closely related.</span></span> <span data-ttu-id="27a25-149">將物件設定為需要交易可自動啟用 COM + JIT 啟用。</span><span class="sxs-lookup"><span data-stu-id="27a25-149">Configuring an object to require transactions enables COM+ JIT activation automatically.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27a25-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="27a25-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27a25-151">COM + 即時啟用工作</span><span class="sxs-lookup"><span data-stu-id="27a25-151">COM+ Just-in-Time Activation Tasks</span></span>](com--just-in-time-activation-tasks.md)
</dt> <dt>

[<span data-ttu-id="27a25-152">物件共用和 COM + JIT 啟用</span><span class="sxs-lookup"><span data-stu-id="27a25-152">Object Pooling and COM+ JIT Activation</span></span>](object-pooling-and-com--jit-activation.md)
</dt> <dt>

[<span data-ttu-id="27a25-153">交易和 COM + JIT 啟用</span><span class="sxs-lookup"><span data-stu-id="27a25-153">Transactions and COM+ JIT Activation</span></span>](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



