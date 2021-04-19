---
title: 非同步名字
description: 非同步名字
ms.assetid: 24c50f7b-f085-4086-aa44-81e5cab011cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e19323af3a972a2b83a290176a4b26fb79382da0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106966060"
---
# <a name="asynchronous-monikers"></a><span data-ttu-id="3627d-103">非同步名字</span><span class="sxs-lookup"><span data-stu-id="3627d-103">Asynchronous Monikers</span></span>

<span data-ttu-id="3627d-104">OLE 標記架構提供一致且可延伸的程式設計模型，可使用網際網路物件、提供剖析名稱的方法， (Url) 為可列印的名稱，以及尋找並系結至 URL 字串所表示的物件。</span><span class="sxs-lookup"><span data-stu-id="3627d-104">The OLE moniker architecture provides a consistent, extensible programming model for working with Internet objects, providing methods for parsing names, representing Universal Resource Locators (URLs) as printable names, and locating and binding to the objects represented by URL strings.</span></span> <span data-ttu-id="3627d-105"> (也會看到 [URL](url-monikers.md)標記) 項。 ) 標準 OLE 標記 (值得注意的是，因為它們是同步的，所以不適合網際網路，因為它們是同步的，因此只有在有所有資料可供使用時，才會傳回物件或其儲存區的指標。</span><span class="sxs-lookup"><span data-stu-id="3627d-105">(Also see [URL Monikers](url-monikers.md).) Standard OLE monikers (notably, item, file, and pointer monikers), however, are inappropriate for the Internet because they are synchronous, returning a pointer to an object or its storage only at such time as all data is available.</span></span> <span data-ttu-id="3627d-106">視所要下載的資料量而定，同步系結可讓用戶端的使用者介面長時間進行系結。</span><span class="sxs-lookup"><span data-stu-id="3627d-106">Depending on the amount of data to be downloaded, binding synchronously can tie up the client's user interface for prolonged periods.</span></span>

<span data-ttu-id="3627d-107">網際網路需要新的應用程式設計方法。</span><span class="sxs-lookup"><span data-stu-id="3627d-107">The Internet requires new approaches to application design.</span></span> <span data-ttu-id="3627d-108">應用程式應該能夠以非同步方式執行所有昂貴的網路作業，以避免拖延使用者介面。</span><span class="sxs-lookup"><span data-stu-id="3627d-108">Applications should be able to perform all expensive network operations asynchronously to avoid stalling the user interface.</span></span> <span data-ttu-id="3627d-109">應用程式應該能夠觸發作業，並在完整或部分完成時收到通知。</span><span class="sxs-lookup"><span data-stu-id="3627d-109">An application should be able to trigger an operation and receive notification on full or partial completion.</span></span> <span data-ttu-id="3627d-110">屆時，應用程式應該可以選擇繼續進行作業的下一個步驟，或視需要提供其他資訊。</span><span class="sxs-lookup"><span data-stu-id="3627d-110">At that point, the application should have the choice either of proceeding with the next step of the operation or providing additional information as needed.</span></span> <span data-ttu-id="3627d-111">當您進行下載時，應用程式應該也可以為使用者提供進度資訊，以及隨時取消作業的機會。</span><span class="sxs-lookup"><span data-stu-id="3627d-111">As a download proceeds, an application should also be able to provide users with progress information and the opportunity to cancel the operation at any time.</span></span>

<span data-ttu-id="3627d-112">非同步標記可提供這些功能以及各種層級的非同步系結行為，同時為不知道或不需要非同步行為的應用程式提供回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="3627d-112">Asynchronous monikers provide these capabilities, as well as various levels of asynchronous binding behavior, while providing backward compatibility for applications that are either unaware of or do not require asynchronous behavior.</span></span> <span data-ttu-id="3627d-113">另一項 OLE 技術（非同步儲存）可與非同步名字區搭配使用，以提供非同步下載網際網路物件的持續性狀態。</span><span class="sxs-lookup"><span data-stu-id="3627d-113">Another OLE technology, asynchronous storage, works with asynchronous monikers to provide asynchronous downloading of an Internet object's persistent state.</span></span> <span data-ttu-id="3627d-114">非同步標記會觸發系結作業，並設定必要的元件，包括儲存和資料流程物件、位元組陣列物件和通知接收。</span><span class="sxs-lookup"><span data-stu-id="3627d-114">The asynchronous moniker triggers the bind operation and sets up the necessary components, including storage and stream objects, byte-array objects, and notification sinks.</span></span> <span data-ttu-id="3627d-115">一旦連接元件之後，就會出現此標記，且系結的其餘部分主要是在執行非同步儲存元件和物件的元件之間執行。</span><span class="sxs-lookup"><span data-stu-id="3627d-115">Once the components are connected, the moniker gets out of the way and the rest of the bind is executed mainly between the components implementing the asynchronous storage components and the object.</span></span>

<span data-ttu-id="3627d-116">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="3627d-116">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="3627d-117">非同步和同步的名字標記</span><span class="sxs-lookup"><span data-stu-id="3627d-117">Asynchronous and Synchronous Monikers</span></span>](./asynchronous-vs.-synchronous-monikers.md)
-   [<span data-ttu-id="3627d-118">非同步和同步系結</span><span class="sxs-lookup"><span data-stu-id="3627d-118">Asynchronous and Synchronous Binding</span></span>](./asynchronous-vs.-synchronous-binding.md)
-   [<span data-ttu-id="3627d-119">非同步和同步儲存體</span><span class="sxs-lookup"><span data-stu-id="3627d-119">Asynchronous and Synchronous Storage</span></span>](./asynchronous-vs.-synchronous-storage.md)
-   [<span data-ttu-id="3627d-120">資料提取模型和 Data-Push 模型</span><span class="sxs-lookup"><span data-stu-id="3627d-120">Data-Pull Model and Data-Push Model</span></span>](./data-pull-model-vs.-data-push-model.md)

## <a name="related-topics"></a><span data-ttu-id="3627d-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="3627d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3627d-122">URL 的名字</span><span class="sxs-lookup"><span data-stu-id="3627d-122">URL Monikers</span></span>](url-monikers.md)
</dt> </dl>

 

 