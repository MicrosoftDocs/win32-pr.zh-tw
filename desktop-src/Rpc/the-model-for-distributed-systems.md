---
title: 分散式系統的模型
description: 傳統上，在多部電腦上執行整合型系統，表示將系統分割成不同的用戶端和伺服器元件。
ms.assetid: 6055bcef-e34c-4f2d-92b9-9aec75cf3cec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82cd1ea3301d68e77562a63c542bc075692e5192
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932042"
---
# <a name="the-model-for-distributed-systems"></a><span data-ttu-id="31ca4-103">分散式系統的模型</span><span class="sxs-lookup"><span data-stu-id="31ca4-103">The Model for Distributed Systems</span></span>

<span data-ttu-id="31ca4-104">傳統上，在多部電腦上執行整合型系統，表示將系統分割成不同的用戶端和伺服器元件。</span><span class="sxs-lookup"><span data-stu-id="31ca4-104">Traditionally, having a monolithic system run across multiple computers meant splitting the system into separate client and server components.</span></span> <span data-ttu-id="31ca4-105">在這類系統中，用戶端元件會處理使用者介面和伺服器提供的後端處理，例如資料庫存取、列印等等。</span><span class="sxs-lookup"><span data-stu-id="31ca4-105">In such systems, the client component handled the user interface and the server provided back-end processing, such as database access, printing, and so on.</span></span> <span data-ttu-id="31ca4-106">隨著電腦的擴散、降低成本，以及變成經過更高頻寬的網路連線，將軟體系統分割成多個元件變得更方便，每個元件都在不同的電腦上執行，並執行特殊功能。</span><span class="sxs-lookup"><span data-stu-id="31ca4-106">As computers proliferated, dropped in cost, and became connected by ever-higher bandwidth networks, splitting software systems into multiple components became more convenient, with each component running on a different computer and performing a specialized function.</span></span> <span data-ttu-id="31ca4-107">這種方法簡化了開發、管理、系統管理，而且通常會改善效能和穩定性，因為一部電腦的失敗不一定會停用整個系統。</span><span class="sxs-lookup"><span data-stu-id="31ca4-107">This approach simplified development, management, administration, and often improved performance and robustness, since failure in one computer did not necessarily disable the entire system.</span></span>

<span data-ttu-id="31ca4-108">在許多情況下，系統會以不透明的雲端形式出現在執行必要作業的用戶端，即使分散式系統是由個別節點組成，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="31ca4-108">In many cases the system appears to the client as an opaque cloud that performs the necessary operations, even though the distributed system is composed of individual nodes, as illustrated in the following figure.</span></span>

![用戶端會在以不透明雲端形式出現在用戶端外部的 rpc 伺服器系統中存取服務](images/indy-nodes.png)

<span data-ttu-id="31ca4-110">因為會代表用戶端叫用計算作業，所以會維護雲端的不透明度。</span><span class="sxs-lookup"><span data-stu-id="31ca4-110">The opacity of the cloud is maintained because computing operations are invoked on behalf of the client.</span></span> <span data-ttu-id="31ca4-111">因此，用戶端可以在雲端中找出 (*節點*) 的電腦，並要求指定的作業;在執行此作業時，該電腦可以在雲端中的其他電腦上叫用功能，而不會將其他步驟或其執行所在的電腦公開至用戶端。</span><span class="sxs-lookup"><span data-stu-id="31ca4-111">As such, clients can locate a computer (a *node*) within the cloud and request a given operation; in performing the operation, that computer can invoke functionality on other computers within the cloud without exposing the additional steps, or the computer on which they were carried out, to the client.</span></span>

<span data-ttu-id="31ca4-112">在此範例中，分散式、類似雲端的系統的機制可細分為許多個別的封包交換，或個別節點之間的交談。</span><span class="sxs-lookup"><span data-stu-id="31ca4-112">With this paradigm, the mechanics of a distributed, cloud-like system can be broken down into many individual packet exchanges, or conversations between individual nodes.</span></span>

<span data-ttu-id="31ca4-113">傳統的用戶端-伺服器系統有兩個節點具有固定角色和責任。</span><span class="sxs-lookup"><span data-stu-id="31ca4-113">Traditional client-server systems have two nodes with fixed roles and responsibilities.</span></span> <span data-ttu-id="31ca4-114">新式分散式系統可以有兩個以上的節點，而其角色通常是動態的。</span><span class="sxs-lookup"><span data-stu-id="31ca4-114">Modern-distributed systems can have more than two nodes, and their roles are often dynamic.</span></span> <span data-ttu-id="31ca4-115">在一個對話中，節點可以是用戶端，而在另一個對話中，節點可以是伺服器。</span><span class="sxs-lookup"><span data-stu-id="31ca4-115">In one conversation a node can be a client, while in another conversation the node can be the server.</span></span> <span data-ttu-id="31ca4-116">在許多情況下，公開功能的最終取用者是使用者坐在鍵盤上的用戶端，以監看輸出。</span><span class="sxs-lookup"><span data-stu-id="31ca4-116">In many cases, the ultimate consumer of the exposed functionality is a client with a user sitting at a keyboard, watching the output.</span></span> <span data-ttu-id="31ca4-117">在其他情況下，分散式系統會自動執行背景作業。</span><span class="sxs-lookup"><span data-stu-id="31ca4-117">In other cases the distributed system functions unattended, performing background operations.</span></span>

<span data-ttu-id="31ca4-118">分散式系統可能沒有專用的用戶端和伺服器可用於每個特定的封包交換，但請務必記住，有呼叫端、 (或啟動器，其中之一通常稱為用戶端) 。</span><span class="sxs-lookup"><span data-stu-id="31ca4-118">The distributed system may not have dedicated clients and servers for each particular packet exchange, but it is important to remember there is a caller, (or initiator, either of which is often referred to as the client).</span></span> <span data-ttu-id="31ca4-119">另外還有呼叫的收件者 (通常稱為伺服器) 。</span><span class="sxs-lookup"><span data-stu-id="31ca4-119">There is also the recipient of the call (often referred to as the server).</span></span> <span data-ttu-id="31ca4-120">不需要以分散式系統的要求-回復格式進行雙向封包交換;訊息通常只會傳送一種方式。</span><span class="sxs-lookup"><span data-stu-id="31ca4-120">It is not necessary to have two-way packet exchanges in the request-reply format of a distributed system; often messages are sent only one way.</span></span>

 

 




