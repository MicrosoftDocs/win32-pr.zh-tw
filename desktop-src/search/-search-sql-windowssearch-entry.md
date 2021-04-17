---
description: Windows Search 提供支援全文檢索搜尋的內容編目和搜尋功能。 Windows Search 使用的查詢語言會延伸標準的 SQL-92 和 SQL-99 資料庫查詢語法，以利用文字搜尋來增強其實用性。
ms.assetid: a2eb550a-bb55-4dbd-9ca1-60b776eb9339
title: 使用 Windows Search SQL 語法來查詢索引
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5696891b14340e8d8fe97f0c0cfbdc75db08e464
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468792"
---
# <a name="querying-the-index-with-windows-search-sql-syntax"></a><span data-ttu-id="cf483-104">使用 Windows Search SQL 語法來查詢索引</span><span class="sxs-lookup"><span data-stu-id="cf483-104">Querying the Index with Windows Search SQL Syntax</span></span>

<span data-ttu-id="cf483-105">Windows Search 提供支援全文檢索搜尋的內容編目和搜尋功能。</span><span class="sxs-lookup"><span data-stu-id="cf483-105">Windows Search provides content crawling and search features that support full-text searching.</span></span> <span data-ttu-id="cf483-106">Windows Search 使用的查詢語言會延伸標準的 SQL-92 和 SQL-99 資料庫查詢語法，以利用文字搜尋來增強其實用性。</span><span class="sxs-lookup"><span data-stu-id="cf483-106">The query language used by Windows Search extends the standard SQL-92 and SQL-99 database query syntax to enhance its usefulness with text-based searches.</span></span>

<span data-ttu-id="cf483-107">Windows Search 結構化查詢語言 (SQL)  (SQL) 的所有功能都與 Windows Vista 和更新版本上的 Windows Search 相容，包括所有版本的 Windows 10。</span><span class="sxs-lookup"><span data-stu-id="cf483-107">All features of Windows Search Structured Query Language (SQL) are compatible with Windows Search on Windows Vista, and later, including all versions of Windows 10.</span></span>

<span data-ttu-id="cf483-108">本節概述 Windows Search 中的 SQL 語法，並包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="cf483-108">This section provides an overview of SQL syntax in Windows Search, and includes the following topics:</span></span>

- [<span data-ttu-id="cf483-109">SQL 語法 Windows Search 總覽</span><span class="sxs-lookup"><span data-stu-id="cf483-109">Overview of Windows Search SQL Syntax</span></span>](-search-sql-ovwofsearchquery.md)
- [<span data-ttu-id="cf483-110">一般查詢語言資訊</span><span class="sxs-lookup"><span data-stu-id="cf483-110">General Query Language Information</span></span>](-search-sql-generalqueryinfo.md)
- [<span data-ttu-id="cf483-111">分組依據 .。。OVER .。。聲明</span><span class="sxs-lookup"><span data-stu-id="cf483-111">GROUP ON ... OVER... Statement</span></span>](-search-sql-group-on-over.md)
- [<span data-ttu-id="cf483-112">SELECT 語句</span><span class="sxs-lookup"><span data-stu-id="cf483-112">SELECT Statement</span></span>](-search-sql-select.md)
- [<span data-ttu-id="cf483-113">FROM 子句</span><span class="sxs-lookup"><span data-stu-id="cf483-113">FROM Clause</span></span>](-search-sql-from.md)
- [<span data-ttu-id="cf483-114">WHERE 子句</span><span class="sxs-lookup"><span data-stu-id="cf483-114">WHERE Clause</span></span>](-search-sql-where.md)
- [<span data-ttu-id="cf483-115">ORDER BY 子句</span><span class="sxs-lookup"><span data-stu-id="cf483-115">ORDER BY Clause</span></span>](-search-sql-orderby.md)
- [<span data-ttu-id="cf483-116">RANK BY 子句</span><span class="sxs-lookup"><span data-stu-id="cf483-116">RANK BY Clause</span></span>](-search-sql-rankby.md)
- [<span data-ttu-id="cf483-117">SET 語句</span><span class="sxs-lookup"><span data-stu-id="cf483-117">SET Statement</span></span>](-search-sql-set.md)
- [<span data-ttu-id="cf483-118">資料列集屬性</span><span class="sxs-lookup"><span data-stu-id="cf483-118">Rowset Properties</span></span>](-search-sql-rowset-properties.md)

<span data-ttu-id="cf483-119">本檔假設您已熟悉物件連結與嵌入資料庫 (OLE DB) 和 SQL。</span><span class="sxs-lookup"><span data-stu-id="cf483-119">This documentation assumes familiarity with Object Linking and Embedding Database (OLE DB), and SQL.</span></span>

## <a name="code-samples"></a><span data-ttu-id="cf483-120">程式碼範例</span><span class="sxs-lookup"><span data-stu-id="cf483-120">Code samples</span></span>

<span data-ttu-id="cf483-121">WSSQL 程式碼範例會示範如何透過 SQL 在 Microsoft OLE DB 和 Windows Search 之間進行通訊。</span><span class="sxs-lookup"><span data-stu-id="cf483-121">The WSSQL code sample demonstrates how to communicate between Microsoft OLE DB and Windows Search through SQL.</span></span> <span data-ttu-id="cf483-122">WSOleDB 程式碼範例說明 Active Template Library (ATL) OLE DB Windows Search 應用程式的存取權，以及兩種從 Windows Search 抓取結果的額外方法。</span><span class="sxs-lookup"><span data-stu-id="cf483-122">The WSOleDB code sample illustrates Active Template Library (ATL) OLE DB access to Windows Search applications, and two additional methods for retrieving results from Windows Search.</span></span> <span data-ttu-id="cf483-123">[Windows Search 範例](-search-samples-ovw.md)和[Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)都有提供這兩個範例</span><span class="sxs-lookup"><span data-stu-id="cf483-123">Both samples are available in the [Windows Search Samples](-search-samples-ovw.md) and the [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf483-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="cf483-124">Related topics</span></span>

[<span data-ttu-id="cf483-125">以程式設計方式查詢索引</span><span class="sxs-lookup"><span data-stu-id="cf483-125">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)

[<span data-ttu-id="cf483-126">使用 SQL 和 AQS 方法來查詢索引</span><span class="sxs-lookup"><span data-stu-id="cf483-126">Using SQL and AQS Approaches to Query the Index</span></span>](-search-3x-wds-qryidx-overview.md)

[<span data-ttu-id="cf483-127">使用 ISearchQueryHelper 查詢索引</span><span class="sxs-lookup"><span data-stu-id="cf483-127">Querying the Index with ISearchQueryHelper</span></span>](-search-3x-wds-qryidx-searchqueryhelper.md)

[<span data-ttu-id="cf483-128">使用搜尋-ms 通訊協定來查詢索引</span><span class="sxs-lookup"><span data-stu-id="cf483-128">Querying the Index with the search-ms Protocol</span></span>](-search-3x-wds-qryidx-searchms.md)

[<span data-ttu-id="cf483-129">使用 Windows Search SQL 語法來查詢索引</span><span class="sxs-lookup"><span data-stu-id="cf483-129">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)

[<span data-ttu-id="cf483-130">以程式設計方式使用 Advanced 查詢語法</span><span class="sxs-lookup"><span data-stu-id="cf483-130">Using Advanced Query Syntax Programmatically</span></span>](-search-3x-advancedquerysyntax.md)
