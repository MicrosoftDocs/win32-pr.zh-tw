---
description: 共用物件必須符合特定需求，才能讓多個用戶端使用單一物件實例。
ms.assetid: 2cd4211e-be12-4197-8b43-5cb9f2321016
title: 共用物件的需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78d6834210f180ad8b514b51b6926b5cd30714fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936262"
---
# <a name="requirements-for-poolable-objects"></a><span data-ttu-id="7f45a-103">共用物件的需求</span><span class="sxs-lookup"><span data-stu-id="7f45a-103">Requirements for Poolable Objects</span></span>

<span data-ttu-id="7f45a-104">共用物件必須符合特定需求，才能讓多個用戶端使用單一物件實例。</span><span class="sxs-lookup"><span data-stu-id="7f45a-104">Poolable objects must meet certain requirements to enable a single object instance to be used by multiple clients.</span></span>

## <a name="stateless"></a><span data-ttu-id="7f45a-105">無狀態</span><span class="sxs-lookup"><span data-stu-id="7f45a-105">Stateless</span></span>

<span data-ttu-id="7f45a-106">為了維護安全性、一致性和隔離，共用物件應該不會將用戶端特定的狀態從用戶端保留給用戶端。</span><span class="sxs-lookup"><span data-stu-id="7f45a-106">To maintain security, consistency, and isolation, poolable objects should hold no client-specific state from client to client.</span></span> <span data-ttu-id="7f45a-107">您可以使用 [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol)來管理任何每個用戶端狀態，使用 [**IObjectControl：： Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) 執行內容特定的初始化，並使用 [**IObjectControl：:D eactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate)來清除任何用戶端狀態。</span><span class="sxs-lookup"><span data-stu-id="7f45a-107">You can manage any per-client state by using [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol), performing context-specific initialization with [**IObjectControl::Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) and cleaning up any client state with [**IObjectControl::Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate).</span></span> <span data-ttu-id="7f45a-108">如需詳細資訊，請參閱 [控制物件存留期和狀態](controlling-object-lifetime-and-state.md)。</span><span class="sxs-lookup"><span data-stu-id="7f45a-108">For more detail, see [Controlling Object Lifetime and State](controlling-object-lifetime-and-state.md).</span></span>

## <a name="no-thread-affinity"></a><span data-ttu-id="7f45a-109">無線程親和性</span><span class="sxs-lookup"><span data-stu-id="7f45a-109">No Thread Affinity</span></span>

<span data-ttu-id="7f45a-110">共用物件無法系結至特定的執行緒;否則，效能可能會造成災難性的後果。</span><span class="sxs-lookup"><span data-stu-id="7f45a-110">Poolable objects cannot be bound to a particular thread; otherwise, performance could be potentially disastrous.</span></span> <span data-ttu-id="7f45a-111">基於這個理由，共用物件不能標示為在單元模型中執行;它們必須在多執行緒單元或中立的單元中執行。</span><span class="sxs-lookup"><span data-stu-id="7f45a-111">For this reason, poolable objects cannot be marked to run in the apartment model; they must run in the multithreaded apartment or the neutral apartment.</span></span> <span data-ttu-id="7f45a-112">此外，共用物件不應該使用執行緒區域儲存區，也不應該匯總無限制執行緒封送處理器。</span><span class="sxs-lookup"><span data-stu-id="7f45a-112">In addition, poolable objects should not use thread local storage nor should they aggregate the free-threaded marshaler.</span></span> <span data-ttu-id="7f45a-113">如需 COM + 中線程的詳細資訊，請參閱 [Com + 執行緒模型](com--threading-models.md)。</span><span class="sxs-lookup"><span data-stu-id="7f45a-113">For more detail about threading in COM+, see [COM+ Threading Models](com--threading-models.md).</span></span>

> [!Note]  
> <span data-ttu-id="7f45a-114">Microsoft Visual Basic 6.0 及更早版本的開發環境只能建立單元模型元件。</span><span class="sxs-lookup"><span data-stu-id="7f45a-114">The Microsoft Visual Basic 6.0 and earlier development environments can create only apartment model components.</span></span> <span data-ttu-id="7f45a-115">不過，在 Visual Basic .NET 中，可以將元件共用。</span><span class="sxs-lookup"><span data-stu-id="7f45a-115">However, in Visual Basic .NET, components can be pooled.</span></span>

 

