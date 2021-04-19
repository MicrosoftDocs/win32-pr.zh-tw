---
title: 列舉使用者
description: 不同于 Windows NT 4.0 網域，Windows 2000 使用者可以放在任何容器或組織單位 (OU) 在網域中，也可以放在網域的根目錄中。
ms.assetid: 4a35af7a-f43b-4cf9-a030-77f6c2518ae7
ms.tgt_platform: multiple
keywords:
- 列舉使用者廣告
- 使用者廣告，列舉使用者
- Active Directory、使用、使用者、列舉使用者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e922d92f4313ed0238ff068f7ae1c0fbf693d497
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "106967254"
---
# <a name="enumerating-users"></a><span data-ttu-id="1606b-106">列舉使用者</span><span class="sxs-lookup"><span data-stu-id="1606b-106">Enumerating Users</span></span>

<span data-ttu-id="1606b-107">不同于 Windows NT 4.0 網域，Windows 2000 使用者可以放在任何容器或組織單位 (OU) 在網域中，也可以放在網域的根目錄中。</span><span class="sxs-lookup"><span data-stu-id="1606b-107">Unlike Windows NT 4.0 domains, Windows 2000 users can be placed in any container or organizational unit (OU) in a domain as well as the root of the domain.</span></span> <span data-ttu-id="1606b-108">這表示使用者可以位於目錄階層中的多個位置。</span><span class="sxs-lookup"><span data-stu-id="1606b-108">This means that users can be in numerous locations in the directory hierarchy.</span></span> <span data-ttu-id="1606b-109">因此，您有兩個列舉使用者的選擇：</span><span class="sxs-lookup"><span data-stu-id="1606b-109">Therefore, you have two choices for enumerating users:</span></span>

