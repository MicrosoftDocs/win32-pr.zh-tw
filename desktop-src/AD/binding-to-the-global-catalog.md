---
title: 系結至通用類別目錄
description: 通用類別目錄是命名空間，其中包含樹系中所有網域的目錄資料。
ms.assetid: c3c131c7-d9dd-4dbd-a909-abd0ffd9f375
ms.tgt_platform: multiple
keywords:
- 系結至通用類別目錄 AD
- 通用類別目錄 AD，系結至
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08fe40b944130f66617b0c111b361ca51cbef126
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023287"
---
# <a name="binding-to-the-global-catalog"></a><span data-ttu-id="40a17-105">系結至通用類別目錄</span><span class="sxs-lookup"><span data-stu-id="40a17-105">Binding to the Global Catalog</span></span>

<span data-ttu-id="40a17-106">通用類別目錄是命名空間，其中包含樹系中所有網域的目錄資料。</span><span class="sxs-lookup"><span data-stu-id="40a17-106">The Global Catalog is a namespace that contains directory data for all domains in a forest.</span></span> <span data-ttu-id="40a17-107">通用類別目錄包含每個網域目錄的部分複本。</span><span class="sxs-lookup"><span data-stu-id="40a17-107">The Global Catalog contains a partial replica of every domain directory.</span></span> <span data-ttu-id="40a17-108">它包含企業樹系中每個物件的專案，但不包含每個物件的所有屬性。</span><span class="sxs-lookup"><span data-stu-id="40a17-108">It contains an entry for every object in the enterprise forest, but does not contain all the properties of each object.</span></span> <span data-ttu-id="40a17-109">相反地，它只包含指定要包含在通用類別目錄中的屬性。</span><span class="sxs-lookup"><span data-stu-id="40a17-109">Instead, it contains only the properties specified for inclusion in the Global Catalog.</span></span>

<span data-ttu-id="40a17-110">通用類別目錄儲存在整個企業的特定伺服器上。</span><span class="sxs-lookup"><span data-stu-id="40a17-110">The Global Catalog is stored on specific servers throughout the enterprise.</span></span> <span data-ttu-id="40a17-111">只有網域控制站可以做為通用類別目錄伺服器。</span><span class="sxs-lookup"><span data-stu-id="40a17-111">Only domain controllers can serve as Global Catalog servers.</span></span> <span data-ttu-id="40a17-112">系統管理員會使用 Active Directory 的網站和服務管理員，來指出指定的網域控制站是否保留通用類別目錄。</span><span class="sxs-lookup"><span data-stu-id="40a17-112">Administrators indicate whether a given domain controller holds a Global Catalog by using the Active Directory Sites and Services Manager.</span></span>

<span data-ttu-id="40a17-113">若要使用 ADSI 系結至通用類別目錄，請使用 "GC：" 標記。</span><span class="sxs-lookup"><span data-stu-id="40a17-113">To bind to the Global Catalog with ADSI, use the "GC:" moniker.</span></span>

<span data-ttu-id="40a17-114">有兩種方式可以系結至通用類別目錄，以在樹系中執行搜尋：</span><span class="sxs-lookup"><span data-stu-id="40a17-114">There are two ways to bind to the Global Catalog to perform a search in a forest:</span></span>

-   <span data-ttu-id="40a17-115">系結至企業根物件，以搜尋樹系中的所有網域。</span><span class="sxs-lookup"><span data-stu-id="40a17-115">Bind to the enterprise root object to search across all domains in the forest.</span></span>
-   <span data-ttu-id="40a17-116">系結至特定物件，以搜尋該物件和其子系。</span><span class="sxs-lookup"><span data-stu-id="40a17-116">Bind to a specific object to search that object and its children.</span></span> <span data-ttu-id="40a17-117">例如，如果您系結至樹系中的網域樹狀目錄下有兩個網域的網域，您可以在這三個網域之間進行搜尋。</span><span class="sxs-lookup"><span data-stu-id="40a17-117">For example, if you bind to a domain that has two domains beneath it in a domain tree in the forest, you can search across those three domains.</span></span> <span data-ttu-id="40a17-118">請注意，要系結之物件的辨別名稱，與用來系結至 "LDAP：" 命名空間的分辨名稱完全相同。</span><span class="sxs-lookup"><span data-stu-id="40a17-118">Be aware that the distinguished name for the object to bind to is exactly the same as the distinguished name used to bind to the "LDAP:" namespace.</span></span> <span data-ttu-id="40a17-119">回想一下，「LDAP：」是單一網域的完整複本，而「GC：」是樹系中所有網域的部分複本。</span><span class="sxs-lookup"><span data-stu-id="40a17-119">Recall that "LDAP:" is a full replica of a single domain and that "GC:" is a partial replica of all domains in the forest.</span></span>

