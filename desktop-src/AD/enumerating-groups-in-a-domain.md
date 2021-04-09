---
title: 列舉定義域中的群組
description: 群組可以放在任何容器或組織單位中， (OU) 在網域中，也可以放在網域的根目錄中。
ms.assetid: 7f9d3c90-b6f4-4bfa-960f-58f380aa487c
ms.tgt_platform: multiple
keywords:
- 列舉網域 AD 中的群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3586b8c6d261c769cabe56def2aa9396a58fa3a5
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681673"
---
# <a name="enumerating-groups-in-a-domain"></a><span data-ttu-id="752c3-104">列舉定義域中的群組</span><span class="sxs-lookup"><span data-stu-id="752c3-104">Enumerating Groups in a Domain</span></span>

<span data-ttu-id="752c3-105">群組可以放在任何容器或組織單位中， (OU) 在網域中，也可以放在網域的根目錄中。</span><span class="sxs-lookup"><span data-stu-id="752c3-105">Groups can be placed in any container or organizational unit (OU) in a domain as well as the root of the domain.</span></span> <span data-ttu-id="752c3-106">這表示群組可以位於目錄階層中的多個位置。</span><span class="sxs-lookup"><span data-stu-id="752c3-106">This means that groups can be in numerous locations in the directory hierarchy.</span></span> <span data-ttu-id="752c3-107">因此，您有兩個列舉群組的選擇：</span><span class="sxs-lookup"><span data-stu-id="752c3-107">Therefore, you have two choices for enumerating groups:</span></span>

1.  <span data-ttu-id="752c3-108">列舉直接包含在容器、OU 或網域根目錄中的群組。</span><span class="sxs-lookup"><span data-stu-id="752c3-108">Enumerate the groups directly contained in a container, OU, or at the root of the domain.</span></span>

    <span data-ttu-id="752c3-109">明確系結至包含要列舉之群組的容器物件，使用 [**IADsContainer. filter**](/windows/desktop/api/iads/nn-iads-iadscontainer)屬性將包含 "groups" 的篩選器設定為類別，並使用 [**IADsContainer：： get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum)方法來列舉群組物件。</span><span class="sxs-lookup"><span data-stu-id="752c3-109">Explicitly bind to the container object that contains the groups to enumerate, set a filter that contains "groups" as the class using the [**IADsContainer.Filter**](/windows/desktop/api/iads/nn-iads-iadscontainer) property, and use the [**IADsContainer::get\_\_NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) method to enumerate the group objects.</span></span>

    <span data-ttu-id="752c3-110">這項技術會列舉直接包含在容器或 OU 物件中的群組。</span><span class="sxs-lookup"><span data-stu-id="752c3-110">This technique enumerates groups contained directly in a container or OU object.</span></span> <span data-ttu-id="752c3-111">如果容器包含其他可能包含其他群組的容器，您就必須系結至這些容器，並以遞迴方式列舉這些容器上的群組。</span><span class="sxs-lookup"><span data-stu-id="752c3-111">If the container contains other containers that can potentially contain other groups, you must bind to those containers and recursively enumerate the groups on those containers.</span></span> <span data-ttu-id="752c3-112">若要操作群組物件和唯讀特定屬性，請使用選項2中所述的深層搜尋。</span><span class="sxs-lookup"><span data-stu-id="752c3-112">To manipulate the group objects and read only specific properties, use the deep search described in Option 2.</span></span>

    <span data-ttu-id="752c3-113">因為列舉會傳回代表每個群組物件的 ADSI COM 物件的指標，所以您可以呼叫 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 來取得群組物件的 [**IADs**](/windows/desktop/api/iads/nn-iads-iads)、 [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup)和 [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist) 介面指標。也就是說，您可以取得容器中每個列舉群組物件的介面指標，而不需要明確地系結至每個群組物件。</span><span class="sxs-lookup"><span data-stu-id="752c3-113">Because enumeration returns pointers to ADSI COM objects representing each group object, you can call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to get [**IADs**](/windows/desktop/api/iads/nn-iads-iads), [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup), and [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist) interface pointers to the group object; that is, you can get interface pointers to each enumerated group object in a container without having to explicitly bind to each group object.</span></span> <span data-ttu-id="752c3-114">若要直接在容器內對所有群組執行作業，列舉不需要系結至每個群組，就能呼叫 **IADs** 或 **IADsGroup** 方法。</span><span class="sxs-lookup"><span data-stu-id="752c3-114">To perform operations on all the groups directly within a container, enumeration does not require binding to each group in order to call **IADs** or **IADsGroup** methods.</span></span> <span data-ttu-id="752c3-115">若要從群組取出特定屬性，請使用 [**>idirectorysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) ，如第二個選項所述。</span><span class="sxs-lookup"><span data-stu-id="752c3-115">To retrieve specific properties from groups, use [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) as described in the second option.</span></span>

    <span data-ttu-id="752c3-116">當您嘗試列舉包含 W w n 安全性主體之成員的群組（例如 Everyone、已驗證的使用者、批次等等）時，就會發生例外狀況。</span><span class="sxs-lookup"><span data-stu-id="752c3-116">An exception to this occurs when you attempt to enumerate a group that contains members that are wellKnown security principals, such as Everyone, Authenticated users, BATCH, and so on.</span></span> <span data-ttu-id="752c3-117">由於您無法系結至這些類型的物件，因此當您列舉 WinNT 範圍中的群組時，就不會列出這些物件，因為某些 IADs 方法（例如類別、ADsPath 和名稱）會在列舉成員上叫用時傳回正確的結果。</span><span class="sxs-lookup"><span data-stu-id="752c3-117">Because you cannot bind to these types of objects, they are not listed when you enumerate groups in the WinNT scope, even though it may appear to bind, because certain IADs methods such as Class, ADsPath, and Name return correct results when invoked on enumerated members.</span></span>

