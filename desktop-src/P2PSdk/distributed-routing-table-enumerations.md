---
description: 下列列舉支援分散式路由表 (DRT) API。
ms.assetid: 38ce95a0-1603-42c2-8a5e-4370f52c8fc9
title: 分散式路由表列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c432b156a9299a9f70026a394a6fd97f06528a25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976905"
---
# <a name="distributed-routing-table-enumerations"></a><span data-ttu-id="53c2d-103">分散式路由表列舉</span><span class="sxs-lookup"><span data-stu-id="53c2d-103">Distributed Routing Table Enumerations</span></span>

<span data-ttu-id="53c2d-104">下列列舉支援分散式路由表 (DRT) API。</span><span class="sxs-lookup"><span data-stu-id="53c2d-104">The following enumerations support the Distributed Routing Table (DRT) API.</span></span>



| <span data-ttu-id="53c2d-105">列舉型別</span><span class="sxs-lookup"><span data-stu-id="53c2d-105">Enumeration</span></span>                                                            | <span data-ttu-id="53c2d-106">描述</span><span class="sxs-lookup"><span data-stu-id="53c2d-106">Description</span></span>                                                                                                                                                           |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="53c2d-107">**DRT \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="53c2d-107">**DRT\_SCOPE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_scope)                                        | <span data-ttu-id="53c2d-108">定義在使用 [**DrtCreateIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport)所建立的 ipv6 UDP 傳輸時，將在其中執行的一組 ipv6 範圍。</span><span class="sxs-lookup"><span data-stu-id="53c2d-108">Defines the set of IPv6 scopes in which DRT will operate when using the IPv6 UDP transport created by [**DrtCreateIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport).</span></span> |
| [<span data-ttu-id="53c2d-109">**DRT \_ 位址 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="53c2d-109">**DRT\_ADDRESS\_FLAGS**</span></span>](/windows/desktop/api/drt/ne-drt-drt_address_flags)                       | <span data-ttu-id="53c2d-110">定義在執行索引鍵搜尋時，中繼節點可能會傳回的回應集合。</span><span class="sxs-lookup"><span data-stu-id="53c2d-110">Defines the set of responses that may be returned by an intermediate node when performing a search for a key.</span></span>                                                         |
| [<span data-ttu-id="53c2d-111">**DRT \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="53c2d-111">**DRT\_STATUS**</span></span>](/windows/desktop/api/drt/ne-drt-drt_status)                                      | <span data-ttu-id="53c2d-112">定義本機節點的可能連接和錯誤狀態。</span><span class="sxs-lookup"><span data-stu-id="53c2d-112">Defines the possible connectivity and error states of a local node.</span></span>                                                                                                   |
| [<span data-ttu-id="53c2d-113">**DRT \_ 相符 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="53c2d-113">**DRT\_MATCH\_TYPE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_match_type)                             | <span data-ttu-id="53c2d-114">定義執行搜尋時傳回的結果 exactness。</span><span class="sxs-lookup"><span data-stu-id="53c2d-114">Defines the exactness of results returned when a search is performed.</span></span>                                                                                                 |
| [<span data-ttu-id="53c2d-115">**DRT \_ LEAFSET \_ 金鑰 \_ 變更 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="53c2d-115">**DRT\_LEAFSET\_KEY\_CHANGE\_TYPE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_leafset_key_change_type) | <span data-ttu-id="53c2d-116">定義可以在本機 DRT 快取的本機分葉集節點上執行的一組變更類型。</span><span class="sxs-lookup"><span data-stu-id="53c2d-116">Defines the set of change types that can be performed on a local leaf set node in the local DRT cache.</span></span>                                                                |
| [<span data-ttu-id="53c2d-117">**DRT \_ 事件 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="53c2d-117">**DRT\_EVENT\_TYPE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_event_type)                             | <span data-ttu-id="53c2d-118">定義可由 DRT 引發的事件集。</span><span class="sxs-lookup"><span data-stu-id="53c2d-118">Defines the set of events that can be raised by the DRT.</span></span>                                                                                                              |
| [<span data-ttu-id="53c2d-119">**DRT \_ 安全性 \_ 模式**</span><span class="sxs-lookup"><span data-stu-id="53c2d-119">**DRT\_SECURITY\_MODE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_security_mode)                       | <span data-ttu-id="53c2d-120">定義 DRT 可能的安全性模式。</span><span class="sxs-lookup"><span data-stu-id="53c2d-120">Defines the possible security modes of the DRT.</span></span> <span data-ttu-id="53c2d-121">此列舉型別是一種 [**DRT \_ 設定**](/windows/desktop/api/drt/ns-drt-drt_settings) 結構的欄位。</span><span class="sxs-lookup"><span data-stu-id="53c2d-121">This enumeration is a field of the [**DRT\_SETTINGS**](/windows/desktop/api/drt/ns-drt-drt_settings) structure.</span></span>                                   |
| [<span data-ttu-id="53c2d-122">**DRT \_ 註冊 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="53c2d-122">**DRT\_REGISTRATION\_STATE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_registration_state)             | <span data-ttu-id="53c2d-123">定義已註冊金鑰的狀態。</span><span class="sxs-lookup"><span data-stu-id="53c2d-123">Defines the state of a registered key.</span></span>                                                                                                                                |



 

## <a name="related-topics"></a><span data-ttu-id="53c2d-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="53c2d-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53c2d-125">分散式路由表結構</span><span class="sxs-lookup"><span data-stu-id="53c2d-125">Distributed Routing Table Structures</span></span>](distributed-routing-table-structures.md)
</dt> <dt>

[<span data-ttu-id="53c2d-126">分散式路由表函數</span><span class="sxs-lookup"><span data-stu-id="53c2d-126">Distributed Routing Table Functions</span></span>](distributed-routing-table-functions.md)
</dt> <dt>

[<span data-ttu-id="53c2d-127">分散式路由資料表 API 參考</span><span class="sxs-lookup"><span data-stu-id="53c2d-127">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



