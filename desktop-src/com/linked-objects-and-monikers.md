---
title: 連結的物件和名字
description: 連結化物件（例如内嵌物件）會依賴物件處理常式來與伺服器應用程式進行通訊。
ms.assetid: f72557b9-cd24-4d96-8144-94a5344ec2ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7c14f4cc74ee84fbf745e730d77203ebb4f43b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104184011"
---
# <a name="linked-objects-and-monikers"></a><span data-ttu-id="7e887-103">連結的物件和名字</span><span class="sxs-lookup"><span data-stu-id="7e887-103">Linked Objects and Monikers</span></span>

<span data-ttu-id="7e887-104">連結化物件（例如内嵌物件）會依賴物件處理常式來與伺服器應用程式進行通訊。</span><span class="sxs-lookup"><span data-stu-id="7e887-104">Linked objects, like embedded objects, rely on an object handler to communicate with server applications.</span></span> <span data-ttu-id="7e887-105">但是，連結的物件本身會管理連結來源的命名和追蹤。</span><span class="sxs-lookup"><span data-stu-id="7e887-105">The linked object itself, however, manages the naming and tracking of link sources.</span></span> <span data-ttu-id="7e887-106">連結化物件的作用就像同進程伺服器。</span><span class="sxs-lookup"><span data-stu-id="7e887-106">The linked object acts like an in-process server.</span></span> <span data-ttu-id="7e887-107">例如，當啟用時，連結的物件會尋找並啟動做為連結來源的 OLE 伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="7e887-107">For example, when activated, a linked object locates and launches the OLE server application that is the link source.</span></span>

