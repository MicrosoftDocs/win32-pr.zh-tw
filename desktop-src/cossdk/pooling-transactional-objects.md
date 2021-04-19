---
description: 要共用的交易元件具有特殊需求。
ms.assetid: 32e2f830-c30a-4dbc-8e69-dd2038851998
title: 共用交易對象
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 006ba32ad2ac550be4fa4418dde322ded26c64c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972971"
---
# <a name="pooling-transactional-objects"></a><span data-ttu-id="fff64-103">共用交易對象</span><span class="sxs-lookup"><span data-stu-id="fff64-103">Pooling Transactional Objects</span></span>

<span data-ttu-id="fff64-104">要共用的交易元件具有特殊需求。</span><span class="sxs-lookup"><span data-stu-id="fff64-104">Transactional components that are to be pooled have special requirements.</span></span>

## <a name="manually-enlisting-resources"></a><span data-ttu-id="fff64-105">手動登記資源</span><span class="sxs-lookup"><span data-stu-id="fff64-105">Manually Enlisting Resources</span></span>

<span data-ttu-id="fff64-106">參與交易的共用物件必須手動登錄 managed 資源。</span><span class="sxs-lookup"><span data-stu-id="fff64-106">Poolable objects that participate in transactions must manually enlist managed resources.</span></span> <span data-ttu-id="fff64-107">如果物件在用戶端之間保有受控資源，當物件在指定的內容中啟動時，資源管理員將無法自動在交易中登記。</span><span class="sxs-lookup"><span data-stu-id="fff64-107">If an object holds managed resources between clients, there will be no way for the resource manager to automatically enlist in a transaction when the object is activated in a given context.</span></span>

<span data-ttu-id="fff64-108">物件本身必須處理偵測交易的邏輯，關閉 resource manager 的自動登記，並手動登錄其保留的任何資源。</span><span class="sxs-lookup"><span data-stu-id="fff64-108">The object itself must handle the logic of detecting the transaction, turning off the resource manager's auto-enlistment, and manually enlisting any resources that it holds.</span></span> <span data-ttu-id="fff64-109">執行此操作的步驟是您所使用的資源管理員專用的步驟。</span><span class="sxs-lookup"><span data-stu-id="fff64-109">The steps for doing this are specific to the resource manager that you are using.</span></span> <span data-ttu-id="fff64-110">如果您需要手動登記，請參閱資源管理員的說明文件。</span><span class="sxs-lookup"><span data-stu-id="fff64-110">If you need to do manual enlistment, consult the documentation for your resource manager.</span></span>

<span data-ttu-id="fff64-111">如下所述，當交易在使用中時，物件可以與交易親和性共用，如果是由與該交易相關聯的用戶端呼叫，則可以使用交易親和性來啟用。</span><span class="sxs-lookup"><span data-stu-id="fff64-111">As described below, objects can be pooled with transaction affinity while a transaction is active and can be activated with transaction affinity if called by a client associated with that transaction.</span></span> <span data-ttu-id="fff64-112">在登記資源之前，您應該先檢查交易親和性。</span><span class="sxs-lookup"><span data-stu-id="fff64-112">Before enlisting resources, you should first check for transaction affinity.</span></span> <span data-ttu-id="fff64-113">如果物件是取自該交易專屬的集區，它已經在該交易中完成工作並登記其資源。</span><span class="sxs-lookup"><span data-stu-id="fff64-113">If the object has been taken from the pool specific to that transaction, it has already done work in that transaction and enlisted its resources.</span></span>

## <a name="turning-off-automatic-enlistment"></a><span data-ttu-id="fff64-114">關閉自動登記</span><span class="sxs-lookup"><span data-stu-id="fff64-114">Turning Off Automatic Enlistment</span></span>

<span data-ttu-id="fff64-115">在取得資源之後，應關閉自動登記，通常是在物件的函式中。</span><span class="sxs-lookup"><span data-stu-id="fff64-115">Automatic enlistment should be turned off after the resource is acquired, usually in the object's constructor.</span></span> <span data-ttu-id="fff64-116">也就是說，您會停用自動登記，然後連接。</span><span class="sxs-lookup"><span data-stu-id="fff64-116">That is, you disable automatic enlistment and then connect.</span></span>

<span data-ttu-id="fff64-117">停用自動登記有時可能是微妙的程式，特別是在分層資料存取提供者的情況下。</span><span class="sxs-lookup"><span data-stu-id="fff64-117">Disabling auto-enlistment can sometimes be a subtle procedure, particularly in the case of layered data access providers.</span></span> <span data-ttu-id="fff64-118">自動登記有時會與連接共用（如同 ODBC）結合，有時也不會與 OLE DB 一樣。</span><span class="sxs-lookup"><span data-stu-id="fff64-118">Auto-enlistment is sometimes coupled with connection pooling, as with ODBC, and sometimes not, as with OLE DB.</span></span> <span data-ttu-id="fff64-119">您可能需要確定已在數個層級的提供者上關閉自動登記。</span><span class="sxs-lookup"><span data-stu-id="fff64-119">You might need to ensure that auto-enlistment is off at several levels of providers.</span></span>

