---
description: Windows Search SDK 提供 interopability 元件，可讓您使用元件物件模型 (COM) 物件，這些物件是使用 managed 程式碼針對介面和類別所公開的 Windows Search 和其他程式。
ms.assetid: 9ade6f55-de65-4f73-9d22-1be819549704
title: 搭配 Shell 資料和 Windows Search 使用 Managed 程式碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0a4c0f4182739fe553c21b45bcfc3a3af7a68f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112492"
---
# <a name="using-managed-code-with-shell-data-and-windows-search"></a><span data-ttu-id="ca44d-103">搭配 Shell 資料和 Windows Search 使用 Managed 程式碼</span><span class="sxs-lookup"><span data-stu-id="ca44d-103">Using Managed Code with Shell Data and Windows Search</span></span>

<span data-ttu-id="ca44d-104">Windows Search SDK 提供 interopability 元件，可讓您使用元件物件模型 (COM) 物件，這些物件是使用 managed 程式碼針對介面和類別所公開的 Windows Search 和其他程式。</span><span class="sxs-lookup"><span data-stu-id="ca44d-104">The Windows Search SDK provides an interopability assembly for you to work with Component Object Model (COM) objects that are exposed by Windows Search and other programs against the interfaces and classes using managed code.</span></span> <span data-ttu-id="ca44d-105">Interopability 元件是由 Microsoft 數位簽署，可透過 [Windows Search 範例](-search-samples-ovw.md)找到。</span><span class="sxs-lookup"><span data-stu-id="ca44d-105">The interopability assembly is digitally signed by Microsoft and can be found with the [Windows Search samples](-search-samples-ovw.md).</span></span>

