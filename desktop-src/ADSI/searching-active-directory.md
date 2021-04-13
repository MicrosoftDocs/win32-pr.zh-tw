---
title: 搜尋 Active Directory
description: Active Directory 的一項重要功能，就是解析人員的資料查詢，以及電腦和服務的設定資料。
ms.assetid: 8427d69b-0974-4adc-9732-790e5d31db7a
ms.tgt_platform: multiple
keywords:
- 搜尋 Active Directory ADSI
- ADSI ADSI，搜尋 Active Directory
- 查詢 ADSI、搜尋 Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1881872be6092312015f22eba477599ed9394df7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300056"
---
# <a name="searching-active-directory"></a><span data-ttu-id="5b53e-106">搜尋 Active Directory</span><span class="sxs-lookup"><span data-stu-id="5b53e-106">Searching Active Directory</span></span>

<span data-ttu-id="5b53e-107">Active Directory 的一項重要功能，就是解析人員的資料查詢，以及電腦和服務的設定資料。</span><span class="sxs-lookup"><span data-stu-id="5b53e-107">An important function of Active Directory is to resolve data queries for people, as well as configuration data for computers and services.</span></span> <span data-ttu-id="5b53e-108">若要為 Active Directory 撰寫有效率的查詢，最好先熟悉下列各項：</span><span class="sxs-lookup"><span data-stu-id="5b53e-108">To write efficient queries for Active Directory, it is helpful to be familiar with the following:</span></span>

-   <span data-ttu-id="5b53e-109">判斷查詢的範圍：用戶端是否必須針對可能位於樹系內任何位置的物件尋找屬性，或僅在一個網域內或在指定的組織單位內找到 (OU) ？</span><span class="sxs-lookup"><span data-stu-id="5b53e-109">Determining the scope of the query: Must the client find properties for objects that might be located anywhere within a forest, or only within one domain, or within a given organizational unit (OU)?</span></span>
-   <span data-ttu-id="5b53e-110">判斷查詢的深度：查詢必須只搜尋一個層級，或可能會跨越其他 LDAP 目錄？</span><span class="sxs-lookup"><span data-stu-id="5b53e-110">Determining the depth of the query: Must the query only search one level or might it cross into other LDAP directories?</span></span>
-   <span data-ttu-id="5b53e-111">效能和處理大型結果集：用戶端應該如何有效地處理大型結果集的可能性？</span><span class="sxs-lookup"><span data-stu-id="5b53e-111">Performance and handling large result sets: How should the client effectively handle the potential of a large result set?</span></span>
-   <span data-ttu-id="5b53e-112">判斷最佳查詢：何種類型的查詢能提供最有效率的結果？</span><span class="sxs-lookup"><span data-stu-id="5b53e-112">Determining the best queries: What type of queries provide the most efficient results?</span></span> <span data-ttu-id="5b53e-113">開發人員應避免何種查詢？</span><span class="sxs-lookup"><span data-stu-id="5b53e-113">What type of queries should the developer avoid?</span></span>
-   <span data-ttu-id="5b53e-114">瞭解查詢語法： ADSI 支援 RFC 2254 中所述的 LDAP 語法，以及 SQL 的子集。</span><span class="sxs-lookup"><span data-stu-id="5b53e-114">Understanding the query syntax: ADSI supports both the LDAP syntax as documented in RFC 2254, as well as a subset of SQL.</span></span>
-   <span data-ttu-id="5b53e-115">選擇的介面： ADSI 同時提供 OLE DB 支援以及 C/c + + 介面（稱為 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)）。</span><span class="sxs-lookup"><span data-stu-id="5b53e-115">Choice of interfaces: ADSI provides both OLE DB support as well as a C/C++ interface called [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch).</span></span> <span data-ttu-id="5b53e-116">因為 ADSI 適用于多個命名空間，所以您可以使用這些介面來查詢其他命名空間（例如 Exchange）以及 Active Directory。</span><span class="sxs-lookup"><span data-stu-id="5b53e-116">Because ADSI works for multiple namespaces, you can use these interfaces for querying other namespaces such as Exchange, as well as Active Directory.</span></span> <span data-ttu-id="5b53e-117">因為 (ADO) 的 ActiveX 資料物件是簡單的可編寫腳本資料存取物件模型，在 OLE DB 上，OLE DB 介面適用于 Visual Basic 程式設計人員和網頁腳本寫入器。</span><span class="sxs-lookup"><span data-stu-id="5b53e-117">Because the ActiveX Data Object (ADO) is a simple scriptable data access object model on top of OLE DB, the OLE DB interfaces work well for Visual Basic programmers and webpage script writers.</span></span> <span data-ttu-id="5b53e-118">利用 ADO 和 OLE DB 的 Visual Studio 和 Office 應用程式內的新資料存取功能，現在可以用與從其他 OLE DB 提供者（例如 SQL Server）存取資料的相同方式來存取 Active Directory 資料。</span><span class="sxs-lookup"><span data-stu-id="5b53e-118">The new data access features within Visual Studio and Office applications that take advantage of ADO and OLE DB can now access Active Directory data in the same way that they access data from other OLE DB providers, such as SQL Server.</span></span> <span data-ttu-id="5b53e-119">但是，如果 C/c + + 開發人員必須執行簡單的目錄搜尋，則 **>idirectorysearch** 介面可能比 OLE DB 介面更適合。</span><span class="sxs-lookup"><span data-stu-id="5b53e-119">However, if a C/C++ developer must perform a simple directory search, the **IDirectorySearch** interface might be more appropriate than the OLE DB interfaces.</span></span>

<span data-ttu-id="5b53e-120">下列主題說明如何搜尋 Active Directory，以確保您的應用程式會根據用戶端的需求，發出最有效率的查詢：</span><span class="sxs-lookup"><span data-stu-id="5b53e-120">The following topics describe how to search Active Directory to ensure your application issues the most efficient query, given the requirements of the client:</span></span>

-   [<span data-ttu-id="5b53e-121">查詢的範圍</span><span class="sxs-lookup"><span data-stu-id="5b53e-121">Scope of Query</span></span>](scope-of-query.md)
-   [<span data-ttu-id="5b53e-122">效能和處理大型結果集</span><span class="sxs-lookup"><span data-stu-id="5b53e-122">Performance and Handling Large Result Sets</span></span>](performance-and-handling-large-result-sets.md)
-   [<span data-ttu-id="5b53e-123">搜尋篩選語法</span><span class="sxs-lookup"><span data-stu-id="5b53e-123">Search Filter Syntax</span></span>](search-filter-syntax.md)
-   [<span data-ttu-id="5b53e-124">查詢介面</span><span class="sxs-lookup"><span data-stu-id="5b53e-124">Query Interfaces</span></span>](query-interfaces.md)
-   [<span data-ttu-id="5b53e-125">搜尋二進位資料</span><span class="sxs-lookup"><span data-stu-id="5b53e-125">Searching Binary Data</span></span>](searching-binary-data.md)
-   [<span data-ttu-id="5b53e-126">Distributed Query</span><span class="sxs-lookup"><span data-stu-id="5b53e-126">Distributed Query</span></span>](distributed-query.md)

 

 




