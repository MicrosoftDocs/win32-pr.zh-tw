---
title: 批次寫入/修改作業的快速系結選項
description: 當目錄服務物件系結至時，ADSI 會建立代表指定目錄物件的 COM 物件。
ms.assetid: cf41b0c4-7459-49cf-945b-8462c7d19947
ms.tgt_platform: multiple
keywords:
- 批次寫入/修改作業的快速系結選項 ADSI
- 適用于批次寫入/修改作業的 ADSI ADSI、Using、Fast Binding 選項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322cf3c8b5f40dc43304f95d08ff53a7c5c14217
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104508132"
---
# <a name="fast-binding-option-for-batch-writemodify-operations"></a><span data-ttu-id="2dbe4-105">批次寫入/修改作業的快速系結選項</span><span class="sxs-lookup"><span data-stu-id="2dbe4-105">Fast Binding Option for Batch Write/Modify Operations</span></span>

<span data-ttu-id="2dbe4-106">當目錄服務物件系結至時，ADSI 會建立代表指定目錄物件的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="2dbe4-106">When a directory service object is bound to, ADSI creates a COM object that represents the specified directory object.</span></span> <span data-ttu-id="2dbe4-107">當系結時，ADSI 通常會取出 **objectClass** 屬性，讓 adsi 能夠公開適用于該物件類別的 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="2dbe4-107">When binding, ADSI will typically retrieve the **objectClass** attribute so that ADSI can expose the COM interfaces that are appropriate for that class of object.</span></span> <span data-ttu-id="2dbe4-108">例如，除了支援所有物件的基底 ADSI 介面外，使用者物件也會公開 [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) 介面。</span><span class="sxs-lookup"><span data-stu-id="2dbe4-108">For example, a user object would expose the [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) interface in addition to the base ADSI interfaces supported for all objects.</span></span> <span data-ttu-id="2dbe4-109">針對單一作業，這應該不會影響效能。</span><span class="sxs-lookup"><span data-stu-id="2dbe4-109">For a single operation, this should have no effect on performance.</span></span> <span data-ttu-id="2dbe4-110">但是，如果執行的批次作業需要數百個或數千個系結，而且這些作業正在將資料寫入目錄服務，則可能需要交換完整物件支援以加快系結的速度。</span><span class="sxs-lookup"><span data-stu-id="2dbe4-110">However, if batch operations are performed that require hundreds or thousands of bindings over a slow connection and those operations are writing data to the directory service, it may be desirable to exchange full object support for faster binding.</span></span> <span data-ttu-id="2dbe4-111">這就是所謂的快速系結，可在呼叫 [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)或 [**IADsOpenDSObject：： Objdso.opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject)時指定 **ADS \_ fast \_ bind** 旗標來完成。</span><span class="sxs-lookup"><span data-stu-id="2dbe4-111">This is known as a fast-bind and is accomplished by specifying the **ADS\_FAST\_BIND** flag when [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) or [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) is called.</span></span>

<span data-ttu-id="2dbe4-112">快速系結具有下列限制：</span><span class="sxs-lookup"><span data-stu-id="2dbe4-112">Fast-binding has the following restrictions:</span></span>

-   <span data-ttu-id="2dbe4-113">系結作業必須使用 [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) 函數或 [**IADsOpenDSObject：： objdso.opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) 方法來執行。</span><span class="sxs-lookup"><span data-stu-id="2dbe4-113">The bind operation must be performed with the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function or [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method.</span></span> <span data-ttu-id="2dbe4-114">系結作業會移至目錄伺服器一次，而不是兩次。</span><span class="sxs-lookup"><span data-stu-id="2dbe4-114">The bind operation goes to the directory server once instead of twice.</span></span> <span data-ttu-id="2dbe4-115">ADSI 不會取出 **objectClass** 屬性，因此只會公開物件的基底 ADSI 介面。</span><span class="sxs-lookup"><span data-stu-id="2dbe4-115">ADSI does not retrieve the **objectClass** attribute and, therefore, exposes only the base ADSI interfaces for the object.</span></span>
-   <span data-ttu-id="2dbe4-116">COM 物件支援下列介面：</span><span class="sxs-lookup"><span data-stu-id="2dbe4-116">The following interfaces are supported for the COM object:</span></span>

    -   [<span data-ttu-id="2dbe4-117">**IADs**</span><span class="sxs-lookup"><span data-stu-id="2dbe4-117">**IADs**</span></span>](/windows/desktop/api/Iads/nn-iads-iads)
    -   [<span data-ttu-id="2dbe4-118">**IADsContainer**</span><span class="sxs-lookup"><span data-stu-id="2dbe4-118">**IADsContainer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscontainer)
    -   [<span data-ttu-id="2dbe4-119">**IDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="2dbe4-119">**IDirectoryObject**</span></span>](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
    -   [<span data-ttu-id="2dbe4-120">**>idirectorysearch**</span><span class="sxs-lookup"><span data-stu-id="2dbe4-120">**IDirectorySearch**</span></span>](/windows/desktop/api/Iads/nn-iads-idirectorysearch)
    -   [<span data-ttu-id="2dbe4-121">**IADsPropertyList**</span><span class="sxs-lookup"><span data-stu-id="2dbe4-121">**IADsPropertyList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertylist)
    -   [<span data-ttu-id="2dbe4-122">**IADsObjectOptions**</span><span class="sxs-lookup"><span data-stu-id="2dbe4-122">**IADsObjectOptions**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions)
    -   [<span data-ttu-id="2dbe4-123">**ISupportErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="2dbe4-123">**ISupportErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)
    -   [<span data-ttu-id="2dbe4-124">**IADsDeleteOps**</span><span class="sxs-lookup"><span data-stu-id="2dbe4-124">**IADsDeleteOps**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsdeleteops)

-   <span data-ttu-id="2dbe4-125">如果使用 [**IADsContainer：： GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) 方法系結至子物件，子物件就會具有與父系相同的快速系結特性。</span><span class="sxs-lookup"><span data-stu-id="2dbe4-125">If the [**IADsContainer::GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) method is used to bind to child objects, the child object has the same fast-bind characteristics as the parent.</span></span>
-   <span data-ttu-id="2dbe4-126">系結作業期間不會驗證要系結的物件，因此，如果物件不存在，後續的方法呼叫會失敗。</span><span class="sxs-lookup"><span data-stu-id="2dbe4-126">The existence of the object being bound to is not verified during the bind operation, so subsequent method calls will fail if the object does not exist.</span></span> <span data-ttu-id="2dbe4-127">因此，快速系結應僅用於已知存在的物件，例如，在執行傳回所系結之物件辨別名稱的查詢之後，直接系結。</span><span class="sxs-lookup"><span data-stu-id="2dbe4-127">Because of this, fast-binding should only be used for objects that are known to exist, for example, directly after performing a query that returned the distinguished names of the objects being bound to.</span></span>
-   <span data-ttu-id="2dbe4-128">ADSI 擴充功能會公開給 **top** 類別的物件。</span><span class="sxs-lookup"><span data-stu-id="2dbe4-128">ADSI extensions are exposed for objects of class **top**.</span></span> <span data-ttu-id="2dbe4-129">因此，只會公開上面所列之基底 ADSI 介面的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="2dbe4-129">Therefore, only the extensions for the base ADSI interfaces listed above are exposed.</span></span>

 

 