## <a name="aggregatable"></a><span data-ttu-id="7f45a-116">可彙總</span><span class="sxs-lookup"><span data-stu-id="7f45a-116">Aggregatable</span></span>

<span data-ttu-id="7f45a-117">共用物件必須支援匯總，也就是，它們必須支援使用非 Null 的 *pUnkOuter* 引數叫用 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)來建立。</span><span class="sxs-lookup"><span data-stu-id="7f45a-117">Poolable objects must support aggregation—that is, they must support being created by invoking [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) with a non-NULL *pUnkOuter* argument.</span></span> <span data-ttu-id="7f45a-118">當 COM + 啟動集區物件時，它會建立匯總來管理集區物件的存留期，並在 [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol)上呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="7f45a-118">When COM+ activates a pooled object, it creates an aggregate to manage the lifetime of the pooled object and to call methods on [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol).</span></span> <span data-ttu-id="7f45a-119">如需有關撰寫可匯總物件的詳細資訊，請參閱 [匯總](/windows/desktop/com/aggregation)。</span><span class="sxs-lookup"><span data-stu-id="7f45a-119">For details on writing aggregatable objects, see [Aggregation](/windows/desktop/com/aggregation).</span></span>

## <a name="transactional-components"></a><span data-ttu-id="7f45a-120">交易元件</span><span class="sxs-lookup"><span data-stu-id="7f45a-120">Transactional Components</span></span>

<span data-ttu-id="7f45a-121">參與交易的共用物件必須手動登錄 managed 資源。</span><span class="sxs-lookup"><span data-stu-id="7f45a-121">Poolable objects that participate in transactions must manually enlist managed resources.</span></span> <span data-ttu-id="7f45a-122">在共用時，如果您的物件持有受控資源（例如資料庫連線），則當物件在指定的內容中啟動時，資源管理員將無法自動在交易中登記。</span><span class="sxs-lookup"><span data-stu-id="7f45a-122">While it is pooled, if your object holds a managed resource such as a database connection, there will be no way for the resource manager to automatically enlist in a transaction when the object is activated in given context.</span></span> <span data-ttu-id="7f45a-123">因此，物件本身必須處理偵測交易的邏輯，關閉 resource manager 的自動登記，並手動登錄其保留的任何資源。</span><span class="sxs-lookup"><span data-stu-id="7f45a-123">Therefore, the object itself must handle the logic of detecting the transaction, turning off the resource manager's auto-enlistment and manually enlisting any resources that it holds.</span></span> <span data-ttu-id="7f45a-124">此外，交易式集區物件應該會在 [**IObjectControl：： CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)的參數值中反映其資源的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="7f45a-124">In addition, a transactional pooled object should reflect the current state of its resources in the parameter values of [**IObjectControl::CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).</span></span> <span data-ttu-id="7f45a-125">如需詳細資訊，請參閱共用 [交易對象](pooling-transactional-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="7f45a-125">For more detail, see [Pooling Transactional Objects](pooling-transactional-objects.md).</span></span>

## <a name="implement-iobjectcontrol-to-manage-the-object-lifetime"></a><span data-ttu-id="7f45a-126">執行 IObjectControl 以管理物件存留期</span><span class="sxs-lookup"><span data-stu-id="7f45a-126">Implement IObjectControl to Manage the Object Lifetime</span></span>

