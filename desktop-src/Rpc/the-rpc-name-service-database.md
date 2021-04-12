---
title: RPC 名稱服務資料庫
description: 名稱服務是將名稱對應至物件的服務，通常會在資料庫中維護 (的名稱、物件) 組。
ms.assetid: 9ced2307-cf30-45d5-bcd2-c1e4aae8c63b
keywords:
- 遠端程序呼叫 RPC，描述，名稱服務資料庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19ae37473bcf28ddf995ab0a657f300ce13aa83c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462297"
---
# <a name="the-rpc-name-service-database"></a><span data-ttu-id="441ba-104">RPC 名稱服務資料庫</span><span class="sxs-lookup"><span data-stu-id="441ba-104">The RPC Name Service Database</span></span>

<span data-ttu-id="441ba-105">名稱服務是將名稱對應至物件的服務，通常會在資料庫中維護 (的名稱、物件) 組。</span><span class="sxs-lookup"><span data-stu-id="441ba-105">A name service is a service that maps names to objects, and usually maintains the (name, object) pairs in a database.</span></span> <span data-ttu-id="441ba-106">一般而言，名稱是可讓使用者記住和使用的邏輯名稱。</span><span class="sxs-lookup"><span data-stu-id="441ba-106">Generally, the name is a logical name that is easy for users to remember and use.</span></span> <span data-ttu-id="441ba-107">例如，名稱服務可讓使用者使用邏輯名稱 "laserprinter"。</span><span class="sxs-lookup"><span data-stu-id="441ba-107">For example, a name service would allow a user to use the logical name "laserprinter."</span></span> <span data-ttu-id="441ba-108">名稱服務會將此名稱對應至列印伺服器所使用的網路特定名稱。</span><span class="sxs-lookup"><span data-stu-id="441ba-108">The name service maps this name to the network-specific name used by the print server.</span></span>

<span data-ttu-id="441ba-109">為了使用簡單的說明，RPC 名稱服務會將名稱對應至系結控制碼，並在 RPC 名稱服務資料庫中維護 (名稱、系結控制碼) 對應。</span><span class="sxs-lookup"><span data-stu-id="441ba-109">To use a simplified explanation, the RPC name service maps a name to a binding handle and maintains the (name, binding handle) mappings in the RPC name service database.</span></span> <span data-ttu-id="441ba-110">RPC 名稱服務可讓用戶端應用程式使用邏輯名稱，而不是特定的通訊協定順序和網路位址。</span><span class="sxs-lookup"><span data-stu-id="441ba-110">The RPC name service allows client applications to use a logical name instead of a specific protocol sequence and network address.</span></span> <span data-ttu-id="441ba-111">使用邏輯名稱可讓網路系統管理員更輕鬆地安裝和設定您的分散式應用程式。</span><span class="sxs-lookup"><span data-stu-id="441ba-111">The use of the logical name makes it easier for network administrators to install and configure your distributed application.</span></span>

<span data-ttu-id="441ba-112">RPC 名稱服務資料庫專案具有下列其中一個屬性： **伺服器**、 **群組** 或 **設定檔**。</span><span class="sxs-lookup"><span data-stu-id="441ba-112">An RPC name service database entry has one of the following attributes: **server**, **group**, or **profile**.</span></span> <span data-ttu-id="441ba-113">在 Microsoft 的執行中，專案只能有一個屬性，因此這些專案也稱為「伺服器專案」、「群組專案」和「設定檔專案」。</span><span class="sxs-lookup"><span data-stu-id="441ba-113">In the Microsoft implementation, entries can have only one attribute, so these entries are also known as server entries, group entries, and profile entries.</span></span>

