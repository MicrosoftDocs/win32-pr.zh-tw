---
description: 交易內的 COM + 管理作業
ms.assetid: 832f2e6d-26ff-416e-a92e-ebaa33d4e7e5
title: 交易內的 COM + 管理作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21612ffec1b9f082dc6a91861882a71f18fb07be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689224"
---
# <a name="com-administration-operations-within-transactions"></a><span data-ttu-id="26f39-103">交易內的 COM + 管理作業</span><span class="sxs-lookup"><span data-stu-id="26f39-103">COM+ Administration Operations Within Transactions</span></span>

<span data-ttu-id="26f39-104">COM + 註冊資料庫 (RegDB) 是可參與 COM + 交易的交易式資源管理員。</span><span class="sxs-lookup"><span data-stu-id="26f39-104">The COM+ registration database (RegDB) is a transacted resource manager that can participate in COM+ transactions.</span></span> <span data-ttu-id="26f39-105">這可讓您在交易內執行管理作業，並將所有設定變更認可或中止為不可部分完成的作業，即使是在多部電腦上也一樣。</span><span class="sxs-lookup"><span data-stu-id="26f39-105">This enables you to perform administration operations within a transaction and have all configuration changes committed or aborted as an atomic operation, even across multiple computers.</span></span> <span data-ttu-id="26f39-106">在某些情況下，執行這項作業可能會很有説明，雖然您應該將隔離和封鎖的行為納入考慮，而且在交易內執行管理工作，也不會對一般管理程式設計模型造成些許變更。</span><span class="sxs-lookup"><span data-stu-id="26f39-106">In some circumstances, it can be very beneficial to do this, although there is isolation and blocking behavior that you should take into account, and performing administration tasks within transactions does involve slight changes to the normal administration programming model.</span></span>

## <a name="benefits-of-doing-administration-operations-within-transactions"></a><span data-ttu-id="26f39-107">在交易內執行管理作業的優點</span><span class="sxs-lookup"><span data-stu-id="26f39-107">Benefits of Doing Administration Operations Within Transactions</span></span>

-   <span data-ttu-id="26f39-108">**資料的一致性：** 在交易內執行的系統管理作業會以整體方式認可或中止，雖然有些非交易式 COM + 類別目錄資源可能不是這種情況。</span><span class="sxs-lookup"><span data-stu-id="26f39-108">**Consistency of data—** Administration operations performed within a transaction are committed or aborted as a whole, although there are some non-transactional COM+ catalog resources for which this may not be the case.</span></span> <span data-ttu-id="26f39-109"> (請參閱下方的非交易式 COM + 類別目錄資源。 ) </span><span class="sxs-lookup"><span data-stu-id="26f39-109">(See Non-Transactional COM+ Catalog Resources below.)</span></span>
-   <span data-ttu-id="26f39-110">**跨多部電腦進行一致的部署—** 如果您要在多部伺服器上部署 COM + 應用程式，可以確保所有伺服器都保留相同的設定。</span><span class="sxs-lookup"><span data-stu-id="26f39-110">**Consistent deployment across multiple machines—** If you are deploying COM+ applications across multiple servers, you can guarantee that all servers are left with identical configurations.</span></span>
-   <span data-ttu-id="26f39-111">**調整規模和效能—** 當您在交易內執行多項作業時，會一次對 RegDB 執行所有寫入作業。</span><span class="sxs-lookup"><span data-stu-id="26f39-111">**Scaling and performance—** When you do multiple operations within a transaction, all writes to RegDB are performed at once.</span></span> <span data-ttu-id="26f39-112">RegDB 的持續寫入是相當昂貴的作業;如果您要對 RegDB 進行許多寫入，您可以從一次執行全部（而不是每次呼叫 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)）獲得大幅的效能優勢。</span><span class="sxs-lookup"><span data-stu-id="26f39-112">Persisted writes to RegDB are a relatively expensive operation; if you are making many writes to RegDB, you can get a big performance benefit from doing them all at once instead of every time you call [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges).</span></span>

