---
description: 下列結構支援分散式路由表 (DRT) API 函式。
ms.assetid: 3ff85b24-5ec0-4b26-b30e-1bf8030a575d
title: 分散式路由表結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d454d2c28008422da897dc91ca9a3dc29db374b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983646"
---
# <a name="distributed-routing-table-structures"></a><span data-ttu-id="a3c1e-103">分散式路由表結構</span><span class="sxs-lookup"><span data-stu-id="a3c1e-103">Distributed Routing Table Structures</span></span>

<span data-ttu-id="a3c1e-104">下列結構支援分散式路由表 (DRT) API 函式。</span><span class="sxs-lookup"><span data-stu-id="a3c1e-104">The following structures support the Distributed Routing Table (DRT) API functions.</span></span>



| <span data-ttu-id="a3c1e-105">結構</span><span class="sxs-lookup"><span data-stu-id="a3c1e-105">Structure</span></span>                                                  | <span data-ttu-id="a3c1e-106">Description</span><span class="sxs-lookup"><span data-stu-id="a3c1e-106">Description</span></span>                                                                                                                                                                              |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a3c1e-107">**DRT \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="a3c1e-107">**DRT\_DATA**</span></span>](/windows/desktop/api/drt/ns-drt-drt_data)                              | <span data-ttu-id="a3c1e-108">包含資料 blob。</span><span class="sxs-lookup"><span data-stu-id="a3c1e-108">Contains a data blob.</span></span> <span data-ttu-id="a3c1e-109">此結構是由數個 DRT 函數所使用。</span><span class="sxs-lookup"><span data-stu-id="a3c1e-109">This structure is used by several DRT functions.</span></span>                                                                                                                   |
| [<span data-ttu-id="a3c1e-110">**DRT \_ 註冊**</span><span class="sxs-lookup"><span data-stu-id="a3c1e-110">**DRT\_REGISTRATION**</span></span>](/windows/desktop/api/drt/ns-drt-drt_registration)              | <span data-ttu-id="a3c1e-111">包含金鑰註冊。</span><span class="sxs-lookup"><span data-stu-id="a3c1e-111">Contains the key registration.</span></span> <span data-ttu-id="a3c1e-112">這是「 [**DRT \_ 搜尋」 \_ 結果**](/windows/desktop/api/drt/ns-drt-drt_search_result) 結構的成員，而且是傳遞給 [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey)的引數。</span><span class="sxs-lookup"><span data-stu-id="a3c1e-112">This is a member of the [**DRT\_SEARCH\_RESULT**](/windows/desktop/api/drt/ns-drt-drt_search_result) structure and is an argument passed to [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey).</span></span> |
| [<span data-ttu-id="a3c1e-113">**DRT \_ 位址**</span><span class="sxs-lookup"><span data-stu-id="a3c1e-113">**DRT\_ADDRESS**</span></span>](/windows/desktop/api/drt/ns-drt-drt_address)                        | <span data-ttu-id="a3c1e-114">包含參與搜尋之 DRT 節點的相關端點資訊。</span><span class="sxs-lookup"><span data-stu-id="a3c1e-114">Contains endpoint information about a DRT node that participated in a search.</span></span> <span data-ttu-id="a3c1e-115">這項資訊適用于將連線能力問題進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="a3c1e-115">This information is intended for use in debugging connectivity problems.</span></span>                                   |
| [<span data-ttu-id="a3c1e-116">**DRT \_ 位址 \_ 清單**</span><span class="sxs-lookup"><span data-stu-id="a3c1e-116">**DRT\_ADDRESS\_LIST**</span></span>](/windows/desktop/api/drt/ns-drt-drt_address_list)             | <span data-ttu-id="a3c1e-117">包含一組代表在搜尋金鑰期間所聯繫之節點的 [**DRT \_ 位址**](/windows/desktop/api/drt/ns-drt-drt_address) 結構。</span><span class="sxs-lookup"><span data-stu-id="a3c1e-117">Contains a set of [**DRT\_ADDRESS**](/windows/desktop/api/drt/ns-drt-drt_address) structures representing the nodes contacted during a search for a key.</span></span>                                                             |
| [<span data-ttu-id="a3c1e-118">**DRT \_ 安全性 \_ 提供者**</span><span class="sxs-lookup"><span data-stu-id="a3c1e-118">**DRT\_SECURITY\_PROVIDER**</span></span>](/windows/desktop/api/Drt/ns-drt-drt_security_provider)   | <span data-ttu-id="a3c1e-119">定義必須由安全性提供者所執行的介面。</span><span class="sxs-lookup"><span data-stu-id="a3c1e-119">Defines the interface that must be implemented by a security provider.</span></span>                                                                                                                   |
| [<span data-ttu-id="a3c1e-120">**DRT \_ 啟動 \_ 程式提供者**</span><span class="sxs-lookup"><span data-stu-id="a3c1e-120">**DRT\_BOOTSTRAP\_PROVIDER**</span></span>](/windows/desktop/api/drt/ns-drt-drt_bootstrap_provider) | <span data-ttu-id="a3c1e-121">定義啟動載入器提供者必須執行的介面。</span><span class="sxs-lookup"><span data-stu-id="a3c1e-121">Defines the interface that must be implemented by a bootstrap provider.</span></span>                                                                                                                  |
| [<span data-ttu-id="a3c1e-122">**DRT \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="a3c1e-122">**DRT\_SETTINGS**</span></span>](/windows/desktop/api/drt/ns-drt-drt_settings)                      | <span data-ttu-id="a3c1e-123">在初始化時定義 DRT 設定。</span><span class="sxs-lookup"><span data-stu-id="a3c1e-123">Defines DRT settings at initialization.</span></span> <span data-ttu-id="a3c1e-124">此結構會作為引數傳遞至 [**DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen)。</span><span class="sxs-lookup"><span data-stu-id="a3c1e-124">This structure is passed as an argument to [**DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen).</span></span>                                                                           |
| [<span data-ttu-id="a3c1e-125">**DRT \_ 搜尋 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="a3c1e-125">**DRT\_SEARCH\_INFO**</span></span>](/windows/desktop/api/drt/ns-drt-drt_search_info)               | <span data-ttu-id="a3c1e-126">定義搜尋查詢。</span><span class="sxs-lookup"><span data-stu-id="a3c1e-126">Defines a search query.</span></span> <span data-ttu-id="a3c1e-127">此結構會作為引數傳遞至 [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch)。</span><span class="sxs-lookup"><span data-stu-id="a3c1e-127">This structure is passed as an argument to [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch).</span></span>                                                                             |
| [<span data-ttu-id="a3c1e-128">**DRT \_ 搜尋 \_ 結果**</span><span class="sxs-lookup"><span data-stu-id="a3c1e-128">**DRT\_SEARCH\_RESULT**</span></span>](/windows/desktop/api/drt/ns-drt-drt_search_result)           | <span data-ttu-id="a3c1e-129">包含搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="a3c1e-129">Contains a search result.</span></span> <span data-ttu-id="a3c1e-130">[**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult)會傳回這個結構。</span><span class="sxs-lookup"><span data-stu-id="a3c1e-130">This structure is returned by [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult).</span></span>                                                                                |
| [<span data-ttu-id="a3c1e-131">**DRT \_ 事件 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="a3c1e-131">**DRT\_EVENT\_DATA**</span></span>](/windows/desktop/api/drt/ns-drt-drt_event_data)                 | <span data-ttu-id="a3c1e-132">包含在應用程式收到事件信號之後呼叫 [**DrtGetEventData**](/windows/desktop/api/drt/nf-drt-drtgeteventdata) 所傳回的事件資料。</span><span class="sxs-lookup"><span data-stu-id="a3c1e-132">Contains the event data returned by calling [**DrtGetEventData**](/windows/desktop/api/drt/nf-drt-drtgeteventdata) after an application receives an event signal.</span></span>                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="a3c1e-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="a3c1e-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3c1e-134">分散式路由表列舉</span><span class="sxs-lookup"><span data-stu-id="a3c1e-134">Distributed Routing Table Enumerations</span></span>](distributed-routing-table-enumerations.md)
</dt> <dt>

[<span data-ttu-id="a3c1e-135">分散式路由表函數</span><span class="sxs-lookup"><span data-stu-id="a3c1e-135">Distributed Routing Table Functions</span></span>](distributed-routing-table-functions.md)
</dt> <dt>

[<span data-ttu-id="a3c1e-136">分散式路由資料表 API 參考</span><span class="sxs-lookup"><span data-stu-id="a3c1e-136">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



