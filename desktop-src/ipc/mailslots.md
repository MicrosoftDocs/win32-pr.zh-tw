---
description: 郵筒是單向處理序間通訊的一種機制， (IPC) 。 應用程式可以將訊息儲存在信箱中。 郵筒的擁有者可以取出儲存在該處的訊息。
ms.assetid: e23894ca-edc7-49e6-bcc4-c82f357ecedf
title: Mailslots
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6886e8d6f08206c6104db22c050aa6bb9859f96f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975264"
---
# <a name="mailslots"></a><span data-ttu-id="e59fd-105">Mailslots</span><span class="sxs-lookup"><span data-stu-id="e59fd-105">Mailslots</span></span>

<span data-ttu-id="e59fd-106">*郵筒* 是單向處理序間通訊的一種機制， (IPC) 。</span><span class="sxs-lookup"><span data-stu-id="e59fd-106">A *mailslot* is a mechanism for one-way interprocess communications (IPC).</span></span> <span data-ttu-id="e59fd-107">應用程式可以將訊息儲存在信箱中。</span><span class="sxs-lookup"><span data-stu-id="e59fd-107">Applications can store messages in a mailslot.</span></span> <span data-ttu-id="e59fd-108">郵筒的擁有者可以取出儲存在該處的訊息。</span><span class="sxs-lookup"><span data-stu-id="e59fd-108">The owner of the mailslot can retrieve messages that are stored there.</span></span> <span data-ttu-id="e59fd-109">這些訊息通常會透過網路傳送到指定的電腦或指定網域中的所有電腦。</span><span class="sxs-lookup"><span data-stu-id="e59fd-109">These messages are typically sent over a network to either a specified computer or to all computers in a specified domain.</span></span> <span data-ttu-id="e59fd-110">*網域* 是共用組名的一組工作站和伺服器。</span><span class="sxs-lookup"><span data-stu-id="e59fd-110">A *domain* is a group of workstations and servers that share a group name.</span></span>

-   [<span data-ttu-id="e59fd-111">關於 Mailslots</span><span class="sxs-lookup"><span data-stu-id="e59fd-111">About Mailslots</span></span>](about-mailslots.md)
-   [<span data-ttu-id="e59fd-112">使用 Mailslots</span><span class="sxs-lookup"><span data-stu-id="e59fd-112">Using Mailslots</span></span>](using-mailslots.md)
-   [<span data-ttu-id="e59fd-113">郵筒參考</span><span class="sxs-lookup"><span data-stu-id="e59fd-113">Mailslot Reference</span></span>](mailslot-reference.md)

<span data-ttu-id="e59fd-114">您可以選擇使用 [具名管道](named-pipes.md) 或 [Windows 通訊端](/windows/desktop/WinSock/windows-sockets-start-page-2) ，而非 mailslots 進行處理序間通訊。</span><span class="sxs-lookup"><span data-stu-id="e59fd-114">You can choose to use [named pipes](named-pipes.md) or [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2) instead of mailslots for interprocess communications.</span></span> <span data-ttu-id="e59fd-115">具名管道是一種簡單的方法，可讓兩個進程交換訊息。</span><span class="sxs-lookup"><span data-stu-id="e59fd-115">Named pipes are a simple way for two processes to exchange messages.</span></span> <span data-ttu-id="e59fd-116">相反地，Mailslots 是一種簡單的方式，可讓程式將訊息廣播至多個進程。</span><span class="sxs-lookup"><span data-stu-id="e59fd-116">Mailslots, on the other hand, are a simple way for a process to broadcast messages to multiple processes.</span></span> <span data-ttu-id="e59fd-117">其中一個重要的考慮是 mailslots 使用資料包廣播訊息。</span><span class="sxs-lookup"><span data-stu-id="e59fd-117">One important consideration is that mailslots broadcast messages using datagrams.</span></span> <span data-ttu-id="e59fd-118">*資料包* 是網路在網路上傳送的小型資訊封包。</span><span class="sxs-lookup"><span data-stu-id="e59fd-118">A *datagram* is a small packet of information that the network sends along the wire.</span></span> <span data-ttu-id="e59fd-119">和無線電或電視廣播一樣，資料包不會提供回條的確認;沒有任何方法可保證已收到資料包。</span><span class="sxs-lookup"><span data-stu-id="e59fd-119">Like a radio or television broadcast, a datagram offers no confirmation of receipt; there is no way to guarantee that a datagram has been received.</span></span> <span data-ttu-id="e59fd-120">就像山脈、大型建築或干擾信號可能會導致無線電或電視信號遺失，有一些東西可以防止資料包到達特定目的地。</span><span class="sxs-lookup"><span data-stu-id="e59fd-120">Just as mountains, large buildings, or interfering signals might cause a radio or television signal to get lost, there are things that can prevent a datagram from reaching a particular destination.</span></span> <span data-ttu-id="e59fd-121">具名管道就像電話一樣：您只會與一個合作物件通訊，但您知道訊息正在接收。</span><span class="sxs-lookup"><span data-stu-id="e59fd-121">Named pipes are like telephone calls: you talk only to one party, but you know that the message is being received.</span></span>

 

 