## <a name="isolation-behavior-of-regdb"></a><span data-ttu-id="26f39-113">RegDB 的隔離行為</span><span class="sxs-lookup"><span data-stu-id="26f39-113">Isolation Behavior of RegDB</span></span>

<span data-ttu-id="26f39-114">為了確保適當的資料一致性和可序列化交易，RegDB 會在交易中執行管理作業時，強制執行特定的封鎖和隔離行為。</span><span class="sxs-lookup"><span data-stu-id="26f39-114">To ensure proper data consistency and serializable transactions, RegDB enforces particular blocking and isolation behavior when administration operations are being performed within transactions.</span></span>

<span data-ttu-id="26f39-115">每當在交易內進行工作的元件呼叫任何會導致寫入至 COM + 目錄的方法（例如 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)、 [**InstallApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installapplication)或 [**InstallComponent**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent)）時，就會在 com + 目錄伺服器程式碼上採用寫入器鎖定，此程式碼會封鎖任何其他寫入器進入目前的交易認可或中止為止。</span><span class="sxs-lookup"><span data-stu-id="26f39-115">Whenever a component that is doing work within a transaction calls any method that will cause a write to the COM+ catalog—such as [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), [**InstallApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installapplication), or [**InstallComponent**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent)—a writer lock is taken on COM+ catalog server code that will block any other writers from coming in until the current transaction commits or aborts.</span></span> <span data-ttu-id="26f39-116">也就是說，只有當寫入器具有正確的交易親和性，而且正在參與目前的交易時，才會進入。</span><span class="sxs-lookup"><span data-stu-id="26f39-116">That is, writers can come in only if they have the correct transaction affinity and are participating in the current transaction.</span></span>

<span data-ttu-id="26f39-117">未封鎖讀取器。</span><span class="sxs-lookup"><span data-stu-id="26f39-117">Readers are not blocked.</span></span> <span data-ttu-id="26f39-118">但是，讀取器所看到的資料並不會反映在交易內進行的任何過渡期變更，直到該交易實際認可為止。</span><span class="sxs-lookup"><span data-stu-id="26f39-118">However, the data that readers see does not reflect any interim changes made within the transaction until that transaction actually commits.</span></span> <span data-ttu-id="26f39-119">任何參與該交易的元件都會在讀取資料時看到過渡的資料狀態，但交易以外的所有元件只會在交易完成之後，才會看到這些變更。</span><span class="sxs-lookup"><span data-stu-id="26f39-119">Any components participating in that transaction sees interim data states when they read data, but all components outside the transaction see those changes only after the transaction has completed.</span></span>

## <a name="savechanges-behavior"></a><span data-ttu-id="26f39-120">SaveChanges 行為</span><span class="sxs-lookup"><span data-stu-id="26f39-120">SaveChanges Behavior</span></span>

<span data-ttu-id="26f39-121">為了達成上述的隔離行為，RegDB 可有效提供由交易內的元件所處理的快取。</span><span class="sxs-lookup"><span data-stu-id="26f39-121">To achieve the isolation behavior described above, RegDB effectively provides a cache that is acted on by components within the transaction.</span></span> <span data-ttu-id="26f39-122">這會變更 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) 方法的行為。</span><span class="sxs-lookup"><span data-stu-id="26f39-122">This changes the behavior of the [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) method.</span></span>

<span data-ttu-id="26f39-123">一般情況下，在沒有交易的情況下，任何暫止的變更都會在您呼叫 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)時寫入至目錄，而 **SaveChanges** 在所有寫入完成之前都不會傳回。</span><span class="sxs-lookup"><span data-stu-id="26f39-123">Normally, without the presence of a transaction, any pending changes are written to the catalog when you call [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), and **SaveChanges** doesn't return until all writes are completed.</span></span> <span data-ttu-id="26f39-124">這可保證如果對 **SaveChanges** 的呼叫傳回成功，您可以呼叫 [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) ，它會以最新的資料來啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="26f39-124">This guarantees that if a call to **SaveChanges** returns successfully, you can call [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) and it will activate the application with fresh data.</span></span>

