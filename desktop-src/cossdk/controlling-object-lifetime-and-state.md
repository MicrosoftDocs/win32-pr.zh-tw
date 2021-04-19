---
description: 控制物件存留期和狀態
ms.assetid: 172e07a2-1711-4353-9099-ff9d31a564c6
title: 控制物件存留期和狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525cc1d582d85bc84ef2b1749a427711d1fe26fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972562"
---
# <a name="controlling-object-lifetime-and-state"></a><span data-ttu-id="119c3-103">控制物件存留期和狀態</span><span class="sxs-lookup"><span data-stu-id="119c3-103">Controlling Object Lifetime and State</span></span>

<span data-ttu-id="119c3-104">集區物件可以藉由執行 [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol)來參與 com + 如何管理其集區中的活動。</span><span class="sxs-lookup"><span data-stu-id="119c3-104">A pooled object can participate in how COM+ manages its activity in the pool by implementing [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol).</span></span> <span data-ttu-id="119c3-105">建立集區物件時，會將它匯總成較大的物件，藉由在物件生命週期的一般點上呼叫下列方法來管理物件 **IObjectControl** ：</span><span class="sxs-lookup"><span data-stu-id="119c3-105">When a pooled object is created, it is aggregated into a larger object that will manage the object by calling the following methods on **IObjectControl** at regular points in the object's lifecycle:</span></span>

-   <span data-ttu-id="119c3-106">[**啟用**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)—每當物件傳回至用戶端時呼叫，並在特定內容中啟用。</span><span class="sxs-lookup"><span data-stu-id="119c3-106">[**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)—Called whenever the object is returned to a client, activated in a specific context.</span></span>
-   <span data-ttu-id="119c3-107">[**停用**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate)—每當用戶端釋放物件時呼叫，或在 JIT 啟用物件停用時呼叫。</span><span class="sxs-lookup"><span data-stu-id="119c3-107">[**Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate)—Called whenever an object is released by the client or, in the case of a JIT-activated object, when it is deactivated.</span></span>
-   <span data-ttu-id="119c3-108">[**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)—每次將物件傳回至一般集區時呼叫。</span><span class="sxs-lookup"><span data-stu-id="119c3-108">[**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)—Called whenever an object is to be returned to the general pool.</span></span>

<span data-ttu-id="119c3-109">執行 [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) 是選擇性的，但交易對象除外，其應一律執行 [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) 來監視所持有資源的狀態。</span><span class="sxs-lookup"><span data-stu-id="119c3-109">Implementing [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) is optional, except for transactional objects, which should always implement [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) to monitor the state of the resources they hold.</span></span> <span data-ttu-id="119c3-110">不過，建議您在大部分的情況下執行 **IObjectControl** ，因為它會提供有效的方式來管理集區物件的行為，如下所述。</span><span class="sxs-lookup"><span data-stu-id="119c3-110">However, it is advisable to implement **IObjectControl** in most cases because it provides an efficient way to manage the behavior of a pooled object, as described below.</span></span>

## <a name="performing-context-specific-initialization"></a><span data-ttu-id="119c3-111">正在執行 Context-Specific 初始化</span><span class="sxs-lookup"><span data-stu-id="119c3-111">Performing Context-Specific Initialization</span></span>

<span data-ttu-id="119c3-112">使用「啟動」時，您可以在針對指定用戶端 [**啟動**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)該物件的內容中初始化該物件。</span><span class="sxs-lookup"><span data-stu-id="119c3-112">Using [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate), you can initialize the object in the context in which it is activated for a given client.</span></span> <span data-ttu-id="119c3-113">例如，若要判斷物件是否有交易親和性 (其資源可能已經登錄) ，您可能會取得與內容相關聯的交易識別碼。</span><span class="sxs-lookup"><span data-stu-id="119c3-113">For example, to determine whether the object has transaction affinity (its resources may already be enlisted), you might get the transaction ID associated with the context.</span></span>

<span data-ttu-id="119c3-114">一般來說，您會使用 [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)來執行在物件所公開之任何方法之間一致的初始化，將它視為物件之函式的內容特定部分。</span><span class="sxs-lookup"><span data-stu-id="119c3-114">Typically you would use [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)to perform initialization that is consistent across any methods exposed by the object, treating it as the context-specific portion of the object's constructor.</span></span>