## <a name="implementing-iobjectcontrol"></a><span data-ttu-id="fff64-120">執行 IObjectControl</span><span class="sxs-lookup"><span data-stu-id="fff64-120">Implementing IObjectControl</span></span>

<span data-ttu-id="fff64-121">參與交易的共用物件必須監視其所持有之資源的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="fff64-121">Poolable objects that participate in transactions must monitor the current state of resources they are holding.</span></span> <span data-ttu-id="fff64-122">如果物件偵測到它處於無法重複使用的狀態（例如，如果連接不正確），則 [**IObjectControl：： CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)會傳回 False。</span><span class="sxs-lookup"><span data-stu-id="fff64-122">If the object detects that it is in a non-reusable state—for example, if a connection is bad—it should return False for [**IObjectControl::CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).</span></span> <span data-ttu-id="fff64-123">這將會影響捨棄物件實例，並毀滅交易目前的交易。</span><span class="sxs-lookup"><span data-stu-id="fff64-123">This will have the effect of both discarding the object instance and dooming the current transaction.</span></span>

## <a name="transaction-specific-pools"></a><span data-ttu-id="fff64-124">Transaction-Specific 集區</span><span class="sxs-lookup"><span data-stu-id="fff64-124">Transaction-Specific Pools</span></span>

<span data-ttu-id="fff64-125">物件的集區通常是同質的，且目前未使用的任何集區物件都適合傳回任何用戶端。</span><span class="sxs-lookup"><span data-stu-id="fff64-125">A pool of objects is generally homogenous, and any pooled object not currently in use is good to return to any client.</span></span> <span data-ttu-id="fff64-126">這項規則唯一的例外狀況是交易對象，其物件共用已優化。</span><span class="sxs-lookup"><span data-stu-id="fff64-126">The only exception to this rule is in the case of transactional objects, for which object pooling is optimized.</span></span> <span data-ttu-id="fff64-127">當要求物件的用戶端有相關聯的交易時，COM + 會掃描集區中是否有已與該交易相關聯的可用物件。</span><span class="sxs-lookup"><span data-stu-id="fff64-127">When the client requesting an object has an associated transaction, COM+ will scan the pool for an available object that is already associated with that transaction.</span></span> <span data-ttu-id="fff64-128">如果找到具有交易親和性的物件，則會傳回給用戶端;否則，會傳回來自一般集區的物件。</span><span class="sxs-lookup"><span data-stu-id="fff64-128">If an object with transaction affinity is found, it is returned to the client; otherwise, an object from the general pool is returned.</span></span>

<span data-ttu-id="fff64-129">如此一來，就會保留特殊的 subpools，包含具有特定交易親和性的物件。</span><span class="sxs-lookup"><span data-stu-id="fff64-129">In this manner, special subpools are maintained containing objects with affinity for a particular transaction.</span></span> <span data-ttu-id="fff64-130">當交易認可或中止時，這些物件會傳回至沒有交易親和性的一般集區，可供任何用戶端使用。</span><span class="sxs-lookup"><span data-stu-id="fff64-130">When the transaction commits or aborts, these objects are returned to the general pool with no transaction affinity, ready to be used by any client.</span></span>

<span data-ttu-id="fff64-131">基於這個理由，當您的元件以手動方式在交易中登記其受控資源時，應該先查看是否已登錄。</span><span class="sxs-lookup"><span data-stu-id="fff64-131">For this reason, when your component manually enlists its managed resources in a transaction, it should first check to see whether they are already enlisted.</span></span> <span data-ttu-id="fff64-132">若是如此，就不需要登記。</span><span class="sxs-lookup"><span data-stu-id="fff64-132">If so, there is no need to enlist.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fff64-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="fff64-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fff64-134">COM + 物件的函式字串</span><span class="sxs-lookup"><span data-stu-id="fff64-134">COM+ Object Constructor Strings</span></span>](com--object-constructor-strings.md)
</dt> <dt>

[<span data-ttu-id="fff64-135">控制物件存留期和狀態</span><span class="sxs-lookup"><span data-stu-id="fff64-135">Controlling Object Lifetime and State</span></span>](controlling-object-lifetime-and-state.md)
</dt> <dt>

[<span data-ttu-id="fff64-136">物件共用的運作方式</span><span class="sxs-lookup"><span data-stu-id="fff64-136">How Object Pooling Works</span></span>](how-object-pooling-works.md)
</dt> <dt>

[<span data-ttu-id="fff64-137">使用物件共用改善效能</span><span class="sxs-lookup"><span data-stu-id="fff64-137">Improving Performance with Object Pooling</span></span>](improving-performance-with-object-pooling.md)
</dt> <dt>

[<span data-ttu-id="fff64-138">共用物件的需求</span><span class="sxs-lookup"><span data-stu-id="fff64-138">Requirements for Poolable Objects</span></span>](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



