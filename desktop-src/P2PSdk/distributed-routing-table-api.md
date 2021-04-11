---
description: 分散式路由表 (的 DRT) API 可讓應用程式在對等網路中發佈及解析數位金鑰。
ms.assetid: 17422d71-4c6d-458b-87b6-b31fc2b5bda5
title: 分散式路由資料表 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f8c2b435e1c0c813fb279c40b9bbfa9afb6b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026757"
---
# <a name="distributed-routing-table-api"></a><span data-ttu-id="0b1c5-103">分散式路由資料表 API</span><span class="sxs-lookup"><span data-stu-id="0b1c5-103">Distributed Routing Table API</span></span>

<span data-ttu-id="0b1c5-104">分散式路由表 (的 DRT) API 可讓應用程式在對等網路中發佈及解析數位金鑰。</span><span class="sxs-lookup"><span data-stu-id="0b1c5-104">The Distributed Routing Table (DRT) API allows applications to publish and resolve numeric keys in a peer network.</span></span>

<span data-ttu-id="0b1c5-105">利用 DRT 的應用程式可以完成下列工作：</span><span class="sxs-lookup"><span data-stu-id="0b1c5-105">An application utilizing DRT can accomplish the following:</span></span>

-   <span data-ttu-id="0b1c5-106">建立應用程式特定的分散式路由表。</span><span class="sxs-lookup"><span data-stu-id="0b1c5-106">Create application-specific Distributed Routing Tables.</span></span>
-   <span data-ttu-id="0b1c5-107">註冊金鑰，並將這些金鑰與 IP 位址和應用程式資料產生關聯。</span><span class="sxs-lookup"><span data-stu-id="0b1c5-107">Register keys, and associate these keys with IP addresses and application data.</span></span>
-   <span data-ttu-id="0b1c5-108">搜尋金鑰，並取得與它們相關聯的 IP 位址和應用程式資料。</span><span class="sxs-lookup"><span data-stu-id="0b1c5-108">Search for keys and retrieve the IP addresses and application data associated with them.</span></span> <span data-ttu-id="0b1c5-109">這項功能可以用來建立分散式雜湊表 (DHTs) 、無伺服器名稱解析系統，以及許多拓撲的重迭網格網路。</span><span class="sxs-lookup"><span data-stu-id="0b1c5-109">This functionality can be used to construct Distributed Hash Tables (DHTs), serverless name resolution systems, and overlay mesh networks of many topologies.</span></span>

> [!Note]  
> <span data-ttu-id="0b1c5-110">系統管理員和已啟用 DRT 的應用程式使用者應該讓其應用程式的使用者知道所發佈的資訊。</span><span class="sxs-lookup"><span data-stu-id="0b1c5-110">The administrators and users of DRT-enabled applications should make the end users of their applications aware of the information being published.</span></span> <span data-ttu-id="0b1c5-111">本技術未採用 microsoft 伺服器，而且資訊不會傳送給 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="0b1c5-111">Microsoft servers are not employed by this technology and information is not sent to Microsoft.</span></span>

 

<span data-ttu-id="0b1c5-112">為此 API 提供的檔分為三個部分。</span><span class="sxs-lookup"><span data-stu-id="0b1c5-112">The provided documentation for this API is divided into three sections.</span></span>



| <span data-ttu-id="0b1c5-113">區段</span><span class="sxs-lookup"><span data-stu-id="0b1c5-113">Section</span></span>                                                                                | <span data-ttu-id="0b1c5-114">描述</span><span class="sxs-lookup"><span data-stu-id="0b1c5-114">Description</span></span>                                                                                                          |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b1c5-115">關於分散式路由表</span><span class="sxs-lookup"><span data-stu-id="0b1c5-115">About Distributed Routing Tables</span></span>](about-distributed-routing-tables.md)               | <span data-ttu-id="0b1c5-116">詳述 DRT API 生命週期和狀態變更的資訊。</span><span class="sxs-lookup"><span data-stu-id="0b1c5-116">Information detailing the life cycle and state changes of the DRT API.</span></span><br/>                                    |
| [<span data-ttu-id="0b1c5-117">使用分散式路由資料表 API</span><span class="sxs-lookup"><span data-stu-id="0b1c5-117">Using the Distributed Routing Table API</span></span>](using-the-distributed-routing-table-api.md) | <span data-ttu-id="0b1c5-118">詳細說明的是如何使用的「DRT API」。</span><span class="sxs-lookup"><span data-stu-id="0b1c5-118">Information detailing the general usage of the DRT API.</span></span><br/>                                                   |
| [<span data-ttu-id="0b1c5-119">分散式路由資料表 API 參考</span><span class="sxs-lookup"><span data-stu-id="0b1c5-119">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md) | <span data-ttu-id="0b1c5-120">詳細說明組成 DRT API 的函式、資料結構和列舉常數的資訊。</span><span class="sxs-lookup"><span data-stu-id="0b1c5-120">Information detailing the functions, data structures, and enumerated constants that comprise the DRT API.</span></span><br/> |



 

 

 