<span data-ttu-id="ca44d-106">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="ca44d-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="ca44d-107">使用 Windows API CodePack</span><span class="sxs-lookup"><span data-stu-id="ca44d-107">Using the Windows API CodePack</span></span>](#using-the-windows-api-codepack)
    -   [<span data-ttu-id="ca44d-108">存取索引結果</span><span class="sxs-lookup"><span data-stu-id="ca44d-108">Accessing Index Results</span></span>](#accessing-index-results)
    -   [<span data-ttu-id="ca44d-109">使用 Windows API Codepack 的範例應用程式</span><span class="sxs-lookup"><span data-stu-id="ca44d-109">Sample Application Using the Windows API Codepack</span></span>](#sample-application-using-the-windows-api-codepack)
-   [<span data-ttu-id="ca44d-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="ca44d-110">Related topics</span></span>](#related-topics)

## <a name="using-the-windows-api-codepack"></a><span data-ttu-id="ca44d-111">使用 Windows API CodePack</span><span class="sxs-lookup"><span data-stu-id="ca44d-111">Using the Windows API CodePack</span></span>

<span data-ttu-id="ca44d-112">如果您是在 Microsoft .NET 環境中工作，請使用 [適用于 microsoft .NET Framework 的 WINDOWS API Code Pack](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) 來取得搜尋結果，或只流覽命名空間。</span><span class="sxs-lookup"><span data-stu-id="ca44d-112">If you are working in the Microsoft .NET environment, use the [Windows API Code Pack for Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) to obtain search results, or just browse the namespace.</span></span> <span data-ttu-id="ca44d-113">[適用于 Microsoft .NET Framework 的 WINDOWS API 程式碼套件](https://www.nuget.org/packages/Microsoft.Windows.Compatibility)會提供 Shell 專案的集合，這些專案基本上是原生[IShellItem 介面](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellitem)周圍的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="ca44d-113">The [Windows API Code Pack for Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) provides you with a collection of Shell items that are essentially wrappers around the native [IShellItem Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellitem).</span></span> <span data-ttu-id="ca44d-114">您可以逐一查看此集合，並取得各種屬性值的方式，類似于從物件連結與嵌入資料庫 (OLE DB) 查詢中列舉資料表的結果。</span><span class="sxs-lookup"><span data-stu-id="ca44d-114">You can iterate over this collection and get the various property values in a fashion similar to how you would enumerate the results in a table from an Object Linking and Embedding Database (OLE DB) query.</span></span>

<span data-ttu-id="ca44d-115">下列程式碼片段說明如何逐一查看搜尋專案，以及取得每個專案的屬性值。</span><span class="sxs-lookup"><span data-stu-id="ca44d-115">The following code snippet illustrates how to iterate over Search items and obtain the property values for each.</span></span>


```
foreach (ShellObject so in KnownFolders.SavedSearches)
{
    searchFolder = new ShellSearchFolder(finalSearchCondition, (ShellContainer)so);
    List<ShellObject> items = new List<ShellObject>();
    foreach (ShellObject so2 in searchFolder) items.Add(so2);   
}
```



### <a name="accessing-index-results"></a><span data-ttu-id="ca44d-116">存取索引結果</span><span class="sxs-lookup"><span data-stu-id="ca44d-116">Accessing Index Results</span></span>

<span data-ttu-id="ca44d-117">您可以透過 OLE DB 或 Shell 資料模型來存取索引結果。</span><span class="sxs-lookup"><span data-stu-id="ca44d-117">You can access index results through either OLE DB or the Shell data model.</span></span> <span data-ttu-id="ca44d-118">這兩種方法都有其優點和缺點。</span><span class="sxs-lookup"><span data-stu-id="ca44d-118">There are advantages and disadvantages with either approach.</span></span> <span data-ttu-id="ca44d-119">其中一個優點是資料庫程式設計人員熟悉 OLE DB 和結構化查詢語言 (SQL)  (SQL) 。</span><span class="sxs-lookup"><span data-stu-id="ca44d-119">One advantage is that OLE DB and Structured Query Language (SQL) are familiar to database programmers.</span></span> <span data-ttu-id="ca44d-120">在查詢索引子時，其他優點更能控制效能，以及存取其他功能，例如能夠快速地在新的資料列集中尋找先前的結果。</span><span class="sxs-lookup"><span data-stu-id="ca44d-120">Other advantages are better control over performance when querying only the indexer, and access to additional functionality such as the ability to locate previous results in a new rowset quickly.</span></span>

<span data-ttu-id="ca44d-121">Shell 資料模型的優點是它會在不同的資訊來源（例如 OpenSearch）之間抽象化，並提供其他功能（例如縮圖和屬性處理常式）的存取權。</span><span class="sxs-lookup"><span data-stu-id="ca44d-121">Advantages of the Shell data model are that it abstracts across different sources of information such as OpenSearch, and provides access to additional functionality such as thumbnails and property handlers.</span></span> <span data-ttu-id="ca44d-122">Shell 物件模型也不需要針對非檔案名結果（例如訊息項目和 OneNote 結果）或任何位於使用者索引中的專案進行特殊的案例支援。</span><span class="sxs-lookup"><span data-stu-id="ca44d-122">Nor does the Shell object model require special case support for non-filename results such as mail items and OneNote results, nor for any item that resides in the user's index.</span></span> <span data-ttu-id="ca44d-123">請注意，在 Shell [KNOWNFOLDERID](../shell/knownfolderid.md) 中，是本機索引內容的已知資料夾範圍。</span><span class="sxs-lookup"><span data-stu-id="ca44d-123">Note that in Shell [KNOWNFOLDERID](../shell/knownfolderid.md) is the known folder scope for local indexed content.</span></span> <span data-ttu-id="ca44d-124">如需建立 Shell 資料來源的詳細資訊，請參閱 [執行基本資料夾物件介面](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="ca44d-124">For more information on creating a Shell data source, see [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span></span>

<span data-ttu-id="ca44d-125">在 Windows 7 和更新版本中，不會透過 OLE DB 針對同盟搜尋來公開 OpenSearch 資料來源。</span><span class="sxs-lookup"><span data-stu-id="ca44d-125">OpenSearch data sources are not exposed through OLE DB for federated search in Windows 7 and later.</span></span> <span data-ttu-id="ca44d-126">基於這個理由，我們建議您考慮撰寫 Shell 命名空間的 LINQ 提供者，而不是使用 OLE DB 來存取索引子的結果。</span><span class="sxs-lookup"><span data-stu-id="ca44d-126">For this reason we recommend that you consider writing a LINQ provider for the Shell namespace instead of using OLE DB to access the indexer results.</span></span> <span data-ttu-id="ca44d-127">如需詳細資訊，請參閱 [逐步解說：建立 IQUERYABLE LINQ 提供者](/previous-versions/bb546158(v=vs.140))。</span><span class="sxs-lookup"><span data-stu-id="ca44d-127">For more information, see [Walkthrough: Creating an IQueryable LINQ Provider](/previous-versions/bb546158(v=vs.140)).</span></span>

### <a name="sample-application-using-the-windows-api-codepack"></a><span data-ttu-id="ca44d-128">使用 Windows API Codepack 的範例應用程式</span><span class="sxs-lookup"><span data-stu-id="ca44d-128">Sample Application Using the Windows API Codepack</span></span>

<span data-ttu-id="ca44d-129">下列螢幕擷取畫面表示以 [Microsoft .NET Framework 的 WINDOWS API Code Pack](https://www.nuget.org/packages/Microsoft.Windows.Compatibility)建立的範例應用程式模擬。</span><span class="sxs-lookup"><span data-stu-id="ca44d-129">The following screenshot represents a mock up of a sample application created with the [Windows API Code Pack for Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility).</span></span>

![顯示電子郵件訊息的 media player 應用程式螢幕擷取畫面](images/folderid-searchhome.png)

## <a name="related-topics"></a><span data-ttu-id="ca44d-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="ca44d-131">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ca44d-132">**概念**</span><span class="sxs-lookup"><span data-stu-id="ca44d-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ca44d-133">Windows 中的同盟搜尋</span><span class="sxs-lookup"><span data-stu-id="ca44d-133">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

<span data-ttu-id="ca44d-134">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="ca44d-134">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="ca44d-135">[不同語言之間的互通性](/previous-versions/dotnet/netframework-1.1/730f1wy3(v=vs.71))</span><span class="sxs-lookup"><span data-stu-id="ca44d-135">[Cross-Language Interoperability](/previous-versions/dotnet/netframework-1.1/730f1wy3(v=vs.71))</span></span>
</dt> </dl>

 

 