2.  <span data-ttu-id="752c3-118">執行 "objectCategory = group" 的深層搜尋，以尋找樹狀結構中的所有群組。</span><span class="sxs-lookup"><span data-stu-id="752c3-118">Perform a deep search for "objectCategory=group" to find all groups in a tree.</span></span>

    <span data-ttu-id="752c3-119">首先，系結至要開始搜尋的容器物件。</span><span class="sxs-lookup"><span data-stu-id="752c3-119">First, bind to the container object where to begin the search.</span></span> <span data-ttu-id="752c3-120">例如，若要尋找網域中的所有群組，請系結至網域的根目錄。若要尋找樹系中的所有群組，請系結至通用類別目錄，然後從 GC 的根目錄進行搜尋。</span><span class="sxs-lookup"><span data-stu-id="752c3-120">For example, to find all groups in a domain, bind to root of the domain; to find all groups in the forest, bind to global catalog and search from the root of the GC.</span></span>

    <span data-ttu-id="752c3-121">然後使用 [**>idirectorysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) 來查詢包含 (objectCategory = group) 和搜尋 **ADS \_ 範圍 \_ 子樹** 之喜好設定的搜尋篩選準則。</span><span class="sxs-lookup"><span data-stu-id="752c3-121">Then use [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) to query using a search filter that contains (objectCategory=group) and search preference of **ADS\_SCOPE\_SUBTREE**.</span></span>

    > [!Note]  
    > <span data-ttu-id="752c3-122">您可以使用 **ADS \_ 範圍 \_ ONELEVEL** 的搜尋喜好設定來執行搜尋，以將搜尋限制為您所系結之容器物件的直接內容。</span><span class="sxs-lookup"><span data-stu-id="752c3-122">You can perform a search with a search preference of **ADS\_SCOPE\_ONELEVEL** to limit the search to the direct contents of the container object that you bound to.</span></span>

     

    <span data-ttu-id="752c3-123">[**>idirectorysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) 只會抓取群組中特定屬性的值。</span><span class="sxs-lookup"><span data-stu-id="752c3-123">[**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) retrieves only the values of specific properties from groups.</span></span> <span data-ttu-id="752c3-124">若要取出值，請使用 **>idirectorysearch**。</span><span class="sxs-lookup"><span data-stu-id="752c3-124">To retrieve values, use **IDirectorySearch**.</span></span> <span data-ttu-id="752c3-125">若要操作從搜尋傳回的群組物件，也就是使用 [**IADs**](/windows/desktop/api/iads/nn-iads-iads) 或 [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) 方法，請明確地系結至這些物件。</span><span class="sxs-lookup"><span data-stu-id="752c3-125">To manipulate the group objects returned from a search, that is, to use [**IADs**](/windows/desktop/api/iads/nn-iads-iads) or [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) methods, explicitly bind to them.</span></span> <span data-ttu-id="752c3-126">若要這樣做，請將 **distinguishedName** 指定為要從搜尋傳回的其中一個屬性，並使用傳回的分辨名稱來系結至搜尋中傳回的每個群組。</span><span class="sxs-lookup"><span data-stu-id="752c3-126">To do this, specify **distinguishedName** as one of the properties to return from the search and use the returned distinguished names to bind to each group returned in the search.</span></span>

    <span data-ttu-id="752c3-127">只會抓取特定屬性。</span><span class="sxs-lookup"><span data-stu-id="752c3-127">Only specific properties are retrieved.</span></span> <span data-ttu-id="752c3-128">您無法在未明確指定 group 類別的每個可能屬性的情況下，取得所有屬性。</span><span class="sxs-lookup"><span data-stu-id="752c3-128">You cannot retrieve all attributes without explicitly specifying every possible attribute of the group class.</span></span>

 

 