<span data-ttu-id="26f39-125">不過，在交易內， [**savechanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) 只會影響快取，而不會影響 RegDB 本身，而 **savechanges** 會立即傳回，無論所有變更是否已交易認可至 RegDB。</span><span class="sxs-lookup"><span data-stu-id="26f39-125">However, within a transaction, [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) affects only the cache, not the RegDB itself, and **SaveChanges** returns immediately whether all changes have been transactionally committed to RegDB.</span></span> <span data-ttu-id="26f39-126">不保證 [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) 會在 **SaveChanges** 傳回之後使用新的資料。</span><span class="sxs-lookup"><span data-stu-id="26f39-126">There is no guarantee that [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) is using fresh data subsequent to **SaveChanges** returning.</span></span> <span data-ttu-id="26f39-127">如果您需要在此內容中呼叫 **StartApplication** ，建議您先等候一段時間再執行這項操作。</span><span class="sxs-lookup"><span data-stu-id="26f39-127">If you need to call **StartApplication** in this context, it is advisable to wait for some period of time before doing so.</span></span>

## <a name="transaction-time-out-period"></a><span data-ttu-id="26f39-128">交易 Time-Out 期限</span><span class="sxs-lookup"><span data-stu-id="26f39-128">Transaction Time-Out Period</span></span>

<span data-ttu-id="26f39-129">如果您在交易內進行許多系統管理作業，它可能會是長時間執行的交易。</span><span class="sxs-lookup"><span data-stu-id="26f39-129">If you are doing numerous administration operations within a transaction, it may be a long running transaction.</span></span> <span data-ttu-id="26f39-130">在此情況下，交易超時值可能會是問題。</span><span class="sxs-lookup"><span data-stu-id="26f39-130">In this case, the transaction time-out value can be an issue.</span></span> <span data-ttu-id="26f39-131">這取決於針對起始交易的元件設定的交易超時值，或是該元件執行所在電腦的全電腦超時設定。</span><span class="sxs-lookup"><span data-stu-id="26f39-131">This is determined either by the transaction time-out value set for the component initiating the transaction or by the machine-wide time-out setting for the machine where that component is running.</span></span> <span data-ttu-id="26f39-132">如果您要在交易內執行許多作業，建議您將適當的交易逾時間隔設定為夠長的值，並在完成時還原原始設定（如有必要）。</span><span class="sxs-lookup"><span data-stu-id="26f39-132">If you are doing numerous operations within a transaction, it is advisable to set the appropriate transaction time-out period to a sufficiently long value and, if necessary, to restore the original setting when you are finished.</span></span>

## <a name="non-transactional-com-catalog-resources"></a><span data-ttu-id="26f39-133">非交易式 COM + 類別目錄資源</span><span class="sxs-lookup"><span data-stu-id="26f39-133">Non-Transactional COM+ Catalog Resources</span></span>

<span data-ttu-id="26f39-134">登錄、檔案系統和 Windows Installer (MSI) 是非交易式的 COM + 類別目錄資源。</span><span class="sxs-lookup"><span data-stu-id="26f39-134">The registry, the file system, and Windows Installer (MSI) are COM+ catalog resources that are not transactional.</span></span>

> [!Note]  
> <span data-ttu-id="26f39-135">如果有錯誤會中止交易，這些資源的變更可能不會回復。</span><span class="sxs-lookup"><span data-stu-id="26f39-135">If there is an error that aborts a transaction, changes to these resources may not be rolled back.</span></span>

 

