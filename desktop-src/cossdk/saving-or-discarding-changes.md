---
description: 儲存或捨棄變更
ms.assetid: eba4e794-0929-450c-a172-6de6c2f2f2c4
title: 儲存或捨棄變更
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4946574facd0d41d68f4de8cf2f2f48410eb6e99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847156"
---
# <a name="saving-or-discarding-changes"></a><span data-ttu-id="f1aae-103">儲存或捨棄變更</span><span class="sxs-lookup"><span data-stu-id="f1aae-103">Saving or Discarding Changes</span></span>

<span data-ttu-id="f1aae-104">當您在專案上設定屬性時，在您明確儲存變更之前，不會實際將任何變更記錄至 COM + 類別目錄。</span><span class="sxs-lookup"><span data-stu-id="f1aae-104">When you set properties on an item, no changes are actually recorded to the COM+ catalog until you explicitly save changes.</span></span> <span data-ttu-id="f1aae-105">您可以針對包含專案的集合，使用 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件上的 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)方法來進行這項作業。</span><span class="sxs-lookup"><span data-stu-id="f1aae-105">You do this using the [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) method on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object for the collection containing the item.</span></span>

<span data-ttu-id="f1aae-106">如果您想要捨棄尚未認可的變更，您可以在 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件上呼叫 [**填入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate)方法。</span><span class="sxs-lookup"><span data-stu-id="f1aae-106">If you want to discard changes that have not yet been committed, you can call the [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) method on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span> <span data-ttu-id="f1aae-107">這會從集合中所有專案的 COM + 類別目錄讀取所有持續性資料，以有效地刪除任何暫止的變更。</span><span class="sxs-lookup"><span data-stu-id="f1aae-107">This reads in all persistent data from the COM+ catalog for all items in the collection, effectively deleting any pending changes.</span></span>

<span data-ttu-id="f1aae-108">當您使用 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)時，任何您選擇的屬性設定中的不一致都會導致錯誤，而 **SaveChanges** 無法寫入傳回錯誤的物件。</span><span class="sxs-lookup"><span data-stu-id="f1aae-108">When you use [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), any inconsistencies in property settings that you have chosen result in an error, and **SaveChanges** fails to write the object that returned the error.</span></span> <span data-ttu-id="f1aae-109">指定專案上的所有屬性都是寫入或無法全部寫入。</span><span class="sxs-lookup"><span data-stu-id="f1aae-109">All properties on a given item either are written or fail to be written as a whole.</span></span>

<span data-ttu-id="f1aae-110">不過，發生寫入錯誤時，可能是因為設定不相容;可能發生某些其他失敗。</span><span class="sxs-lookup"><span data-stu-id="f1aae-110">However, when write errors occur, they might not be due to incompatible settings; some other failure might have occurred.</span></span> <span data-ttu-id="f1aae-111">您必須檢查失敗的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f1aae-111">You need to inspect the details of the failure to be certain.</span></span> <span data-ttu-id="f1aae-112">如需詳細資訊，請參閱 [處理 COM + 管理錯誤](handling-com--administration-errors.md) 和 [屬性之間的相互相關性](interdependencies-between-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="f1aae-112">For more information, see [Handling COM+ Administration Errors](handling-com--administration-errors.md) and [Interdependencies Between Properties](interdependencies-between-properties.md).</span></span>

<span data-ttu-id="f1aae-113">一般來說，您嘗試一次儲存的變更越多，特別是對多個物件所做的變更，就越可能得到錯誤，也越難追蹤。</span><span class="sxs-lookup"><span data-stu-id="f1aae-113">As a general rule, the more changes you attempt to save at once, particularly changes to multiple objects, the more likely you are to get an error and the more difficult it is to track down.</span></span>

<span data-ttu-id="f1aae-114">此外，在 [**填入**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) 和 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)的呼叫之間，不會鎖定集合中的專案;可能有競爭情形。</span><span class="sxs-lookup"><span data-stu-id="f1aae-114">Additionally, between calls to [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) and [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), you do not have a lock on the items in the collection; contention is possible.</span></span> <span data-ttu-id="f1aae-115">如需詳細資訊，請參閱 [取得和設定屬性](getting-and-setting-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="f1aae-115">For more details, see [Getting and Setting Properties](getting-and-setting-properties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1aae-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="f1aae-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1aae-117">取得和設定屬性</span><span class="sxs-lookup"><span data-stu-id="f1aae-117">Getting and Setting Properties</span></span>](getting-and-setting-properties.md)
</dt> <dt>

[<span data-ttu-id="f1aae-118">屬性之間的相互相關性</span><span class="sxs-lookup"><span data-stu-id="f1aae-118">Interdependencies Between Properties</span></span>](interdependencies-between-properties.md)
</dt> <dt>

[<span data-ttu-id="f1aae-119">查詢可用的屬性</span><span class="sxs-lookup"><span data-stu-id="f1aae-119">Querying for Available Properties</span></span>](querying-for-available-properties.md)
</dt> </dl>

 

 



