---
title: COM 詞彙
description: 詞彙頁面
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9e2c56a2-0572-48b6-a2ef-650f1cf1b62e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c12f3c021988f0349d9eaf6a2bdbd9505ca8a6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106969940"
---
# <a name="com-glossary"></a><span data-ttu-id="0c7b7-103">COM 詞彙</span><span class="sxs-lookup"><span data-stu-id="0c7b7-103">COM Glossary</span></span>

<dl> <dt>

<span data-ttu-id="0c7b7-104"><span id="com.activation_gloss"></span><span id="COM.ACTIVATION_GLOSS"></span>**啟動**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-104"><span id="com.activation_gloss"></span><span id="COM.ACTIVATION_GLOSS"></span>**activation**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-105">將物件載入記憶體中的程式，使其進入執行狀態。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-105">The process of loading an object in memory, which puts it into the running state.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-106"><span id="com.active_state_gloss"></span><span id="COM.ACTIVE_STATE_GLOSS"></span>**作用中狀態**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-106"><span id="com.active_state_gloss"></span><span id="COM.ACTIVE_STATE_GLOSS"></span>**active state**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-107">處於執行中狀態且具有可見使用者介面的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-107">A COM object that is in the running state and has a visible user interface.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-108"><span id="com.absolute_moniker_gloss"></span><span id="COM.ABSOLUTE_MONIKER_GLOSS"></span>**絕對標記**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-108"><span id="com.absolute_moniker_gloss"></span><span id="COM.ABSOLUTE_MONIKER_GLOSS"></span>**absolute moniker**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-109">指定物件絕對位置的名字。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-109">A moniker that specifies the absolute location of an object.</span></span> <span data-ttu-id="0c7b7-110">絕對的標記類似于完整路徑。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-110">An absolute moniker is analogous to a full path.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-111"><span id="com.advisory_holder_gloss"></span><span id="COM.ADVISORY_HOLDER_GLOSS"></span>**諮詢持有者**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-111"><span id="com.advisory_holder_gloss"></span><span id="COM.ADVISORY_HOLDER_GLOSS"></span>**advisory holder**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-112">COM 物件，可快取、管理和傳送容器應用程式之諮詢接收器的變更通知。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-112">A COM object that caches, manages, and sends notifications of changes to container applications' advisory sinks.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-113"><span id="com.advisory_sink_gloss"></span><span id="COM.ADVISORY_SINK_GLOSS"></span>**諮詢接收**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-113"><span id="com.advisory_sink_gloss"></span><span id="COM.ADVISORY_SINK_GLOSS"></span>**advisory sink**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-114">COM 物件，可接收内嵌物件或連結化物件中之變更的通知，因為它會執行 [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) 或 [**IAdviseSink2**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink2) 介面。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-114">A COM object that can receive notifications of changes in an embedded object or linked object because it implements the [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) or [**IAdviseSink2**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink2) interface.</span></span> <span data-ttu-id="0c7b7-115">需要收到物件變更通知的容器會執行諮詢接收。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-115">Containers that need to be notified of changes in objects implement an advisory sink.</span></span> <span data-ttu-id="0c7b7-116">通知源自伺服器，其使用諮詢持有者物件來快取和管理容器的通知。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-116">Notifications originate in the server, which uses an advisory holder object to cache and manage notifications to containers.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-117"><span id="com.aggregate_object_gloss"></span><span id="COM.AGGREGATE_OBJECT_GLOSS"></span>**aggregate 物件**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-117"><span id="com.aggregate_object_gloss"></span><span id="COM.AGGREGATE_OBJECT_GLOSS"></span>**aggregate object**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-118">由一或多個其他 COM 物件所組成的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-118">A COM object that is made up of one or more other COM objects.</span></span> <span data-ttu-id="0c7b7-119">匯總中的一個物件會指定控制物件，此物件會控制匯總中的哪些介面會公開，哪些是私用的。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-119">One object in the aggregate is designated the controlling object, which controls which interfaces in the aggregate are exposed and which are private.</span></span> <span data-ttu-id="0c7b7-120">此控制物件具有 [**iunknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 的特殊實，稱為控制 **iunknown**。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-120">This controlling object has a special implementation of [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) called the controlling **IUnknown**.</span></span> <span data-ttu-id="0c7b7-121">匯總中的所有物件都必須透過控制 **iunknown** 來傳遞對 **IUnknown** 方法的呼叫。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-121">All objects in the aggregate must pass calls to **IUnknown** methods through the controlling **IUnknown**.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-122"><span id="com.aggregation_gloss"></span><span id="COM.AGGREGATION_GLOSS"></span>**聚集**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-122"><span id="com.aggregation_gloss"></span><span id="COM.AGGREGATION_GLOSS"></span>**aggregation**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-123">用來執行 COM 物件的組合技術。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-123">A composition technique for implementing COM objects.</span></span> <span data-ttu-id="0c7b7-124">它可讓您藉由重複使用一或多個現有物件的介面執行來建立新的物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-124">It allows you to build a new object by reusing one or more existing objects' interface implementations.</span></span> <span data-ttu-id="0c7b7-125">「匯總」物件會選擇要公開給用戶端的介面，而介面會公開為「匯總」物件所執行的介面。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-125">The aggregate object chooses which interfaces to expose to clients, and the interfaces are exposed as if they were implemented by the aggregate object.</span></span> <span data-ttu-id="0c7b7-126">Aggregate 物件的用戶端只會與 aggregate 物件進行通訊。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-126">Clients of the aggregate object communicate only with the aggregate object.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-127"><span id="com.ambient_property_gloss"></span><span id="COM.AMBIENT_PROPERTY_GLOSS"></span>**環境屬性**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-127"><span id="com.ambient_property_gloss"></span><span id="COM.AMBIENT_PROPERTY_GLOSS"></span>**ambient property**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-128">由容器所管理和公開的執行時間屬性。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-128">A run-time property that is managed and exposed by the container.</span></span> <span data-ttu-id="0c7b7-129">環境屬性通常代表表單的特性，例如背景色彩，必須傳達給控制項，讓控制項可以假設其周圍環境的外觀和風格。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-129">Typically, an ambient property represents a characteristic of a form, such as background color, that needs to be communicated to a control so that the control can assume the look and feel of its surrounding environment.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-130"><span id="com.anti_moniker_gloss"></span><span id="COM.ANTI_MONIKER_GLOSS"></span>**反標記**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-130"><span id="com.anti_moniker_gloss"></span><span id="COM.ANTI_MONIKER_GLOSS"></span>**anti-moniker**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-131">檔案、專案或指標標記的反向。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-131">The inverse of a file, item, or pointer moniker.</span></span> <span data-ttu-id="0c7b7-132">反標記會新增至檔案、專案或指標標記的結尾，以使失效它。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-132">An anti-moniker is added to the end of a file, item, or pointer moniker to nullify it.</span></span> <span data-ttu-id="0c7b7-133">反向標記會用於相對的擁有者的結構。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-133">Anti-monikers are used in the construction of relative monikers.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-134"><span id="com.artificial_reference_counting_gloss"></span><span id="COM.ARTIFICIAL_REFERENCE_COUNTING_GLOSS"></span>**人工參考計數**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-134"><span id="com.artificial_reference_counting_gloss"></span><span id="COM.ARTIFICIAL_REFERENCE_COUNTING_GLOSS"></span>**artificial reference counting**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-135">一種技術，用來在呼叫可能會提前終結的函式或方法之前，協助保護物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-135">A technique used to help protect an object before calling a function or method that could prematurely destroy it.</span></span> <span data-ttu-id="0c7b7-136">程式呼叫 **IUnknown：： AddRef** 以遞增物件的參考計數，然後再進行呼叫，以釋放物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-136">A program calls **IUnknown::AddRef** to increment the object's reference count before making the call that could free the object.</span></span> <span data-ttu-id="0c7b7-137">在函式傳回之後，程式會呼叫 **IUnknown：： Release** 來遞減計數。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-137">After the function returns, the program calls **IUnknown::Release** to decrement the count.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-138"><span id="com.asynchronous_binding_gloss"></span><span id="COM.ASYNCHRONOUS_BINDING_GLOSS"></span>**非同步綁定**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-138"><span id="com.asynchronous_binding_gloss"></span><span id="COM.ASYNCHRONOUS_BINDING_GLOSS"></span>**asynchronous binding**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-139">一種系結，在此類型中，必須以非同步方式進行程式，以避免使用者的效能降低。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-139">A type of binding in which it is necessary for the process to occur asynchronously to avoid performance degradation for the end user.</span></span> <span data-ttu-id="0c7b7-140">一般情況下，非同步系結會用於全球 Web 等分散式環境。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-140">Typically, asynchronous binding is used in distributed environments such as the World Wide Web.</span></span> <span data-ttu-id="0c7b7-141">OLE 支援非同步標記類別和回呼機制，可讓您在分散式環境中尋找和初始化物件的程式，在執行其他作業時才會發生。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-141">OLE supports asynchronous moniker classes and callback mechanisms that allow the process of locating and initializing an object in a distributed environment to occur while other operations are being carried out.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-142"><span id="com.asynchronous_call_gloss"></span><span id="COM.ASYNCHRONOUS_CALL_GLOSS"></span>**非同步呼叫**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-142"><span id="com.asynchronous_call_gloss"></span><span id="COM.ASYNCHRONOUS_CALL_GLOSS"></span>**asynchronous call**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-143">呼叫個別執行的函式，讓呼叫端可以繼續處理指示，而不需等待函數傳回。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-143">A call to a function that is executed separately so that the caller can continue processing instructions without waiting for the function to return.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-144"><span id="com.asynchronous_moniker_gloss"></span><span id="COM.ASYNCHRONOUS_MONIKER_GLOSS"></span>**非同步標記**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-144"><span id="com.asynchronous_moniker_gloss"></span><span id="COM.ASYNCHRONOUS_MONIKER_GLOSS"></span>**asynchronous moniker**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-145">支援非同步綁定的標記。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-145">A moniker that supports asynchronous binding.</span></span> <span data-ttu-id="0c7b7-146">例如，系統提供的 URL 標記類別的實例是非同步名字。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-146">For example, instances of the system-supplied URL moniker class are asynchronous monikers.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-147"><span id="com.automation_gloss"></span><span id="COM.AUTOMATION_GLOSS"></span>**自動化**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-147"><span id="com.automation_gloss"></span><span id="COM.AUTOMATION_GLOSS"></span>**automation**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-148">從應用程式外部操作應用程式物件的方法。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-148">A way to manipulate an application's objects from outside the application.</span></span> <span data-ttu-id="0c7b7-149">Automation 通常用來建立應用程式，以將物件公開至程式設計工具和宏語言、建立和操作另一個應用程式的應用程式物件，或建立用來存取和操作物件的工具。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-149">Automation is typically used to create applications that expose objects to programming tools and macro languages, create and manipulate one application's objects from another applications, or to create tools for accessing and manipulating objects.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-150"><span id="com.bind_context_gloss"></span><span id="COM.BIND_CONTEXT_GLOSS"></span>**系結內容**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-150"><span id="com.bind_context_gloss"></span><span id="COM.BIND_CONTEXT_GLOSS"></span>**bind context**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-151">執行 [**IBindCtx**](/windows/desktop/api/ObjIdl/nn-objidl-ibindctx) 介面的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-151">A COM object that implements the [**IBindCtx**](/windows/desktop/api/ObjIdl/nn-objidl-ibindctx) interface.</span></span> <span data-ttu-id="0c7b7-152">在標記系結時，系結內容會在標記作業中用來保存物件的參考。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-152">Bind contexts are used in moniker operations to hold references to the objects activated when a moniker is bound.</span></span> <span data-ttu-id="0c7b7-153">系結內容包含在泛型複合標記系結期間套用至所有作業的參數，並提供可存取其環境相關資訊的標記實行。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-153">The bind context contains parameters that apply to all operations during the binding of a generic composite moniker and provides the moniker implementation with access to information about its environment.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-154"><span id="com.binding_gloss"></span><span id="COM.BINDING_GLOSS"></span>**綁定**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-154"><span id="com.binding_gloss"></span><span id="COM.BINDING_GLOSS"></span>**binding**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-155">將名稱與其引用相關聯。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-155">Associating a name with its referent.</span></span> <span data-ttu-id="0c7b7-156">具體而言，是找出以標記命名的物件，將它放入它的執行中狀態（如果尚未執行），並傳回介面指標給它。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-156">Specifically, locating the object named by a moniker, putting it into its running state if it isn't already, and returning an interface pointer to it.</span></span> <span data-ttu-id="0c7b7-157">您可以在執行時間系結物件 (也稱為晚期繫結或動態繫結) 或在編譯時期 (也稱為靜態系結) 。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-157">Objects can be bound at run time (also called late binding or dynamic binding) or at compile time (also called static binding).</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-158"><span id="com.cache_gloss"></span><span id="COM.CACHE_GLOSS"></span>**緩存**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-158"><span id="com.cache_gloss"></span><span id="COM.CACHE_GLOSS"></span>**cache**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-159"> (通常是暫時) 的資訊本機存放區。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-159">A (usually temporary) local store of information.</span></span> <span data-ttu-id="0c7b7-160">在 OLE 中，快取包含的資訊可在容器開啟時定義連結或内嵌物件的呈現方式。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-160">In OLE, a cache contains information that defines the presentation of a linked or embedded object when the container is opened.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-161"><span id="com.cache_initialization_gloss"></span><span id="COM.CACHE_INITIALIZATION_GLOSS"></span>**快取初始化**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-161"><span id="com.cache_initialization_gloss"></span><span id="COM.CACHE_INITIALIZATION_GLOSS"></span>**cache initialization**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-162">以呈現資料填滿連結或内嵌物件的快取。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-162">Filling a linked or embedded object's cache with presentation data.</span></span> <span data-ttu-id="0c7b7-163">[**IOleCache**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache)介面提供容器可呼叫的方法，以控制為連結或内嵌物件快取的資料。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-163">The [**IOleCache**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) interface provides methods that a container can call to control the data that gets cached for linked or embedded objects.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-164"><span id="com.class_gloss"></span><span id="COM.CLASS_GLOSS"></span>**類**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-164"><span id="com.class_gloss"></span><span id="COM.CLASS_GLOSS"></span>**class**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-165">程式碼中物件的定義。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-165">The definition of an object in code.</span></span> <span data-ttu-id="0c7b7-166">在 c + + 中，物件的類別會定義為資料類型，但在其他語言中則不會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-166">In C++, the class of an object is defined as a data type, but this is not the case in other languages.</span></span> <span data-ttu-id="0c7b7-167">因為 OLE 可以用任何語言撰寫，所以類別是用來參考一般物件定義。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-167">Because OLE can be coded in any language, class is used to refer to the general object definition.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-168"><span id="com.class_factory_gloss"></span><span id="COM.CLASS_FACTORY_GLOSS"></span>**class factory**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-168"><span id="com.class_factory_gloss"></span><span id="COM.CLASS_FACTORY_GLOSS"></span>**class factory**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-169">COM 物件，該物件會執行 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) 介面，並且建立指定類別識別碼所識別之物件的一或多個實例， (CLSID) 。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-169">A COM object that implements the [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) interface and that creates one or more instances of an object identified by a given class identifier(CLSID).</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-170"><span id="com.class_identifier_gloss"></span><span id="COM.CLASS_IDENTIFIER_GLOSS"></span>**(CLSID) 的類別識別碼**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-170"><span id="com.class_identifier_gloss"></span><span id="COM.CLASS_IDENTIFIER_GLOSS"></span>**class identifier (CLSID)**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-171">與 OLE 類別物件相關聯 (GUID) 的全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-171">A globally unique identifier (GUID) associated with an OLE class object.</span></span> <span data-ttu-id="0c7b7-172">如果類別物件將用來建立多個物件實例，則相關聯的伺服器應用程式應該在系統登錄中註冊其 CLSID，讓用戶端可以找出並載入與物件 (的) 相關聯的可執行程式碼。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-172">If a class object will be used to create more than one instance of an object, the associated server application should register its CLSID in the system registry so that clients can locate and load the executable code associated with the object(s).</span></span> <span data-ttu-id="0c7b7-173">允許連結至其内嵌物件的每個 OLE 伺服器或容器，都必須為每個支援的物件定義註冊一個 CLSID。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-173">Every OLE server or container that allows linking to its embedded objects must register a CLSID for each supported object definition.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-174"><span id="com.class_object_gloss"></span><span id="COM.CLASS_OBJECT_GLOSS"></span>**class 物件**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-174"><span id="com.class_object_gloss"></span><span id="COM.CLASS_OBJECT_GLOSS"></span>**class object**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-175">在物件導向程式設計中，物件的狀態會由類別中的所有物件所共用，而且其行為會在該 classwide 狀態資料上運作。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-175">In object-oriented programming, an object whose state is shared by all the objects in a class and whose behavior acts on that classwide state data.</span></span> <span data-ttu-id="0c7b7-176">在 COM 中，類別物件稱為 class factory，而且除了建立類別的新實例之外，通常不會有任何行為。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-176">In COM, class objects are called class factories, and typically have no behavior except to create new instances of the class.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-177"><span id="com.client_gloss"></span><span id="COM.CLIENT_GLOSS"></span>**客戶**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-177"><span id="com.client_gloss"></span><span id="COM.CLIENT_GLOSS"></span>**client**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-178">從另一個物件要求服務的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-178">A COM object that requests services from another object.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-179"><span id="com.client_site_gloss"></span><span id="COM.CLIENT_SITE_GLOSS"></span>**用戶端網站**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-179"><span id="com.client_site_gloss"></span><span id="COM.CLIENT_SITE_GLOSS"></span>**client site**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-180">複合檔案中內嵌或連結化物件的顯示網站。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-180">The display site for an embedded or linked object within a compound document.</span></span> <span data-ttu-id="0c7b7-181">用戶端網站是物件從其容器要求服務的主要方式。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-181">The client site is the principal means by which an object requests services from its container.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-182"><span id="com.clsid_gloss"></span><span id="COM.CLSID_GLOSS"></span>**Clsid**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-182"><span id="com.clsid_gloss"></span><span id="COM.CLSID_GLOSS"></span>**CLSID**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-183">與 OLE 類別物件相關聯 (GUID) 的全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-183">A globally unique identifier (GUID) associated with an OLE class object.</span></span> <span data-ttu-id="0c7b7-184">如果類別物件將用來建立多個物件實例，則相關聯的伺服器應用程式應該在系統登錄中註冊其 CLSID，讓用戶端可以找出並載入與物件 (的) 相關聯的可執行程式碼。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-184">If a class object will be used to create more than one instance of an object, the associated server application should register its CLSID in the system registry so that clients can locate and load the executable code associated with the object(s).</span></span> <span data-ttu-id="0c7b7-185">允許連結至其内嵌物件的每個 OLE 伺服器或容器，都必須為每個支援的物件定義註冊一個 CLSID。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-185">Every OLE server or container that allows linking to its embedded objects must register a CLSID for each supported object definition.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-186"><span id="com.commit_gloss"></span><span id="COM.COMMIT_GLOSS"></span>**提交**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-186"><span id="com.commit_gloss"></span><span id="COM.COMMIT_GLOSS"></span>**commit**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-187">若要持續儲存對儲存體或資料流程物件所做的任何變更，因為它已開啟或上次儲存變更。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-187">To persistently save any changes made to a storage or stream object since it was opened or changes were last saved.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-188"><span id="com.component_gloss"></span><span id="COM.COMPONENT_GLOSS"></span>**元件**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-188"><span id="com.component_gloss"></span><span id="COM.COMPONENT_GLOSS"></span>**component**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-189">封裝資料和程式碼的物件，並提供一組指定的公開可用服務。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-189">An object that encapsulates both data and code, and provides a well-specified set of publicly available services.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-190"><span id="com.component_object_model_gloss"></span><span id="COM.COMPONENT_OBJECT_MODEL_GLOSS"></span>**元件物件模型 (COM)**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-190"><span id="com.component_object_model_gloss"></span><span id="COM.COMPONENT_OBJECT_MODEL_GLOSS"></span>**Component Object Model (COM)**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-191">OLE 物件導向程式設計模型，定義物件在單一進程內或處理常式之間的互動方式。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-191">The OLE object-oriented programming model that defines how objects interact within a single process or between processes.</span></span> <span data-ttu-id="0c7b7-192">在 COM 中，用戶端可以透過在物件上執行的介面存取物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-192">In COM, clients have access to an object through interfaces implemented on the object.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-193"><span id="com.composite_menu_bar_gloss"></span><span id="COM.COMPOSITE_MENU_BAR_GLOSS"></span>**複合功能表列**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-193"><span id="com.composite_menu_bar_gloss"></span><span id="COM.COMPOSITE_MENU_BAR_GLOSS"></span>**composite menu bar**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-194">共用的功能表列，由容器應用程式和就地啟動的伺服器應用程式中的功能表群組所組成。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-194">A shared menu bar composed of menu groups from both a container application and an in-place-activated server application.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-195"><span id="com.composite_moniker_gloss"></span><span id="COM.COMPOSITE_MONIKER_GLOSS"></span>**複合標記**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-195"><span id="com.composite_moniker_gloss"></span><span id="COM.COMPOSITE_MONIKER_GLOSS"></span>**composite moniker**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-196">由兩個或多個被視為一個單位的標記所組成的標記。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-196">A moniker that consists of two or more monikers that are treated as a unit.</span></span> <span data-ttu-id="0c7b7-197">複合的標記可以是非泛型，也就是說，其元件標記具有彼此的特殊知識（或泛型），也就是說，其元件的每個元件都不知道彼此的關係，只不過它們是名字標記</span><span class="sxs-lookup"><span data-stu-id="0c7b7-197">A composite moniker can be non-generic, meaning that its component monikers have special knowledge of each other, or generic, meaning that its component monikers know nothing about each other except that they are monikers</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-198"><span id="com.compound_document_gloss"></span><span id="COM.COMPOUND_DOCUMENT_GLOSS"></span>**複合檔案**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-198"><span id="com.compound_document_gloss"></span><span id="COM.COMPOUND_DOCUMENT_GLOSS"></span>**compound document**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-199">包含連結或内嵌物件的檔，以及其本身的原生資料。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-199">A document that includes linked or embedded objects, as well as its own native data.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-200"><span id="com.compound_file_gloss"></span><span id="COM.COMPOUND_FILE_GLOSS"></span>**複合檔案**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-200"><span id="com.compound_file_gloss"></span><span id="COM.COMPOUND_FILE_GLOSS"></span>**compound file**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-201">OLE 提供的結構化儲存體實作為。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-201">An OLE-provided Structured Storage implementation.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-202"><span id="com.com_object_gloss"></span><span id="COM.COM_OBJECT_GLOSS"></span>**COM 物件**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-202"><span id="com.com_object_gloss"></span><span id="COM.COM_OBJECT_GLOSS"></span>**COM object**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-203">符合 OLE 元件物件模型 (COM) 的物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-203">An object that conforms to the OLE Component Object Model (COM).</span></span> <span data-ttu-id="0c7b7-204">COM 物件是物件定義的實例，可指定物件的資料，以及物件上的一或多個介面介面。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-204">A COM object is an instance of an object definition, which specifies the object's data and one or more implementations of interfaces on the object.</span></span> <span data-ttu-id="0c7b7-205">用戶端只會透過其介面與 COM 物件互動。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-205">Clients interact with a COM object only through its interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-206"><span id="com.connectable_object_gloss"></span><span id="COM.CONNECTABLE_OBJECT_GLOSS"></span>**可連線物件**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-206"><span id="com.connectable_object_gloss"></span><span id="COM.CONNECTABLE_OBJECT_GLOSS"></span>**connectable object**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-207">一種 COM 物件，它至少會為 [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) 介面執行，以管理連接點物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-207">A COM object that implements, at a minimum, the [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) interface, for the management of connection point objects.</span></span> <span data-ttu-id="0c7b7-208">可連線物件支援從伺服器到用戶端的通訊。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-208">Connectable objects support communication from the server to the client.</span></span> <span data-ttu-id="0c7b7-209">可連線物件會建立和管理一個或多個連接點子物件，以從其他物件上所執行的介面接收事件，並將它們傳送至用戶端。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-209">A connectable object creates and manages one or more connection point subobjects, which receive events from interfaces implemented on other objects and send them on to the client.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-210"><span id="com.connection_point_object_gloss"></span><span id="COM.CONNECTION_POINT_OBJECT_GLOSS"></span>**連接點物件**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-210"><span id="com.connection_point_object_gloss"></span><span id="COM.CONNECTION_POINT_OBJECT_GLOSS"></span>**connection point object**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-211">由可連接的物件所管理，並可執行 [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) 介面的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-211">A COM object that is managed by a connectable object and that implements the [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) interface.</span></span> <span data-ttu-id="0c7b7-212">可連線物件可以建立和管理一個或多個連接點物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-212">One or more connection point objects can be created and managed by a connectable object.</span></span> <span data-ttu-id="0c7b7-213">每個連接點物件都會管理來自另一個物件上特定介面的傳入事件，並將這些事件傳送至用戶端。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-213">Each connection point object manages incoming events from a specific interface on another object and sends those events on to the client.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-214"><span id="com.container_application_gloss"></span><span id="COM.CONTAINER_APPLICATION_GLOSS"></span>**容器應用程式**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-214"><span id="com.container_application_gloss"></span><span id="COM.CONTAINER_APPLICATION_GLOSS"></span>**container application**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-215">支援複合檔案的應用程式。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-215">An application that supports compound documents.</span></span> <span data-ttu-id="0c7b7-216">容器應用程式會提供內嵌或連結化物件的儲存體、顯示的網站、對顯示網站的存取，以及接收物件變更通知的諮詢接收。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-216">The container application provides storage for an embedded or linked object, a site for its display, access to the display site, and an advisory sink for receiving notifications of changes in the object.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-217"><span id="com.containment_gloss"></span><span id="COM.CONTAINMENT_GLOSS"></span>**遏制**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-217"><span id="com.containment_gloss"></span><span id="COM.CONTAINMENT_GLOSS"></span>**containment**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-218">用來執行 COM 物件的組合技術。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-218">A composition technique for implementing COM objects.</span></span> <span data-ttu-id="0c7b7-219">它可讓一個物件重複使用一個或多個其他物件的部分或所有介面。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-219">It allows one object to reuse some or all of the interface implementations of one or more other objects.</span></span> <span data-ttu-id="0c7b7-220">外部物件會作為其他物件的用戶端，並在想要使用其中一個包含物件的服務時委派執行。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-220">The outer object acts as a client to the other objects, delegating implementation when it wishes to use the services of one of the contained objects.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-221"><span id="com.context_gloss"></span><span id="COM.CONTEXT_GLOSS"></span>**上下文**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-221"><span id="com.context_gloss"></span><span id="COM.CONTEXT_GLOSS"></span>**context**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-222">在 COM + 中，一組與一或多個 COM 物件相關聯的執行時間屬性，可用來為這些物件提供服務。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-222">In COM+, a set of run-time properties associated with one or more COM objects that are used to provide services for those objects.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-223"><span id="com.control_gloss"></span><span id="COM.CONTROL_GLOSS"></span>**控制**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-223"><span id="com.control_gloss"></span><span id="COM.CONTROL_GLOSS"></span>**control**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-224">最少支援 [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) 介面的可內嵌、可重複使用的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-224">An embeddable, reusable COM object that supports, at a minimum, the [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) interface.</span></span> <span data-ttu-id="0c7b7-225">控制項通常與使用者介面相關聯。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-225">Controls are typically associated with the user interface.</span></span> <span data-ttu-id="0c7b7-226">它們也支援與容器的通訊，而且可以由多個用戶端重複使用（視授權準則而定）。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-226">They also support communication with a container and can be reused by multiple clients, depending upon licensing criteria.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-227"><span id="com.control_container_gloss"></span><span id="COM.CONTROL_CONTAINER_GLOSS"></span>**控制容器**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-227"><span id="com.control_container_gloss"></span><span id="COM.CONTROL_CONTAINER_GLOSS"></span>**control container**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-228">藉由執行 [**>iolecontrolsite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) 介面，支援內嵌控制項的應用程式。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-228">An application that supports embedding of controls by implementing the [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) interface.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-229"><span id="com.control_property_gloss"></span><span id="COM.CONTROL_PROPERTY_GLOSS"></span>**控制項屬性**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-229"><span id="com.control_property_gloss"></span><span id="COM.CONTROL_PROPERTY_GLOSS"></span>**control property**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-230">由控制項本身公開和管理的執行時間屬性。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-230">A run-time property that is exposed and managed by the control itself.</span></span> <span data-ttu-id="0c7b7-231">例如，控制項所使用的字型和文字大小就是控制項屬性。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-231">For example, the font and text size used by the control are control properties.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-232"><span id="com.controlling_object_gloss"></span><span id="COM.CONTROLLING_OBJECT_GLOSS"></span>**控制物件**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-232"><span id="com.controlling_object_gloss"></span><span id="COM.CONTROLLING_OBJECT_GLOSS"></span>**controlling object**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-233">匯總物件內的物件，可控制匯總物件內的哪些介面是公開的，而是私用的。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-233">The object within an aggregate object that controls which interfaces within the aggregate object are exposed and which are private.</span></span> <span data-ttu-id="0c7b7-234">控制物件的 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 介面稱為控制 **iunknown**。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-234">The [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface of the controlling object is called the controlling **IUnknown**.</span></span> <span data-ttu-id="0c7b7-235">對匯總中其他物件的 **IUnknown** 方法的呼叫必須傳遞至控制 **IUnknown**。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-235">Calls to **IUnknown** methods of other objects in the aggregate must be passed to the controlling **IUnknown**.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-236"><span id="com.control_site_gloss"></span><span id="COM.CONTROL_SITE_GLOSS"></span>**控制網站**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-236"><span id="com.control_site_gloss"></span><span id="COM.CONTROL_SITE_GLOSS"></span>**control site**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-237">控制項容器所執行的結構，用於管理控制項的顯示和儲存。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-237">A structure implemented by a control container for managing the display and storage of a control.</span></span> <span data-ttu-id="0c7b7-238">在指定的容器內，每個控制項都有對應的控制網站。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-238">Within a given container, each control has a corresponding control site.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-239"><span id="com.data_transfer_object_gloss"></span><span id="COM.DATA_TRANSFER_OBJECT_GLOSS"></span>**資料傳輸物件**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-239"><span id="com.data_transfer_object_gloss"></span><span id="COM.DATA_TRANSFER_OBJECT_GLOSS"></span>**data transfer object**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-240">物件，這個物件會執行 [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) 介面，並且包含要透過剪貼簿或拖放作業從某個物件傳送到另一個物件的資料。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-240">An object that implements the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) interface and contains data to be transferred from one object to another through either the Clipboard or drag-and-drop operations.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-241"><span id="com.default_object_handler_gloss"></span><span id="COM.DEFAULT_OBJECT_HANDLER_GLOSS"></span>**預設物件處理常式**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-241"><span id="com.default_object_handler_gloss"></span><span id="COM.DEFAULT_OBJECT_HANDLER_GLOSS"></span>**default object handler**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-242">以 OLE 提供的 DLL，可作為真實物件之容器應用程式的處理空間中的代理。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-242">A DLL provided with OLE that acts as a surrogate in the processing space of the container application for the real object.</span></span>