-   <span data-ttu-id="1606b-110">列舉直接包含在容器、OU 或網域根目錄中的使用者：</span><span class="sxs-lookup"><span data-stu-id="1606b-110">Enumerate the users directly contained in a container, OU, or at the root of the domain:</span></span>

    <span data-ttu-id="1606b-111">明確系結至包含您感興趣列舉之使用者的容器物件，使用 [**IADsContainer. filter**](/windows/desktop/ADSI/iadscontainer-property-methods)屬性將包含 "user" 的篩選設定為類別，並使用 [**IADsContainer：： get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum)方法來列舉使用者物件。</span><span class="sxs-lookup"><span data-stu-id="1606b-111">Explicitly bind to the container object that contains the users you are interested in enumerating, set a filter containing "user" as the class using the [**IADsContainer.Filter**](/windows/desktop/ADSI/iadscontainer-property-methods) property, and use the [**IADsContainer::get\_\_NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) method to enumerate the user objects.</span></span>

    <span data-ttu-id="1606b-112">這項技術可以用來列舉直接包含在容器或 OU 物件中的使用者。</span><span class="sxs-lookup"><span data-stu-id="1606b-112">This technique can be used to enumerate users that are directly contained in a container or OU object.</span></span> <span data-ttu-id="1606b-113">如果容器包含可能包含其他使用者的其他容器，您必須系結至這些容器，並以遞迴方式列舉這些容器上的使用者。</span><span class="sxs-lookup"><span data-stu-id="1606b-113">If the container contains other containers that can potentially contain other users, you must bind to those containers and recursively enumerate the users on those containers.</span></span> <span data-ttu-id="1606b-114">如果您不需要操作使用者物件，且只需要讀取特定屬性，請使用選項2中所述的深層搜尋。</span><span class="sxs-lookup"><span data-stu-id="1606b-114">If it is not required that you manipulate the user objects, and only need to read specific properties, use the deep search described in Option 2.</span></span>

    <span data-ttu-id="1606b-115">因為列舉會傳回代表每個使用者物件之 ADSI COM 物件的指標，所以您可以呼叫 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 來取得使用者物件的 [**IADs**](/windows/desktop/api/iads/nn-iads-iads)、 [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser)和 [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="1606b-115">Because enumeration returns pointers to ADSI COM objects representing each user object, you can call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to get [**IADs**](/windows/desktop/api/iads/nn-iads-iads), [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser), and [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist) interface pointers to the user object.</span></span> <span data-ttu-id="1606b-116">這表示您可以取得容器中每個列舉使用者物件的介面指標，而不需要明確地系結至每個使用者物件。</span><span class="sxs-lookup"><span data-stu-id="1606b-116">This means you can get interface pointers to each enumerated user object in a container without having to explicitly bind to each user object.</span></span> <span data-ttu-id="1606b-117">若要直接對容器內的所有使用者執行作業，列舉可避免必須系結至每個使用者，才能呼叫 **IADs** 或 **IADsUser** 方法。</span><span class="sxs-lookup"><span data-stu-id="1606b-117">To perform operations on all the users directly within a container, enumeration avoids having to bind to each user in order to call **IADs** or **IADsUser** methods.</span></span> <span data-ttu-id="1606b-118">若要取得使用者的特定屬性，請使用 [**>idirectorysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) ，如選項2所述。</span><span class="sxs-lookup"><span data-stu-id="1606b-118">To retrieve specific properties from users, use [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) as described in option 2.</span></span>

-   <span data-ttu-id="1606b-119">針對 (& (objectClass = user)  (objectCategory = person) ) 尋找樹狀結構中的所有使用者，執行深層搜尋：</span><span class="sxs-lookup"><span data-stu-id="1606b-119">Perform a deep search for (&(objectClass=user)(objectCategory=person)) to find all users in a tree:</span></span>

    <span data-ttu-id="1606b-120">首先，系結至要開始搜尋的容器物件。</span><span class="sxs-lookup"><span data-stu-id="1606b-120">First, bind to the container object where to begin the search.</span></span> <span data-ttu-id="1606b-121">例如，若要尋找網域中的所有使用者，請系結至網域的根目錄。若要尋找樹系中的所有使用者，請系結至通用類別目錄，然後從 GC 的根目錄進行搜尋。</span><span class="sxs-lookup"><span data-stu-id="1606b-121">For example, to find all users in a domain, bind to root of the domain; to find all users in the forest, bind to the global catalog and search from the root of the GC.</span></span>

    <span data-ttu-id="1606b-122">然後使用 [**>idirectorysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) 來查詢包含 (& 的搜尋篩選準則， (objectClass = User)  (objectCategory = person) ) 和搜尋偏好的 ADS \_ 範圍 \_ 子樹。</span><span class="sxs-lookup"><span data-stu-id="1606b-122">Then use [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) to query using a search filter containing (&(objectClass=user)(objectCategory=person)) and search preference of ADS\_SCOPE\_SUBTREE.</span></span>

    <span data-ttu-id="1606b-123">您可以使用 ADS 範圍 ONELEVEL 的搜尋喜好設定來執行搜尋 \_ \_ ，以將搜尋限制為您所系結之容器物件的直接內容。</span><span class="sxs-lookup"><span data-stu-id="1606b-123">You can perform a search with a search preference of ADS\_SCOPE\_ONELEVEL to limit the search to the direct contents of the container object that you bound to.</span></span>

    <span data-ttu-id="1606b-124">[**>idirectorysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) 只會抓取使用者的特定屬性值。</span><span class="sxs-lookup"><span data-stu-id="1606b-124">[**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) retrieves only the values of specific properties from users.</span></span> <span data-ttu-id="1606b-125">若要取出值，請使用 **>idirectorysearch**。</span><span class="sxs-lookup"><span data-stu-id="1606b-125">To retrieve values, use **IDirectorySearch**.</span></span> <span data-ttu-id="1606b-126">若要操作從搜尋傳回的使用者物件，也就是您想要使用 [**IADs**](/windows/desktop/api/iads/nn-iads-iads) 或 [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) 方法，您必須明確地系結至這些方法。</span><span class="sxs-lookup"><span data-stu-id="1606b-126">To manipulate the user objects returned from a search, that is, you want to use [**IADs**](/windows/desktop/api/iads/nn-iads-iads) or [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) methods, you must explicitly bind to them.</span></span> <span data-ttu-id="1606b-127">若要這樣做，請將 **distinguishedName** 指定為要從搜尋傳回的其中一個屬性，並使用傳回的分辨名稱來系結至搜尋中傳回的每個使用者。</span><span class="sxs-lookup"><span data-stu-id="1606b-127">To do this, specify **distinguishedName** as one of the properties to return from the search and use the returned distinguished names to bind to each user returned in the search.</span></span>

    <span data-ttu-id="1606b-128">只會抓取特定屬性。</span><span class="sxs-lookup"><span data-stu-id="1606b-128">Only specific properties are retrieved.</span></span> <span data-ttu-id="1606b-129">您無法在未明確指定使用者類別的每個可能屬性的情況下，取得所有屬性。</span><span class="sxs-lookup"><span data-stu-id="1606b-129">You cannot retrieve all attributes without explicitly specifying every possible attribute of the user class.</span></span>

 

 