<span data-ttu-id="40a17-120">如同 "LDAP：" 的名字，您可以使用無伺服器系結或系結至特定的通用類別目錄伺服器。</span><span class="sxs-lookup"><span data-stu-id="40a17-120">As with the "LDAP:" moniker, you can use serverless binding or bind to a specific Global Catalog server.</span></span> <span data-ttu-id="40a17-121">如果在目前樹系中搜尋，請使用無伺服器系結。</span><span class="sxs-lookup"><span data-stu-id="40a17-121">If searching in the current forest, use serverless binding.</span></span> <span data-ttu-id="40a17-122">但是，如果是在另一個樹系中搜尋，請指定要系結的功能變數名稱或通用類別目錄伺服器，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="40a17-122">However, if searching in another forest, specify either a domain name or a Global Catalog server to bind to, such as shown in the following examples.</span></span>

<span data-ttu-id="40a17-123">使用功能變數名稱進行系結：</span><span class="sxs-lookup"><span data-stu-id="40a17-123">Bind using the domain name:</span></span>

``` syntax
GC://fabrikam.com
```

<span data-ttu-id="40a17-124">使用伺服器名稱進行系結：</span><span class="sxs-lookup"><span data-stu-id="40a17-124">Bind using the server name:</span></span>

``` syntax
GC://servername
```

<span data-ttu-id="40a17-125">您也可以系結至通用類別目錄內的特定物件。</span><span class="sxs-lookup"><span data-stu-id="40a17-125">You can also bind to a specific object within the Global Catalog.</span></span> <span data-ttu-id="40a17-126">若要系結至 fabrikam 網域中的 sales 物件，請使用下列格式。</span><span class="sxs-lookup"><span data-stu-id="40a17-126">To bind to the sales object in the fabrikam domain, use the following format.</span></span>

``` syntax
GC://fabrikam.com/DC=sales,DC=fabrikam,DC=com
```

<span data-ttu-id="40a17-127">或者，若要系結至伺服器上的 sales 物件，請使用下列格式。</span><span class="sxs-lookup"><span data-stu-id="40a17-127">Or, to bind to the sales object on the server, use the following format.</span></span>

``` syntax
GC://servername.fabrikam.com/DC=sales,DC=fabrikam,DC=com
```

<span data-ttu-id="40a17-128">**搜尋整個樹系**</span><span class="sxs-lookup"><span data-stu-id="40a17-128">**To search the entire forest**</span></span>

