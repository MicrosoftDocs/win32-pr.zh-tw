---
description: 當您設定要共用的元件時，COM + 會在集區中維護其實例，並準備好針對任何要求元件的用戶端啟用。 任何物件建立要求都會透過集區管理員來處理。
ms.assetid: 34978b50-cd20-42fd-ad46-410190478ef8
title: 物件共用的運作方式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f78784fc0e5362c14ceb598b404976c6ca494a19
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973578"
---
# <a name="how-object-pooling-works"></a><span data-ttu-id="3c1d7-104">物件共用的運作方式</span><span class="sxs-lookup"><span data-stu-id="3c1d7-104">How Object Pooling Works</span></span>

<span data-ttu-id="3c1d7-105">當您設定要共用的元件時，COM + 會在集區中維護其實例，並準備好針對任何要求元件的用戶端啟用。</span><span class="sxs-lookup"><span data-stu-id="3c1d7-105">When you configure a component to be pooled, COM+ will maintain instances of it in a pool, ready to be activated for any client requesting the component.</span></span> <span data-ttu-id="3c1d7-106">任何物件建立要求都會透過集區管理員來處理。</span><span class="sxs-lookup"><span data-stu-id="3c1d7-106">Any object creation requests will be handled through the pool manager.</span></span>

<span data-ttu-id="3c1d7-107">集區會以每個元件為基礎進行設定和維護。</span><span class="sxs-lookup"><span data-stu-id="3c1d7-107">Pools are configured and maintained on a per-component basis.</span></span> <span data-ttu-id="3c1d7-108">集區是由共用相同 CLSID 的同質物件所組成。</span><span class="sxs-lookup"><span data-stu-id="3c1d7-108">A pool consists of homogeneous objects that share the same CLSID.</span></span> <span data-ttu-id="3c1d7-109">唯一的例外是交易對象，其 subpools 會在交易暫止時，維護包含具有交易親和性之物件的物件。</span><span class="sxs-lookup"><span data-stu-id="3c1d7-109">The only exception is for transactional objects, for which subpools are maintained containing objects that have transaction affinity while a transaction is pending.</span></span>

<span data-ttu-id="3c1d7-110">當應用程式啟動時，只要物件建立成功，集區就會填入您所指定的最低層級。</span><span class="sxs-lookup"><span data-stu-id="3c1d7-110">When the application starts, the pool will be populated up to the minimum level that you have administratively specified, as long as object creation succeeds.</span></span> <span data-ttu-id="3c1d7-111">當元件的用戶端要求進入時，就會從集區以 first 優先的基礎來滿足這些要求。</span><span class="sxs-lookup"><span data-stu-id="3c1d7-111">As client requests for the component come in, they are satisfied on a first-come first-served basis from the pool.</span></span> <span data-ttu-id="3c1d7-112">如果沒有可用的集區物件，且集區尚未達到指定的最大層級，就會為用戶端建立和啟用新的物件。</span><span class="sxs-lookup"><span data-stu-id="3c1d7-112">If no pooled objects are available and the pool is not yet at its specified maximum level, a new object is created and activated for the client.</span></span>