<span data-ttu-id="7f45a-127">雖然並非絕對必要，但共用物件仍應執行 [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol)。</span><span class="sxs-lookup"><span data-stu-id="7f45a-127">Poolable objects should implement [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol), although it is not strictly necessary to do so.</span></span> <span data-ttu-id="7f45a-128">但是，共用的交易元件必須執行 **IObjectControl**。</span><span class="sxs-lookup"><span data-stu-id="7f45a-128">Transactional components that are pooled, however, must implement **IObjectControl**.</span></span> <span data-ttu-id="7f45a-129">這些元件應該監視所持有資源的狀態，並指出無法重複使用的時間;當 [**IObjectControl：： CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) 傳回 false 時，它會毀滅交易。</span><span class="sxs-lookup"><span data-stu-id="7f45a-129">These components should monitor the state of the resources they hold and indicate when they can't be reused; when [**IObjectControl::CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) returns false, it will doom a transaction.</span></span> <span data-ttu-id="7f45a-130">如需詳細資訊，請參閱 [控制物件存留期和狀態](controlling-object-lifetime-and-state.md)。</span><span class="sxs-lookup"><span data-stu-id="7f45a-130">For more detail, see [Controlling Object Lifetime and State](controlling-object-lifetime-and-state.md).</span></span>

## <a name="language-restrictions"></a><span data-ttu-id="7f45a-131">語言限制</span><span class="sxs-lookup"><span data-stu-id="7f45a-131">Language Restrictions</span></span>

<span data-ttu-id="7f45a-132">使用 Microsoft Visual Basic 6.0 及更早版本所開發的元件無法進行集區，因為這些元件將會是單元模型執行緒。</span><span class="sxs-lookup"><span data-stu-id="7f45a-132">Components developed using Microsoft Visual Basic 6.0 and earlier cannot be pooled because these components will be apartment-model threaded.</span></span> <span data-ttu-id="7f45a-133">不過，在 Visual Basic .NET 中，可以將元件共用。</span><span class="sxs-lookup"><span data-stu-id="7f45a-133">However, in Visual Basic .NET, components can be pooled.</span></span>

## <a name="legacy-components"></a><span data-ttu-id="7f45a-134">傳統元件</span><span class="sxs-lookup"><span data-stu-id="7f45a-134">Legacy Components</span></span>

<span data-ttu-id="7f45a-135">只要它們為非交易式且符合適當的先前需求，即使元件並未特別以共用功能寫入，也可以共用。</span><span class="sxs-lookup"><span data-stu-id="7f45a-135">As long as they are non-transactional and conform to the appropriate preceding requirements, components can be pooled even if they were not specifically written with pooling capability in mind.</span></span> <span data-ttu-id="7f45a-136">不需要執行 [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol);沒有這麼做的元件，就不會參與管理其存留期。</span><span class="sxs-lookup"><span data-stu-id="7f45a-136">It is not necessary to implement [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol); a component that does not do so simply won't participate in managing its lifetime.</span></span> <span data-ttu-id="7f45a-137">如果未執行 [**IObjectControl：： CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) ，則會繼續重複使用物件，直到集區並達到大小上限為止。</span><span class="sxs-lookup"><span data-stu-id="7f45a-137">If [**IObjectControl::CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) is not implemented, the object will continue to be reused until the pool attains maximum size.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f45a-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="7f45a-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f45a-139">COM + 物件的函式字串</span><span class="sxs-lookup"><span data-stu-id="7f45a-139">COM+ Object Constructor Strings</span></span>](com--object-constructor-strings.md)
</dt> <dt>

[<span data-ttu-id="7f45a-140">控制物件存留期和狀態</span><span class="sxs-lookup"><span data-stu-id="7f45a-140">Controlling Object Lifetime and State</span></span>](controlling-object-lifetime-and-state.md)
</dt> <dt>

[<span data-ttu-id="7f45a-141">物件共用的運作方式</span><span class="sxs-lookup"><span data-stu-id="7f45a-141">How Object Pooling Works</span></span>](how-object-pooling-works.md)
</dt> <dt>

[<span data-ttu-id="7f45a-142">使用物件共用改善效能</span><span class="sxs-lookup"><span data-stu-id="7f45a-142">Improving Performance with Object Pooling</span></span>](improving-performance-with-object-pooling.md)
</dt> <dt>

[<span data-ttu-id="7f45a-143">共用交易對象</span><span class="sxs-lookup"><span data-stu-id="7f45a-143">Pooling Transactional Objects</span></span>](pooling-transactional-objects.md)
</dt> </dl>

 

 
