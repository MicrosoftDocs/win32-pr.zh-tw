---
description: Microsoft Windows Search 查詢語言是以 (SQL) 的結構化查詢語言 (SQL) 為基礎。但是，它不會在具有使用者定義資料表或索引的關係資料庫中搜尋。
ms.assetid: e81c436e-3a33-4b00-9860-9a54bc0eebbf
title: Microsoft Windows Search 中無法使用 SQL 功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20cf0e082a10a7775ca2d880be6153b7d99b6bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001328"
---
# <a name="sql-features-unavailable-in-microsoft-windows-search"></a><span data-ttu-id="b03e1-103">Microsoft Windows Search 中無法使用 SQL 功能</span><span class="sxs-lookup"><span data-stu-id="b03e1-103">SQL Features Unavailable in Microsoft Windows Search</span></span>

<span data-ttu-id="b03e1-104">Microsoft Windows Search 查詢語言是以 (SQL) 的結構化查詢語言 (SQL) 為基礎。但是，它不會在具有使用者定義資料表或索引的關係資料庫中搜尋。</span><span class="sxs-lookup"><span data-stu-id="b03e1-104">Microsoft Windows Search query language is based on Structured Query Language (SQL); however, it does not search in a relational database with user-defined tables or indexes.</span></span> <span data-ttu-id="b03e1-105">因此，許多標準 SQL 語句和語法功能都不適用。</span><span class="sxs-lookup"><span data-stu-id="b03e1-105">Because of this, many standard SQL statements and syntax features do not apply.</span></span> <span data-ttu-id="b03e1-106">以下是 Windows Search 中不支援之更重要 SQL 功能的清單。</span><span class="sxs-lookup"><span data-stu-id="b03e1-106">The following is a list of the more significant SQL features that are not supported in Windows Search.</span></span>


-   <span data-ttu-id="b03e1-107">批次語句</span><span class="sxs-lookup"><span data-stu-id="b03e1-107">BATCH statements</span></span>
-   <span data-ttu-id="b03e1-108">聯合 \_ 資料表函數</span><span class="sxs-lookup"><span data-stu-id="b03e1-108">COALESCE\_TABLE function</span></span>
-   <span data-ttu-id="b03e1-109">CONVERT 函數 (改用 CAST 函數) </span><span class="sxs-lookup"><span data-stu-id="b03e1-109">CONVERT function (use the CAST functions instead)</span></span>
-   <span data-ttu-id="b03e1-110">CREATE VIEW 陳述式</span><span class="sxs-lookup"><span data-stu-id="b03e1-110">CREATE VIEW statement</span></span>
-   <span data-ttu-id="b03e1-111">資料定義語言</span><span class="sxs-lookup"><span data-stu-id="b03e1-111">Data definition language</span></span>
-   <span data-ttu-id="b03e1-112">DATASOURCE 語句</span><span class="sxs-lookup"><span data-stu-id="b03e1-112">DATASOURCE statement</span></span>
-   <span data-ttu-id="b03e1-113">ISO 日期和時間戳記以外的日期和時間格式</span><span class="sxs-lookup"><span data-stu-id="b03e1-113">Date and Time formats other than ISO date and time stamp</span></span>
-   <span data-ttu-id="b03e1-114">DELETE 陳述式</span><span class="sxs-lookup"><span data-stu-id="b03e1-114">DELETE statement</span></span>
-   <span data-ttu-id="b03e1-115">GRANT 陳述式</span><span class="sxs-lookup"><span data-stu-id="b03e1-115">GRANT statement</span></span>
-   <span data-ttu-id="b03e1-116">資訊架構</span><span class="sxs-lookup"><span data-stu-id="b03e1-116">Information schema</span></span>
-   <span data-ttu-id="b03e1-117">INSERT 陳述式</span><span class="sxs-lookup"><span data-stu-id="b03e1-117">INSERT statement</span></span>
-   <span data-ttu-id="b03e1-118">OLE DB 資料類型</span><span class="sxs-lookup"><span data-stu-id="b03e1-118">OLE DB data types</span></span>
-   <span data-ttu-id="b03e1-119">SQL-標準正則運算式 (使用 CONTAINS 或 LIKE 取代) </span><span class="sxs-lookup"><span data-stu-id="b03e1-119">SQL-standard regular expressions (use CONTAINS or LIKE instead)</span></span>
-   <span data-ttu-id="b03e1-120">SQL 查詢的參數</span><span class="sxs-lookup"><span data-stu-id="b03e1-120">Parameters to SQL queries</span></span>
-   <span data-ttu-id="b03e1-121">關聯式資料行比較</span><span class="sxs-lookup"><span data-stu-id="b03e1-121">Relational column comparison</span></span>
-   <span data-ttu-id="b03e1-122">修訂識別碼標頭</span><span class="sxs-lookup"><span data-stu-id="b03e1-122">Revision ID header</span></span>
-   <span data-ttu-id="b03e1-123">REVOKE 陳述式</span><span class="sxs-lookup"><span data-stu-id="b03e1-123">REVOKE statement</span></span>
-   <span data-ttu-id="b03e1-124">範圍別名或修訂編號</span><span class="sxs-lookup"><span data-stu-id="b03e1-124">SCOPE aliases or revision numbers</span></span>
-   <span data-ttu-id="b03e1-125">選取 [全部] (自動移除重複專案) </span><span class="sxs-lookup"><span data-stu-id="b03e1-125">SELECT ALL (removes duplicates automatically)</span></span>
-   <span data-ttu-id="b03e1-126">預存程序</span><span class="sxs-lookup"><span data-stu-id="b03e1-126">Stored procedures</span></span>
-   <span data-ttu-id="b03e1-127">結構化檔擴充</span><span class="sxs-lookup"><span data-stu-id="b03e1-127">Structured document expansion</span></span>
-   <span data-ttu-id="b03e1-128">UNION ALL</span><span class="sxs-lookup"><span data-stu-id="b03e1-128">UNION ALL</span></span>
-   <span data-ttu-id="b03e1-129">未知的關鍵字</span><span class="sxs-lookup"><span data-stu-id="b03e1-129">UNKNOWN keyword</span></span>
-   <span data-ttu-id="b03e1-130">UPDATE 陳述式</span><span class="sxs-lookup"><span data-stu-id="b03e1-130">UPDATE statement</span></span>

<span data-ttu-id="b03e1-131">Windows Search 不支援同義字和非搜尋字。</span><span class="sxs-lookup"><span data-stu-id="b03e1-131">Windows Search does not support Thesaurus and Noise Words.</span></span>

 

 