1.  <span data-ttu-id="40a17-129">系結至通用類別目錄命名空間的根目錄。</span><span class="sxs-lookup"><span data-stu-id="40a17-129">Bind to the root of the Global Catalog namespace.</span></span>
2.  <span data-ttu-id="40a17-130">列舉通用類別目錄容器。</span><span class="sxs-lookup"><span data-stu-id="40a17-130">Enumerate the Global Catalog container.</span></span> <span data-ttu-id="40a17-131">通用類別目錄容器包含單一物件，可供您用來搜尋整個樹系。</span><span class="sxs-lookup"><span data-stu-id="40a17-131">The Global Catalog container contains a single object that you can use to search the entire forest.</span></span>
3.  <span data-ttu-id="40a17-132">使用容器中的物件來執行搜尋。</span><span class="sxs-lookup"><span data-stu-id="40a17-132">Use the object in the container to perform the search.</span></span> <span data-ttu-id="40a17-133">在 C/c + + 中，呼叫 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 以取得物件的 [**>idirectorysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) 指標，讓您可以使用 **>idirectorysearch** 介面來執行搜尋。</span><span class="sxs-lookup"><span data-stu-id="40a17-133">In C/C++, call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to get an [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pointer on the object so that you can use the **IDirectorySearch** interface to perform the search.</span></span> <span data-ttu-id="40a17-134">在 Visual Basic 中，請使用在您 ADO 查詢中從列舉傳回的物件。</span><span class="sxs-lookup"><span data-stu-id="40a17-134">In Visual Basic, use the object returned from the enumeration in your ADO query.</span></span>

<span data-ttu-id="40a17-135">若要列舉網站中的通用類別目錄伺服器，請使用下列篩選字串來執行「cn = <yoursite> ，cn = sites」的 LDAP 子樹搜尋 <DN of the configurationNamingContext> 。</span><span class="sxs-lookup"><span data-stu-id="40a17-135">To enumerate the Global Catalog servers in a site, perform an LDAP subtree search of "cn=<yoursite>,cn=sites,<DN of the configurationNamingContext>", using the following filter string.</span></span>

``` syntax
(&(objectCategory=nTDSDSA)(options:1.2.840.113556.1.4.803:=1))
```

<span data-ttu-id="40a17-136">此篩選器會使用 LDAP 比對 **\_ \_ 規則 \_ 位 \_ 和** 比對規則運算子 (1.2.840.113556.1.4.803) 來尋找在 **options** 屬性的位元遮罩中設定低序位位的 **nTDSDSA** 物件。</span><span class="sxs-lookup"><span data-stu-id="40a17-136">This filter uses the **LDAP\_MATCHING\_RULE\_BIT\_AND** matching rule operator (1.2.840.113556.1.4.803) to find **nTDSDSA** objects that have the low-order bit set in the bitmask of the **options** attribute.</span></span> <span data-ttu-id="40a17-137">低序位位，對應于 Ntdsapi 中定義的 **NTDSDSA \_ OPT \_ 是 \_ GC** 常數，識別通用類別目錄伺服器的 **NTDSDSA** 物件。</span><span class="sxs-lookup"><span data-stu-id="40a17-137">The low-order bit, which corresponds to the **NTDSDSA\_OPT\_IS\_GC** constant defined in Ntdsapi.h, identifies the **nTDSDSA** object of a Global Catalog server.</span></span> <span data-ttu-id="40a17-138">如需相符規則的詳細資訊，請參閱 [搜尋篩選語法](/windows/desktop/ADSI/search-filter-syntax)。</span><span class="sxs-lookup"><span data-stu-id="40a17-138">For more information about matching rules, see [Search Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span></span>

<span data-ttu-id="40a17-139">**NTDSDSA** 物件的父系是 server 物件，而伺服器物件的 **DNSHostName** 屬性是通用類別目錄伺服器的 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="40a17-139">The parent of the **nTDSDSA** object is the server object, and the **dNSHostName** property of the server object is the DNS name of the Global Catalog server.</span></span>

<span data-ttu-id="40a17-140">您無法使用 \# 定義常數，例如 **NTDSDSA \_ OPT \_ 是 \_ GC** 和 **LDAP \_ \_ 比對規則 \_ 位 \_ ，以及** 直接在搜尋篩選字串中。</span><span class="sxs-lookup"><span data-stu-id="40a17-140">You cannot use \#define constants such as **NTDSDSA\_OPT\_IS\_GC** and **LDAP\_MATCHING\_RULE\_BIT\_AND** directly in a search filter string.</span></span> <span data-ttu-id="40a17-141">不過，您可以使用這些常數作為函式（例如 swprintf） [**的 \_**](/windows/win32/api/winuser/nf-winuser-wsprintfa) 引數，以將常數值插入篩選字串中。</span><span class="sxs-lookup"><span data-stu-id="40a17-141">However, you could use these constants as arguments to a function such as [**swprintf\_s**](/windows/win32/api/winuser/nf-winuser-wsprintfa) to insert the constant values into a filter string.</span></span>

<span data-ttu-id="40a17-142">通用類別目錄不代表整個樹系樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="40a17-142">The global catalog does not represent the entire forest tree structure.</span></span> <span data-ttu-id="40a17-143">例如，您可能會預期下列程式碼範例會列舉樹系中的所有網域，以及每個網域的所有子物件。</span><span class="sxs-lookup"><span data-stu-id="40a17-143">For example, you might expect that the following code example would enumerate all of the domains in the forest and all child objects of each domain.</span></span> <span data-ttu-id="40a17-144">實際上，它實際上是列舉樹系中的所有網域，但是沒有任何列舉的網域物件包含任何子系。</span><span class="sxs-lookup"><span data-stu-id="40a17-144">In reality, what it actually does is enumerate all of the domains in the forest, but none of the enumerated domain objects contain any children.</span></span> <span data-ttu-id="40a17-145">這是通用類別目錄的限制。</span><span class="sxs-lookup"><span data-stu-id="40a17-145">This is a limitation of the global catalog.</span></span>


```VB
Dim oGC As IADs
Dim oDomain As IADs
Dim oChild As IADs

Set oGC = GetObject("GC:")
For Each oDomain In oGC
    ' Print the name of the domain.
    Debug.Print oDomain.Name
    
    ' Enumerate the child objects of the domain.
    For Each oChild In oDomain
        Debug.Print oChild.Name
    Next
Next
```



<span data-ttu-id="40a17-146">若要修正這個錯誤，必須系結至每個網域物件，然後列舉每個網域的子物件。</span><span class="sxs-lookup"><span data-stu-id="40a17-146">To correct this, it is necessary to bind to each domain object and then enumerate the child objects of each domain.</span></span> <span data-ttu-id="40a17-147">下列程式碼範例會顯示適當的技巧。</span><span class="sxs-lookup"><span data-stu-id="40a17-147">The proper technique is shown in the following code example.</span></span>


```VB
Dim oGC As IADs
Dim oDomainEnum As IADs
Dim oDomainBind As IADs
Dim oChild As IADs

Set oGC = GetObject("GC:")
For Each oDomainEnum In oGC
    ' Print the name of the domain.
    Debug.Print oDomainEnum.Name
    
    ' Bind to the domain.
    Set oDomainBind = GetObject("LDAP://" + oDomainEnum.Name)
    
    ' Enumerate the child objects of the domain.
    For Each oChild In oDomainBind
        Debug.Print oChild.Name
    Next
Next
```



<span data-ttu-id="40a17-148">如需示範如何搜尋整個樹系的詳細資訊和程式碼範例，請參閱 [搜尋樹系的範例程式碼](example-code-for-searching-a-forest.md)。</span><span class="sxs-lookup"><span data-stu-id="40a17-148">For more information and code examples that show how to search an entire forest, see [Example Code for Searching a Forest](example-code-for-searching-a-forest.md).</span></span>

 

 