---
title: 複合檔案
description: OLE 複合檔案可讓使用者在單一應用程式中運作，以操作以各種格式撰寫並衍生自多個來源的資料。
ms.assetid: d17dc0dd-3115-4830-8c6b-694a8d1accaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f12e0228b7c8c1d74e4ec33d8069490351f77f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104093407"
---
# <a name="compound-documents"></a><span data-ttu-id="b18f3-103">複合檔案</span><span class="sxs-lookup"><span data-stu-id="b18f3-103">Compound Documents</span></span>

<span data-ttu-id="b18f3-104">OLE 複合檔案可讓使用者在單一應用程式中運作，以操作以各種格式撰寫並衍生自多個來源的資料。</span><span class="sxs-lookup"><span data-stu-id="b18f3-104">OLE compound documents enable users working within a single application to manipulate data written in various formats and derived from multiple sources.</span></span> <span data-ttu-id="b18f3-105">例如，使用者可能會在第二個應用程式中建立的圖形和在第三個應用程式中建立的音效物件插入文字處理檔中。</span><span class="sxs-lookup"><span data-stu-id="b18f3-105">For example, a user might insert into a word processing document a graph created in a second application and a sound object created in a third application.</span></span> <span data-ttu-id="b18f3-106">啟用圖形會導致第二個應用程式載入其使用者介面，或至少包含編輯物件所需工具的元件。</span><span class="sxs-lookup"><span data-stu-id="b18f3-106">Activating the graph causes the second application to load its user interface, or at least that part containing tools necessary to edit the object.</span></span> <span data-ttu-id="b18f3-107">啟用音效物件會導致第三個應用程式播放它。</span><span class="sxs-lookup"><span data-stu-id="b18f3-107">Activating the sound object causes the third application to play it.</span></span> <span data-ttu-id="b18f3-108">在這兩種情況下，使用者都可以從單一檔的內容中，操作來自外部來源的資料。</span><span class="sxs-lookup"><span data-stu-id="b18f3-108">In both cases, a user is able to manipulate data from external sources from within the context of a single document.</span></span>

<span data-ttu-id="b18f3-109">OLE 複合檔案技術是在由 COM、結構化儲存體和制式資料傳輸所組成的基礎上。</span><span class="sxs-lookup"><span data-stu-id="b18f3-109">OLE compound document technology rests on a foundation consisting of COM, structured storage, and uniform data transfer.</span></span> <span data-ttu-id="b18f3-110">如下所示，每個核心技術在 OLE 複合檔案中扮演著重要的角色：</span><span class="sxs-lookup"><span data-stu-id="b18f3-110">As summarized below, each of these core technologies plays a critical role in OLE compound documents:</span></span>

<dl> <dt>

<span data-ttu-id="b18f3-111"><span id="COM"></span><span id="com"></span>Com</span><span class="sxs-lookup"><span data-stu-id="b18f3-111"><span id="COM"></span><span id="com"></span>COM</span></span>
</dt> <dd>

<span data-ttu-id="b18f3-112">複合檔案物件基本上是可內嵌或連結至現有檔的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="b18f3-112">A compound document object is essentially a COM object that can be embedded in, or linked to, an existing document.</span></span> <span data-ttu-id="b18f3-113">複合檔案物件是 COM 物件，它會公開 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 介面，讓用戶端可以透過此介面取得其其他介面的指標，包括數個，例如 [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject)、 [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink)和 [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)，以提供複合檔案物件特有的特殊功能。</span><span class="sxs-lookup"><span data-stu-id="b18f3-113">As a COM object, a compound document object exposes the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface, through which clients can obtain pointers to its other interfaces, including several, such as [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject), [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink), and [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2), that provide special features unique to compound document objects.</span></span>

</dd> <dt>

<span data-ttu-id="b18f3-114"><span id="Structured_Storage"></span><span id="structured_storage"></span><span id="STRUCTURED_STORAGE"></span>結構化儲存體</span><span class="sxs-lookup"><span data-stu-id="b18f3-114"><span id="Structured_Storage"></span><span id="structured_storage"></span><span id="STRUCTURED_STORAGE"></span>Structured Storage</span></span>
</dt> <dd>

<span data-ttu-id="b18f3-115">複合檔案物件必須執行 [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) 或（選擇性） [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) 介面來管理本身的儲存體。</span><span class="sxs-lookup"><span data-stu-id="b18f3-115">A compound document object must implement the [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) or, optionally, [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) interfaces to manage its own storage.</span></span> <span data-ttu-id="b18f3-116">用來建立複合檔案的容器必須提供 [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) 介面，物件可透過這些介面儲存和取出資料。</span><span class="sxs-lookup"><span data-stu-id="b18f3-116">A container used to create compound documents must supply the [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) interface, through which objects store and retrieve data.</span></span> <span data-ttu-id="b18f3-117">容器幾乎一律會提供從 OLE 的複合檔案執行所取得的 **IStorage** 實例。</span><span class="sxs-lookup"><span data-stu-id="b18f3-117">Containers almost always provide instances of **IStorage** obtained from OLE's Compound Files implementation.</span></span> <span data-ttu-id="b18f3-118">容器也必須使用物件的 **IPersistStorage** 和/或 **IPersistStream** 介面。</span><span class="sxs-lookup"><span data-stu-id="b18f3-118">Containers must also use an object's **IPersistStorage** and/or **IPersistStream** interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="b18f3-119"><span id="Uniform_Data_Transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>制式資料傳輸</span><span class="sxs-lookup"><span data-stu-id="b18f3-119"><span id="Uniform_Data_Transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Uniform Data Transfer</span></span>
</dt> <dd>

