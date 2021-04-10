---
title: In-Process 伺服器
description: In-Process 伺服器
ms.assetid: cc0c4350-fa75-4321-834f-711158776cb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4886932b9669aa2d3cdd49979324f9ccc6e03d44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183465"
---
# <a name="in-process-servers"></a><span data-ttu-id="130c0-103">In-Process 伺服器</span><span class="sxs-lookup"><span data-stu-id="130c0-103">In-Process Servers</span></span>

<span data-ttu-id="130c0-104">如果您將 OLE 伺服器應用程式實作為同進程伺服器，則在容器應用程式的進程空間中執行的 DLL （而不是本機伺服器）會在其本身的進程空間中執行，因為兩者之間的通訊可能會採用一般函式呼叫的形式。</span><span class="sxs-lookup"><span data-stu-id="130c0-104">If you implement an OLE server application as an in-process server — a DLL running in the process space of the container application — rather than as a local server — an EXE running in its own process space — communication between container and server is simplified because communication between the two can take the form of normal function calls.</span></span> <span data-ttu-id="130c0-105">不需要遠端程序呼叫，因為這兩個應用程式會在相同的進程空間中執行。</span><span class="sxs-lookup"><span data-stu-id="130c0-105">Remote procedure calls are not required because the two applications run in the same process space.</span></span> <span data-ttu-id="130c0-106">如您所預期，管理參數封送處理的物件也是不必要的，雖然它們可能會在 DLL 內匯總，而不會干擾容器與伺服器之間的通訊。</span><span class="sxs-lookup"><span data-stu-id="130c0-106">As you would expect, the objects that manage the marshaling of parameters are also unnecessary, although they may be aggregated within the DLL without interfering with the communication between container and server.</span></span>

<span data-ttu-id="130c0-107">當 OLE 伺服器應用程式實作為同進程伺服器時，不需要個別的物件處理常式，因為伺服器本身會存在於用戶端的進程空間中。</span><span class="sxs-lookup"><span data-stu-id="130c0-107">When an OLE server application is implemented as an in-process server, a separate object handler is not required because the server itself lives in the client's process space.</span></span> <span data-ttu-id="130c0-108">同進程伺服器和物件處理常式之間的主要差異在於，當處理常式無法時，伺服器可以管理處于執行中狀態的物件。</span><span class="sxs-lookup"><span data-stu-id="130c0-108">The main difference between an in-process server and object handler is that the server is able to manage the object in a running state while the handler cannot.</span></span> <span data-ttu-id="130c0-109">這項差異的其中一個結果是，伺服器必須提供使用者介面來操作執行中的物件，而處理常式則將這項需求委派給物件的伺服器。</span><span class="sxs-lookup"><span data-stu-id="130c0-109">One consequence of this difference is that a server must provide a user interface for manipulating the running object, while a handler delegates this requirement to the object's server.</span></span> <span data-ttu-id="130c0-110">在建立同進程伺服器的情況下，您可以在 OLE 預設處理常式上匯總，讓它在您只執行處理常式未提供或未以您所需的方式執行的服務時，處理基本的工作，例如顯示、儲存和通知。</span><span class="sxs-lookup"><span data-stu-id="130c0-110">In creating an in-process server, you can aggregate on the OLE default handler, letting it handle basic chores, such as display, storage, and notifications while you implement only those services that the handler either does not provide or does not implement in the way you require.</span></span>

<span data-ttu-id="130c0-111">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="130c0-111">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="130c0-112">優點</span><span class="sxs-lookup"><span data-stu-id="130c0-112">Advantages</span></span>](advantages.md)
-   [<span data-ttu-id="130c0-113">缺點</span><span class="sxs-lookup"><span data-stu-id="130c0-113">Disadvantages</span></span>](disadvantages.md)

## <a name="related-topics"></a><span data-ttu-id="130c0-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="130c0-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="130c0-115">複合檔案</span><span class="sxs-lookup"><span data-stu-id="130c0-115">Compound Documents</span></span>](compound-documents.md)
</dt> </dl>

 

 




