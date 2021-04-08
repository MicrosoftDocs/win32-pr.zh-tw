---
title: 使用 objectGUID 系結至物件
description: 如果物件已重新命名或移動，則物件辨別名稱會變更，因此辨別名稱不是可靠的物件識別碼。
ms.assetid: 6c038005-3ecb-4c00-b1a3-a231d3aea64e
ms.tgt_platform: multiple
keywords:
- 使用 objectGUID 系結至物件廣告
- objectGUID AD
- objectGUID AD，用來系結至物件
- Active Directory、使用、系結、使用 objectGUID 系結至物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 045c6194cf27b1697cc478b547105fb10335c219
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023209"
---
# <a name="using-objectguid-to-bind-to-an-object"></a><span data-ttu-id="d2cc3-107">使用 objectGUID 系結至物件</span><span class="sxs-lookup"><span data-stu-id="d2cc3-107">Using objectGUID to Bind to an Object</span></span>

<span data-ttu-id="d2cc3-108">如果物件已重新命名或移動，則物件辨別名稱會變更，因此辨別名稱不是可靠的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="d2cc3-108">An object distinguished name changes if the object is renamed or moved, therefore the distinguished name is not a reliable object identifier.</span></span> <span data-ttu-id="d2cc3-109">在 Active Directory Domain Services 中，即使物件已重新命名或移動，物件的 **objectGUID** 屬性也永遠不會變更。</span><span class="sxs-lookup"><span data-stu-id="d2cc3-109">In Active Directory Domain Services, an object's **objectGUID** property never changes, even if the object is renamed or moved.</span></span> <span data-ttu-id="d2cc3-110">如需 **objectGUID** 和識別碼的詳細資訊，請參閱 [物件名稱和](object-names-and-identities.md)識別。</span><span class="sxs-lookup"><span data-stu-id="d2cc3-110">For more information about **objectGUID** and identifiers, see [Object Names and Identities](object-names-and-identities.md).</span></span>

<span data-ttu-id="d2cc3-111">Active Directory LDAP 提供者會提供方法，以使用物件 GUID 系結至物件。</span><span class="sxs-lookup"><span data-stu-id="d2cc3-111">The Active Directory LDAP provider provides a method to bind to an object using the object GUID.</span></span> <span data-ttu-id="d2cc3-112">系結字串格式如下所示：</span><span class="sxs-lookup"><span data-stu-id="d2cc3-112">The binding string format is as follows:</span></span>


```C++
LDAP://servername/<GUID=XXXXX>
```



<span data-ttu-id="d2cc3-113">在此範例中，"servername" 是目錄伺服器的名稱，而 "XXXXX" 是 GUID 十六進位值的字串表示。</span><span class="sxs-lookup"><span data-stu-id="d2cc3-113">In this example, "servername" is the name of the directory server and "XXXXX" is the string representation of the hexadecimal value of the GUID.</span></span> <span data-ttu-id="d2cc3-114">"Servername" 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="d2cc3-114">The "servername" is optional.</span></span> <span data-ttu-id="d2cc3-115">GUID 字串是在 "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX" 表單中指定。</span><span class="sxs-lookup"><span data-stu-id="d2cc3-115">The GUID string is specified in the "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX" form.</span></span> <span data-ttu-id="d2cc3-116">GUID 字串也可以採用 "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX" 格式，此格式與 [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) 函式所產生的字串相同，沒有周圍的大括弧 " {} "。</span><span class="sxs-lookup"><span data-stu-id="d2cc3-116">The GUID string can also take the form "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX", which is the same form as the string produced by the [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) function, without the surrounding braces "{}".</span></span> <span data-ttu-id="d2cc3-117">如需詳細資訊和示範如何從 GUID 建立可系結字串的程式碼範例，請參閱 [建立 guid 之可系結字串表示的範例程式碼](example-code-for-creating-a-bindable-string-representation-of-a-guid.md)。</span><span class="sxs-lookup"><span data-stu-id="d2cc3-117">For more information and a code example that shows how to create a bindable string from a GUID, see [Example Code for Creating a Bindable String Representation of a GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md).</span></span> <span data-ttu-id="d2cc3-118">[**IADS guid**](/windows/desktop/ADSI/iads-property-methods)屬性可以用來抓取 GUID 的適當字串形式。</span><span class="sxs-lookup"><span data-stu-id="d2cc3-118">The [**IADs.GUID**](/windows/desktop/ADSI/iads-property-methods) property can be used to retrieve the proper string form of the GUID.</span></span>

