---
description: 與多個管道用戶端通訊以及服務多個管道實例的策略。
ms.assetid: c764bde5-e053-4124-b859-1d2839ada918
title: 具名管道實例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b7d1ec591996e83853ae6faede899ecd4e4ea2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985007"
---
# <a name="named-pipe-instances"></a><span data-ttu-id="8a6e0-103">具名管道實例</span><span class="sxs-lookup"><span data-stu-id="8a6e0-103">Named Pipe Instances</span></span>

<span data-ttu-id="8a6e0-104">最簡單的管道伺服器會建立一個管道的單一實例、連接到單一用戶端、與用戶端進行通訊、中斷與用戶端的連線、關閉管道控制碼，然後終止。</span><span class="sxs-lookup"><span data-stu-id="8a6e0-104">The simplest pipe server creates a single instance of a pipe, connects to a single client, communicates with the client, disconnects from the client, closes the pipe handle, and terminates.</span></span> <span data-ttu-id="8a6e0-105">不過，管道伺服器與多個管道用戶端的通訊比較常見。</span><span class="sxs-lookup"><span data-stu-id="8a6e0-105">However, it is more common for a pipe server to communicate with multiple pipe clients.</span></span> <span data-ttu-id="8a6e0-106">管道伺服器可以透過連接到每個用戶端，並從每個用戶端中斷連線，使用單一管道實例連接多個管道用戶端，但效能會變差。</span><span class="sxs-lookup"><span data-stu-id="8a6e0-106">A pipe server could use a single pipe instance to connect with multiple pipe clients by connecting to and disconnecting from each client in sequence, but performance would be poor.</span></span> <span data-ttu-id="8a6e0-107">管道伺服器必須建立多個管道實例，才能有效率地同時處理多個用戶端。</span><span class="sxs-lookup"><span data-stu-id="8a6e0-107">The pipe server must create multiple pipe instances to efficiently handle multiple clients simultaneously.</span></span>

<span data-ttu-id="8a6e0-108">有三種基本策略可提供多個管道實例的服務。</span><span class="sxs-lookup"><span data-stu-id="8a6e0-108">There are three basic strategies for servicing multiple pipe instances.</span></span>

-   <span data-ttu-id="8a6e0-109">為每個管道實例建立個別的執行緒。</span><span class="sxs-lookup"><span data-stu-id="8a6e0-109">Create a separate thread for each instance of the pipe.</span></span> <span data-ttu-id="8a6e0-110">如需多執行緒管道伺服器的範例，請參閱 [多執行緒管道伺服器](multithreaded-pipe-server.md)。</span><span class="sxs-lookup"><span data-stu-id="8a6e0-110">For an example of a multithreaded pipe server, see [Multithreaded Pipe Server](multithreaded-pipe-server.md).</span></span>
-   <span data-ttu-id="8a6e0-111">藉由在 [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)、 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)和 [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)函數中指定重迭 [**的結構，**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)來使用重迭的作業。</span><span class="sxs-lookup"><span data-stu-id="8a6e0-111">Use overlapped operations by specifying an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure in the [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), and [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) functions.</span></span> <span data-ttu-id="8a6e0-112">如需範例，請參閱使用重迭 [i/o 的具名管道伺服器](named-pipe-server-using-overlapped-i-o.md)。</span><span class="sxs-lookup"><span data-stu-id="8a6e0-112">For an example, see [Named Pipe Server Using Overlapped I/O](named-pipe-server-using-overlapped-i-o.md).</span></span>
-   <span data-ttu-id="8a6e0-113">使用 [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) 和 [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) 函數來使用重迭的作業，這會指定完成作業時要執行的完成常式。</span><span class="sxs-lookup"><span data-stu-id="8a6e0-113">Use overlapped operations by using the [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) and [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) functions, which specify a completion routine to be executed when the operation is completed.</span></span> <span data-ttu-id="8a6e0-114">如需範例，請參閱 [使用完成常式的具名管道伺服器](named-pipe-server-using-completion-routines.md)。</span><span class="sxs-lookup"><span data-stu-id="8a6e0-114">For an example, see [Named Pipe Server Using Completion Routines](named-pipe-server-using-completion-routines.md).</span></span>

<span data-ttu-id="8a6e0-115">多執行緒管道伺服器最容易寫入，因為每個實例的執行緒都會處理單一管道用戶端的通訊。</span><span class="sxs-lookup"><span data-stu-id="8a6e0-115">The multithreaded pipe server is easiest to write, because the thread for each instance handles communications for a single pipe client.</span></span> <span data-ttu-id="8a6e0-116">系統會視需要將處理器時間分配給每個執行緒。</span><span class="sxs-lookup"><span data-stu-id="8a6e0-116">The system allocates processor time to each thread as needed.</span></span> <span data-ttu-id="8a6e0-117">但每個執行緒都使用系統資源，這是處理大量用戶端之管道伺服器的缺點。</span><span class="sxs-lookup"><span data-stu-id="8a6e0-117">But each thread uses system resources, which is a disadvantage for a pipe server that handles a large number of clients.</span></span>

<span data-ttu-id="8a6e0-118">使用單一執行緒的伺服器，可以更輕鬆地協調影響多個用戶端的作業，而且可以更輕鬆地保護共用資源，使其無法同時存取多個用戶端。</span><span class="sxs-lookup"><span data-stu-id="8a6e0-118">With a single-threaded server, it is easier to coordinate operations that affect multiple clients, and it is easier to protect shared resources from simultaneous access by multiple clients.</span></span> <span data-ttu-id="8a6e0-119">單一執行緒伺服器的挑戰是需要協調重迭的作業，以配置處理器時間來處理用戶端的同時需求。</span><span class="sxs-lookup"><span data-stu-id="8a6e0-119">The challenge of a single-threaded server is that it requires coordination of overlapped operations to allocate processor time for handling the simultaneous needs of clients.</span></span>

 

 