<span data-ttu-id="26f39-136">如果從 .msi 檔案安裝現有的 COM + 應用程式時發生錯誤，則應用程式不會出現在 [元件服務] 嵌入式管理單元中，但它可能會出現在 [新增/移除程式] 中，在此情況下，您必須手動將其移除。</span><span class="sxs-lookup"><span data-stu-id="26f39-136">If there is an error while installing an existing COM+ application from an .msi file, the application doesn't appear in the Component Services snap-in but it might appear in Add/Remove programs, in which case you need to manually remove it.</span></span>

## <a name="recovering-in-the-event-of-system-hangs"></a><span data-ttu-id="26f39-137">在發生系統停止回應時復原</span><span class="sxs-lookup"><span data-stu-id="26f39-137">Recovering in the Event of System Hangs</span></span>

<span data-ttu-id="26f39-138">如果在交易內執行管理作業的元件在保存目錄伺服器程式碼的寫入器鎖定時停止回應，則會封鎖其他人對目錄進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="26f39-138">If a component doing administration operations within a transaction were to hang while it holds a writer lock on the catalog server code, it would block everyone else from making any changes to the catalog.</span></span> <span data-ttu-id="26f39-139">如果發生這種情況，您可以藉由關閉並重新啟動系統應用程式，清除目錄上的鎖定。</span><span class="sxs-lookup"><span data-stu-id="26f39-139">Should this happen, you can clear the lock on the catalog by shutting down and restarting the System application.</span></span>

## <a name="scripting-with-a-transactioncontext-object"></a><span data-ttu-id="26f39-140">使用 TransactionCoNtext 物件編寫腳本</span><span class="sxs-lookup"><span data-stu-id="26f39-140">Scripting with a TransactionContext Object</span></span>

<span data-ttu-id="26f39-141">在交易內執行管理作業的簡單方式，就是使用 [**TransactionCoNtext**](transactioncontext.md) 物件來控制交易。</span><span class="sxs-lookup"><span data-stu-id="26f39-141">A simple way to do administration operations within transactions is to use a [**TransactionContext**](transactioncontext.md) object to control the transaction.</span></span> <span data-ttu-id="26f39-142">例如，下列 Visual Basic 腳本會示範如何以交易方式加入兩個新的應用程式，讓兩個應用程式或兩個應用程式都不會建立：</span><span class="sxs-lookup"><span data-stu-id="26f39-142">For example, the following Visual Basic script demonstrates how to transactionally add two new applications so that either both applications or neither application is created:</span></span>


```VB
Dim txctx
Dim cat
Dim apps
Dim app1
Dim app2
  
WScript.Echo "Starting"
Set txctx = CreateObject("TxCtx.TransactionContext")
Set cat = txctx.CreateInstance("COMAdmin.COMAdminCatalog")
Set apps = cat.GetCollection("Applications")
Set app1 = apps.Add
app1.Value("Name") = "Test App #1"
apps.SaveChanges
Set app2 = apps.Add
app2.Value("Name") = "Test App #2"
apps.SaveChanges
  
WScript.Echo "Ending"
txctx.Commit

```



## <a name="related-topics"></a><span data-ttu-id="26f39-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="26f39-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26f39-144">處理 COM + 管理錯誤</span><span class="sxs-lookup"><span data-stu-id="26f39-144">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
</dt> <dt>

[<span data-ttu-id="26f39-145">使用 COM + 系統管理目錄的簡介範例</span><span class="sxs-lookup"><span data-stu-id="26f39-145">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[<span data-ttu-id="26f39-146">COMAdmin 物件的總覽</span><span class="sxs-lookup"><span data-stu-id="26f39-146">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> <dt>

[<span data-ttu-id="26f39-147">在 COM + 類別目錄上取出集合</span><span class="sxs-lookup"><span data-stu-id="26f39-147">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[<span data-ttu-id="26f39-148">設定屬性並將變更儲存至 COM + 類別目錄</span><span class="sxs-lookup"><span data-stu-id="26f39-148">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