<span data-ttu-id="0c7b7-243">您可以使用預設物件處理常式來查看物件的儲存資料，而不需要實際啟用物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-243">With the default object handler, it is possible to look at an object's stored data without actually activating the object.</span></span> <span data-ttu-id="0c7b7-244">預設物件處理常式會執行其他工作，例如在物件載入記憶體時，從其快取狀態轉譯物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-244">The default object handler performs other tasks, such as rendering an object from its cached state when the object is loaded into memory.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-245"><span id="com.dependent_object_gloss"></span><span id="COM.DEPENDENT_OBJECT_GLOSS"></span>**相依物件**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-245"><span id="com.dependent_object_gloss"></span><span id="COM.DEPENDENT_OBJECT_GLOSS"></span>**dependent object**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-246">COM 物件，通常由另一個物件初始化， (主物件) 。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-246">A COM object that is typically initialized by another object (the host object).</span></span> <span data-ttu-id="0c7b7-247">雖然相依物件的存留期在主物件的存留期內可能只有意義，但主機物件不會做為相依物件的控制 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-247">Although the dependent object's lifetime may only make sense during the lifetime of the host object, the host object does not function as the controlling [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) for the dependent object.</span></span> <span data-ttu-id="0c7b7-248">相反地，當物件的存留期 (藉由管理物件完全控制) 的參考計數時，物件就是匯總物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-248">In contrast, an object is an aggregated object when its lifetime (by means of its reference count) is completely controlled by the managing object.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-249"><span id="com.direct_access_mode_gloss"></span><span id="COM.DIRECT_ACCESS_MODE_GLOSS"></span>**直接存取模式**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-249"><span id="com.direct_access_mode_gloss"></span><span id="COM.DIRECT_ACCESS_MODE_GLOSS"></span>**direct access mode**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-250">可以開啟儲存物件的兩種存取模式之一。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-250">One of two access modes in which a storage object can be opened.</span></span> <span data-ttu-id="0c7b7-251">在直接模式中，所有變更都會立即認可至根儲存物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-251">In direct mode, all changes are immediately committed to the root storage object.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-252"><span id="com.document_object_gloss"></span><span id="COM.DOCUMENT_OBJECT_GLOSS"></span>**document 物件**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-252"><span id="com.document_object_gloss"></span><span id="COM.DOCUMENT_OBJECT_GLOSS"></span>**document object**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-253">可以在原生或外部的框架（例如瀏覽器）中，顯示其資料的一或多個就地啟用資料檢視，同時保留其使用者介面的完整控制權的 OLE 檔。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-253">An OLE document that can display one or more in-place activated views of its data within a native or foreign frame, such as a browser, while retaining full control over its user interface.</span></span> <span data-ttu-id="0c7b7-254">除了執行一般的 OLE 檔和就地啟用介面之外，檔物件還必須執行 [**IOleDocument**](/windows/desktop/api/DocObj/nn-docobj-ioledocument)，而且每一個視圖都 (檔視圖物件的格式，) 必須執行 [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview)。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-254">In addition to implementing the usual OLE document and in-place activation interfaces, a document object must implement [**IOleDocument**](/windows/desktop/api/DocObj/nn-docobj-ioledocument), and each of its views (in the form of a document view object) must implement [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview).</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-255"><span id="com.document_object_container_gloss"></span><span id="COM.DOCUMENT_OBJECT_CONTAINER_GLOSS"></span>**檔物件容器**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-255"><span id="com.document_object_container_gloss"></span><span id="COM.DOCUMENT_OBJECT_CONTAINER_GLOSS"></span>**document object container**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-256">容器應用程式，能夠顯示一個或多個檔物件的一或多個視圖，以及管理檔案內所有包含的檔物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-256">A container application capable of displaying one or more views of one or more document objects and of managing all contained document objects within a file.</span></span> <span data-ttu-id="0c7b7-257">每個檔物件都與一個檔網站相關聯，而每個檔網站都包含一或多個對應至檔物件所支援之視圖的檔視圖網站。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-257">Each document object is associated with a document site, and each document site contains one or more document view sites corresponding to the views supported by the document object.</span></span> <span data-ttu-id="0c7b7-258">檔物件容器也包含一個容器框架，可處理功能表和工具列的協商以及所包含物件的列舉。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-258">A document object container also includes a container frame, which handles menu and toolbar negotiation and the enumeration of contained objects.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-259"><span id="com.document_object_server_gloss"></span><span id="COM.DOCUMENT_OBJECT_SERVER_GLOSS"></span>**檔物件服務器**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-259"><span id="com.document_object_server_gloss"></span><span id="COM.DOCUMENT_OBJECT_SERVER_GLOSS"></span>**document object server**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-260">能夠提供檔物件的伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-260">A server application capable of providing document objects.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-261"><span id="com.document_site_gloss"></span><span id="COM.DOCUMENT_SITE_GLOSS"></span>**檔網站**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-261"><span id="com.document_site_gloss"></span><span id="COM.DOCUMENT_SITE_GLOSS"></span>**document site**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-262">由檔物件容器所執行的用戶端網站，用來管理檔物件的顯示和儲存。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-262">A client site implemented by a document object container for managing the display and storage of a document object.</span></span> <span data-ttu-id="0c7b7-263">容器中的每個檔物件都有對應的檔網站。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-263">Each document object in a container has a corresponding document site.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-264"><span id="com.document_site_object_gloss"></span><span id="COM.DOCUMENT_SITE_OBJECT_GLOSS"></span>**檔網站物件**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-264"><span id="com.document_site_object_gloss"></span><span id="COM.DOCUMENT_SITE_OBJECT_GLOSS"></span>**document site object**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-265">除了一般的用戶端網站介面 (（例如 [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)) ）之外，還會執行 [**IOLEDOCUMENTSITE**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentsite)介面的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-265">A COM object that implements the [**IOleDocumentSite**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentsite) interface, in addition to the usual client-site interfaces (such as [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)).</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-266"><span id="com.document_view_gloss"></span><span id="COM.DOCUMENT_VIEW_GLOSS"></span>**檔視圖**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-266"><span id="com.document_view_gloss"></span><span id="COM.DOCUMENT_VIEW_GLOSS"></span>**document view**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-267">檔資料的特定標記法。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-267">A particular presentation of a document's data.</span></span> <span data-ttu-id="0c7b7-268">單一檔物件可以有一或多個視圖，但是單一檔視圖只能屬於一個檔物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-268">A single document object can have one or more views, but a single document view can belong to one and only one document object.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-269"><span id="com.document_view_object_gloss"></span><span id="COM.DOCUMENT_VIEW_OBJECT_GLOSS"></span>**document view 物件**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-269"><span id="com.document_view_object_gloss"></span><span id="COM.DOCUMENT_VIEW_OBJECT_GLOSS"></span>**document view object**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-270">COM 物件，它會執行 [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview) 介面並對應至特定的檔查看。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-270">A COM object that implements the [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview) interface and corresponds to a particular document view.</span></span> <span data-ttu-id="0c7b7-271">具有多個檔視圖的物件會匯總每個視圖的個別檔視圖物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-271">An object with multiple document views aggregates a separate document view object for each view.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-272"><span id="com.document_view_site_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_GLOSS"></span>**檔視圖網站**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-272"><span id="com.document_view_site_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_GLOSS"></span>**document view site**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-273">由檔網站物件匯總的物件，用於管理檔物件之特定視圖的顯示空間。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-273">An object aggregated by a document site object for managing the display space for a particular view of a document object.</span></span> <span data-ttu-id="0c7b7-274">在給定的檔網站內，每個檔視圖都有對應的檔視圖網站。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-274">Within a given document site, each document view has a corresponding document view site.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-275"><span id="com.document_view_site_object_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_OBJECT_GLOSS"></span>**檔視圖網站物件**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-275"><span id="com.document_view_site_object_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_OBJECT_GLOSS"></span>**document view site object**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-276">在檔網站物件中匯總的 COM 物件，並可執行 [**IOleInPlaceSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite) 介面和（選擇性） [**IContinueCallback**](/windows/desktop/api/DocObj/nn-docobj-icontinuecallback) 介面。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-276">A COM object that is aggregated in a document site object and implements the [**IOleInPlaceSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite) interface and, optionally, the [**IContinueCallback**](/windows/desktop/api/DocObj/nn-docobj-icontinuecallback) interface.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-277"><span id="com.drag_and_drop_gloss"></span><span id="COM.DRAG_AND_DROP_GLOSS"></span>**拖放**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-277"><span id="com.drag_and_drop_gloss"></span><span id="COM.DRAG_AND_DROP_GLOSS"></span>**drag and drop**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-278">使用者使用滑鼠或其他指標裝置將資料移至相同視窗或另一個視窗中的另一個位置的操作。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-278">An operation in which the end user uses the mouse or other pointing device to move data to another location in the same window or another window.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-279"><span id="com.embed_gloss"></span><span id="COM.EMBED_GLOSS"></span>**嵌入**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-279"><span id="com.embed_gloss"></span><span id="COM.EMBED_GLOSS"></span>**embed**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-280">將物件插入複合檔案中，以保留該物件的原生資料格式，並使用其伺服器所公開的工具，在其容器內進行編輯。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-280">To insert an object into a compound document in such a way as to preserve the data formats native to that object, and to enable it to be edited from within its container using tools exposed by its server.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-281"><span id="com.embedded_object_gloss"></span><span id="COM.EMBEDDED_OBJECT_GLOSS"></span>**embedded 物件**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-281"><span id="com.embedded_object_gloss"></span><span id="COM.EMBEDDED_OBJECT_GLOSS"></span>**embedded object**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-282">物件，其資料會儲存在複合檔案中，但物件會在其伺服器的進程空間中執行。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-282">An object whose data is stored in a compound document, but the object runs in the process space of its server.</span></span> <span data-ttu-id="0c7b7-283">預設物件處理常式會在容器應用程式的處理空間中提供實際物件的代理。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-283">The default object handler provides a surrogate in the processing space of the container application for the real object.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-284"><span id="com.extended_property_gloss"></span><span id="COM.EXTENDED_PROPERTY_GLOSS"></span>**擴充屬性**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-284"><span id="com.extended_property_gloss"></span><span id="COM.EXTENDED_PROPERTY_GLOSS"></span>**extended property**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-285">執行時間屬性，例如控制項的位置和大小，使用者會假設該控制項會由控制項公開，但會由容器公開和管理。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-285">A run-time property, such as a control's position and size, that a user would assume to be exposed by the control but is exposed and managed by the container.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-286"><span id="com.file_moniker_gloss"></span><span id="COM.FILE_MONIKER_GLOSS"></span>**檔案標記**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-286"><span id="com.file_moniker_gloss"></span><span id="COM.FILE_MONIKER_GLOSS"></span>**file moniker**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-287">以檔案系統中的路徑為基礎的名字。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-287">A moniker based on a path in the file system.</span></span> <span data-ttu-id="0c7b7-288">檔案標記可以用來識別儲存在自己檔案中的物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-288">File monikers can be used to identify objects that are saved in their own files.</span></span> <span data-ttu-id="0c7b7-289">檔案標記是一種 COM 物件，可針對檔案的標記類別支援 [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) 介面的系統提供的實作為。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-289">A file moniker is a COM object that supports the system-provided implementation of the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface for the file moniker class.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-290"><span id="com.font_object_gloss"></span><span id="COM.FONT_OBJECT_GLOSS"></span>**字型物件**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-290"><span id="com.font_object_gloss"></span><span id="COM.FONT_OBJECT_GLOSS"></span>**font object**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-291">COM 物件，可透過實 [**>ifont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) 介面，提供對圖形裝置介面 (GDI) 字型的存取權。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-291">A COM object that provides access to Graphics Device Interface (GDI) fonts by implementing the [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) interface.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-292"><span id="com.format_identifier_gloss"></span><span id="COM.FORMAT_IDENTIFIER_GLOSS"></span>**格式識別碼**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-292"><span id="com.format_identifier_gloss"></span><span id="COM.FORMAT_IDENTIFIER_GLOSS"></span>**format identifier**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-293">識別持續性屬性集的 GUID。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-293">A GUID that identifies a persistent property set.</span></span> <span data-ttu-id="0c7b7-294">也稱為 FMTID。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-294">Also referred to as FMTID.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-295"><span id="com.frame_gloss"></span><span id="COM.FRAME_GLOSS"></span>**框架**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-295"><span id="com.frame_gloss"></span><span id="COM.FRAME_GLOSS"></span>**frame**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-296">容器應用程式的一部分，負責以內嵌的 COM 物件或檔物件來協調功能表、快速鍵、工具列和其他共用的使用者介面元素。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-296">The part of a container application responsible for negotiating menus, accelerator keys, toolbars, and other shared user-interface elements with an embedded COM object or a document object.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-297"><span id="com.frame_object_gloss"></span><span id="COM.FRAME_OBJECT_GLOSS"></span>**frame 物件**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-297"><span id="com.frame_object_gloss"></span><span id="COM.FRAME_OBJECT_GLOSS"></span>**frame object**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-298">COM 物件，它會執行 [**IOleInPlaceFrame**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe) 介面和（選擇性） [**IOleCommandTarget**](/windows/desktop/api/DocObj/nn-docobj-iolecommandtarget) 介面。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-298">A COM object that implements the [**IOleInPlaceFrame**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe) interface and, optionally, the [**IOleCommandTarget**](/windows/desktop/api/DocObj/nn-docobj-iolecommandtarget) interface.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-299"><span id="com.generic_composite_moniker_gloss"></span><span id="COM.GENERIC_COMPOSITE_MONIKER_GLOSS"></span>**泛型複合標記**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-299"><span id="com.generic_composite_moniker_gloss"></span><span id="COM.GENERIC_COMPOSITE_MONIKER_GLOSS"></span>**generic composite moniker**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-300">依序排序的標記集合，開頭為檔案的標記，以提供檔層級路徑，並繼續進行一或多個以整體方式執行的專案名字標記，以唯一的方式識別物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-300">A sequenced collection of monikers, starting with a file moniker to provide the document-level path and continuing with one or more item monikers that, taken as a whole, uniquely identifies an object.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-301"><span id="com.helper_function_gloss"></span><span id="COM.HELPER_FUNCTION_GLOSS"></span>**helper 函式**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-301"><span id="com.helper_function_gloss"></span><span id="COM.HELPER_FUNCTION_GLOSS"></span>**helper function**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-302">此函式會將呼叫封裝至 OLE SDK 中公開提供的其他函式和介面方法。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-302">A function that encapsulates calls to other functions and interface methods publicly available in the OLE SDK.</span></span> <span data-ttu-id="0c7b7-303">Helper 函式是一種便利的方式，可呼叫用來完成一般工作的常用函數和方法呼叫序列。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-303">Helper functions are a convenient way to call frequently used sequences of function and method calls that accomplish common tasks.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-304"><span id="com.host_object_gloss"></span><span id="COM.HOST_OBJECT_GLOSS"></span>**主機物件**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-304"><span id="com.host_object_gloss"></span><span id="COM.HOST_OBJECT_GLOSS"></span>**host object**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-305">COM 物件，與一或多個其他 COM 物件形成階層式關聯性，稱為相依物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-305">A COM object that forms a hierarchical relationship with one or more other COM objects, known as the dependent objects.</span></span> <span data-ttu-id="0c7b7-306">通常，主機物件會將相依物件具現化，而且其存在只有在主機物件的存留期內才有意義。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-306">Typically, the host object instantiates the dependent objects, and their existence only makes sense within the lifetime of the host object.</span></span> <span data-ttu-id="0c7b7-307">但是，主機物件不會做為相依物件的控制 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) ，也不會直接委派給這些物件的介面實現。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-307">However, the host object does not act as the controlling [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) for the dependent objects, nor does it directly delegate to the interface implementations of those objects.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-308"><span id="com.hresult_gloss"></span><span id="COM.HRESULT_GLOSS"></span>**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-308"><span id="com.hresult_gloss"></span><span id="COM.HRESULT_GLOSS"></span>**HRESULT**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-309">從函式成功傳回時，定義為零的不透明結果控制碼，如果傳回錯誤或狀態資訊，則為非零。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-309">An opaque result handle defined to be zero for a successful return from a function and nonzero if error or status information is returned.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-310"><span id="com.hyperlink_object_gloss"></span><span id="COM.HYPERLINK_OBJECT_GLOSS"></span>**hyperlink 物件**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-310"><span id="com.hyperlink_object_gloss"></span><span id="COM.HYPERLINK_OBJECT_GLOSS"></span>**hyperlink object**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-311">至少會執行 [**IHlink**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767974(v=vs.85)) 介面的 COM 物件，做為目標)  (位於另一個位置的物件連結。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-311">A COM object that implements, at a minimum, the [**IHlink**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767974(v=vs.85)) interface and acts as a link to an object at another location (the target).</span></span> <span data-ttu-id="0c7b7-312">超連結是由四個部分所組成：識別目標位置的標記：目標內位置的字串;目標的易記或可顯示名稱;以及可以包含其他參數的字串。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-312">A hyperlink is made up of four parts: a moniker that identifies the target's location; a string for the location within the target; a friendly, or displayable, name for the target; and a string that can contain additional parameters.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-313"><span id="com.hyperlink_browse_context_gloss"></span><span id="COM.HYPERLINK_BROWSE_CONTEXT_GLOSS"></span>**超連結流覽內容**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-313"><span id="com.hyperlink_browse_context_gloss"></span><span id="COM.HYPERLINK_BROWSE_CONTEXT_GLOSS"></span>**hyperlink browse context**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-314">COM 物件，它會執行 [**IHlinkBrowseCoNtext**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767949(v=vs.85)) 介面並維護超連結導覽堆疊。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-314">A COM object that implements the [**IHlinkBrowseContext**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767949(v=vs.85)) interface and maintains the hyperlink navigation stack.</span></span> <span data-ttu-id="0c7b7-315">流覽內容物件會管理超連結框架視窗和超連結目標物件的視窗。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-315">The browse context object manages the hyperlink frame window and hyperlink target object's window.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-316"><span id="com.hyperlink_container_gloss"></span><span id="COM.HYPERLINK_CONTAINER_GLOSS"></span>**超連結容器**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-316"><span id="com.hyperlink_container_gloss"></span><span id="COM.HYPERLINK_CONTAINER_GLOSS"></span>**hyperlink container**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-317">藉由執行 [**IHlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) 介面，以及容器的物件可以是其他超連結（ [**IHlinkTarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) 介面）的目標，來支援超連結的容器應用程式。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-317">A container application that supports hyperlinks by implementing the [**IHlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) interface and, if the container's objects can be targets of other hyperlinks, the [**IHlinkTarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) interface.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-318"><span id="com.hyperlink_frame_object_gloss"></span><span id="COM.HYPERLINK_FRAME_OBJECT_GLOSS"></span>**超連結框架物件**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-318"><span id="com.hyperlink_frame_object_gloss"></span><span id="COM.HYPERLINK_FRAME_OBJECT_GLOSS"></span>**hyperlink frame object**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-319">COM 物件，該物件會執行 [**IHlinkFrame**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767938(v=vs.85)) 介面，並控制框架容器和超連結目標伺服器的超連結的最上層導覽和顯示。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-319">A COM object that implements the [**IHlinkFrame**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767938(v=vs.85)) interface and controls the top-level navigation and display of hyperlinks for the frame's container and the hyperlink target's server.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-320"><span id="com.hyperlink_site_object_gloss"></span><span id="COM.HYPERLINK_SITE_OBJECT_GLOSS"></span>**超連結網站物件**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-320"><span id="com.hyperlink_site_object_gloss"></span><span id="COM.HYPERLINK_SITE_OBJECT_GLOSS"></span>**hyperlink site object**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-321">COM 物件，它會執行 [**IHlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) 介面並提供其超連結容器的標記或介面識別碼。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-321">A COM object that implements the [**IHlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) interface and supplies either the moniker or interface identifier of its hyperlink container.</span></span> <span data-ttu-id="0c7b7-322">其中一個超連結網站可以提供多個超連結。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-322">One hyperlink site can serve multiple hyperlinks.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-323"><span id="com.hyperlink_target_object_gloss"></span><span id="COM.HYPERLINK_TARGET_OBJECT_GLOSS"></span>**超連結目標物件**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-323"><span id="com.hyperlink_target_object_gloss"></span><span id="COM.HYPERLINK_TARGET_OBJECT_GLOSS"></span>**hyperlink target object**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-324">COM 物件，它會執行 [**IHlinkTarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) 介面並提供其標記、易記名稱，以及其他超連結物件將用來導覽的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-324">A COM object that implements the [**IHlinkTarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) interface and supplies its moniker, friendly name, and other information that other hyperlink objects will use to navigate to it.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-325"><span id="com.in_parameter_gloss"></span><span id="COM.IN_PARAMETER_GLOSS"></span>**in 參數**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-325"><span id="com.in_parameter_gloss"></span><span id="COM.IN_PARAMETER_GLOSS"></span>**in parameter**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-326">由函式或介面方法的呼叫端所配置、設定和釋放的參數。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-326">A parameter that is allocated, set, and freed by the caller of a function or interface method.</span></span> <span data-ttu-id="0c7b7-327">呼叫的函式不會修改 in 參數。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-327">An in parameter is not modified by the called function.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-328"><span id="com.in_out_parameter_gloss"></span><span id="COM.IN_OUT_PARAMETER_GLOSS"></span>**in/out 參數**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-328"><span id="com.in_out_parameter_gloss"></span><span id="COM.IN_OUT_PARAMETER_GLOSS"></span>**in/out parameter**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-329">一開始由函式或介面方法的呼叫端配置的參數，並視需要由呼叫的進程進行設定、釋放和重新配置。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-329">A parameter that is initially allocated by the caller of a function or interface method, and set, freed, and reallocated, if necessary, by the process that is called.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-330"><span id="com.in_place_activation_gloss"></span><span id="COM.IN_PLACE_ACTIVATION_GLOSS"></span>**就地啟用**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-330"><span id="com.in_place_activation_gloss"></span><span id="COM.IN_PLACE_ACTIVATION_GLOSS"></span>**in-place activation**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-331">使用伺服器所提供的工具，在其容器的視窗內編輯內嵌的物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-331">Editing an embedded object within the window of its container, using tools provided by the server.</span></span> <span data-ttu-id="0c7b7-332">連結化物件不支援就地啟用;它們一律是在伺服器的視窗中進行編輯。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-332">Linked objects do not support in-place activation; they are always edited in the window of the server.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-333"><span id="com.in_process_server_gloss"></span><span id="COM.IN_PROCESS_SERVER_GLOSS"></span>**同進程伺服器**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-333"><span id="com.in_process_server_gloss"></span><span id="COM.IN_PROCESS_SERVER_GLOSS"></span>**in-process server**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-334">實作為 DLL 的伺服器，會在用戶端的進程空間中執行。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-334">A server implemented as a DLL that runs in the process space of the client.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-335"><span id="com.instance_gloss"></span><span id="COM.INSTANCE_GLOSS"></span>**實例**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-335"><span id="com.instance_gloss"></span><span id="COM.INSTANCE_GLOSS"></span>**instance**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-336">配置給其記憶體或持續性的物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-336">An object for which memory is allocated or which is persistent.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-337"><span id="com.interface_gloss"></span><span id="COM.INTERFACE_GLOSS"></span>**介面**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-337"><span id="com.interface_gloss"></span><span id="COM.INTERFACE_GLOSS"></span>**interface**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-338">一組語義相關的函式，可提供 COM 物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-338">A group of semantically related functions that provide access to a COM object.</span></span> <span data-ttu-id="0c7b7-339">每個 OLE 介面都會定義一個合約，讓物件可以根據元件物件模型 (COM) 進行互動。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-339">Each OLE interface defines a contract that allows objects to interact according to the Component Object Model (COM).</span></span> <span data-ttu-id="0c7b7-340">雖然 OLE 提供許多介面，但大部分的介面也可以由開發人員設計 OLE 應用程式的開發人員來實行。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-340">While OLE provides many interface implementations, most interfaces can also be implemented by developers designing OLE applications.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-341"><span id="com.interface_identifier_iid_gloss"></span><span id="COM.INTERFACE_IDENTIFIER_IID_GLOSS"></span>**(IID 的介面識別碼)**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-341"><span id="com.interface_identifier_iid_gloss"></span><span id="COM.INTERFACE_IDENTIFIER_IID_GLOSS"></span>**interface identifier (IID)**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-342">全域唯一識別碼 (GUID) 與介面相關聯。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-342">A globally unique identifier (GUID) associated with an interface.</span></span> <span data-ttu-id="0c7b7-343">有些函式會接受 Iid 做為參數，以允許呼叫端指定應該傳回的介面指標。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-343">Some functions take IIDs as parameters to allow the caller to specify which interface pointer should be returned.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-344"><span id="com.item_moniker_gloss"></span><span id="COM.ITEM_MONIKER_GLOSS"></span>**專案標記**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-344"><span id="com.item_moniker_gloss"></span><span id="COM.ITEM_MONIKER_GLOSS"></span>**item moniker**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-345">以識別容器中物件的字串為基礎的標記。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-345">A moniker based on a string that identifies an object in a container.</span></span> <span data-ttu-id="0c7b7-346">專案專案識別碼可以識別出小於檔案的物件（包括複合檔案中的内嵌物件）或虛擬物件 (例如試算表中的資料格範圍) 。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-346">Item monikers can identify objects smaller than a file, including embedded objects in a compound document, or a pseudo-object (like a range of cells in a spreadsheet).</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-347"><span id="com.licensing_gloss"></span><span id="COM.LICENSING_GLOSS"></span>**發 牌**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-347"><span id="com.licensing_gloss"></span><span id="COM.LICENSING_GLOSS"></span>**licensing**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-348">COM 的功能，可控制物件的建立。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-348">A feature of COM that provides control over object creation.</span></span> <span data-ttu-id="0c7b7-349">授權物件只能由獲得授權使用的用戶端建立。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-349">Licensed objects can be created only by clients that are authorized to use them.</span></span> <span data-ttu-id="0c7b7-350">授權是透過 [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) 介面在 COM 中執行，並支援可在執行時間傳遞的授權金鑰。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-350">Licensing is implemented in COM through the [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) interface and by support for a license key that can be passed at run time.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-351"><span id="com.link_object_gloss"></span><span id="COM.LINK_OBJECT_GLOSS"></span>**連結化物件**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-351"><span id="com.link_object_gloss"></span><span id="COM.LINK_OBJECT_GLOSS"></span>**link object**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-352">建立或載入連結的 COM 物件時，所建立的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-352">A COM object that is created when a linked COM object is created or loaded.</span></span> <span data-ttu-id="0c7b7-353">Link 物件是由 OLE 提供，並會執行 [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink) 介面。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-353">The link object is provided by OLE and implements the [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink) interface.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-354"><span id="com.linked_object_gloss"></span><span id="COM.LINKED_OBJECT_GLOSS"></span>**連結化物件**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-354"><span id="com.linked_object_gloss"></span><span id="COM.LINKED_OBJECT_GLOSS"></span>**linked object**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-355">其來來源資料實際上位於其最初建立位置的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-355">A COM object whose source data physically resides where it was initially created.</span></span> <span data-ttu-id="0c7b7-356">只有表示來源資料的標記法和適當的呈現資料會保存在複合檔案中。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-356">Only a moniker that represents the source data and the appropriate presentation data are kept with the compound document.</span></span> <span data-ttu-id="0c7b7-357">對連結來源所做的變更會自動反映在連結的物件中。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-357">Changes made to the link source are automatically reflected in the linked object.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-358"><span id="com.link_source_gloss"></span><span id="COM.LINK_SOURCE_GLOSS"></span>**連結來源**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-358"><span id="com.link_source_gloss"></span><span id="COM.LINK_SOURCE_GLOSS"></span>**link source**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-359">連結化物件來源的資料。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-359">The data that is the source of a linked object.</span></span> <span data-ttu-id="0c7b7-360">連結來源可能是檔案或檔案的一部分，例如檔案內選取的儲存格範圍 (也稱為虛擬物件) 。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-360">A link source may be a file or a portion of a file, such as a selected range of cells within a file (also called a pseudo object).</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-361"><span id="com.loaded_state_gloss"></span><span id="COM.LOADED_STATE_GLOSS"></span>**載入狀態**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-361"><span id="com.loaded_state_gloss"></span><span id="COM.LOADED_STATE_GLOSS"></span>**loaded state**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-362">物件的資料結構載入至記憶體並可供用戶端進程存取之後的狀態。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-362">The state of an object after its data structures have been loaded into memory and are accessible to the client process.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-363"><span id="com.local_server_gloss"></span><span id="COM.LOCAL_SERVER_GLOSS"></span>**本機伺服器**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-363"><span id="com.local_server_gloss"></span><span id="COM.LOCAL_SERVER_GLOSS"></span>**local server**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-364">實作為的跨進程伺服器。EXE 應用程式在與用戶端應用程式相同的電腦上執行。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-364">An out-of-process server implemented as an .EXE application running on the same computer as its client application.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-365"><span id="com.lock_gloss"></span><span id="COM.LOCK_GLOSS"></span>**鎖**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-365"><span id="com.lock_gloss"></span><span id="COM.LOCK_GLOSS"></span>**lock**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-366">指標，也可能是在執行中的物件上遞增的參考計數。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-366">A pointer held to-and possibly, a reference count incremented on-a running object.</span></span> <span data-ttu-id="0c7b7-367">OLE 定義了兩種類型的鎖定，可保留在物件上：強式和弱式。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-367">OLE defines two types of locks that can be held on an object: strong and weak.</span></span> <span data-ttu-id="0c7b7-368">若要執行強式鎖定，伺服器必須同時維持指標和參考計數，如此一來，物件才會在記憶體中保持「鎖定」狀態，直到伺服器呼叫 [**IUnknown：： Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)為止。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-368">To implement a strong lock, a server must maintain both a pointer and a reference count, so that the object will remain "locked" in memory at least until the server calls [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="0c7b7-369">若要執行弱式鎖定，伺服器只會維護物件的指標，讓其他進程可以終結物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-369">To implement a weak lock, the server maintains only a pointer to the object, so that the object can be destroyed by another process.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-370"><span id="com.marshaling_gloss"></span><span id="COM.MARSHALING_GLOSS"></span>**編組**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-370"><span id="com.marshaling_gloss"></span><span id="COM.MARSHALING_GLOSS"></span>**marshaling**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-371">跨執行緒或進程界限封裝和傳送介面方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-371">Packaging and sending interface method calls across thread or process boundaries.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-372"><span id="com.media_type_gloss"></span><span id="COM.MEDIA_TYPE_GLOSS"></span>**媒體類型**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-372"><span id="com.media_type_gloss"></span><span id="COM.MEDIA_TYPE_GLOSS"></span>**media type**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-373">MIME 的延伸模組，可在用戶端與物件之間進行資料格式的協商。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-373">An extension of MIME that allows data format negotiation between a client and an object.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-374"><span id="com.mime_content_type_gloss"></span><span id="COM.MIME_CONTENT_TYPE_GLOSS"></span>**MIME 內容類型**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-374"><span id="com.mime_content_type_gloss"></span><span id="COM.MIME_CONTENT_TYPE_GLOSS"></span>**MIME content type**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-375">MIME 的延伸模組，可在用戶端與物件之間進行資料格式的協商。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-375">An extension of MIME that allows data format negotiation between a client and an object.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-376"><span id="com.multipurpose_internet_mail_extension_gloss"></span><span id="COM.MULTIPURPOSE_INTERNET_MAIL_EXTENSION_GLOSS"></span>**多用途網際網路郵件延伸 (MIME)**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-376"><span id="com.multipurpose_internet_mail_extension_gloss"></span><span id="COM.MULTIPURPOSE_INTERNET_MAIL_EXTENSION_GLOSS"></span>**Multipurpose Internet Mail Extension (MIME)**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-377">一種網際網路通訊協定，最初開發的目的是為了允許跨異類網路、電腦和電子郵件環境的豐富內容交換電子郵件訊息。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-377">An Internet protocol originally developed to allow exchange of electronic mail messages with rich content across heterogeneous network, computer, and email environments.</span></span> <span data-ttu-id="0c7b7-378">在實務上，MIME 也是由非郵件應用程式採用和延伸。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-378">In practice, MIME has also been adopted and extended by non-mail applications.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-379"><span id="com.moniker_gloss"></span><span id="COM.MONIKER_GLOSS"></span>**綽號**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-379"><span id="com.moniker_gloss"></span><span id="COM.MONIKER_GLOSS"></span>**moniker**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-380">實 [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) 介面的物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-380">An object that implements the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface.</span></span> <span data-ttu-id="0c7b7-381">標記可做為唯一識別 COM 物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-381">A moniker acts as a name that uniquely identifies a COM object.</span></span> <span data-ttu-id="0c7b7-382">與路徑在檔案系統中識別檔案的方式相同，標記會識別目錄命名空間中的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-382">In the same way that a path identifies a file in the file system, a moniker identifies a COM object in the directory namespace.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-383"><span id="com.moniker_class_gloss"></span><span id="COM.MONIKER_CLASS_GLOSS"></span>**標記類別**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-383"><span id="com.moniker_class_gloss"></span><span id="COM.MONIKER_CLASS_GLOSS"></span>**moniker class**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-384">[**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker)介面的實作為。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-384">An implementation of the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface.</span></span> <span data-ttu-id="0c7b7-385">系統提供的標記類別包括檔案的名字、專案的名字、泛型複合標記、反標記、指標的標記，以及 URL 的名字。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-385">System-supplied moniker classes include file monikers, item monikers, generic composite monikers, anti-monikers, pointer monikers, and URL monikers.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-386"><span id="com.moniker_client_gloss"></span><span id="COM.MONIKER_CLIENT_GLOSS"></span>**標記用戶端**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-386"><span id="com.moniker_client_gloss"></span><span id="COM.MONIKER_CLIENT_GLOSS"></span>**moniker client**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-387">使用標記來取得其他應用程式所管理之物件的介面指標的應用程式。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-387">An application that uses monikers to acquire interface pointers to objects managed by another application.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-388"><span id="com.moniker_provider_gloss"></span><span id="COM.MONIKER_PROVIDER_GLOSS"></span>**標記提供者**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-388"><span id="com.moniker_provider_gloss"></span><span id="COM.MONIKER_PROVIDER_GLOSS"></span>**moniker provider**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-389">此應用程式可讓提供者識別其所管理的物件，讓其他應用程式可以存取這些物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-389">An application that makes available monikers that identify the objects it manages, so that the objects are accessible to other applications.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-390"><span id="com.namespace_extension_gloss"></span><span id="COM.NAMESPACE_EXTENSION_GLOSS"></span>**命名空間延伸模組**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-390"><span id="com.namespace_extension_gloss"></span><span id="COM.NAMESPACE_EXTENSION_GLOSS"></span>**namespace extension**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-391">處理 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)、 [**IPersistFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder)和 [**IShellView**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellview)的同進程 COM 物件，有時稱為命名空間延伸模組介面。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-391">An in-process COM object that implements [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), [**IPersistFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder), and [**IShellView**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellview), which are sometimes referred to as the namespace extension interfaces.</span></span> <span data-ttu-id="0c7b7-392">您可以使用命名空間延伸模組來擴充 shell 的命名空間，或建立個別的命名空間。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-392">A namespace extension is used either to extend the shell's namespace or to create a separate namespace.</span></span> <span data-ttu-id="0c7b7-393">[主要使用者] 是 [Windows 檔案總管] 和 [一般檔案] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-393">Primary users are the Windows Explorer and common file dialog boxes.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-394"><span id="com.native_data_gloss"></span><span id="COM.NATIVE_DATA_GLOSS"></span>**原生資料**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-394"><span id="com.native_data_gloss"></span><span id="COM.NATIVE_DATA_GLOSS"></span>**native data**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-395">OLE 伺服器應用程式在編輯内嵌物件時所使用的資料。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-395">The data used by an OLE server application when editing an embedded object.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-396"><span id="com.object_gloss"></span><span id="COM.OBJECT_GLOSS"></span>**物件**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-396"><span id="com.object_gloss"></span><span id="COM.OBJECT_GLOSS"></span>**object**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-397">在 OLE 中，程式設計結構會將定義和配置的資料和功能，同時封裝成單一單位，而且只會透過程式設計結構的介面來進行公用存取。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-397">In OLE, a programming structure encapsulating both data and functionality that are defined and allocated as a single unit and for which the only public access is through the programming structure's interfaces.</span></span> <span data-ttu-id="0c7b7-398">COM 物件至少必須支援 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 介面，此介面會在使用時維持物件的存在，並提供物件其他介面的存取權。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-398">A COM object must support, at a minimum, the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface, which maintains the object's existence while it is being used and provides access to the object's other interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-399"><span id="com.object_state_gloss"></span><span id="COM.OBJECT_STATE_GLOSS"></span>**物件狀態**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-399"><span id="com.object_state_gloss"></span><span id="COM.OBJECT_STATE_GLOSS"></span>**object state**</span></span> 
</dt> <dd>

<span data-ttu-id="0c7b7-400">其容器中的複合檔案物件和負責物件建立的應用程式之間的關聯性：主動、被動、已載入或執行中。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-400">The relationship between a compound document object in its container and the application responsible for the object's creation: active, passive, loaded, or running.</span></span> <span data-ttu-id="0c7b7-401">被動式物件儲存在磁片上或資料庫中，且物件未選取或作用中。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-401">Passive objects are stored on disk or in a database, and the object is not selected or active.</span></span> <span data-ttu-id="0c7b7-402">在載入狀態中，物件的資料結構已載入至記憶體中，但無法供編輯等作業使用。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-402">In the loaded state, the object's data structures have been loaded into memory, but they are not available for operations such as editing.</span></span> <span data-ttu-id="0c7b7-403">執行中的物件都已載入，並可供所有作業使用。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-403">Running objects are both loaded and available for all operations.</span></span> <span data-ttu-id="0c7b7-404">現用物件正在執行具有可見使用者介面的物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-404">Active objects are running objects that have a visible user interface.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-405"><span id="com.object_type_name_gloss"></span><span id="COM.OBJECT_TYPE_NAME_GLOSS"></span>**物件類型名稱**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-405"><span id="com.object_type_name_gloss"></span><span id="COM.OBJECT_TYPE_NAME_GLOSS"></span>**object type name**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-406">儲存為註冊資料庫中物件之可用資訊一部分的唯一識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-406">A unique identification string that is stored as part of the information available for an object in the registration database.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-407"><span id="com.ole_gloss"></span><span id="COM.OLE_GLOSS"></span>**Ole**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-407"><span id="com.ole_gloss"></span><span id="COM.OLE_GLOSS"></span>**OLE**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-408">Microsoft 以物件為基礎的技術，可跨進程與電腦界限共用資訊與服務。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-408">Microsoft's object-based technology for sharing information and services across process and computer boundaries.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-409"><span id="com.out_of_process_server_gloss"></span><span id="COM.OUT_OF_PROCESS_SERVER_GLOSS"></span>**跨進程伺服器**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-409"><span id="com.out_of_process_server_gloss"></span><span id="COM.OUT_OF_PROCESS_SERVER_GLOSS"></span>**out-of-process server**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-410">實作為的伺服器。EXE 應用程式，它會在其用戶端的進程之外執行，不論是在同一部電腦或遠端電腦上。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-410">A server, implemented as an .EXE application, which runs outside the process of its client, either on the same computer or a remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-411"><span id="com.out_parameter_gloss"></span><span id="COM.OUT_PARAMETER_GLOSS"></span>**out 參數**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-411"><span id="com.out_parameter_gloss"></span><span id="COM.OUT_PARAMETER_GLOSS"></span>**out parameter**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-412">Out 參數是由呼叫的函式所配置，且由呼叫端釋放。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-412">An out parameter is allocated by the function being called, and freed by caller.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-413"><span id="com.passive_state_gloss"></span><span id="COM.PASSIVE_STATE_GLOSS"></span>**被動狀態**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-413"><span id="com.passive_state_gloss"></span><span id="COM.PASSIVE_STATE_GLOSS"></span>**passive state**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-414">當 COM 物件儲存 (磁片或資料庫) 中時，該物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-414">The state of a COM object when it is stored (on disk or in a database).</span></span> <span data-ttu-id="0c7b7-415">未選取或使用中的物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-415">The object is not selected or active.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-416"><span id="com.persistent_property_gloss"></span><span id="COM.PERSISTENT_PROPERTY_GLOSS"></span>**持續性屬性**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-416"><span id="com.persistent_property_gloss"></span><span id="COM.PERSISTENT_PROPERTY_GLOSS"></span>**persistent property**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-417">可以持續儲存為儲存物件（例如檔案或目錄）一部分的資訊。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-417">Information that can be stored persistently as part of a storage object such as a file or directory.</span></span> <span data-ttu-id="0c7b7-418">持續性屬性會分組為可顯示及編輯的屬性集。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-418">Persistent properties are grouped into property sets, which can be displayed and edited.</span></span>

<span data-ttu-id="0c7b7-419">持續性屬性與使用 OLE 控制項和自動化技術建立之物件的執行時間屬性不同，它們可用來影響系統行為。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-419">A persistent property is different from the run-time properties of objects created with OLE Controls and Automation technologies, which can be used to affect system behavior.</span></span> <span data-ttu-id="0c7b7-420">[**PROPVARIANT**](/windows/win32/api/propidl/ns-propidl-propvariant)結構會定義所有有效的持續性屬性類型，而 **VARIANT** 結構會定義所有有效的執行時間屬性類型。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-420">The [**PROPVARIANT**](/windows/win32/api/propidl/ns-propidl-propvariant) structure defines all valid types of persistent properties, whereas the **VARIANT** structure defines all valid types of run-time properties.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-421"><span id="com.persistent_storage_gloss"></span><span id="COM.PERSISTENT_STORAGE_GLOSS"></span>**持續性儲存體**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-421"><span id="com.persistent_storage_gloss"></span><span id="COM.PERSISTENT_STORAGE_GLOSS"></span>**persistent storage**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-422">將檔案或物件儲存在像是檔案系統或資料庫等媒體中，如此一來，當檔案關閉之後再重新開啟時，物件和其資料就會保存下來。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-422">Storage of a file or object in a medium such as a file system or database so that the object and its data persist when the file is closed and then re-opened at a later time.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-423"><span id="com.picture_object_gloss"></span><span id="COM.PICTURE_OBJECT_GLOSS"></span>**圖片物件**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-423"><span id="com.picture_object_gloss"></span><span id="COM.PICTURE_OBJECT_GLOSS"></span>**picture object**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-424">COM 物件，可透過執行 [**圖片**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) 介面，提供對 GDI 影像的存取。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-424">A COM object that provides access to GDI images by implementing the [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) interface.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-425"><span id="com.pointer_moniker_gloss"></span><span id="COM.POINTER_MONIKER_GLOSS"></span>**指標標記**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-425"><span id="com.pointer_moniker_gloss"></span><span id="COM.POINTER_MONIKER_GLOSS"></span>**pointer moniker**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-426">將介面指標對應至記憶體中之物件的標記。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-426">A moniker that maps an interface pointer to an object in memory.</span></span> <span data-ttu-id="0c7b7-427">大部分的名字標記會識別可持續儲存的物件，而指標標記會識別無法進行的物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-427">Whereas most monikers identify objects that can be persistently stored, pointer monikers identify objects that cannot.</span></span> <span data-ttu-id="0c7b7-428">它們允許這類物件參與標記系結作業。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-428">They allow such objects to participate in a moniker binding operation.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-429"><span id="com.presentation_data_gloss"></span><span id="COM.PRESENTATION_DATA_GLOSS"></span>**簡報資料**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-429"><span id="com.presentation_data_gloss"></span><span id="COM.PRESENTATION_DATA_GLOSS"></span>**presentation data**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-430">容器用來顯示內嵌或連結化物件的資料。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-430">The data used by a container to display embedded or linked objects.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-431"><span id="com.primary_verb_gloss"></span><span id="COM.PRIMARY_VERB_GLOSS"></span>**主要動詞**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-431"><span id="com.primary_verb_gloss"></span><span id="COM.PRIMARY_VERB_GLOSS"></span>**primary verb**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-432">與使用者在物件上執行的最常見或慣用操作相關聯的動作。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-432">The action associated with the most common or preferred operation users perform on an object.</span></span> <span data-ttu-id="0c7b7-433">主要動詞一律定義為系統註冊資料庫中的動詞零。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-433">The primary verb is always defined as verb zero in the system registration database.</span></span> <span data-ttu-id="0c7b7-434">在物件上按兩下，即可執行物件的主要動詞。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-434">An object's primary verb is executed by double-clicking on the object.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-435"><span id="com.property_gloss"></span><span id="COM.PROPERTY_GLOSS"></span>**財產**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-435"><span id="com.property_gloss"></span><span id="COM.PROPERTY_GLOSS"></span>**property**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-436">與物件相關聯的資訊。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-436">Information that is associated with an object.</span></span> <span data-ttu-id="0c7b7-437">在 OLE 中，屬性分為兩種類別：執行時間屬性和持續性屬性。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-437">In OLE, properties fall into two categories: run-time properties and persistent properties.</span></span> <span data-ttu-id="0c7b7-438">執行時間屬性通常會與控制項物件或其容器相關聯。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-438">Run-time properties are typically associated with control objects or their containers.</span></span> <span data-ttu-id="0c7b7-439">例如，背景色彩是由控制項容器所設定的執行時間屬性。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-439">For example, background color is a run-time property set by a control's container.</span></span> <span data-ttu-id="0c7b7-440">持續性屬性與儲存的物件相關聯。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-440">Persistent properties are associated with stored objects.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-441"><span id="com.property_frame_gloss"></span><span id="COM.PROPERTY_FRAME_GLOSS"></span>**屬性框架**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-441"><span id="com.property_frame_gloss"></span><span id="COM.PROPERTY_FRAME_GLOSS"></span>**property frame**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-442">顯示控制項一或多個屬性頁的使用者介面機制。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-442">The user interface mechanism that displays one or more property pages for a control.</span></span> <span data-ttu-id="0c7b7-443">OLE 控制項執行時間系統會提供屬性框架的標準實作為，可使用 [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) helper 函數進行存取。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-443">The OLE Controls run-time system provides a standard implementation of a property frame that can be accessed by using the [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) helper function.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-444"><span id="com.property_identifier_gloss"></span><span id="COM.PROPERTY_IDENTIFIER_GLOSS"></span>**屬性識別碼**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-444"><span id="com.property_identifier_gloss"></span><span id="COM.PROPERTY_IDENTIFIER_GLOSS"></span>**property identifier**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-445">四位元組帶正負號的整數，識別屬性集內的持續性屬性。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-445">A four-byte signed integer that identifies a persistent property within a property set.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-446"><span id="com.property_page_gloss"></span><span id="COM.PROPERTY_PAGE_GLOSS"></span>**屬性頁**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-446"><span id="com.property_page_gloss"></span><span id="COM.PROPERTY_PAGE_GLOSS"></span>**property page**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-447">COM 物件，其具有屬於使用者介面一部分、由控制項實作為一部分的 CLSID，並且可讓您查看和設定控制項的屬性。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-447">A COM object with its own CLSID that is part of a user interface, implemented by a control, and allows the control's properties to be viewed and set.</span></span> <span data-ttu-id="0c7b7-448">屬性頁物件會執行 [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) 介面。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-448">Property page objects implement the [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) interface.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-449"><span id="com.property_page_site_gloss"></span><span id="COM.PROPERTY_PAGE_SITE_GLOSS"></span>**屬性頁面網站**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-449"><span id="com.property_page_site_gloss"></span><span id="COM.PROPERTY_PAGE_SITE_GLOSS"></span>**property page site**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-450">顯示內容頁的屬性框架內的位置。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-450">The location within a property frame where a property page is displayed.</span></span> <span data-ttu-id="0c7b7-451">屬性框架會執行 [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) 介面，其中包含的方法可管理控制項所提供的每個屬性頁的網站。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-451">The property frame implements the [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) interface, which contains methods to manage the sites of each of the property pages supplied by a control.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-452"><span id="com.property_set_gloss"></span><span id="COM.PROPERTY_SET_GLOSS"></span>**屬性集**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-452"><span id="com.property_set_gloss"></span><span id="COM.PROPERTY_SET_GLOSS"></span>**property set**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-453">與持續儲存之物件相關聯之屬性的邏輯相關群組。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-453">A logically related group of properties that is associated with a persistently stored object.</span></span> <span data-ttu-id="0c7b7-454">若要建立、開啟、刪除或列舉一或多個屬性集，請執行 [**IPropertySetStorage**](/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage) 介面。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-454">To create, open, delete, or enumerate one or more property sets, implement the [**IPropertySetStorage**](/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage) interface.</span></span> <span data-ttu-id="0c7b7-455">如果您使用複合檔案，您可以使用 OLE 的此介面執行，而不是自行執行。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-455">If you are using compound files, you can use OLE's implementation of this interface rather than implementing your own.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-456"><span id="com.property_set_storage_gloss"></span><span id="COM.PROPERTY_SET_STORAGE_GLOSS"></span>**屬性集儲存體**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-456"><span id="com.property_set_storage_gloss"></span><span id="COM.PROPERTY_SET_STORAGE_GLOSS"></span>**property set storage**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-457">保存屬性集的 COM 儲存物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-457">A COM storage object that holds a property set.</span></span> <span data-ttu-id="0c7b7-458">屬性集儲存區是與儲存物件相關聯和管理的相依物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-458">A property set storage is a dependent object associated with and managed by a storage object.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-459"><span id="com.property_sheet_gloss"></span><span id="COM.PROPERTY_SHEET_GLOSS"></span>**屬性工作表**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-459"><span id="com.property_sheet_gloss"></span><span id="COM.PROPERTY_SHEET_GLOSS"></span>**property sheet**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-460">一或多個物件的一組屬性頁。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-460">A set of property pages for one or more objects.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-461"><span id="com.proxy_gloss"></span><span id="COM.PROXY_GLOSS"></span>**代理**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-461"><span id="com.proxy_gloss"></span><span id="COM.PROXY_GLOSS"></span>**proxy**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-462">介面特定物件，可封裝該介面的參數，以準備遠端方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-462">An interface-specific object that packages parameters for that interface in preparation for a remote method call.</span></span> <span data-ttu-id="0c7b7-463">Proxy 會在寄件者的位址空間中執行，並與接收者位址空間中的對應存根進行通訊。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-463">A proxy runs in the address space of the sender and communicates with a corresponding stub in the receiver's address space.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-464"><span id="com.proxy_manager_gloss"></span><span id="COM.PROXY_MANAGER_GLOSS"></span>**proxy 管理員**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-464"><span id="com.proxy_manager_gloss"></span><span id="COM.PROXY_MANAGER_GLOSS"></span>**proxy manager**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-465">在標準封送處理中，管理單一物件之所有介面 proxy 的 proxy。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-465">In standard marshaling, a proxy that manages all the interface proxies for a single object.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-466"><span id="com.pseudo_object_gloss"></span><span id="COM.PSEUDO_OBJECT_GLOSS"></span>**虛擬物件**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-466"><span id="com.pseudo_object_gloss"></span><span id="COM.PSEUDO_OBJECT_GLOSS"></span>**pseudo object**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-467">檔或内嵌物件的一部分，例如試算表中的資料格範圍，可以是 COM 物件的來源。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-467">A portion of a document or embedded object, such as a range of cells in a spreadsheet, that can be the source for a COM object.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-468"><span id="com.reference_counting_gloss"></span><span id="COM.REFERENCE_COUNTING_GLOSS"></span>**參考計數**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-468"><span id="com.reference_counting_gloss"></span><span id="COM.REFERENCE_COUNTING_GLOSS"></span>**reference counting**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-469">保留物件的每個介面指標的計數，以確保在釋放物件的所有參考之前，不會終結物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-469">Keeping a count of each interface pointer held on an object to ensure that the object is not destroyed before all references to it are released.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-470"><span id="com.relative_moniker_gloss"></span><span id="COM.RELATIVE_MONIKER_GLOSS"></span>**相對的名字**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-470"><span id="com.relative_moniker_gloss"></span><span id="COM.RELATIVE_MONIKER_GLOSS"></span>**relative moniker**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-471">指定物件相對於另一個物件之位置的指定位置的名字。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-471">A moniker that specifies the location of an object relative to the location of another object.</span></span> <span data-ttu-id="0c7b7-472">相對的標記類似于相對路徑，例如。 \\備份 \\ 報表。舊的。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-472">A relative moniker is analogous to a relative path, such as ..\\backup\\report.old.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-473"><span id="com.remote_server_gloss"></span><span id="COM.REMOTE_SERVER_GLOSS"></span>**遠端伺服器**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-473"><span id="com.remote_server_gloss"></span><span id="COM.REMOTE_SERVER_GLOSS"></span>**remote server**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-474">從用戶端應用程式使用它在不同電腦上執行的伺服器應用程式，它會實作為 EXE。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-474">A server application, implemented as an EXE, running on a different computer from the client application using it.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-475"><span id="com.revert_gloss"></span><span id="COM.REVERT_GLOSS"></span>**恢復**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-475"><span id="com.revert_gloss"></span><span id="COM.REVERT_GLOSS"></span>**revert**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-476">捨棄自上次認可變更或開啟物件的儲存體之後，對物件所做的任何變更。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-476">To discard any changes made to an object since the last time the changes were committed or the object's storage was opened.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-477"><span id="com.root_storage_object_gloss"></span><span id="COM.ROOT_STORAGE_OBJECT_GLOSS"></span>**根儲存物件**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-477"><span id="com.root_storage_object_gloss"></span><span id="COM.ROOT_STORAGE_OBJECT_GLOSS"></span>**root storage object**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-478">檔中最外層的儲存物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-478">The outermost storage object in a document.</span></span> <span data-ttu-id="0c7b7-479">根儲存物件可以包含其他的嵌套儲存和資料流程物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-479">A root storage object can contain other nested storage and stream objects.</span></span> <span data-ttu-id="0c7b7-480">例如，複合檔案會儲存在磁片上，作為根儲存物件內的一系列儲存體和資料流程物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-480">For example, a compound document is saved on disk as a series of storage and stream objects within a root storage object.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-481"><span id="com.running_state_gloss"></span><span id="COM.RUNNING_STATE_GLOSS"></span>**正在執行狀態**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-481"><span id="com.running_state_gloss"></span><span id="COM.RUNNING_STATE_GLOSS"></span>**running state**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-482">COM 物件的伺服器應用程式執行時的狀態，而且可以存取其介面並接收變更的通知。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-482">The state of a COM object when its server application is running and it is possible to access its interfaces and receive notification of changes.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-483"><span id="com.running_object_table_gloss"></span><span id="COM.RUNNING_OBJECT_TABLE_GLOSS"></span>**正在執行物件資料表 (的 ROT)**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-483"><span id="com.running_object_table_gloss"></span><span id="COM.RUNNING_OBJECT_TABLE_GLOSS"></span>**running object table (ROT)**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-484">每一部電腦上可全域存取的資料表，這些資料表會追蹤處於執行中狀態的所有 COM 物件（可由標記識別）。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-484">A globally accessible table on each computer that keeps track of all COM objects in the running state that can be identified by a moniker.</span></span> <span data-ttu-id="0c7b7-485">在資料表中，「標記提供者」會將物件註冊，以遞增物件的參考計數。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-485">Moniker providers register an object in the table, which increments the object's reference count.</span></span> <span data-ttu-id="0c7b7-486">在可以終結物件之前，必須先從資料表釋放其標記。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-486">Before the object can be destroyed, its moniker must be released from the table.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-487"><span id="com.run_time_property_gloss"></span><span id="COM.RUN_TIME_PROPERTY_GLOSS"></span>**執行時間屬性**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-487"><span id="com.run_time_property_gloss"></span><span id="COM.RUN_TIME_PROPERTY_GLOSS"></span>**run-time property**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-488">與控制項物件或其容器相關聯的離散狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-488">Discrete state information associated with a control object or its container.</span></span> <span data-ttu-id="0c7b7-489">執行時間屬性有三種類型：環境屬性、控制項屬性和擴充屬性。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-489">There are three types of run-time properties: ambient properties, control properties, and extended properties.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-490"><span id="com.self_registration_gloss"></span><span id="COM.SELF_REGISTRATION_GLOSS"></span>**自我註冊**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-490"><span id="com.self_registration_gloss"></span><span id="COM.SELF_REGISTRATION_GLOSS"></span>**self-registration**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-491">伺服器可以執行自己的登錄作業的進程。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-491">The process by which a server can perform its own registry operations.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-492"><span id="com.server_application_gloss"></span><span id="COM.SERVER_APPLICATION_GLOSS"></span>**伺服器應用程式**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-492"><span id="com.server_application_gloss"></span><span id="COM.SERVER_APPLICATION_GLOSS"></span>**server application**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-493">可以建立 COM 物件的應用程式。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-493">An application that can create COM objects.</span></span> <span data-ttu-id="0c7b7-494">容器應用程式接著可以內嵌或連結至這些物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-494">Container applications can then embed or link to these objects.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-495"><span id="com.static_object_gloss"></span><span id="COM.STATIC_OBJECT_GLOSS"></span>**靜態物件**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-495"><span id="com.static_object_gloss"></span><span id="COM.STATIC_OBJECT_GLOSS"></span>**static object**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-496">物件，其中只包含標記法，沒有原生資料。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-496">An object that contains only a presentation, with no native data.</span></span> <span data-ttu-id="0c7b7-497">容器可以將靜態物件視為連結或內嵌的物件，但不可能編輯靜態物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-497">A container can treat a static object as though it were a linked or embedded object, except that it is not possible to edit a static object.</span></span>

<span data-ttu-id="0c7b7-498">例如，可能會導致靜態物件中斷連結化物件的連結（也就是伺服器應用程式無法使用），或使用者不想再更新連結化物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-498">A static object can result, for example, from the breaking of a link on a linked object-that is, the server application is unavailable, or the user doesn't want the linked object to be updated anymore.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-499"><span id="com.storage_object_gloss"></span><span id="COM.STORAGE_OBJECT_GLOSS"></span>**儲存物件**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-499"><span id="com.storage_object_gloss"></span><span id="COM.STORAGE_OBJECT_GLOSS"></span>**storage object**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-500">執行 [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) 介面的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-500">A COM object that implements the [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) interface.</span></span> <span data-ttu-id="0c7b7-501">儲存體物件包含嵌套的儲存物件或資料流程物件，它會在單一檔案中產生相當於目錄/檔案結構的專案。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-501">A storage object contains nested storage objects or stream objects, resulting in the equivalent of a directory/file structure within a single file.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-502"><span id="com.stream_object_gloss"></span><span id="COM.STREAM_OBJECT_GLOSS"></span>**stream 物件**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-502"><span id="com.stream_object_gloss"></span><span id="COM.STREAM_OBJECT_GLOSS"></span>**stream object**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-503">實作為 [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) 介面的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-503">A COM object that implements the [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface.</span></span> <span data-ttu-id="0c7b7-504">資料流程物件類似于目錄/檔案系統中的檔案。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-504">A stream object is analogous to a file in a directory/file system.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-505"><span id="com.structured_storage_gloss"></span><span id="COM.STRUCTURED_STORAGE_GLOSS"></span>**結構化儲存體**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-505"><span id="com.structured_storage_gloss"></span><span id="COM.STRUCTURED_STORAGE_GLOSS"></span>**Structured Storage**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-506">OLE 的技術，可將複合檔案儲存在原生檔案系統中。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-506">OLE's technology for storing compound files in native file systems.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-507"><span id="com.stub_gloss"></span><span id="COM.STUB_GLOSS"></span>**存根**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-507"><span id="com.stub_gloss"></span><span id="COM.STUB_GLOSS"></span>**stub**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-508">當函式或介面方法的參數跨進程界限封送處理時，存根是介面特定的物件，可 unpackages 已封送處理的參數並呼叫所需的方法。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-508">When a function's or interface method's parameters are marshaled across a process boundary, the stub is an interface-specific object that unpackages the marshaled parameters and calls the required method.</span></span> <span data-ttu-id="0c7b7-509">Stub 會在接收者的位址空間中執行，並與寄件者位址空間中的對應 proxy 進行通訊。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-509">The stub runs in the receiver's address space and communicates with a corresponding proxy in the sender's address space.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-510"><span id="com.stub_manager_gloss"></span><span id="COM.STUB_MANAGER_GLOSS"></span>**存根管理員**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-510"><span id="com.stub_manager_gloss"></span><span id="COM.STUB_MANAGER_GLOSS"></span>**stub manager**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-511">管理單一物件的所有介面存根。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-511">Manages all of the interface stubs for a single object.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-512"><span id="com.synchronous_call_gloss"></span><span id="COM.SYNCHRONOUS_CALL_GLOSS"></span>**同步呼叫**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-512"><span id="com.synchronous_call_gloss"></span><span id="COM.SYNCHRONOUS_CALL_GLOSS"></span>**synchronous call**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-513">函式呼叫，在函式傳回之前，不允許執行呼叫進程中的進一步指示。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-513">A function call that does not allow further instructions in the calling process to be executed until the function returns.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-514"><span id="com.system_registry_gloss"></span><span id="COM.SYSTEM_REGISTRY_GLOSS"></span>**系統登錄**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-514"><span id="com.system_registry_gloss"></span><span id="COM.SYSTEM_REGISTRY_GLOSS"></span>**system registry**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-515">Windows 所支援資訊的全系統儲存機制，其中包含有關系統和其應用程式（包括 OLE 用戶端和伺服器）的資訊。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-515">A system-wide repository of information supported by Windows, which contains information about the system and its applications, including OLE clients and servers.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-516"><span id="com.transacted_access_mode_gloss"></span><span id="COM.TRANSACTED_ACCESS_MODE_GLOSS"></span>**交易存取模式**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-516"><span id="com.transacted_access_mode_gloss"></span><span id="COM.TRANSACTED_ACCESS_MODE_GLOSS"></span>**transacted access mode**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-517">可以開啟儲存物件的兩種存取模式之一。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-517">One of two access modes in which a storage object can be opened.</span></span> <span data-ttu-id="0c7b7-518">在交易模式中開啟時，變更會儲存在緩衝區中，直到根儲存物件認可其變更為止。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-518">When opened in transacted mode, changes are stored in buffers until the root storage object commits its changes.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-519"><span id="com.type_information_gloss"></span><span id="COM.TYPE_INFORMATION_GLOSS"></span>**類型資訊**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-519"><span id="com.type_information_gloss"></span><span id="COM.TYPE_INFORMATION_GLOSS"></span>**type information**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-520">類型程式庫所提供之物件類別的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-520">Information about an object's class provided by a type library.</span></span> <span data-ttu-id="0c7b7-521">為了提供型別資訊，COM 物件會實 [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) 介面。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-521">To provide type information, a COM object implements the [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) interface.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-522"><span id="com.uniform_data_transfer_gloss"></span><span id="COM.UNIFORM_DATA_TRANSFER_GLOSS"></span>**制式資料傳輸**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-522"><span id="com.uniform_data_transfer_gloss"></span><span id="COM.UNIFORM_DATA_TRANSFER_GLOSS"></span>**uniform data transfer**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-523">透過「剪貼簿」、「拖放」或「自動化」來傳送資料的模型。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-523">A model for transferring data through the clipboard, drag and drop, or Automation.</span></span> <span data-ttu-id="0c7b7-524">符合此模型的物件會執行 [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) 介面。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-524">Objects conforming to this model implement the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) interface.</span></span> <span data-ttu-id="0c7b7-525">此模型取代了 DDE (動態資料交換) 。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-525">This model replaces DDE (dynamic data exchange).</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-526"><span id="com.unmarshaling_gloss"></span><span id="COM.UNMARSHALING_GLOSS"></span>**送**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-526"><span id="com.unmarshaling_gloss"></span><span id="COM.UNMARSHALING_GLOSS"></span>**unmarshaling**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-527">將已傳送至跨進程界限的 proxy 解壓縮參數。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-527">Unpacking parameters that have been sent to a proxy across process boundaries.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-528"><span id="com.universal_resource_locator_gloss"></span><span id="COM.UNIVERSAL_RESOURCE_LOCATOR_GLOSS"></span>**(URL) 的通用資源定位器**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-528"><span id="com.universal_resource_locator_gloss"></span><span id="COM.UNIVERSAL_RESOURCE_LOCATOR_GLOSS"></span>**universal resource locator (URL)**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-529">萬維網的識別碼，用於網際網路上的物件名稱和位置。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-529">The identifier used by the World Wide Web for the names and locations of objects on the Internet.</span></span> <span data-ttu-id="0c7b7-530">OLE 提供一個標記類別，也就是一個 URL 名字，可使用它來將用戶端系結至 URL 所識別的物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-530">OLE provides a moniker class, URL moniker, whose implementation can be used to bind a client to objects identified by a URL.</span></span>

</dd> <dt>

<span data-ttu-id="0c7b7-531"><span id="com.url_moniker_gloss"></span><span id="COM.URL_MONIKER_GLOSS"></span>**URL 標記**</span><span class="sxs-lookup"><span data-stu-id="0c7b7-531"><span id="com.url_moniker_gloss"></span><span id="COM.URL_MONIKER_GLOSS"></span>**URL moniker**</span></span>
</dt> <dd>

<span data-ttu-id="0c7b7-532">以通用資源定位器為基礎的名字， (URL) 。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-532">A moniker based on a universal resource locator (URL).</span></span> <span data-ttu-id="0c7b7-533">用戶端可以使用 URL 標記系系結至位於網際網路上的物件。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-533">A client can use URL monikers to bind to objects that reside on the Internet.</span></span> <span data-ttu-id="0c7b7-534">系統提供的 URL 標記類別支援同步和非同步系結。</span><span class="sxs-lookup"><span data-stu-id="0c7b7-534">The system-supplied URL moniker class supports both synchronous and asynchronous binding.</span></span>

</dd> </dl>

 

 