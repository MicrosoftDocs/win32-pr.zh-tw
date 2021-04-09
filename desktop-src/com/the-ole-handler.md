---
title: OLE 處理常式
description: OLE 處理常式是一個 DLL，其中包含數個用於連結和內嵌的互動元件。
ms.assetid: 5a01b4be-38cf-4019-ba20-ee67b836a3e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb9579f18b44a36a794ff807d9d616dd3a06dd1b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021519"
---
# <a name="the-ole-handler"></a><span data-ttu-id="87764-103">OLE 處理常式</span><span class="sxs-lookup"><span data-stu-id="87764-103">The OLE Handler</span></span>

<span data-ttu-id="87764-104">*OLE 處理常式* 是一個 DLL，其中包含數個用於連結和內嵌的互動元件。</span><span class="sxs-lookup"><span data-stu-id="87764-104">An *OLE handler* is a DLL containing several interacting components used for linking and embedding.</span></span> <span data-ttu-id="87764-105">為了避免容器與其伺服器之間的固定處理序間通訊，會將處理常式載入容器的進程空間，以代表伺服器作為代理程式的一種方式來執行動作。</span><span class="sxs-lookup"><span data-stu-id="87764-105">To avoid the expense of constant interprocess communication between a container and its server, the handler is loaded into the container's process space to act on behalf of a server as a sort of surrogate process.</span></span> <span data-ttu-id="87764-106">OLE 處理常式會管理不需要注意伺服器應用程式的容器要求，例如繪圖的要求。</span><span class="sxs-lookup"><span data-stu-id="87764-106">The OLE handler manages container requests that do not require the attention of the server application, such as requests for drawing.</span></span> <span data-ttu-id="87764-107">當容器要求物件處理常式無法提供的內容時，處理常式會使用 COM 跨進程通訊機制與伺服器應用程式進行通訊。</span><span class="sxs-lookup"><span data-stu-id="87764-107">When a container requests something that the object handler cannot provide, the handler communicates with the server application using the COM out-of-process communication mechanism.</span></span>

<span data-ttu-id="87764-108">OLE 處理常式元件包含遠端處理元件，可管理處理程式和其伺服器之間的通訊、儲存物件資料的快取 (以及如何格式化和顯示該資料) 的相關資訊，以及可協調 DLL 其他元件活動的控制物件。</span><span class="sxs-lookup"><span data-stu-id="87764-108">The OLE handler components include remoting pieces to manage communication between the handler and its server, a cache for storing an object's data (along with information on how that data should be formatted and displayed), and a controlling object that coordinates the activities of the DLL's other components.</span></span> <span data-ttu-id="87764-109">此外，如果物件是連結，DLL 也會包含連結元件或 *連結的物件*，以追蹤連結來源的名稱和位置。</span><span class="sxs-lookup"><span data-stu-id="87764-109">In addition, if an object is a link, the DLL also includes a linking component, or *linked object*, which keeps track of the name and location of the link source.</span></span>