<span data-ttu-id="3c1d7-113">當集區達到其最大等級時，用戶端要求會排入佇列，並接收來自集區的第一個可用物件。</span><span class="sxs-lookup"><span data-stu-id="3c1d7-113">When the pool reaches its maximum level, client requests are queued and will receive the first available object from the pool.</span></span> <span data-ttu-id="3c1d7-114">物件數目（包括已啟用和已停用）永遠不會超過最大的集區值。</span><span class="sxs-lookup"><span data-stu-id="3c1d7-114">The number of objects, including both activated and deactivated, will never exceed the maximum pool value.</span></span> <span data-ttu-id="3c1d7-115">物件建立要求會在系統管理員指定的期間之後過期，讓您可以控制用戶端等候物件建立的時間長度。</span><span class="sxs-lookup"><span data-stu-id="3c1d7-115">Object creation requests will time out after an administratively specified period so that you can control how long clients will wait for object creation.</span></span> <span data-ttu-id="3c1d7-116">發生逾時錯誤時，用戶端會 \_ 從 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)取回錯誤 E TIMEOUT。</span><span class="sxs-lookup"><span data-stu-id="3c1d7-116">Upon a time-out failure, the client will get back the error E\_TIMEOUT from [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="3c1d7-117">在可能的情況下，COM + 會在用戶端釋放之後，嘗試重複使用物件，直到集區達到其最大層級為止。</span><span class="sxs-lookup"><span data-stu-id="3c1d7-117">Whenever possible, COM+ will attempt to reuse an object after a client releases it, until the pool reaches its maximum level.</span></span> <span data-ttu-id="3c1d7-118">物件負責監視其狀態，以判斷它是否可以重複使用，並應該針對 [**IObjectControl：： CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)傳回適當的值。</span><span class="sxs-lookup"><span data-stu-id="3c1d7-118">The object is responsible for monitoring its state to determine whether it can be reused and should return an appropriate value for [**IObjectControl::CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).</span></span>

<span data-ttu-id="3c1d7-119">建立集區物件時，會將它匯總成較大的物件，以管理物件的存留期。</span><span class="sxs-lookup"><span data-stu-id="3c1d7-119">When a pooled object is created, it is aggregated into a larger object that will manage the object's lifetime.</span></span> <span data-ttu-id="3c1d7-120">外部物件會在物件的生命週期中，于適當的時間呼叫 [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) 的方法，如下所示：</span><span class="sxs-lookup"><span data-stu-id="3c1d7-120">The outer object calls methods on [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) at appropriate times in the object's life cycle, as follows:</span></span>

-   <span data-ttu-id="3c1d7-121">每當物件傳回給用戶端時，就會呼叫 [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) 方法，而該物件會在特定內容中啟用。</span><span class="sxs-lookup"><span data-stu-id="3c1d7-121">The [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) method is called whenever the object is returned to a client, activated in a specific context.</span></span>
-   <span data-ttu-id="3c1d7-122">只要用戶端釋出物件，或在 JIT 啟動的物件停用時，就會呼叫 [**停用**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) 方法。</span><span class="sxs-lookup"><span data-stu-id="3c1d7-122">The [**Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) method is called whenever an object is released by the client or, in the case of a JIT-activated object, when it is deactivated.</span></span>
-   <span data-ttu-id="3c1d7-123">只要將物件傳回至一般集區，就會呼叫 [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) 方法。</span><span class="sxs-lookup"><span data-stu-id="3c1d7-123">The [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) method is called whenever an object is to be returned to the general pool.</span></span> <span data-ttu-id="3c1d7-124">如果物件偵測到某些可重複使用的資源處於不正常的狀態，它應該會針對此方法傳回 **FALSE** ，而集區管理員會捨棄物件。</span><span class="sxs-lookup"><span data-stu-id="3c1d7-124">If the object detects that some reusable resource is in a bad state, it should return **FALSE** for this method and the pool manager will discard the object.</span></span>

<span data-ttu-id="3c1d7-125">物件不一定需要執行 [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol)。</span><span class="sxs-lookup"><span data-stu-id="3c1d7-125">An object does not necessarily need to implement [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol).</span></span> <span data-ttu-id="3c1d7-126">如果不是，則會一律重複使用實例，直到達到集區的最大層級為止。</span><span class="sxs-lookup"><span data-stu-id="3c1d7-126">If it does not, instances will always be reused, until the pool maximum level is reached.</span></span>

<span data-ttu-id="3c1d7-127">如需有關如何設定要共用之元件的詳細資訊，請參閱設定 [要共用的元件](configuring-a-component-to-be-pooled.md)。</span><span class="sxs-lookup"><span data-stu-id="3c1d7-127">For details about how to configure components to be pooled, see [Configuring a Component to Be Pooled](configuring-a-component-to-be-pooled.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c1d7-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="3c1d7-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c1d7-129">COM + 物件的函式字串</span><span class="sxs-lookup"><span data-stu-id="3c1d7-129">COM+ Object Constructor Strings</span></span>](com--object-constructor-strings.md)
</dt> <dt>

[<span data-ttu-id="3c1d7-130">控制物件存留期和狀態</span><span class="sxs-lookup"><span data-stu-id="3c1d7-130">Controlling Object Lifetime and State</span></span>](controlling-object-lifetime-and-state.md)
</dt> <dt>

[<span data-ttu-id="3c1d7-131">使用物件共用改善效能</span><span class="sxs-lookup"><span data-stu-id="3c1d7-131">Improving Performance with Object Pooling</span></span>](improving-performance-with-object-pooling.md)
</dt> <dt>

[<span data-ttu-id="3c1d7-132">共用交易對象</span><span class="sxs-lookup"><span data-stu-id="3c1d7-132">Pooling Transactional Objects</span></span>](pooling-transactional-objects.md)
</dt> <dt>

[<span data-ttu-id="3c1d7-133">共用物件的需求</span><span class="sxs-lookup"><span data-stu-id="3c1d7-133">Requirements for Poolable Objects</span></span>](requirements-for-poolable-objects.md)
</dt> </dl>

 

 
