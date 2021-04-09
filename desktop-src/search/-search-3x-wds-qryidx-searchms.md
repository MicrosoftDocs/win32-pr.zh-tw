---
description: 搜尋 ms 應用程式協定是查詢 Windows Search 索引的慣例。
ms.assetid: ab2695ed-4ef3-4687-81b0-416ca7086e5f
title: 使用搜尋-ms 通訊協定來查詢索引
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0d835b6db1c9b05b97d5d075b62158069d89029
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689887"
---
# <a name="querying-the-index-with-the-search-ms-protocol"></a><span data-ttu-id="28c79-103">使用搜尋-ms 通訊協定來查詢索引</span><span class="sxs-lookup"><span data-stu-id="28c79-103">Querying the Index with the search-ms Protocol</span></span>

<span data-ttu-id="28c79-104">**搜尋 ms**[應用程式協定](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85))是查詢 Windows Search 索引的慣例。  </span><span class="sxs-lookup"><span data-stu-id="28c79-104">The **search-ms**  [application protocol](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) is a convention for querying the Windows Search index.</span></span> <span data-ttu-id="28c79-105">此通訊協定可讓應用程式（例如 Windows 檔案總管）查詢具有參數值引數的索引，包括屬性引數、先前儲存的搜尋、先進的查詢語法 (AQS) 、自然查詢語法 (NQS) ，以及 (索引子和查詢本身的語言程式碼識別碼) Lcid。</span><span class="sxs-lookup"><span data-stu-id="28c79-105">The protocol enables applications, like Windows Explorer, to query the index with parameter-value arguments, including property arguments, previously saved searches, Advanced Query Syntax (AQS), Natural Query Syntax (NQS), and language code identifiers (LCIDs) for both the indexer and the query itself.</span></span>

<span data-ttu-id="28c79-106">本節的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="28c79-106">This section is organized as follows:</span></span>

-   [<span data-ttu-id="28c79-107">具有 Parameter-Value 引數的開始使用</span><span class="sxs-lookup"><span data-stu-id="28c79-107">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
-   [<span data-ttu-id="28c79-108">地區設定識別碼引數</span><span class="sxs-lookup"><span data-stu-id="28c79-108">Locale Identifier Arguments</span></span>](-search-3x-wds-qryidx-localeidentifiers.md)
-   [<span data-ttu-id="28c79-109">連結引數</span><span class="sxs-lookup"><span data-stu-id="28c79-109">CRUMB Argument</span></span>](-search-3x-wds-qryidx-crumb.md)
-   [<span data-ttu-id="28c79-110">語法引數</span><span class="sxs-lookup"><span data-stu-id="28c79-110">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
-   [<span data-ttu-id="28c79-111">STACKEDBY 引數</span><span class="sxs-lookup"><span data-stu-id="28c79-111">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
-   [<span data-ttu-id="28c79-112">子查詢引數</span><span class="sxs-lookup"><span data-stu-id="28c79-112">SUBQUERY Argument</span></span>](-search-3x-wds-qryidx-subquery.md)

## <a name="related-topics"></a><span data-ttu-id="28c79-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="28c79-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28c79-114">以程式設計方式查詢索引</span><span class="sxs-lookup"><span data-stu-id="28c79-114">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="28c79-115">使用 SQL 和 AQS 方法來查詢索引</span><span class="sxs-lookup"><span data-stu-id="28c79-115">Using SQL and AQS Approaches to Query the Index</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="28c79-116">使用 ISearchQueryHelper 查詢索引</span><span class="sxs-lookup"><span data-stu-id="28c79-116">Querying the Index with ISearchQueryHelper</span></span>](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[<span data-ttu-id="28c79-117">使用 Windows Search SQL 語法來查詢索引</span><span class="sxs-lookup"><span data-stu-id="28c79-117">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)
</dt> <dt>

[<span data-ttu-id="28c79-118">以程式設計方式使用 Advanced 查詢語法</span><span class="sxs-lookup"><span data-stu-id="28c79-118">Using Advanced Query Syntax Programmatically</span></span>](-search-3x-advancedquerysyntax.md)
</dt> </dl>

 

 