<span data-ttu-id="b18f3-120">支援複合檔案的應用程式必須執行 [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) ，因為嵌入的物件和連結的物件是以使用特殊 OLE 剪貼簿格式（而非標準 Microsoft Windows 剪貼簿格式）傳輸的資料作為開頭。</span><span class="sxs-lookup"><span data-stu-id="b18f3-120">Applications that support compound documents must implement [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) because embedded objects and linked objects begin as data that has been transferred using special OLE clipboard formats, rather than standard Microsoft Windows clipboard formats.</span></span> <span data-ttu-id="b18f3-121">換句話說，以內嵌或連結化物件的格式設定資料，只是 OLE 的制式資料傳輸模型提供的另一個選項。</span><span class="sxs-lookup"><span data-stu-id="b18f3-121">In other words, formatting data as an embedded or linked object is simply one more option provided by OLE's uniform data transfer model.</span></span>

</dd> </dl>

<span data-ttu-id="b18f3-122">OLE 的複合檔案技術同時也受益軟體發展人員和使用者。</span><span class="sxs-lookup"><span data-stu-id="b18f3-122">OLE's compound document technology benefits both software developers and users alike.</span></span> <span data-ttu-id="b18f3-123">軟體發展人員如果想要將每個可想像的功能 cram 到單一應用程式，而不是想要開發更小且更具焦點的應用程式，而這些應用程式依賴其他應用程式來提供其他功能。</span><span class="sxs-lookup"><span data-stu-id="b18f3-123">Instead of feeling obligated to cram every conceivable feature into a single application, software developers are now free, if they like, to develop smaller, more focused applications that rely on other applications to supply additional features.</span></span> <span data-ttu-id="b18f3-124">如果軟體發展人員決定提供的應用程式的功能超出其核心功能，開發人員可以將這些額外的服務實作為個別的 Dll，而這些 Dll 只有在需要服務時才會載入到記憶體中。</span><span class="sxs-lookup"><span data-stu-id="b18f3-124">In cases where a software developer decides to provide an application with capabilities beyond its core features, the developer can implement these additional services as separate DLLs, which are loaded into memory only when their services are required.</span></span> <span data-ttu-id="b18f3-125">使用者可受益于更小、更快速、更強大的軟體，這些軟體可以視需要混合和比對，從單一主檔案內操作所有必要的元件。</span><span class="sxs-lookup"><span data-stu-id="b18f3-125">Users benefit from smaller, faster, more capable software that they can mix and match as needed, manipulating all required components from within a single master document.</span></span>

<span data-ttu-id="b18f3-126">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="b18f3-126">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="b18f3-127">容器和伺服器</span><span class="sxs-lookup"><span data-stu-id="b18f3-127">Containers and Servers</span></span>](containers-and-servers.md)
-   [<span data-ttu-id="b18f3-128">連結和內嵌</span><span class="sxs-lookup"><span data-stu-id="b18f3-128">Linking and Embedding</span></span>](linking-and-embedding.md)
-   [<span data-ttu-id="b18f3-129">物件處理常式</span><span class="sxs-lookup"><span data-stu-id="b18f3-129">Object Handlers</span></span>](object-handlers.md)
-   [<span data-ttu-id="b18f3-130">同進程伺服器</span><span class="sxs-lookup"><span data-stu-id="b18f3-130">In-Process Servers</span></span>](in-process-servers.md)
-   [<span data-ttu-id="b18f3-131">連結的物件和名字</span><span class="sxs-lookup"><span data-stu-id="b18f3-131">Linked Objects and Monikers</span></span>](linked-objects-and-monikers.md)
-   [<span data-ttu-id="b18f3-132">通知</span><span class="sxs-lookup"><span data-stu-id="b18f3-132">Notifications</span></span>](notifications.md)
-   [<span data-ttu-id="b18f3-133">複合檔案介面</span><span class="sxs-lookup"><span data-stu-id="b18f3-133">Compound Document Interfaces</span></span>](compound-document-interfaces.md)
-   [<span data-ttu-id="b18f3-134">物件狀態</span><span class="sxs-lookup"><span data-stu-id="b18f3-134">Object States</span></span>](object-states.md)
-   [<span data-ttu-id="b18f3-135">執行 In-Place 啟用</span><span class="sxs-lookup"><span data-stu-id="b18f3-135">Implementing In-Place Activation</span></span>](implementing-in-place-activation.md)
-   [<span data-ttu-id="b18f3-136">從現有資料建立連結和內嵌物件</span><span class="sxs-lookup"><span data-stu-id="b18f3-136">Creating Linked and Embedded Objects from Existing Data</span></span>](creating-linked-and-embedded-objects-from-existing-data.md)
-   [<span data-ttu-id="b18f3-137">視圖快取</span><span class="sxs-lookup"><span data-stu-id="b18f3-137">View Caching</span></span>](view-caching.md)

## <a name="related-topics"></a><span data-ttu-id="b18f3-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="b18f3-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b18f3-139">資料轉送</span><span class="sxs-lookup"><span data-stu-id="b18f3-139">Data Transfer</span></span>](data-transfer.md)
</dt> <dt>

[<span data-ttu-id="b18f3-140">結構化儲存體</span><span class="sxs-lookup"><span data-stu-id="b18f3-140">Structured Storage</span></span>](/windows/desktop/Stg/structured-storage-start-page)
</dt> </dl>

 

 