<span data-ttu-id="441ba-114">伺服器專案是由介面 Uuid、物件 Uuid (在伺服器執行多重進入點) 、網路位址、通訊協定順序，以及與已知端點相關聯的任何端點資訊時所需。</span><span class="sxs-lookup"><span data-stu-id="441ba-114">The server entry consists of interface UUIDs, object UUIDs (needed when the server implements multiple-entry points), network address, protocol sequence, and any endpoint information associated with well-known endpoints.</span></span> <span data-ttu-id="441ba-115">使用動態端點時，端點資訊會保存在端點對應資料庫中，而不是名稱服務資料庫中，而端點的解析就像任何其他動態端點一樣。</span><span class="sxs-lookup"><span data-stu-id="441ba-115">When a dynamic endpoint is used, the endpoint information is kept in the endpoint-map database rather than the name service database, and the endpoint is resolved like any other dynamic endpoint.</span></span> <span data-ttu-id="441ba-116">伺服器專案是由開頭為 "RpcNsBinding" 前置詞的函式所管理。</span><span class="sxs-lookup"><span data-stu-id="441ba-116">Server entries are managed by functions that start with the prefix "RpcNsBinding".</span></span>

<span data-ttu-id="441ba-117">群組專案可以包含伺服器專案或其他群組專案。</span><span class="sxs-lookup"><span data-stu-id="441ba-117">The group entry can contain server entries or other group entries.</span></span> <span data-ttu-id="441ba-118">群組專案是由開頭為 "RpcNsGroup" 前置詞的函式所管理。</span><span class="sxs-lookup"><span data-stu-id="441ba-118">Group entries are managed by functions that start with the prefix "RpcNsGroup".</span></span>

<span data-ttu-id="441ba-119">設定檔專案可以包含設定檔、群組或伺服器專案。</span><span class="sxs-lookup"><span data-stu-id="441ba-119">The profile entry can contain profile, group, or server entries.</span></span> <span data-ttu-id="441ba-120">設定檔專案是由開頭為 "RpcNsProfile" 前置詞的函式所管理。</span><span class="sxs-lookup"><span data-stu-id="441ba-120">Profile entries are managed by the functions that start with the prefix "RpcNsProfile".</span></span>

<span data-ttu-id="441ba-121">本節提供下列主題中名稱服務資料庫的總覽：</span><span class="sxs-lookup"><span data-stu-id="441ba-121">This section presents an overview of the name service database in the following topics:</span></span>

-   [<span data-ttu-id="441ba-122">名稱服務應用程式指導方針</span><span class="sxs-lookup"><span data-stu-id="441ba-122">Name Service Application Guidelines</span></span>](name-service-application-guidelines.md)
-   [<span data-ttu-id="441ba-123">名稱服務專案的總覽</span><span class="sxs-lookup"><span data-stu-id="441ba-123">An Overview of the Name Service Entry</span></span>](an-overview-of-the-name-service-entry.md)
-   [<span data-ttu-id="441ba-124">名稱服務專案的準則</span><span class="sxs-lookup"><span data-stu-id="441ba-124">Criteria for Name Service Entries</span></span>](criteria-for-name-service-entries.md)
-   [<span data-ttu-id="441ba-125">名稱服務專案清除</span><span class="sxs-lookup"><span data-stu-id="441ba-125">Name Service Entry Cleanup</span></span>](name-service-entry-cleanup.md)
-   [<span data-ttu-id="441ba-126">查詢期間發生的情況</span><span class="sxs-lookup"><span data-stu-id="441ba-126">What Happens During a Query</span></span>](what-happens-during-a-query.md)
-   [<span data-ttu-id="441ba-127">使用 Microsoft 定位器</span><span class="sxs-lookup"><span data-stu-id="441ba-127">Using Microsoft Locator</span></span>](using-microsoft-locator.md)
-   [<span data-ttu-id="441ba-128">使用 Cell Directory 服務 (CD) </span><span class="sxs-lookup"><span data-stu-id="441ba-128">Using the Cell Directory Service (CDS)</span></span>](using-the-cell-directory-service-cds-.md)
-   [<span data-ttu-id="441ba-129">名稱語法</span><span class="sxs-lookup"><span data-stu-id="441ba-129">Name Syntax</span></span>](name-syntax.md)

 

 




