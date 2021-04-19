---
description: 郵筒是位於記憶體中的 pseudofile，而且您會使用標準的檔案函式來存取它。
ms.assetid: 9a68905d-c235-4c72-bc71-1cccdf5cdadc
title: 關於 Mailslots
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bd83fc0d952577efdb149d4c7f25fffbab9784f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997272"
---
# <a name="about-mailslots"></a><span data-ttu-id="a82f6-103">關於 Mailslots</span><span class="sxs-lookup"><span data-stu-id="a82f6-103">About Mailslots</span></span>

<span data-ttu-id="a82f6-104">郵筒是位於記憶體中的 pseudofile，而且您會使用標準的檔案函式來存取它。</span><span class="sxs-lookup"><span data-stu-id="a82f6-104">A mailslot is a pseudofile that resides in memory, and you use standard file functions to access it.</span></span> <span data-ttu-id="a82f6-105">郵筒訊息中的資料可以是任何形式，但在電腦之間傳送時不能大於424位元組。</span><span class="sxs-lookup"><span data-stu-id="a82f6-105">The data in a mailslot message can be in any form, but cannot be larger than 424 bytes when sent between computers.</span></span> <span data-ttu-id="a82f6-106">不同于磁片檔案，mailslots 是暫時性的。</span><span class="sxs-lookup"><span data-stu-id="a82f6-106">Unlike disk files, mailslots are temporary.</span></span> <span data-ttu-id="a82f6-107">當郵筒的所有控制碼都關閉時，會刪除信箱和其包含的所有資料。</span><span class="sxs-lookup"><span data-stu-id="a82f6-107">When all handles to a mailslot are closed, the mailslot and all the data it contains are deleted.</span></span>

<span data-ttu-id="a82f6-108">*郵筒伺服器* 是建立並擁有郵筒的進程。</span><span class="sxs-lookup"><span data-stu-id="a82f6-108">A *mailslot server* is a process that creates and owns a mailslot.</span></span> <span data-ttu-id="a82f6-109">當伺服器建立信箱時，它會接收信箱控制碼。</span><span class="sxs-lookup"><span data-stu-id="a82f6-109">When the server creates a mailslot, it receives a mailslot handle.</span></span> <span data-ttu-id="a82f6-110">當進程從郵件傳送程式讀取訊息時，必須使用這個控制碼。</span><span class="sxs-lookup"><span data-stu-id="a82f6-110">This handle must be used when a process reads messages from the mailslot.</span></span> <span data-ttu-id="a82f6-111">只有建立郵筒的進程，或已透過其他機制取得控制碼 (例如繼承) 可以從信箱讀取。</span><span class="sxs-lookup"><span data-stu-id="a82f6-111">Only the process that creates a mailslot or has obtained the handle by some other mechanism (such as inheritance) can read from the mailslot.</span></span> <span data-ttu-id="a82f6-112">所有的 mailslots 都是建立它們的進程的本機。</span><span class="sxs-lookup"><span data-stu-id="a82f6-112">All mailslots are local to the process that creates them.</span></span> <span data-ttu-id="a82f6-113">進程無法建立遠端郵筒。</span><span class="sxs-lookup"><span data-stu-id="a82f6-113">A process cannot create a remote mailslot.</span></span>

<span data-ttu-id="a82f6-114">*郵筒用戶端* 是將訊息寫入郵筒的進程。</span><span class="sxs-lookup"><span data-stu-id="a82f6-114">A *mailslot client* is a process that writes a message to a mailslot.</span></span> <span data-ttu-id="a82f6-115">任何具有信箱名稱的進程都可以在該處放入訊息。</span><span class="sxs-lookup"><span data-stu-id="a82f6-115">Any process that has the name of a mailslot can put a message there.</span></span> <span data-ttu-id="a82f6-116">新的訊息會在信箱中的任何現有訊息之後。</span><span class="sxs-lookup"><span data-stu-id="a82f6-116">New messages follow any existing messages in the mailslot.</span></span>

<span data-ttu-id="a82f6-117">Mailslots 可以廣播網域內的訊息。</span><span class="sxs-lookup"><span data-stu-id="a82f6-117">Mailslots can broadcast messages within a domain.</span></span> <span data-ttu-id="a82f6-118">如果網域中的數個進程每個都使用相同的名稱來建立一個信箱，則參與的進程就會收到每個定址至該信箱並傳送至網域的訊息。</span><span class="sxs-lookup"><span data-stu-id="a82f6-118">If several processes in a domain each create a mailslot using the same name, every message that is addressed to that mailslot and sent to the domain is received by the participating processes.</span></span> <span data-ttu-id="a82f6-119">因為一個進程可以同時控制伺服器信箱控制碼和用戶端控制碼，當打開封入器開啟進行寫入作業時，應用程式可以輕鬆地在網域內執行簡單的訊息傳遞功能。</span><span class="sxs-lookup"><span data-stu-id="a82f6-119">Because one process can control both a server mailslot handle and the client handle retrieved when the mailslot is opened for a write operation, applications can easily implement a simple message-passing facility within a domain.</span></span>

<span data-ttu-id="a82f6-120">若要在電腦之間傳送大於424位元組的訊息，請改用 [具名管道](named-pipes.md) 或 [Windows 通訊端](/windows/desktop/WinSock/windows-sockets-start-page-2) 。</span><span class="sxs-lookup"><span data-stu-id="a82f6-120">To send messages that are larger than 424 bytes between computers, use [named pipes](named-pipes.md) or [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2) instead.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a82f6-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="a82f6-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a82f6-122">郵筒名稱</span><span class="sxs-lookup"><span data-stu-id="a82f6-122">Mailslot Names</span></span>](mailslot-names.md)
</dt> <dt>

[<span data-ttu-id="a82f6-123">郵筒作業</span><span class="sxs-lookup"><span data-stu-id="a82f6-123">Mailslot Operations</span></span>](mailslot-operations.md)
</dt> </dl>

 

 