<span data-ttu-id="87764-110">OLE 提供了一個預設的處理常式，大部分的應用程式都使用這些處理常式來連結和內嵌</span><span class="sxs-lookup"><span data-stu-id="87764-110">OLE provides a default handler that most applications use for linking and embedding.</span></span> <span data-ttu-id="87764-111">如果預設值不符合伺服器的需求，您可以完全取代預設處理常式，或使用它在適當時提供的部分功能。</span><span class="sxs-lookup"><span data-stu-id="87764-111">If the default does not match the requirements of your server, you can either completely replace the default handler or use parts of the functionality it provides where appropriate.</span></span> <span data-ttu-id="87764-112">在後者的情況下，應用程式處理常式會實作為由新控制項物件和預設處理常式組成的匯總物件。</span><span class="sxs-lookup"><span data-stu-id="87764-112">In the latter case, the application handler is implemented as an aggregate object composed of a new control object and the default handler.</span></span> <span data-ttu-id="87764-113">組合應用程式/預設處理常式也稱為同 *進程處理* 程式。</span><span class="sxs-lookup"><span data-stu-id="87764-113">Combination application/default handlers are also known as *in-process handlers*.</span></span> <span data-ttu-id="87764-114">*遠端處理處理常式* 用於未在系統登錄中指派 CLSID 或沒有指定處理常式的物件。</span><span class="sxs-lookup"><span data-stu-id="87764-114">The *remoting handler* is used for objects that are not assigned a CLSID in the system registry or that have no specified handler.</span></span> <span data-ttu-id="87764-115">這些物件類型的處理常式所需的全部都是在整個進程界限之間傳遞資訊。</span><span class="sxs-lookup"><span data-stu-id="87764-115">All that is required from a handler for these types of objects is that they pass information across the process boundary.</span></span> <span data-ttu-id="87764-116">若要建立預設處理常式的新實例，請呼叫 [**OleCreateDefaultHandler**](/windows/desktop/api/Ole2/nf-ole2-olecreatedefaulthandler)。</span><span class="sxs-lookup"><span data-stu-id="87764-116">To create a new instance of the default handler, call [**OleCreateDefaultHandler**](/windows/desktop/api/Ole2/nf-ole2-olecreatedefaulthandler).</span></span> <span data-ttu-id="87764-117">在某些特殊情況下，請呼叫 [**OleCreateEmbeddingHelper**](/windows/desktop/api/Ole2/nf-ole2-olecreateembeddinghelper)。</span><span class="sxs-lookup"><span data-stu-id="87764-117">For some special circumstances, call [**OleCreateEmbeddingHelper**](/windows/desktop/api/Ole2/nf-ole2-olecreateembeddinghelper).</span></span>

<span data-ttu-id="87764-118">當您為某個類別建立處理常式的實例時，您不能將它用於另一個類別。</span><span class="sxs-lookup"><span data-stu-id="87764-118">When you create an instance of a handler for one class, you cannot use it for another.</span></span> <span data-ttu-id="87764-119">用於複合檔案時，當您從遠端存取特定類別的物件時，OLE 處理常式會執行容器端資料結構。</span><span class="sxs-lookup"><span data-stu-id="87764-119">When used for a compound document, the OLE handler implements the container-side data structures when objects of a particular class are accessed remotely.</span></span>

<span data-ttu-id="87764-120">OLE 定義了複合檔案本機伺服器用戶端的預設處理常式。</span><span class="sxs-lookup"><span data-stu-id="87764-120">OLE defined the default handler for clients of compound document local servers.</span></span> <span data-ttu-id="87764-121">預設處理常式會執行一般伺服器不會執行的一些介面。</span><span class="sxs-lookup"><span data-stu-id="87764-121">The default handler implemented a number of interfaces that the typical server did not.</span></span> <span data-ttu-id="87764-122">當 OLE 之後允許複合檔案的同進程伺服器時，他們必須建立內嵌協助程式來執行這些額外的介面，讓用戶端可以順暢地使用它們。</span><span class="sxs-lookup"><span data-stu-id="87764-122">When OLE subsequently allowed in-process servers for compound documents, they had to create an embedding helper that implemented these extra interfaces so that clients could seamlessly work with them.</span></span>

<span data-ttu-id="87764-123">定義和執行用戶端處理常式的架構設計人員應該在其設計中考慮這個問題，而且應該為相同的原因提供同等的同進程 helper。</span><span class="sxs-lookup"><span data-stu-id="87764-123">Framework designers that define and implement a client-side handler should consider this issue in their design and should provide an equivalent in-process helper for the same reasons.</span></span> <span data-ttu-id="87764-124">即使設計工具目前未在伺服器不公開的處理常式上執行介面，它們仍可能想要立即定義協助程式，以便日後可以加入。</span><span class="sxs-lookup"><span data-stu-id="87764-124">Even if the designers currently don't implement interfaces on the handler that the servers don't expose, they may want to define a helper now so that they can add them in the future.</span></span> <span data-ttu-id="87764-125">或者，您可以在伺服器物件本身上執行額外的介面。</span><span class="sxs-lookup"><span data-stu-id="87764-125">Alternatively, one could implement the extra interfaces on the server object itself.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87764-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="87764-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87764-127">輕量 Client-Side 處理常式</span><span class="sxs-lookup"><span data-stu-id="87764-127">The Lightweight Client-Side Handler</span></span>](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 




