---
title: 動態虛擬通道
description: 動態虛擬通道 (DVC) Api 擴充現有的虛擬通道 Api，以供遠端桌面服務（稱為靜態虛擬通道 (SVC) Api）。
ms.assetid: bddf0048-482d-40f3-a973-9d7bc15be8fa
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3181c0960b50289846018c3ace773a8351cb20
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372145"
---
# <a name="dynamic-virtual-channels"></a><span data-ttu-id="8fd45-103">動態虛擬通道</span><span class="sxs-lookup"><span data-stu-id="8fd45-103">Dynamic Virtual Channels</span></span>

<span data-ttu-id="8fd45-104">動態虛擬通道 (DVC) Api 擴充現有的虛擬通道 Api，以供遠端桌面服務（稱為靜態虛擬通道 (SVC) Api）。</span><span class="sxs-lookup"><span data-stu-id="8fd45-104">Dynamic virtual channel (DVC) APIs extend the existing virtual channel APIs for Remote Desktop Services, known as static virtual channel (SVC) APIs.</span></span> <span data-ttu-id="8fd45-105">DVC Api 可解決用戶端與伺服器之間的 SVC Api 中存在的數個限制，例如：</span><span class="sxs-lookup"><span data-stu-id="8fd45-105">DVC APIs address several limitations that existed in SVC APIs between the client and server, such as:</span></span>

-   <span data-ttu-id="8fd45-106">頻道數量有限</span><span class="sxs-lookup"><span data-stu-id="8fd45-106">A limited number of channels</span></span>
-   <span data-ttu-id="8fd45-107">封包重建</span><span class="sxs-lookup"><span data-stu-id="8fd45-107">Packet reconstruction</span></span>

<span data-ttu-id="8fd45-108">DVC Api 將協助您在伺服器和用戶端上，在與彼此通訊的遠端桌面服務連接上執行模組。</span><span class="sxs-lookup"><span data-stu-id="8fd45-108">DVC APIs will help you to implement modules on the server and client side of a Remote Desktop Services connection that communicate with each other.</span></span>

<span data-ttu-id="8fd45-109">就像許多其他用戶端/伺服器架構一樣，系統會根據常同意的資料片段（稱為端點）來建立連接。</span><span class="sxs-lookup"><span data-stu-id="8fd45-109">Like many other client/server architectures, a connection is established based on a commonly agreed upon piece of data, referred to as an endpoint.</span></span> <span data-ttu-id="8fd45-110">類似的範例是 TCP/IP，也就是透過伺服器 IP 位址和埠名稱的組合來建立端點。</span><span class="sxs-lookup"><span data-stu-id="8fd45-110">A similar example is TCP/IP, where an endpoint is established through a combination of server IP address and the port name.</span></span> <span data-ttu-id="8fd45-111">另一個範例是具名管道，其中端點是伺服器名稱和管道名稱的組合。</span><span class="sxs-lookup"><span data-stu-id="8fd45-111">Another example is named pipes, where an endpoint is a combination of the server name and the pipe name.</span></span> <span data-ttu-id="8fd45-112">在遠端桌面服務連接中，只涉及兩個邊。</span><span class="sxs-lookup"><span data-stu-id="8fd45-112">In a Remote Desktop Services connection there are only two sides involved.</span></span> <span data-ttu-id="8fd45-113">因此，端點是由可唯一識別連接的簡單任一字元串所組成。</span><span class="sxs-lookup"><span data-stu-id="8fd45-113">Therefore, the endpoint consists of a simple arbitrary string that uniquely identifies the connection.</span></span> <span data-ttu-id="8fd45-114">就像 TCP/IP 和具名管道一樣，可以從相同的端點名稱起始多個連接。</span><span class="sxs-lookup"><span data-stu-id="8fd45-114">Much like TCP/IP and named pipes, multiple connections can initiate from the same endpoint name.</span></span> <span data-ttu-id="8fd45-115">在這種情況下，連接沒有名稱;只有接聽程式會等候端點上的傳入要求。</span><span class="sxs-lookup"><span data-stu-id="8fd45-115">In that sense, connections do not have names; just a listener that waits for incoming requests on the endpoint.</span></span>

<span data-ttu-id="8fd45-116">DVC Api 包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="8fd45-116">The DVC APIs consist of the following:</span></span>

-   <span data-ttu-id="8fd45-117">用戶端 API</span><span class="sxs-lookup"><span data-stu-id="8fd45-117">Client APIs</span></span>

    <span data-ttu-id="8fd45-118">這些 Api 可在遠端桌面連線 (RDC) 用戶端以外掛程式的形式提供。</span><span class="sxs-lookup"><span data-stu-id="8fd45-118">These APIs are available in the Remote Desktop Connection (RDC) client as a plug-in.</span></span> <span data-ttu-id="8fd45-119">用戶端處於被動模式，它會接聽連入連線，但不會主動建立連線。</span><span class="sxs-lookup"><span data-stu-id="8fd45-119">The client side is in passive mode, where it listens for incoming connections but does not actively establish a connection.</span></span>

-   <span data-ttu-id="8fd45-120">伺服器 Api</span><span class="sxs-lookup"><span data-stu-id="8fd45-120">Server APIs</span></span>

    <span data-ttu-id="8fd45-121">這些 Api 會主動起始連接。</span><span class="sxs-lookup"><span data-stu-id="8fd45-121">These APIs actively initiate the connection.</span></span>

<span data-ttu-id="8fd45-122">如需如何將動態虛擬通道寫入 (DVC) 模組的相關資訊，請參閱 [DVC 的實作為詳細資料](dvc-implementation-details.md)。</span><span class="sxs-lookup"><span data-stu-id="8fd45-122">For information about how to write a dynamic virtual channel (DVC) module, see [DVC Implementation Details](dvc-implementation-details.md).</span></span>

 

 