## <a name="cleaning-up-any-client-state"></a><span data-ttu-id="119c3-115">清除任何用戶端狀態</span><span class="sxs-lookup"><span data-stu-id="119c3-115">Cleaning Up Any Client State</span></span>

<span data-ttu-id="119c3-116">使用「 [**停用**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate)」時，您可以擺脫可能存在的任何用戶端特定狀態，讓您的物件以完全一般的狀態回到集區，並可供任何用戶端使用，而不會危及安全性或隔離。</span><span class="sxs-lookup"><span data-stu-id="119c3-116">Using [**Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate), you can get rid of any client-specific state that might exist so that your object returns to the pool in a completely generic state and can then be used by any client without compromising security or isolation.</span></span>

## <a name="controlling-reuse-of-the-object"></a><span data-ttu-id="119c3-117">控制物件重複使用</span><span class="sxs-lookup"><span data-stu-id="119c3-117">Controlling Reuse of the Object</span></span>

<span data-ttu-id="119c3-118">您可以使用 [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)來監視物件的內部狀態，並報告其是否適合重複使用。</span><span class="sxs-lookup"><span data-stu-id="119c3-118">Using [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled), you can monitor the internal state of your object and report on whether it is fit for its reuse.</span></span> <span data-ttu-id="119c3-119">如果 **CanBePooled** 傳回 True 且未達到集區最大值，則會將物件放回一般集區中。</span><span class="sxs-lookup"><span data-stu-id="119c3-119">If **CanBePooled** returns True and the pool maximum has not been reached, the object is placed back in the general pool.</span></span> <span data-ttu-id="119c3-120">如果 **CanBePooled** 傳回 False，則會捨棄物件。</span><span class="sxs-lookup"><span data-stu-id="119c3-120">If **CanBePooled** returns False, the object is discarded.</span></span> <span data-ttu-id="119c3-121">在交易式元件的案例中，傳回 False 將會毀滅目前的交易。</span><span class="sxs-lookup"><span data-stu-id="119c3-121">In the case of transactional components, returning False will doom the current transaction.</span></span>

<span data-ttu-id="119c3-122">一般而言，您會保留物件的一些全域資料成員，如果您偵測到連接不正確，或某個資源的狀態不正確，請設定此項以反映目前的狀況，並透過 [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)傳回。</span><span class="sxs-lookup"><span data-stu-id="119c3-122">Typically, you would keep some global data member for the object, and if you detect a connection to be bad or a resource of some kind to be in a bad state, set this to reflect the current situation and return it through [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).</span></span>

<span data-ttu-id="119c3-123">如果物件不會執行 [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)，則會繼續重複使用實例，直到達到集區最大層級為止。</span><span class="sxs-lookup"><span data-stu-id="119c3-123">If an object does not implement [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled), instances will continue to be reused until the pool maximum level is reached.</span></span>

## <a name="related-topics"></a><span data-ttu-id="119c3-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="119c3-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="119c3-125">COM + 物件的函式字串</span><span class="sxs-lookup"><span data-stu-id="119c3-125">COM+ Object Constructor Strings</span></span>](com--object-constructor-strings.md)
</dt> <dt>

[<span data-ttu-id="119c3-126">物件共用的運作方式</span><span class="sxs-lookup"><span data-stu-id="119c3-126">How Object Pooling Works</span></span>](how-object-pooling-works.md)
</dt> <dt>

[<span data-ttu-id="119c3-127">使用物件共用改善效能</span><span class="sxs-lookup"><span data-stu-id="119c3-127">Improving Performance with Object Pooling</span></span>](improving-performance-with-object-pooling.md)
</dt> <dt>

[<span data-ttu-id="119c3-128">共用交易對象</span><span class="sxs-lookup"><span data-stu-id="119c3-128">Pooling Transactional Objects</span></span>](pooling-transactional-objects.md)
</dt> <dt>

[<span data-ttu-id="119c3-129">共用物件的需求</span><span class="sxs-lookup"><span data-stu-id="119c3-129">Requirements for Poolable Objects</span></span>](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



