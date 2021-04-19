---
description: 圖形 API 會使用下列結構：
ms.assetid: 6bf06e90-5a1c-461c-8053-93cf4d4bfc95
title: 圖形 API 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85b4c4f5da5a89a821e1abbf669d5eae0c6cb1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980858"
---
# <a name="graphing-api-structures"></a><span data-ttu-id="a256a-103">圖形 API 結構</span><span class="sxs-lookup"><span data-stu-id="a256a-103">Graphing API Structures</span></span>

<span data-ttu-id="a256a-104">圖形 API 會使用下列結構：</span><span class="sxs-lookup"><span data-stu-id="a256a-104">The Graphing API uses the following structures:</span></span>



| <span data-ttu-id="a256a-105">結構</span><span class="sxs-lookup"><span data-stu-id="a256a-105">Structure</span></span>                                                                 | <span data-ttu-id="a256a-106">Description</span><span class="sxs-lookup"><span data-stu-id="a256a-106">Description</span></span>                                                                                                   |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a256a-107">**對等 \_ 事件 \_ 節點 \_ 變更 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="a256a-107">**PEER\_EVENT\_NODE\_CHANGE\_DATA**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_event_node_change_data)    | <span data-ttu-id="a256a-108">如果觸發 **對等 \_ 圖形 \_ 事件 \_ 節點 \_ 變更** 事件，則包含資料的指標。</span><span class="sxs-lookup"><span data-stu-id="a256a-108">Contains a pointer to the data if a **PEER\_GRAPH\_EVENT\_NODE\_CHANGE** event is triggered.</span></span>                  |
| [<span data-ttu-id="a256a-109">**對等 \_ 事件同步處理的 \_ \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="a256a-109">**PEER\_EVENT\_SYNCHRONIZED\_DATA**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_event_synchronized_data)   | <span data-ttu-id="a256a-110">表示已同步處理的記錄類型。</span><span class="sxs-lookup"><span data-stu-id="a256a-110">Indicates the type of record that has been synchronized.</span></span>                                                      |
| [<span data-ttu-id="a256a-111">**對等 \_ 圖形 \_ 事件 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="a256a-111">**PEER\_GRAPH\_EVENT\_DATA**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_data)                 | <span data-ttu-id="a256a-112">包含與對等事件相關聯的資料。</span><span class="sxs-lookup"><span data-stu-id="a256a-112">Contains data associated with a peer event.</span></span>                                                                   |
| [<span data-ttu-id="a256a-113">**對等 \_ 圖形 \_ 事件 \_ 註冊**</span><span class="sxs-lookup"><span data-stu-id="a256a-113">**PEER\_GRAPH\_EVENT\_REGISTRATION**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_registration) | <span data-ttu-id="a256a-114">指定應用程式需要通知的對等事件。</span><span class="sxs-lookup"><span data-stu-id="a256a-114">Specifies which peer events an application requires notifications for.</span></span>                                        |
| [<span data-ttu-id="a256a-115">**對等 \_ 圖形 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="a256a-115">**PEER\_GRAPH\_PROPERTIES**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_graph_properties)                  | <span data-ttu-id="a256a-116">包含對等圖形、識別碼、範圍和其他資訊之原則的相關資料。</span><span class="sxs-lookup"><span data-stu-id="a256a-116">Contains data about the policy of a peer graph, ID, scope, and other information.</span></span>                             |
| [<span data-ttu-id="a256a-117">**對等 \_ 節點 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="a256a-117">**PEER\_NODE\_INFO**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_node_info)                                | <span data-ttu-id="a256a-118">包含對等圖形中特定節點的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="a256a-118">Contains information that is specific to a particular node in a peer graph.</span></span>                                   |
| [<span data-ttu-id="a256a-119">**對等 \_ 安全性 \_ 介面**</span><span class="sxs-lookup"><span data-stu-id="a256a-119">**PEER\_SECURITY\_INTERFACE**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_security_interface)              | <span data-ttu-id="a256a-120">指定對對等圖形 Api 呼叫的安全性介面，以用來驗證、保護和釋放記錄。</span><span class="sxs-lookup"><span data-stu-id="a256a-120">Specifies the security interfaces that calls to Peer Graphing APIs use to validate, secure, and free records.</span></span> |



 

 

 