<span data-ttu-id="7e887-108">連結化物件的處理常式是由兩個主要元件所組成：處理常式元件和連結元件。</span><span class="sxs-lookup"><span data-stu-id="7e887-108">A linked object's handler is made up of two main components: the handler component and the linking component.</span></span> <span data-ttu-id="7e887-109">處理常式元件包含控制和遠端處理片段和函式，與内嵌物件的處理常式非常類似。</span><span class="sxs-lookup"><span data-stu-id="7e887-109">The handler component contains the controlling and remoting pieces and functions much like a handler for an embedded object.</span></span> <span data-ttu-id="7e887-110">連結元件有自己的控制器和快取，並可讓您存取物件的結構化儲存體。</span><span class="sxs-lookup"><span data-stu-id="7e887-110">The linking component has its own controller and cache and provides access to the object's structured storage.</span></span> <span data-ttu-id="7e887-111">連結元件控制器可透過使用標記來支援來源命名，而系結則支援尋找和執行連結來源的進程。</span><span class="sxs-lookup"><span data-stu-id="7e887-111">The linking components controller supports source naming through the use of monikers, and binding, the process of locating and running the link source.</span></span> <span data-ttu-id="7e887-112"> (如需有關名字和系結的詳細資訊，請參閱 [元件物件模型](the-component-object-model.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="7e887-112">(For more information on monikers and binding, see [The Component Object Model](the-component-object-model.md).)</span></span>

<span data-ttu-id="7e887-113">當使用者一開始建立連結化物件或從儲存體載入現有的物件時，容器會將連結元件的實例連同物件處理常式一起載入至記憶體。</span><span class="sxs-lookup"><span data-stu-id="7e887-113">When a user initially creates a linked object or loads an existing one from storage, the container loads an instance of the linking component into memory, along with the object handler.</span></span> <span data-ttu-id="7e887-114">連結元件提供介面（尤其是 [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink)），可將物件識別為連結，並讓它管理其連結來源的命名、追蹤和更新。</span><span class="sxs-lookup"><span data-stu-id="7e887-114">The linking component supplies interfaces — most notably [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink)— that identify the object as a link and enable it to manage the naming, tracking, and updating of its link source.</span></span>

<span data-ttu-id="7e887-115">藉由執行 [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink) 介面，連結的物件會提供其容器與支援連結的函式。</span><span class="sxs-lookup"><span data-stu-id="7e887-115">By implementing the [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink) interface, a linked object provides its container with functions that support linking.</span></span> <span data-ttu-id="7e887-116">只有連結的物件會執行 **IOleLink**，而且藉由查詢此介面，容器可以判斷指定的物件是否為內嵌或連結。</span><span class="sxs-lookup"><span data-stu-id="7e887-116">Only linked objects implement **IOleLink**, and by querying for this interface a container can determine whether a given object is embedded or linked.</span></span> <span data-ttu-id="7e887-117">**IOleLink** 所提供最重要的函式可讓容器系結至連結化物件的來源，也就是啟用儲存連結化物件原生資料之檔的連接。</span><span class="sxs-lookup"><span data-stu-id="7e887-117">The most important function provided by **IOleLink** enables a container to binding to the source of the linked object, that is, to activate the connection to the document that stores the linked object's native data.</span></span> <span data-ttu-id="7e887-118">**IOleLink** 也會定義用來管理連結化物件相關資訊的函式，例如快取的呈現資料和連結來源的位置。</span><span class="sxs-lookup"><span data-stu-id="7e887-118">**IOleLink** also defines functions for managing information about the linked object, such as cached presentation data and the location of the link source.</span></span>

<span data-ttu-id="7e887-119">當儲存包含連結化物件的複合檔案時，連結的資料會與連結來源儲存在一起，而不是與容器一起儲存。</span><span class="sxs-lookup"><span data-stu-id="7e887-119">When a compound document containing a linked object is saved, the link's data is saved with the link source, not with the container.</span></span> <span data-ttu-id="7e887-120">只有有關其名稱和位置的資訊會與複合檔案一起儲存。</span><span class="sxs-lookup"><span data-stu-id="7e887-120">Only information about its name and location is saved along with the compound document.</span></span> <span data-ttu-id="7e887-121">這種行為與内嵌物件的行為相較之下，其資料會連同容器的資料一起儲存。</span><span class="sxs-lookup"><span data-stu-id="7e887-121">This behavior is in contrast to that of an embedded object, whose data is stored along with that of its container.</span></span>

<span data-ttu-id="7e887-122">容器應用程式可以提供其内嵌物件的相關資訊，讓後者或其部分可作為連結來源。</span><span class="sxs-lookup"><span data-stu-id="7e887-122">Container applications can provide information about their embedded objects such that the latter, or portions thereof, can act as link sources.</span></span> <span data-ttu-id="7e887-123">藉由實作為連結至容器内嵌物件的支援，您可以進行嵌套內嵌，讓使用者不必追蹤需要連結的每個内嵌物件的原始物件。</span><span class="sxs-lookup"><span data-stu-id="7e887-123">By implementing support for linking to your container's embedded objects, you make nested embeddings possible, relieving the user of having to track down the originals of every embedding object to which a link is desired.</span></span> <span data-ttu-id="7e887-124">例如，如果使用者想要在 Microsoft Word 中內嵌 Microsoft Excel 工作表，而且工作表包含在畫刷中建立的點陣圖，則使用者可以連結至包含在工作表中的點陣圖複本，而不是原始的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="7e887-124">For example, if a user wants to embed a Microsoft Excel worksheet in Microsoft Word, and the worksheet contains a bitmap created in Paintbrush, the user can link to a copy of the bitmap contained in the worksheet rather than the original.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e887-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="7e887-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e887-126">複合檔案</span><span class="sxs-lookup"><span data-stu-id="7e887-126">Compound Documents</span></span>](compound-documents.md)
</dt> <dt>

[<span data-ttu-id="7e887-127">同進程伺服器</span><span class="sxs-lookup"><span data-stu-id="7e887-127">In-Process Servers</span></span>](in-process-servers.md)
</dt> <dt>

[<span data-ttu-id="7e887-128">物件處理常式</span><span class="sxs-lookup"><span data-stu-id="7e887-128">Object Handlers</span></span>](object-handlers.md)
</dt> </dl>

 

 




