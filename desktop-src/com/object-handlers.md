---
title: 物件處理常式
description: 物件處理常式
ms.assetid: a5b51e07-246d-42a2-b33f-2bd0c608f41a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7294ddd48d2acaa010ad15c0e2497fd33c7f071
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839528"
---
# <a name="object-handlers"></a><span data-ttu-id="dddb0-103">物件處理常式</span><span class="sxs-lookup"><span data-stu-id="dddb0-103">Object Handlers</span></span>

<span data-ttu-id="dddb0-104">如果 OLE 伺服器應用程式是本機伺服器，這表示它會在自己的進程空間中執行，則容器與伺服器之間的通訊必須跨進程界限進行。</span><span class="sxs-lookup"><span data-stu-id="dddb0-104">If an OLE server application is a local server, meaning that it runs in its own process space, communication between container and server must occur across process boundaries.</span></span> <span data-ttu-id="dddb0-105">因為這個程式很昂貴，所以 OLE 依賴載入容器進程空間的代理物件來代表本機伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="dddb0-105">Because this process is expensive, OLE relies on a surrogate object loaded into the container's process space to act on behalf of a local server application.</span></span> <span data-ttu-id="dddb0-106">這個代理物件（稱為 *物件處理常式*）是不需要注意伺服器應用程式的服務容器要求，例如繪圖的要求。</span><span class="sxs-lookup"><span data-stu-id="dddb0-106">This surrogate object, known as an *object handler*, services container requests that do not require the attention of the server application, such as requests for drawing.</span></span> <span data-ttu-id="dddb0-107">當容器要求物件處理常式無法提供的內容時，處理常式會使用 COM 的跨進程通訊機制與伺服器應用程式進行通訊。</span><span class="sxs-lookup"><span data-stu-id="dddb0-107">When a container requests something that the object handler cannot provide, the handler communicates with the server application using COM's out-of-process communication mechanism.</span></span>

<span data-ttu-id="dddb0-108">物件處理常式對物件類別而言是唯一的。</span><span class="sxs-lookup"><span data-stu-id="dddb0-108">An object handler is unique to an object class.</span></span> <span data-ttu-id="dddb0-109">當您為某個類別建立處理常式的實例時，您不能將它用於另一個類別。</span><span class="sxs-lookup"><span data-stu-id="dddb0-109">When you create an instance of a handler for one class, you cannot use it for another.</span></span> <span data-ttu-id="dddb0-110">用於複合檔案時，當您從遠端存取特定類別的物件時，物件處理常式會執行容器端資料結構。</span><span class="sxs-lookup"><span data-stu-id="dddb0-110">When used for a compound document, the object handler implements the container-side data structures when objects of a particular class are accessed remotely.</span></span>

<span data-ttu-id="dddb0-111">OLE 提供可讓本機伺服器應用程式使用的預設物件處理常式。</span><span class="sxs-lookup"><span data-stu-id="dddb0-111">OLE provides a default object handler that local server applications can use.</span></span> <span data-ttu-id="dddb0-112">對於需要特殊行為的應用程式，開發人員可以執行自訂處理常式來取代預設處理常式，或使用它來提供特定的預設行為。</span><span class="sxs-lookup"><span data-stu-id="dddb0-112">For applications that require special behaviors, developers can implement a custom handler that either replaces the default handler or uses it to provide certain default behaviors.</span></span>

<span data-ttu-id="dddb0-113">物件處理常式是包含數個互動元件的 DLL。</span><span class="sxs-lookup"><span data-stu-id="dddb0-113">An object handler is a DLL containing several interacting components.</span></span> <span data-ttu-id="dddb0-114">這些元件包括遠端處理元件，以管理處理程式與其伺服器應用程式之間的通訊、儲存物件資料的快取，以及如何格式化和顯示該資料的相關資訊，以及可協調 DLL 其他元件活動的控制物件。</span><span class="sxs-lookup"><span data-stu-id="dddb0-114">These components include remoting pieces to manage communication between the handler and its server application, a cache for storing an object's data, along with information on how that data should be formatted and displayed, and a controlling object that coordinates the activities of the DLL's other components.</span></span> <span data-ttu-id="dddb0-115">此外，如果物件是連結，DLL 也會包含連結元件或 *連結的物件*，以追蹤連結來源的名稱和位置。</span><span class="sxs-lookup"><span data-stu-id="dddb0-115">In addition, if an object is a link, the DLL also includes a linking component, or *linked object*, which keeps track of the name and location of the link source.</span></span>

<span data-ttu-id="dddb0-116">快 *取包含足夠* 的資料和呈現資訊，可讓處理常式在其容器中顯示已載入但未執行的物件。</span><span class="sxs-lookup"><span data-stu-id="dddb0-116">The *cache* contains data and presentation information sufficient for the handler to display a loaded, but not running, object in its container.</span></span> <span data-ttu-id="dddb0-117">OLE 提供 OLE 的預設物件處理常式和連結化物件所使用之快取的執行。</span><span class="sxs-lookup"><span data-stu-id="dddb0-117">OLE provides an implementation of the cache used by OLE's default object handler and the link object.</span></span> <span data-ttu-id="dddb0-118">快取會以物件處理常式所需的格式來儲存資料，以滿足容器繪製要求。</span><span class="sxs-lookup"><span data-stu-id="dddb0-118">The cache stores data in formats needed by the object handler to satisfy container draw requests.</span></span> <span data-ttu-id="dddb0-119">當物件的資料變更時，物件會將通知傳送至快取，以便進行更新。</span><span class="sxs-lookup"><span data-stu-id="dddb0-119">When an object's data changes, the object sends a notification to the cache so that an update can occur.</span></span> <span data-ttu-id="dddb0-120">如需快取的詳細資訊，請參閱 [View](view-caching.md)cache。</span><span class="sxs-lookup"><span data-stu-id="dddb0-120">For more information on the cache, see [View Caching](view-caching.md).</span></span>

<span data-ttu-id="dddb0-121">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="dddb0-121">For more information, see the following topic:</span></span>

-   [<span data-ttu-id="dddb0-122">預設處理常式和自訂處理常式</span><span class="sxs-lookup"><span data-stu-id="dddb0-122">The Default Handler and Custom Handlers</span></span>](the-default-handler-and-custom-handlers.md)

## <a name="related-topics"></a><span data-ttu-id="dddb0-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="dddb0-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dddb0-124">複合檔案</span><span class="sxs-lookup"><span data-stu-id="dddb0-124">Compound Documents</span></span>](compound-documents.md)
</dt> </dl>

 

 