<span data-ttu-id="d2cc3-119">使用物件 GUID 進行系結時，不支援某些 [**IADs**](/windows/desktop/api/iads/nn-iads-iads) 和 [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) 方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="d2cc3-119">When binding using the object GUID, some [**IADs**](/windows/desktop/api/iads/nn-iads-iads) and [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) methods and properties are not supported.</span></span> <span data-ttu-id="d2cc3-120">使用物件 GUID 的系結所取得的物件不支援下列 **IADs** 屬性：</span><span class="sxs-lookup"><span data-stu-id="d2cc3-120">The following **IADs** properties are not supported by objects obtained by binding using the object GUID:</span></span>

-   [<span data-ttu-id="d2cc3-121">**ADsPath**</span><span class="sxs-lookup"><span data-stu-id="d2cc3-121">**ADsPath**</span></span>](/windows/desktop/ADSI/iads-property-methods)
-   [<span data-ttu-id="d2cc3-122">**Name**</span><span class="sxs-lookup"><span data-stu-id="d2cc3-122">**Name**</span></span>](/windows/desktop/ADSI/iads-property-methods)
-   [<span data-ttu-id="d2cc3-123">**父代**</span><span class="sxs-lookup"><span data-stu-id="d2cc3-123">**Parent**</span></span>](/windows/desktop/ADSI/iads-property-methods)

<span data-ttu-id="d2cc3-124">使用物件 GUID 的系結所取得的物件不支援下列 **IADsContainer** 方法：</span><span class="sxs-lookup"><span data-stu-id="d2cc3-124">The following **IADsContainer** methods are not supported by objects obtained by binding using the object GUID:</span></span>

-   [<span data-ttu-id="d2cc3-125">**GetObject**</span><span class="sxs-lookup"><span data-stu-id="d2cc3-125">**GetObject**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject)
-   [<span data-ttu-id="d2cc3-126">**建立**</span><span class="sxs-lookup"><span data-stu-id="d2cc3-126">**Create**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-create)
-   [<span data-ttu-id="d2cc3-127">**刪除**</span><span class="sxs-lookup"><span data-stu-id="d2cc3-127">**Delete**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)
-   [<span data-ttu-id="d2cc3-128">**CopyHere**</span><span class="sxs-lookup"><span data-stu-id="d2cc3-128">**CopyHere**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-copyhere)
-   [<span data-ttu-id="d2cc3-129">**MoveHere**</span><span class="sxs-lookup"><span data-stu-id="d2cc3-129">**MoveHere**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

<span data-ttu-id="d2cc3-130">若要在使用物件 GUID 系結至物件之後使用這些方法和屬性，請使用 [**IADs 取得**](/windows/desktop/api/iads/nf-iads-iads-get) 物件辨別名稱，然後使用辨別名稱再次系結至物件。</span><span class="sxs-lookup"><span data-stu-id="d2cc3-130">To use these methods and properties after binding to an object using the object GUID, use the [**IADs.Get**](/windows/desktop/api/iads/nf-iads-iads-get) method to retrieve the object distinguished name and then use the distinguished name to bind to the object again.</span></span>

<span data-ttu-id="d2cc3-131">如果應用程式儲存或快取識別碼或參考儲存在 Active Directory Domain Services 中的物件，則物件 GUID 是要使用的最佳識別碼，原因如下：</span><span class="sxs-lookup"><span data-stu-id="d2cc3-131">If an application stores or caches identifiers or references to objects stored in Active Directory Domain Services, the object GUID is the best identifier to use for several reasons:</span></span>

-   <span data-ttu-id="d2cc3-132">即使物件已重新命名或移動，on 物件的 **objectGUID** 屬性也永遠不會變更。</span><span class="sxs-lookup"><span data-stu-id="d2cc3-132">The **objectGUID** property of on object never changes even if the object is renamed or moved.</span></span>
-   <span data-ttu-id="d2cc3-133">使用物件 GUID 系結至物件很容易。</span><span class="sxs-lookup"><span data-stu-id="d2cc3-133">It is easy to bind to the object using the object GUID.</span></span>
-   <span data-ttu-id="d2cc3-134">如果物件已重新命名或移動， **objectGUID** 屬性會提供單一識別碼，可用來快速尋找和識別物件，而不需要撰寫具有可識別該物件之所有屬性條件的查詢。</span><span class="sxs-lookup"><span data-stu-id="d2cc3-134">If the object is renamed or moved, the **objectGUID** property provides a single identifier that can be used to quickly find and identify the object rather than having to compose a query that has conditions for all properties that would identify that object.</span></span>

 

 