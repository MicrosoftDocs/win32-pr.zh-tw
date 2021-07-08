---
description: 本文說明如何將屬性處理常式初始化，以與 Windows 的屬性系統搭配使用。
ms.assetid: 3b54dd65-b7db-4e6a-bc3d-1008fdabcfa9
title: 初始化屬性處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4482af2a029a91049d421ee49eb0f439c5fd8d0e
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481903"
---
# <a name="initializing-property-handlers"></a><span data-ttu-id="9844e-103">初始化屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="9844e-103">Initializing Property Handlers</span></span>

<span data-ttu-id="9844e-104">本主題說明如何建立和註冊屬性處理常式，以便與 Windows 的屬性系統搭配使用。</span><span class="sxs-lookup"><span data-stu-id="9844e-104">This topic explains how to create and register property handlers to work with the Windows property system.</span></span>

<span data-ttu-id="9844e-105">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="9844e-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="9844e-106">屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="9844e-106">Property Handlers</span></span>](#property-handlers)
-   [<span data-ttu-id="9844e-107">開始之前</span><span class="sxs-lookup"><span data-stu-id="9844e-107">Before You Begin</span></span>](#before-you-begin)
-   [<span data-ttu-id="9844e-108">初始化屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="9844e-108">Initializing Property Handlers</span></span>](#initializing-property-handlers)
-   [<span data-ttu-id="9844e-109">記憶體中屬性儲存區</span><span class="sxs-lookup"><span data-stu-id="9844e-109">In-Memory Property Store</span></span>](#in-memory-property-store)
-   [<span data-ttu-id="9844e-110">處理 PROPVARIANT-Based 值</span><span class="sxs-lookup"><span data-stu-id="9844e-110">Dealing with PROPVARIANT-Based Values</span></span>](#dealing-with-propvariant-based-values)
-   [<span data-ttu-id="9844e-111">支援開放中繼資料</span><span class="sxs-lookup"><span data-stu-id="9844e-111">Supporting Open Metadata</span></span>](#supporting-open-metadata)
-   [<span data-ttu-id="9844e-112">全文檢索內容</span><span class="sxs-lookup"><span data-stu-id="9844e-112">Full-Text Contents</span></span>](#full-text-contents)
-   [<span data-ttu-id="9844e-113">提供屬性的值</span><span class="sxs-lookup"><span data-stu-id="9844e-113">Providing Values for Properties</span></span>](#providing-values-for-properties)
-   [<span data-ttu-id="9844e-114">回寫值</span><span class="sxs-lookup"><span data-stu-id="9844e-114">Writing Back Values</span></span>](#writing-back-values)
-   [<span data-ttu-id="9844e-115">執行 IPropertyStoreCapabilities</span><span class="sxs-lookup"><span data-stu-id="9844e-115">Implementing IPropertyStoreCapabilities</span></span>](#implementing-ipropertystorecapabilities)
-   [<span data-ttu-id="9844e-116">註冊和散發屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="9844e-116">Registering and Distributing Property Handlers</span></span>](#registering-and-distributing-property-handlers)
-   [<span data-ttu-id="9844e-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="9844e-117">Related topics</span></span>](#related-topics)

## <a name="property-handlers"></a><span data-ttu-id="9844e-118">屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="9844e-118">Property Handlers</span></span>

<span data-ttu-id="9844e-119">屬性處理常式是屬性系統的重要部分。</span><span class="sxs-lookup"><span data-stu-id="9844e-119">Property handlers are a crucial part of the property system.</span></span> <span data-ttu-id="9844e-120">索引子會在同進程中叫用它們，以讀取和編制屬性值的索引，而且也會透過 Windows 檔案總管同進程來叫用，以便直接在檔案中讀取和寫入屬性值。</span><span class="sxs-lookup"><span data-stu-id="9844e-120">They are invoked in-process by the indexer to read and index property values, and are also invoked by Windows Explorer in-process to read and write property values directly in the files.</span></span> <span data-ttu-id="9844e-121">這些處理常式必須經過謹慎撰寫和測試，以避免效能降低或受影響檔案中的資料遺失。</span><span class="sxs-lookup"><span data-stu-id="9844e-121">These handlers need to be carefully written and tested to prevent degraded performance or the loss of data in the affected files.</span></span> <span data-ttu-id="9844e-122">如需會影響屬性處理常式執行之索引子特定考慮的詳細資訊，請參閱[開發 Windows Search 的屬性處理常式](../search/-search-3x-wds-extidx-propertyhandlers.md)。</span><span class="sxs-lookup"><span data-stu-id="9844e-122">For more information on indexer-specific considerations that affect property handler implementation, see [Developing Property Handlers for Windows Search](../search/-search-3x-wds-extidx-propertyhandlers.md).</span></span>

<span data-ttu-id="9844e-123">本主題將討論以範例 XML 為基礎的檔案格式，以描述具有配方副檔名的配方。</span><span class="sxs-lookup"><span data-stu-id="9844e-123">This topic discusses a sample XML-based file format that describes a recipe with a .recipe file name extension.</span></span> <span data-ttu-id="9844e-124">配方副檔名會註冊為它自己的相異檔案格式，而不是依賴更一般的 .xml 檔案格式，而其處理常式會使用次要資料流程來儲存屬性。</span><span class="sxs-lookup"><span data-stu-id="9844e-124">The .recipe file name extension is registered as its own distinct file format rather than relying on the more generic .xml file format, whose handler uses a secondary stream to store properties.</span></span> <span data-ttu-id="9844e-125">建議您為您的檔案類型註冊唯一的副檔名。</span><span class="sxs-lookup"><span data-stu-id="9844e-125">We recommend that you register unique file name extensions for your file types.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="9844e-126">開始之前</span><span class="sxs-lookup"><span data-stu-id="9844e-126">Before You Begin</span></span>

<span data-ttu-id="9844e-127">屬性處理常式是為特定檔案格式建立 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 抽象的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="9844e-127">Property handlers are COM objects that create the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) abstraction for a specific file format.</span></span> <span data-ttu-id="9844e-128">他們讀取 (剖析) ，並以符合其規格的方式寫入此檔案格式。</span><span class="sxs-lookup"><span data-stu-id="9844e-128">They read (parse) and write this file format in a manner that conforms to its specification.</span></span> <span data-ttu-id="9844e-129">某些屬性處理常式會根據抽象存取特定檔案格式的 Api 來執行其工作。</span><span class="sxs-lookup"><span data-stu-id="9844e-129">Some property handlers do their work based on APIs that abstract access to a specific file format.</span></span> <span data-ttu-id="9844e-130">在開發檔案格式的屬性處理常式之前，您必須先瞭解檔案格式儲存屬性的方式，以及這些屬性 (名稱和值) 如何對應至屬性存放區抽象。</span><span class="sxs-lookup"><span data-stu-id="9844e-130">Before you develop a property handler for your file format, you need to understand how your file format stores properties, and how those properties (names and values) are mapped into the property store abstraction.</span></span>

<span data-ttu-id="9844e-131">在規劃您的執行時，請記住，屬性處理常式是在進程（例如 Windows 檔案總管、Windows Search 索引子和使用 Shell 專案程式設計模型的協力廠商應用程式）內容中載入的低層級元件。</span><span class="sxs-lookup"><span data-stu-id="9844e-131">When planning your implementation, remember that property handlers are low-level components that are loaded in the context of processes like Windows Explorer, the Windows Search indexer, and third-party applications that use the Shell item programming model.</span></span> <span data-ttu-id="9844e-132">因此，屬性處理常式無法在 managed 程式碼中執行，而且應該在 c + + 中執行。</span><span class="sxs-lookup"><span data-stu-id="9844e-132">As a result, property handlers cannot be implemented in managed code, and should be implemented in C++.</span></span> <span data-ttu-id="9844e-133">如果您的處理常式使用任何 Api 或服務來執行其工作，您必須確保在載入屬性處理常式的環境 () 中，這些服務可以正常運作。</span><span class="sxs-lookup"><span data-stu-id="9844e-133">If your handler uses any APIs or services to do its work, you must ensure that those services can function properly in the environment(s) in which your property handler is loaded.</span></span>

> [!Note]  
> <span data-ttu-id="9844e-134">屬性處理常式一律會與特定檔案類型相關聯;因此，如果您的檔案格式包含需要自訂屬性處理常式的屬性，您應該一律為每個檔案格式註冊唯一的副檔名。</span><span class="sxs-lookup"><span data-stu-id="9844e-134">Property handlers are always associated with specific file types; thus, if your file format contains properties that require a custom property handler, you should always register a unique file name extension for each file format.</span></span>

 

## <a name="initializing-property-handlers"></a><span data-ttu-id="9844e-135">初始化屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="9844e-135">Initializing Property Handlers</span></span>

<span data-ttu-id="9844e-136">在系統使用屬性之前，它會藉由呼叫 [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)的執行來初始化。</span><span class="sxs-lookup"><span data-stu-id="9844e-136">Before a property is used by the system, it is initialized by calling an implementation of [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream).</span></span> <span data-ttu-id="9844e-137">屬性處理常式的初始化方式是讓系統將資料流程指派給它，而不是將該指派保留給處理常式的執行。</span><span class="sxs-lookup"><span data-stu-id="9844e-137">The property handler should be initialized by having the system assign it a stream rather than leaving that assignment to the handler implementation.</span></span> <span data-ttu-id="9844e-138">此初始化方法可確保下列事項：</span><span class="sxs-lookup"><span data-stu-id="9844e-138">This method of initialization ensures the following things:</span></span>

-   <span data-ttu-id="9844e-139">屬性處理常式可以在受限制的程式中執行 (重要的安全性功能) 沒有直接讀取或寫入檔案的存取權限，而是透過資料流程存取其內容。</span><span class="sxs-lookup"><span data-stu-id="9844e-139">The property handler can run in a restricted process (an important security feature) without having access rights to directly read or write files, rather accessing their content through the stream.</span></span>
-   <span data-ttu-id="9844e-140">系統可信任以正確地處理檔案 oplock，這是一項重要的可靠性措施。</span><span class="sxs-lookup"><span data-stu-id="9844e-140">The system can be trusted to handle the file oplocks correctly, which is an important reliability measure.</span></span>
-   <span data-ttu-id="9844e-141">屬性系統會提供自動安全儲存服務，而不需要屬性處理常式執行所需的任何額外功能。</span><span class="sxs-lookup"><span data-stu-id="9844e-141">The property system provides an automatic safe saving service without any extra functionality required from the property handler implementation.</span></span> <span data-ttu-id="9844e-142">如需資料流程的詳細資訊，請參閱 [寫回值](#writing-back-values) 一節。</span><span class="sxs-lookup"><span data-stu-id="9844e-142">See the [Writing Back Values](#writing-back-values) section for more information about streams.</span></span>
-   <span data-ttu-id="9844e-143">使用 [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) 會將您的實作為檔案系統詳細資料的摘要。</span><span class="sxs-lookup"><span data-stu-id="9844e-143">Use of the [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) abstracts your implementation from file system details.</span></span> <span data-ttu-id="9844e-144">這可讓處理常式透過替代的儲存體（例如檔案傳輸通訊協定 (FTP) 資料夾或副檔名 .zip 的壓縮檔）支援初始化。</span><span class="sxs-lookup"><span data-stu-id="9844e-144">This enables the handler to support initialization through alternative storages such as a File Transfer Protocol (FTP) folder or a compressed file with a .zip file name extension.</span></span>

<span data-ttu-id="9844e-145">在某些情況下，不可能使用資料流程進行初始化。</span><span class="sxs-lookup"><span data-stu-id="9844e-145">There are cases where initialization with streams is not possible.</span></span> <span data-ttu-id="9844e-146">在這些情況下，屬性處理常式可以執行兩個進一步的介面： [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile) 和 [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)。</span><span class="sxs-lookup"><span data-stu-id="9844e-146">In those situations, there are two further interfaces that property handlers can implement: [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile) and [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem).</span></span> <span data-ttu-id="9844e-147">如果屬性處理常式未執行 [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)，它必須選擇不在隔離的進程中執行，如果資料流程有變更，系統索引子預設會將它放在其中。</span><span class="sxs-lookup"><span data-stu-id="9844e-147">If a property handler does not implement the [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), it must opt out of running in the isolated process into which the system indexer would place it by default if there were a change to the stream.</span></span> <span data-ttu-id="9844e-148">若要退出宣告這項功能，請設定下列登錄值。</span><span class="sxs-lookup"><span data-stu-id="9844e-148">To opt out of this feature, set the following registry value.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         DisableProcessIsolation = 1
```

<span data-ttu-id="9844e-149">不過，最好是執行 [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) 並進行以資料流程為基礎的初始化。</span><span class="sxs-lookup"><span data-stu-id="9844e-149">However, it is far better to implement [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream) and do a stream-based initialization.</span></span> <span data-ttu-id="9844e-150">因此，您的屬性處理常式會更安全且更可靠。</span><span class="sxs-lookup"><span data-stu-id="9844e-150">Your property handler will be safer and more reliable as a result.</span></span> <span data-ttu-id="9844e-151">停用進程隔離通常僅適用于舊版的屬性處理常式，而任何新的程式碼都應避免 strenuously。</span><span class="sxs-lookup"><span data-stu-id="9844e-151">Disabling process isolation is generally intended only for legacy property handlers and should be strenuously avoided by any new code.</span></span>

<span data-ttu-id="9844e-152">若要詳細檢查屬性處理常式的執行，請查看下列程式碼範例，這是 [**IInitializeWithStream：： Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize)的實作為。</span><span class="sxs-lookup"><span data-stu-id="9844e-152">To examine the implementation of a property handler in detail, look at the following code example, which is an implementation of [**IInitializeWithStream::Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize).</span></span> <span data-ttu-id="9844e-153">處理常式的初始化方式是透過該檔相關聯的 [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) 實例的指標載入以 XML 為基礎的配方檔。</span><span class="sxs-lookup"><span data-stu-id="9844e-153">The handler is initialized by loading an XML-based recipe document through a pointer to that document's associated [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) instance.</span></span> <span data-ttu-id="9844e-154">接近程式碼範例結尾所使用的 **\_ spDocEle** 變數，在範例中稍早定義為 Msxml2.h：： IXMLDOMElementPtr。</span><span class="sxs-lookup"><span data-stu-id="9844e-154">The **\_spDocEle** variable used near the end of the code example is defined earlier in the sample as an MSXML2::IXMLDOMElementPtr.</span></span>

> [!Note]  
> <span data-ttu-id="9844e-155">下列和所有後續的程式碼範例取自 Windows 軟體開發套件 (SDK) 中包含的配方處理常式範例。</span><span class="sxs-lookup"><span data-stu-id="9844e-155">The following and all subsequent code examples are taken from the recipe handler sample included in the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9844e-156">.</span><span class="sxs-lookup"><span data-stu-id="9844e-156">.</span></span>

 


```
HRESULT CRecipePropertyStore::Initialize(IStream *pStream, DWORD grfMode)
{
    HRESULT hr = E_FAIL;
    
    try
    {
        if (!_spStream)
        {
            hr = _spDomDoc.CreateInstance(__uuidof(MSXML2::DOMDocument60));
            
            if (SUCCEEDED(hr))
            {
                if (VARIANT_TRUE == _spDomDoc->load(static_cast<IUnknown *>(pStream)))
                {
                    _spDocEle = _spDomDoc->documentElement;
                }
```



<span data-ttu-id="9844e-157">Â</span><span class="sxs-lookup"><span data-stu-id="9844e-157">Â</span></span> 

<span data-ttu-id="9844e-158">載入檔本身之後，Windows 檔案總管中顯示的屬性會藉由呼叫受保護的 **\_ microsoft.sqlserver.replication.replicationobject.loadproperties** 方法來載入，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="9844e-158">After the document itself is loaded, the properties to be displayed in Windows Explorer are loaded by calling the protected **\_LoadProperties** method, as illustrated in the following code example.</span></span> <span data-ttu-id="9844e-159">此程式會在下一節中詳細檢查。</span><span class="sxs-lookup"><span data-stu-id="9844e-159">This process is examined in detail in the next section.</span></span>


```
                if (_spDocEle)
                {
                    hr = _LoadProperties();
    
                    if (SUCCEEDED(hr))
                    {
                        _spStream = pStream;
                    }
                }
                else
                {
                    hr = E_FAIL;  // parse error
                }
            }
        }
        else
        {
            hr = E_UNEXPECTED;
        }
    }
    
    catch (_com_error &e)
    {
        hr = e.Error();
    }
    
    return hr;
}
```



<span data-ttu-id="9844e-160">如果資料流程是唯讀的，但 *grfMode* 參數包含 STGM \_ READWRITE 旗標，則初始化應該會失敗，並傳回 stg. \_ E \_ ACCESSDENIED。</span><span class="sxs-lookup"><span data-stu-id="9844e-160">If the stream is read-only but the *grfMode* parameter contains the STGM\_READWRITE flag, the initialization should fail and return STG\_E\_ACCESSDENIED.</span></span> <span data-ttu-id="9844e-161">如果沒有這種檢查，Windows 檔案總管會將屬性值顯示為可寫入，即使它們不是，也會導致令人困惑的終端使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="9844e-161">Without this check, Windows Explorer shows the property values as writable even though they are not, leading to a confusing end-user experience.</span></span>

<span data-ttu-id="9844e-162">屬性處理常式在其存留期內只會初始化一次。</span><span class="sxs-lookup"><span data-stu-id="9844e-162">The property handler is initialized only once in its lifetime.</span></span> <span data-ttu-id="9844e-163">如果要求第二個初始化，則處理常式應該會傳回 `HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)` 。</span><span class="sxs-lookup"><span data-stu-id="9844e-163">If a second initialization is requested, the handler should return `HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)`.</span></span>

## <a name="in-memory-property-store"></a><span data-ttu-id="9844e-164">In-Memory 屬性儲存區</span><span class="sxs-lookup"><span data-stu-id="9844e-164">In-Memory Property Store</span></span>

<span data-ttu-id="9844e-165">在查看 **\_ microsoft.sqlserver.replication.replicationobject.loadproperties** 的執行之前，您應該瞭解範例中使用的 **SYSTEM.WINDOWS.FORMS.INTEGRATION.PROPERTYMAP.ADD** 陣列，將 XML 檔中的屬性對應至屬性系統中的現有屬性（透過其 PKEY 值）。</span><span class="sxs-lookup"><span data-stu-id="9844e-165">Before looking at the implementation of **\_LoadProperties**, you should understand the **PropertyMap** array used in the sample to map properties in the XML document to existing properties in the property system through their PKEY values.</span></span>

<span data-ttu-id="9844e-166">您不應該將 XML 檔案中的每個元素和屬性公開為屬性。</span><span class="sxs-lookup"><span data-stu-id="9844e-166">You should not expose every element and attribute in the XML file as a property.</span></span> <span data-ttu-id="9844e-167">相反地，請只選取您認為對其檔組織中的使用者很有用的使用者 (在此案例中，配方) 。</span><span class="sxs-lookup"><span data-stu-id="9844e-167">Instead, select only those that you believe will be useful to end users in the organization of their documents (in this case, recipes).</span></span> <span data-ttu-id="9844e-168">當您開發屬性處理常式時，這是要牢記在心的重要概念：在組織案例中真正有用的資訊，以及屬於檔案詳細資料的資訊，都可以藉由開啟檔案本身來查看。</span><span class="sxs-lookup"><span data-stu-id="9844e-168">This is an important concept to keep in mind as you develop your property handlers: the difference between information that is truly useful for organizational scenarios, and information that belongs to the details of your file and can be seen by opening the file itself.</span></span> <span data-ttu-id="9844e-169">屬性不會是 XML 檔案的完整複製。</span><span class="sxs-lookup"><span data-stu-id="9844e-169">Properties are not intended to be a full duplication of an XML file.</span></span>


```
PropertyMap c_rgPropertyMap[] =
{
{ L"Recipe/Title", PKEY_Title, 
                   VT_LPWSTR, 
                   NULL, 
                   PKEY_Null },
{ L"Recipe/Comments", PKEY_Comment, 
                      VT_LPWSTR, 
                      NULL, 
                      PKEY_Null },
{ L"Recipe/Background", PKEY_Author, 
                        VT_VECTOR | VT_LPWSTR, 
                        L"Author", 
                        PKEY_Null },
{ L"Recipe/RecipeKeywords", PKEY_Keywords, 
                            VT_VECTOR | VT_LPWSTR, 
                            L"Keyword", 
                            PKEY_KeywordCount },
};
```



<span data-ttu-id="9844e-170">以下是 [**IInitializeWithStream：： Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize)所呼叫之 **\_ microsoft.sqlserver.replication.replicationobject.loadproperties** 方法的完整實作為。</span><span class="sxs-lookup"><span data-stu-id="9844e-170">Here is the full implementation of the **\_LoadProperties** method called by [**IInitializeWithStream::Initialize**](/windows/win32/api/propsys/nf-propsys-iinitializewithstream-initialize).</span></span>


```
HRESULT CRecipePropertyStore::_LoadProperties()
{
    HRESULT hr = E_FAIL;    
    
    if (_spCache)
    {
        hr = <mark type="const">S_OK</mark>;
    }
    else
    {
        // Create the in-memory property store.
        hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&_spCache));
    
        if (SUCCEEDED(hr))
        {
            // Cycle through each mapped property.
            for (UINT i = 0; i < ARRAYSIZE(c_rgPropertyMap); ++i)
            {
                _LoadProperty(c_rgPropertyMap[i]);
            }
    
            _LoadExtendedProperties();
            _LoadSearchContent();
        }
    }
    return hr;
}
```



<span data-ttu-id="9844e-171">**\_ Microsoft.sqlserver.replication.replicationobject.loadproperties** 方法會呼叫 Shell 協助程式函式 [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) ，為處理的屬性建立記憶體中的屬性存放區 (cache) 。</span><span class="sxs-lookup"><span data-stu-id="9844e-171">The **\_LoadProperties** method calls the Shell helper function [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) to create an in-memory property store (cache) for the handled properties.</span></span> <span data-ttu-id="9844e-172">藉由使用快取，系統會追蹤您的變更。</span><span class="sxs-lookup"><span data-stu-id="9844e-172">By using a cache, changes are tracked for you.</span></span> <span data-ttu-id="9844e-173">這可讓您無法追蹤屬性值是否已在快取中變更，但尚未儲存至保存的儲存體。</span><span class="sxs-lookup"><span data-stu-id="9844e-173">This frees you from tracking whether a property value has been changed in the cache but not yet saved to persisted storage.</span></span> <span data-ttu-id="9844e-174">它也可讓您不必要地保存未變更的屬性值。</span><span class="sxs-lookup"><span data-stu-id="9844e-174">It also frees you from needlessly persisting property values that have not changed.</span></span>

<span data-ttu-id="9844e-175">**\_ Microsoft.sqlserver.replication.replicationobject.loadproperties** 方法也會在下列程式碼中呼叫 **\_ LoadProperty** ，以針對每個對應的屬性) 一次。</span><span class="sxs-lookup"><span data-stu-id="9844e-175">The **\_LoadProperties** method also calls **\_LoadProperty** whose implementation is illustrated in the following code) once for each mapped property.</span></span> <span data-ttu-id="9844e-176">**\_ LoadProperty** 會取得 XML 資料流程中 **system.windows.forms.integration.propertymap.add** 元素所指定的屬性值，並透過呼叫 [**IPropertyStoreCache：： SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate)，將它指派給記憶體中的快取。</span><span class="sxs-lookup"><span data-stu-id="9844e-176">**\_LoadProperty** gets the value of the property as specified in the **PropertyMap** element in the XML stream and assigns it to the in-memory cache through a call to [**IPropertyStoreCache::SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate).</span></span> <span data-ttu-id="9844e-177">\_ **IPropertyStoreCache：： SetValueAndState** 呼叫中的 PSC NORMAL 旗標，表示屬性值自其進入快取以來尚未改變。</span><span class="sxs-lookup"><span data-stu-id="9844e-177">The PSC\_NORMAL flag in the call to **IPropertyStoreCache::SetValueAndState** indicates that the property value has not been altered since the time it entered the cache.</span></span>


```
HRESULT CRecipePropertyStore::_LoadProperty(PropertyMap &map)
{
    HRESULT hr = S_FALSE;
    
    MSXML2::IXMLDOMNodePtr spXmlNode(_spDomDoc->selectSingleNode(map.pszXPath));
    if (spXmlNode)
    {
        PROPVARIANT propvar = { 0 };
        propvar.vt = map.vt;
        
        if (map.vt == (VT_VECTOR | VT_LPWSTR))
        {
            hr = _LoadVectorProperty(spXmlNode, &propvar, map);
        }
        else
        {
            // If there is no value, set to VT_EMPTY to indicate
            // that it is not there. Do not return failure.
            if (spXmlNode->text.length() == 0)
            {
                propvar.vt = VT_EMPTY;
                hr = <mark type="const">S_OK</mark>;
            }
            else
            {
                // SimplePropVariantFromString is a helper function.
                // particular to the sample. It is found in Util.cpp.
                hr = SimplePropVariantFromString(spXmlNode->text, &propvar);
            }
        }
    
        if (S_OK == hr)
        {
            hr = _spCache->SetValueAndState(map.key, &propvar, PSC_NORMAL);
            PropVariantClear(&propvar);
        }
    }
    return hr;
}
```



## <a name="dealing-with-propvariant-based-values"></a><span data-ttu-id="9844e-178">處理 PROPVARIANT-Based 值</span><span class="sxs-lookup"><span data-stu-id="9844e-178">Dealing with PROPVARIANT-Based Values</span></span>

<span data-ttu-id="9844e-179">在 **\_ LoadProperty** 的執行中，會以 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)的形式提供屬性值。</span><span class="sxs-lookup"><span data-stu-id="9844e-179">In the implementation of **\_LoadProperty**, a property value is provided in the form of a [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span></span> <span data-ttu-id="9844e-180">軟體發展工具組 (SDK) 提供一組 Api，可從 **PROPVARIANT** 類型等基本類型（例如 **PWSTR** 或 **int** ）轉換。</span><span class="sxs-lookup"><span data-stu-id="9844e-180">A set of APIs in the software development kit (SDK) is provided to convert from primitive types such as **PWSTR** or **int** to or from **PROPVARIANT** types.</span></span> <span data-ttu-id="9844e-181">這些 Api 可在 Propvarutil 中找到。</span><span class="sxs-lookup"><span data-stu-id="9844e-181">These APIs are found in Propvarutil.h.</span></span>

<span data-ttu-id="9844e-182">例如，若要將 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 轉換為字串，您可以使用 [**PropVariantToString**](/windows/win32/api/propvarutil/nf-propvarutil-propvarianttostring) ，如下所示。</span><span class="sxs-lookup"><span data-stu-id="9844e-182">For example, to convert a [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) to a string, you can use [**PropVariantToString**](/windows/win32/api/propvarutil/nf-propvarutil-propvarianttostring) as illustrated here.</span></span>


```
PropVariantToString(REFPROPVARIANT propvar, PWSTR psz, UINT cch);
```



<span data-ttu-id="9844e-183">若要從字串初始化 PROPVARIANT，您可以使用 [**InitPropVariantFromString**](/windows/win32/api/propvarutil/nf-propvarutil-initpropvariantfromstring)。</span><span class="sxs-lookup"><span data-stu-id="9844e-183">To initialize a PROPVARIANT from a string, you can use [**InitPropVariantFromString**](/windows/win32/api/propvarutil/nf-propvarutil-initpropvariantfromstring).</span></span>


```
InitPropVariantFromString(PCWSTR psz, PROPVARIANT *ppropvar);
```



<span data-ttu-id="9844e-184">您可以在範例中所包含的任何配方檔案中看到，每個檔案中都可以有一個以上的關鍵字。</span><span class="sxs-lookup"><span data-stu-id="9844e-184">As you can see in any of the recipe files included in the sample, there can be more than one keyword in each file.</span></span> <span data-ttu-id="9844e-185">為了因應此情況，屬性系統支援以字串向量表示的多重值字串， (例如 "VT \_ vector \| VT \_ LPWSTR" ) 。</span><span class="sxs-lookup"><span data-stu-id="9844e-185">To account for this, the property system supports multi-valued strings represented as a vector of strings (for instance "VT\_VECTOR \| VT\_LPWSTR").</span></span> <span data-ttu-id="9844e-186">範例中的 **\_ LoadVectorProperty** 方法會使用以向量為基礎的值。</span><span class="sxs-lookup"><span data-stu-id="9844e-186">The **\_LoadVectorProperty** method in the example uses vector-based values.</span></span>


```
HRESULT CRecipePropertyStore::_LoadVectorProperty
                                (MSXML2::IXMLDOMNode *pNodeParent,
                                 PROPVARIANT *ppropvar,
                                 struct PropertyMap &map)
{
    HRESULT hr = S_FALSE;
    MSXML2::IXMLDOMNodeListPtr spList = pNodeParent->selectNodes(map.pszSubNodeName);
    
    if (spList)
    {
        UINT cElems = spList->length;
        ppropvar->calpwstr.cElems = cElems;
        ppropvar->calpwstr.pElems = (PWSTR*)CoTaskMemAlloc(sizeof(PWSTR)*cElems);
    
        if (ppropvar->calpwstr.pElems)
        {
            for (UINT i = 0; (SUCCEEDED(hr) && i < cElems); ++i)
            {
                hr = SHStrDup(spList->item[i]->text, 
                              &(ppropvar->calpwstr.pElems[i]));
            }
    
            if (SUCCEEDED(hr))
            {
                if (!IsEqualPropertyKey(map.keyCount, PKEY_Null))
                {
                    PROPVARIANT propvarCount = { VT_UI4 };
                    propvarCount.uintVal = cElems;
                    
                    _spCache->SetValueAndState(map.keyCount,
                                               &propvarCount, 
                                               PSC_NORMAL);
                }
            }
            else
            {
                PropVariantClear(ppropvar);
            }
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }
    }
    
    return hr;
}
```



<span data-ttu-id="9844e-187">如果值不存在於檔案中，則不會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="9844e-187">If a value does not exist in the file, do not return an error.</span></span> <span data-ttu-id="9844e-188">相反地，請將值設定為 VT \_ 空白，並傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="9844e-188">Instead, set the value to VT\_EMPTY and return **S\_OK**.</span></span> <span data-ttu-id="9844e-189">VT \_ 空白表示屬性值不存在。</span><span class="sxs-lookup"><span data-stu-id="9844e-189">VT\_EMPTY indicates that the property value does not exist.</span></span>

## <a name="supporting-open-metadata"></a><span data-ttu-id="9844e-190">支援開放中繼資料</span><span class="sxs-lookup"><span data-stu-id="9844e-190">Supporting Open Metadata</span></span>

<span data-ttu-id="9844e-191">這個範例會使用以 XML 為基礎的檔案格式。</span><span class="sxs-lookup"><span data-stu-id="9844e-191">This example uses an XML-based file format.</span></span> <span data-ttu-id="9844e-192">例如，您可以擴充其架構，以支援在 developmet 期間不會考慮的屬性。</span><span class="sxs-lookup"><span data-stu-id="9844e-192">Its schema can be extended to support properties that were not thought of during developmet, for example.</span></span> <span data-ttu-id="9844e-193">這個系統稱為「開放中繼資料」。</span><span class="sxs-lookup"><span data-stu-id="9844e-193">This system is known as open metadata.</span></span> <span data-ttu-id="9844e-194">此範例會在名為 **ExtendedProperties** 的 **配方** 元素底下建立節點，以擴充屬性系統，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="9844e-194">This example extends the property system by creating a node under the **Recipe** element called **ExtendedProperties**, as illustrated in the following code example.</span></span>


```
<ExtendedProperties>
    <Property 
        Name="{65A98875-3C80-40AB-ABBC-EFDAF77DBEE2}, 100"
        EncodedValue="HJKHJDHKJHK"/>
</ExtendedProperties>
```



<span data-ttu-id="9844e-195">若要在初始化期間載入保存的擴充屬性，請執行 **\_ LoadExtendedProperties** 方法，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="9844e-195">To load persisted extended properties during initialization, implement the **\_LoadExtendedProperties** method, as illustrated in the following code example.</span></span>


```
HRESULT CRecipePropertyStore::_LoadExtendedProperties()
{
    HRESULT hr = S_FALSE;
    MSXML2::IXMLDOMNodeListPtr spList = 
                  _spDomDoc->selectNodes(L"Recipe/ExtendedProperties/Property");
    
    if (spList)
    {
        UINT cElems = spList->length;
        
        for (UINT i = 0; i < cElems; ++i)
        {
            MSXML2::IXMLDOMElementPtr spElement;
            
            if (SUCCEEDED(spList->item[i]->QueryInterface(IID_PPV_ARGS(&spElement))))
            {
                PROPERTYKEY key;
                _bstr_t bstrPropName = spElement->getAttribute(L"Name").bstrVal;
    
                if (!!bstrPropName &&
                    (SUCCEEDED(PropertyKeyFromString(bstrPropName, &key))))
                {
                    PROPVARIANT propvar = { 0 };
                    _bstr_t bstrEncodedValue = 
                               spElement->getAttribute(L"EncodedValue").bstrVal;
                   
                    if (!!bstrEncodedValue)
                    {
                        // DeserializePropVariantFromString is a helper function
                        // particular to the sample. It is found in Util.cpp.
                        hr = DeserializePropVariantFromString(bstrEncodedValue, 
                                                              &propvar);
                    }
```



<span data-ttu-id="9844e-196">在 Propsys 中宣告的序列化 Api 會用來將 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 類型序列化和還原序列化成資料的 blob，然後使用 Base64 編碼將這些 blob 序列化成可儲存在 XML 中的字串。</span><span class="sxs-lookup"><span data-stu-id="9844e-196">Serialization APIs declared in Propsys.h are used to serialize and deserialize [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) types into blobs of data, and then Base64 encoding is used to serialize those blobs into strings that can be saved in the XML.</span></span> <span data-ttu-id="9844e-197">這些字串會儲存在 **ExtendedProperties** 元素的 **url-encodedvalue** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="9844e-197">These strings are stored in the **EncodedValue** attribute of the **ExtendedProperties** element.</span></span> <span data-ttu-id="9844e-198">下列公用程式方法（在範例的 Util .cpp 檔案中執行）會執行序列化。</span><span class="sxs-lookup"><span data-stu-id="9844e-198">The following utility method, implemented in the sample's Util.cpp file, performs the serialization.</span></span> <span data-ttu-id="9844e-199">首先，呼叫 [**StgSerializePropVariant**](/windows/win32/api/propvarutil/nf-propvarutil-stgserializepropvariant) 函數來執行二進位序列化，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="9844e-199">It begins with a call to the [**StgSerializePropVariant**](/windows/win32/api/propvarutil/nf-propvarutil-stgserializepropvariant) function to perform the binary serialization, as illustrated in the following code example.</span></span>


```
HRESULT SerializePropVariantAsString(const PROPVARIANT *ppropvar, PWSTR *pszOut)
{
    SERIALIZEDPROPERTYVALUE *pBlob;
    ULONG cbBlob;
    HRESULT hr = StgSerializePropVariant(ppropvar, &pBlob, &cbBlob);
```



<span data-ttu-id="9844e-200">接著， [**CryptBinaryToString**](/windows/win32/api/wincrypt/nf-wincrypt-cryptbinarytostringa)函數（在 Wincrypt 中宣告）會執行 Base64 轉換。</span><span class="sxs-lookup"><span data-stu-id="9844e-200">Next, the [**CryptBinaryToString**](/windows/win32/api/wincrypt/nf-wincrypt-cryptbinarytostringa)Â function, declared in Wincrypt.h, performs the Base64 conversion.</span></span>


```
    if (SUCCEEDED(hr))
    {
        hr = E_FAIL;
        DWORD cchString;
        
        if (CryptBinaryToString((BYTE *)pBlob, 
                                cbBlob,
                                CRYPT_STRING_BASE64, 
                                NULL, 
                                &cchString))
        {
            *pszOut = (PWSTR)CoTaskMemAlloc(sizeof(WCHAR) *cchString);
    
            if (*pszOut)
            {
                if (CryptBinaryToString((BYTE *)pBlob, 
                                         cbBlob,
                                         CRYPT_STRING_BASE64,
                                         *pszOut, 
                                         &cchString))
                {
                    hr = <mark type="const">S_OK</mark>;
                }
                else
                {
                    CoTaskMemFree(*pszOut);
                }
            }
            else
            {
                hr = E_OUTOFMEMORY;
            }
        }
    }
    
    return <mark type="const">S_OK</mark>;}
```



<span data-ttu-id="9844e-201">**DeserializePropVariantFromString** 函式（也可以在 Util 中找到）會反轉作業，並將 XML 檔案中的值還原序列化。</span><span class="sxs-lookup"><span data-stu-id="9844e-201">The **DeserializePropVariantFromString** function, also found in Util.cpp, reverses the operation, deserializing values from the XML file.</span></span>

<span data-ttu-id="9844e-202">如需開啟中繼資料支援的相關資訊，請參閱 [檔案類型](../shell/fa-file-types.md)中的「支援開放中繼資料的檔案類型」。</span><span class="sxs-lookup"><span data-stu-id="9844e-202">For information about support for open metadata, see "File Types that Support Open Metadata" in [File Types](../shell/fa-file-types.md).</span></span>

## <a name="full-text-contents"></a><span data-ttu-id="9844e-203">Full-Text 內容</span><span class="sxs-lookup"><span data-stu-id="9844e-203">Full-Text Contents</span></span>

<span data-ttu-id="9844e-204">屬性處理常式也有助於全文檢索搜尋檔案內容，而且如果檔案格式不太複雜，則可以輕鬆地提供該功能。</span><span class="sxs-lookup"><span data-stu-id="9844e-204">Property handlers can also facilitate a full-text search of the file contents, and they are an easy way to provide that functionality if the file format is not overly complicated.</span></span> <span data-ttu-id="9844e-205">另外還有一個更強大的方法，可透過 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面實行提供檔案的完整文字。</span><span class="sxs-lookup"><span data-stu-id="9844e-205">There is an alternative, more powerful way to provide the full text of the file through the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface implementation.</span></span>

<span data-ttu-id="9844e-206">下表摘要說明使用 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 或 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)的每種方法各有何好處。</span><span class="sxs-lookup"><span data-stu-id="9844e-206">The following table summarizes the benefits of each approach using either [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) or [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>



| <span data-ttu-id="9844e-207">功能</span><span class="sxs-lookup"><span data-stu-id="9844e-207">Capability</span></span>                                   | <span data-ttu-id="9844e-208">IFilter</span><span class="sxs-lookup"><span data-stu-id="9844e-208">IFilter</span></span>                      | <span data-ttu-id="9844e-209">IPropertyStore</span><span class="sxs-lookup"><span data-stu-id="9844e-209">IPropertyStore</span></span> |
|----------------------------------------------|------------------------------|----------------|
| <span data-ttu-id="9844e-210">允許寫回檔案嗎？</span><span class="sxs-lookup"><span data-stu-id="9844e-210">Allows write back to files?</span></span>                  | <span data-ttu-id="9844e-211">否</span><span class="sxs-lookup"><span data-stu-id="9844e-211">No</span></span>                           | <span data-ttu-id="9844e-212">是</span><span class="sxs-lookup"><span data-stu-id="9844e-212">Yes</span></span>            |
| <span data-ttu-id="9844e-213">提供內容和屬性的混合？</span><span class="sxs-lookup"><span data-stu-id="9844e-213">Provides mix of content and properties?</span></span>      | <span data-ttu-id="9844e-214">是</span><span class="sxs-lookup"><span data-stu-id="9844e-214">Yes</span></span>                          | <span data-ttu-id="9844e-215">是</span><span class="sxs-lookup"><span data-stu-id="9844e-215">Yes</span></span>            |
| <span data-ttu-id="9844e-216">多 語種？</span><span class="sxs-lookup"><span data-stu-id="9844e-216">Multilingual?</span></span>                                | <span data-ttu-id="9844e-217">是</span><span class="sxs-lookup"><span data-stu-id="9844e-217">Yes</span></span>                          | <span data-ttu-id="9844e-218">否</span><span class="sxs-lookup"><span data-stu-id="9844e-218">No</span></span>             |
| <span data-ttu-id="9844e-219">MIME/內嵌？</span><span class="sxs-lookup"><span data-stu-id="9844e-219">MIME/Embedded?</span></span>                               | <span data-ttu-id="9844e-220">是</span><span class="sxs-lookup"><span data-stu-id="9844e-220">Yes</span></span>                          | <span data-ttu-id="9844e-221">否</span><span class="sxs-lookup"><span data-stu-id="9844e-221">No</span></span>             |
| <span data-ttu-id="9844e-222">文字界限？</span><span class="sxs-lookup"><span data-stu-id="9844e-222">Text boundaries?</span></span>                             | <span data-ttu-id="9844e-223">句子、段落、章節</span><span class="sxs-lookup"><span data-stu-id="9844e-223">Sentence, paragraph, chapter</span></span> | <span data-ttu-id="9844e-224">無</span><span class="sxs-lookup"><span data-stu-id="9844e-224">None</span></span>           |
| <span data-ttu-id="9844e-225">適用于 SPS/SQL Server 的實作為支援？</span><span class="sxs-lookup"><span data-stu-id="9844e-225">Implementation supported for SPS/SQL Server?</span></span> | <span data-ttu-id="9844e-226">是</span><span class="sxs-lookup"><span data-stu-id="9844e-226">Yes</span></span>                          | <span data-ttu-id="9844e-227">否</span><span class="sxs-lookup"><span data-stu-id="9844e-227">No</span></span>             |
| <span data-ttu-id="9844e-228">實作</span><span class="sxs-lookup"><span data-stu-id="9844e-228">Implementation</span></span>                               | <span data-ttu-id="9844e-229">Complex</span><span class="sxs-lookup"><span data-stu-id="9844e-229">Complex</span></span>                      | <span data-ttu-id="9844e-230">簡單</span><span class="sxs-lookup"><span data-stu-id="9844e-230">Simple</span></span>         |



 

<span data-ttu-id="9844e-231">在配方處理常式範例中，配方檔案格式沒有任何複雜的需求，因此只會針對全文檢索支援執行 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 。</span><span class="sxs-lookup"><span data-stu-id="9844e-231">In the recipe handler sample, the recipe file format does not have any complex requirements, so only [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) has been implemented for full-text support.</span></span> <span data-ttu-id="9844e-232">全文檢索搜尋是針對下列陣列中名為的 XML 節點所執行。</span><span class="sxs-lookup"><span data-stu-id="9844e-232">Full-text search is implemented for the XML nodes named in the following array.</span></span>


```
const PWSTR c_rgszContentXPath[] = {
    L"Recipe/Ingredients/Item",
    L"Recipe/Directions/Step",
    L"Recipe/RecipeInfo/Yield",
    L"Recipe/RecipeKeywords/Keyword",
};
```



<span data-ttu-id="9844e-233">屬性系統包含 `System.Search.Contents` (PKEY \_ 搜尋 \_ 內容) 屬性，此屬性是建立來提供全文檢索內容給索引子。</span><span class="sxs-lookup"><span data-stu-id="9844e-233">The property system contains the `System.Search.Contents` (PKEY\_Search\_Contents) property, which was created to provide full-text content to the indexer.</span></span> <span data-ttu-id="9844e-234">這個屬性的值永遠不會直接顯示在 UI 中;上述陣列中所命名之所有 XML 節點的文字都會串連成單一字串。</span><span class="sxs-lookup"><span data-stu-id="9844e-234">This property's value is never displayed directly in the UI; the text from all of the XML nodes named in the array above are concatenated into a single string.</span></span> <span data-ttu-id="9844e-235">然後透過呼叫 [**IPropertyStoreCache：： SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate) ，將該字串提供給索引子，作為配方檔案的全文檢索內容，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="9844e-235">That string is then provided to the indexer as the full-text content of the recipe file through a call to [**IPropertyStoreCache::SetValueAndState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-setvalueandstate) as illustrated in the following code example.</span></span>


```
HRESULT CRecipePropertyStore::_LoadSearchContent()
{
    HRESULT hr = S_FALSE;
    _bstr_t bstrContent;
    
    for (UINT i = 0; i < ARRAYSIZE(c_rgszContentXPath); ++i)
    {
        MSXML2::IXMLDOMNodeListPtr spList = 
                                  _spDomDoc->selectNodes(c_rgszContentXPath[i]);
    
        if (spList)
        {
            UINT cElems = spList->length;
            
            for (UINT elt = 0; elt < cElems; ++elt)
            {
                bstrContent += L" ";
                bstrContent += spList->item[elt]->text;
            }
        }
    }
    
    if (bstrContent.length() > 0)
    {
        PROPVARIANT propvar = { VT_LPWSTR };
        hr = SHStrDup(bstrContent, &(propvar.pwszVal));
    
        if (SUCCEEDED(hr))
        {
            hr = _spCache->SetValueAndState(PKEY_Search_Contents, 
                                            &propvar, 
                                            PSC_NORMAL);
            PropVariantClear(&propvar);
        }
    }
    
    return hr;}
```



## <a name="providing-values-for-properties"></a><span data-ttu-id="9844e-236">提供屬性的值</span><span class="sxs-lookup"><span data-stu-id="9844e-236">Providing Values for Properties</span></span>

<span data-ttu-id="9844e-237">當用來讀取值時，通常會因為下列其中一個原因而叫用屬性處理常式：</span><span class="sxs-lookup"><span data-stu-id="9844e-237">When used to read values, property handlers are usually invoked for one of the following reasons:</span></span>

-   <span data-ttu-id="9844e-238">以列舉所有屬性值。</span><span class="sxs-lookup"><span data-stu-id="9844e-238">To enumerate all property values.</span></span>
-   <span data-ttu-id="9844e-239">取得特定屬性的值。</span><span class="sxs-lookup"><span data-stu-id="9844e-239">To get the value of a specific property.</span></span>

<span data-ttu-id="9844e-240">若為列舉，則會要求屬性處理常式在編制索引期間或在屬性對話方塊要求屬性顯示于 **另** 一個群組時，列舉其屬性。</span><span class="sxs-lookup"><span data-stu-id="9844e-240">For enumeration, a property handler is asked to enumerate its properties either during indexing or when the properties dialog box asks for properties to display in the **Other** group.</span></span> <span data-ttu-id="9844e-241">編制索引會持續以背景作業的方式來運作。</span><span class="sxs-lookup"><span data-stu-id="9844e-241">Indexing goes on constantly as a background operation.</span></span> <span data-ttu-id="9844e-242">每當檔案變更時，索引子就會收到通知，並藉由要求屬性處理常式來列舉其屬性來重新建立檔案的索引。</span><span class="sxs-lookup"><span data-stu-id="9844e-242">Whenever a file changes, the indexer is notified, and it re-indexes the file by asking the property handler to enumerate its properties.</span></span> <span data-ttu-id="9844e-243">因此，請務必有效率地執行屬性處理常式，並儘快傳回屬性值。</span><span class="sxs-lookup"><span data-stu-id="9844e-243">Therefore, it is critical that property handlers are implemented efficiently and return property values as quickly as possible.</span></span> <span data-ttu-id="9844e-244">列舉所有具有值的屬性，就像您對任何集合所做的一樣，但不會列舉牽涉到記憶體密集計算的屬性，或是可能使抓取速度變慢的網路要求。</span><span class="sxs-lookup"><span data-stu-id="9844e-244">Enumerate all the properties for which you have values, just as you would for any collection, but do not enumerate properties that involve memory-intensive calculations or network requests that could make them slow to retrieve.</span></span>

<span data-ttu-id="9844e-245">撰寫屬性處理常式時，您通常需要考慮下列兩組屬性。</span><span class="sxs-lookup"><span data-stu-id="9844e-245">When writing a property handler, you usually need to consider the following two sets of properties.</span></span>

-   <span data-ttu-id="9844e-246">主要屬性：您的檔案類型原本就支援的屬性。</span><span class="sxs-lookup"><span data-stu-id="9844e-246">Primary properties: Properties that your file type supports natively.</span></span> <span data-ttu-id="9844e-247">例如，交換影像檔案 (EXIF) 中繼資料的相片屬性處理常式原本就支援 `System.Photo.FNumber` 。</span><span class="sxs-lookup"><span data-stu-id="9844e-247">For example, a photo property handler for Exchangeable Image File (EXIF) metadata natively supports `System.Photo.FNumber`.</span></span>
-   <span data-ttu-id="9844e-248">擴充屬性：您的檔案類型支援作為開啟中繼資料一部分的屬性。</span><span class="sxs-lookup"><span data-stu-id="9844e-248">Extended properties: Properties that your file type supports as part of open metadata.</span></span>

<span data-ttu-id="9844e-249">由於範例會使用記憶體內部快取，因此執行 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 方法只是委派給該快取，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="9844e-249">Because the sample uses in-memory cache, implementing [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) methods is just a matter of delegating to that cache, as illustrated in the following code example.</span></span>


```
IFACEMETHODIMP GetCount(__out DWORD *pcProps)
{ return _spCache->GetCount(pcProps); }

IFACEMETHODIMP GetAt(DWORD iProp, __out PROPERTYKEY *pkey)
{ return _spCache->GetAt(iProp, pkey); }

IFACEMETHODIMP GetValue(REFPROPERTYKEY key, __out PROPVARIANT *pPropVar)
{ return _spCache->GetValue(key, pPropVar); }
```



<span data-ttu-id="9844e-250">如果您選擇不要委派至記憶體中的快取，您必須執行您的方法，以提供下列預期的行為>：</span><span class="sxs-lookup"><span data-stu-id="9844e-250">If you choose not to delegate to the in-memory cache, you must implement your methods to provide> the following expected behavior:</span></span>

-   <span data-ttu-id="9844e-251">[**IPropertyStore：： GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85))：如果沒有屬性，此方法會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="9844e-251">[**IPropertyStore::GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)): If there are no properties, this method returns **S\_OK**.</span></span>
-   <span data-ttu-id="9844e-252">[**IPropertyStore：： GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85))：如果 *iProp* 大於或等於 *cProps*，這個方法會傳回 E \_ INVALIDARG，而 *pkey* 參數所指向的結構會填入零。</span><span class="sxs-lookup"><span data-stu-id="9844e-252">[**IPropertyStore::GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)): If *iProp* is greater than or equal to *cProps*, this method returns E\_INVALIDARG and the structure pointed to by the *pkey* parameter is filled with zeroes.</span></span>
-   <span data-ttu-id="9844e-253">[**IPropertyStore：： GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) 和 [**IPropertyStore：： GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) 會反映屬性處理常式的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="9844e-253">[**IPropertyStore::GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) and [**IPropertyStore::GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) reflect the current state of the property handler.</span></span> <span data-ttu-id="9844e-254">如果透過 [**IPropertyStore：： SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85))將 [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey)新增至檔案或從中移除，這兩個方法必須反映下次呼叫它們時的變更。</span><span class="sxs-lookup"><span data-stu-id="9844e-254">If a [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) is added to or removed from the file through [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)), these two methods must reflect that change the next time they are called.</span></span>
-   <span data-ttu-id="9844e-255">[**IPropertyStore：： GetValue**](/previous-versions/windows/desktop/legacy/bb761473(v=vs.85))：如果要求此方法提供不存在的值，則會傳回 **S \_ OK** ，並將值回報為 VT \_ 空白。</span><span class="sxs-lookup"><span data-stu-id="9844e-255">[**IPropertyStore::GetValue**](/previous-versions/windows/desktop/legacy/bb761473(v=vs.85)): If this method is asked for a value that does not exist, it returns **S\_OK** with the value reported as VT\_EMPTY.</span></span>

## <a name="writing-back-values"></a><span data-ttu-id="9844e-256">回寫值</span><span class="sxs-lookup"><span data-stu-id="9844e-256">Writing Back Values</span></span>

<span data-ttu-id="9844e-257">當屬性處理常式使用 [**IPropertyStore：： SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85))寫入屬性的值時，它不會將值寫入至檔案，直到呼叫 [**IPropertyStore：： Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) 為止。</span><span class="sxs-lookup"><span data-stu-id="9844e-257">When the property handler writes the value of a property using [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)), it does not write the value to the file until [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) is called.</span></span> <span data-ttu-id="9844e-258">記憶體內部快取在執行此配置時相當有用。</span><span class="sxs-lookup"><span data-stu-id="9844e-258">The in-memory cache can be useful in implementing this scheme.</span></span> <span data-ttu-id="9844e-259">在範例程式碼中， **IPropertyStore：： SetValue** 執行只會在記憶體內部快取中設定新的值，並將該屬性的狀態設定為 [PSC 已變更] \_ 。</span><span class="sxs-lookup"><span data-stu-id="9844e-259">In the sample code the **IPropertyStore::SetValue** implementation simply sets the new value in the in-memory cache and sets the state of that property to PSC\_DIRTY.</span></span>


```
HRESULT CRecipePropertyStore::SetValue(REFPROPERTYKEY key, const PROPVARIANT *pPropVar)
    {
    
    HRESULT hr = E_FAIL;
    
    if (IsEqualPropertyKey(key, PKEY_Search_Contents))
    {
        // This property is read-only
        hr = HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED);  
    }
    else
    {
        hr = _spCache->SetValueAndState(key, pPropVar, PSC_DIRTY);
    }
    
    return hr;
}
```



<span data-ttu-id="9844e-260">在任何 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 的執行中， [**IPropertyStore：： SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85))預期會有下列行為：</span><span class="sxs-lookup"><span data-stu-id="9844e-260">In any [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) implementation, the following behavior is expected from [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)):</span></span>

-   <span data-ttu-id="9844e-261">如果屬性已經存在，則會設定屬性的值。</span><span class="sxs-lookup"><span data-stu-id="9844e-261">If the property already exists, the value of the property is set.</span></span>
-   <span data-ttu-id="9844e-262">如果屬性不存在，就會加入新的屬性並設定其值。</span><span class="sxs-lookup"><span data-stu-id="9844e-262">If the property does not exist, the new property is added and its value set.</span></span>
-   <span data-ttu-id="9844e-263">如果屬性值不能以與指定 (相同的精確度來保存，就會因為檔案格式) 的大小限制而截斷，所以會將值設定為最遠，而且 \_ \_ 會傳回截斷的。</span><span class="sxs-lookup"><span data-stu-id="9844e-263">If the property value cannot be persisted at the same accuracy as given (for instance, truncation due to size limitations in the file format), the value is set as far as possible and INPLACE\_S\_TRUNCATED is returned.</span></span>
-   <span data-ttu-id="9844e-264">如果屬性處理常式不支援屬性， `HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)` 則會傳回。</span><span class="sxs-lookup"><span data-stu-id="9844e-264">If the property is not supported by the property handler, `HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)` is returned.</span></span>
-   <span data-ttu-id="9844e-265">如果有另一個原因是無法設定屬性值（例如，透過存取控制清單鎖定的檔案或缺少許可權） (Acl) ，則 \_ \_ 會傳回 Stg. E ACCESSDENIED。</span><span class="sxs-lookup"><span data-stu-id="9844e-265">If there is another reason that the property value cannot be set, such as the file being locked or lack of rights to edit through access control lists (ACLs), then STG\_E\_ACCESSDENIED is returned.</span></span>

<span data-ttu-id="9844e-266">使用資料流程作為範例的其中一個主要優點是可靠性。</span><span class="sxs-lookup"><span data-stu-id="9844e-266">One major advantage of using streams, as the sample, is reliability.</span></span> <span data-ttu-id="9844e-267">屬性處理常式必須一律考慮在發生重大失敗時，不會讓檔案處於不一致的狀態。</span><span class="sxs-lookup"><span data-stu-id="9844e-267">Property handlers must always consider that they cannot leave a file in an inconsistent state in the case of a catastrophic failure.</span></span> <span data-ttu-id="9844e-268">顯然應避免使用者的檔案損毀，最好的方法是使用「寫入時複製」機制。</span><span class="sxs-lookup"><span data-stu-id="9844e-268">Corrupting a user's files obviously should be avoided, and the best way to do this is with a "copy-on-write" mechanism.</span></span> <span data-ttu-id="9844e-269">如果您的屬性處理常式使用資料流程來存取檔案，則會自動取得此行為;系統會將任何變更寫入資料流程，只有在認可作業期間以新的複本取代檔案。</span><span class="sxs-lookup"><span data-stu-id="9844e-269">If your property handler uses a stream to access a file, you get this behavior automatically; the system writes any changes to the stream, replacing the file with the new copy only during the commit operation.</span></span>

<span data-ttu-id="9844e-270">若要覆寫這個行為並手動控制檔案儲存程式，您可以在處理常式的登錄專案中設定 ManualSafeSave 值，以退出宣告安全儲存行為，如下所示。</span><span class="sxs-lookup"><span data-stu-id="9844e-270">To override this behavior and control the file saving process manually, you can opt out of the safe save behavior by setting the ManualSafeSave value in your handler's registry entry as illustrated here.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {66742402-F9B9-11D1-A202-0000F81FEDEE}
         ManualSafeSave = 1
```

<span data-ttu-id="9844e-271">當處理常式指定 ManualSafeSave 值時，用來初始化它的資料流程不是交易式資料流程， (STGM \_ 交易) 。</span><span class="sxs-lookup"><span data-stu-id="9844e-271">When a handler specifies the ManualSafeSave value, the stream with which it is initialized is not a transacted stream (STGM\_TRANSACTED).</span></span> <span data-ttu-id="9844e-272">處理常式本身必須執行安全儲存函式，以確保在儲存作業中斷時檔案不會損毀。</span><span class="sxs-lookup"><span data-stu-id="9844e-272">The handler itself must implement the safe save function to ensure that the file is not corrupted if the save operation is interrupted.</span></span> <span data-ttu-id="9844e-273">如果處理常式會就地進行寫入，則會寫入至提供的資料流程。</span><span class="sxs-lookup"><span data-stu-id="9844e-273">If the handler implements in-place writing, it will write to the stream that it is given.</span></span> <span data-ttu-id="9844e-274">如果處理常式不支援這項功能，則必須使用 [**IDestinationStreamFactory：： GetDestinationStream**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream)來取出用來寫入檔案更新複本的資料流程。</span><span class="sxs-lookup"><span data-stu-id="9844e-274">If the handler does not support this feature, then it must retrieve a stream with which to write the updated copy of the file using [**IDestinationStreamFactory::GetDestinationStream**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idestinationstreamfactory-getdestinationstream).</span></span> <span data-ttu-id="9844e-275">完成寫入處理常式之後，它應該在原始資料流程上呼叫 [**IPropertyStore：： Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) 來完成作業，並將原始資料流程的內容取代為檔案的新複本。</span><span class="sxs-lookup"><span data-stu-id="9844e-275">After the handler is done writing, it should call [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)) on the original stream to complete the operation, and replace the contents of the original stream with the new copy of the file.</span></span>

<span data-ttu-id="9844e-276">如果您未使用資料流程初始化處理常式，ManualSafeSave 也是預設情況。</span><span class="sxs-lookup"><span data-stu-id="9844e-276">ManualSafeSave is also the default situation if you do not initialize your handler with a stream.</span></span> <span data-ttu-id="9844e-277">若沒有原始資料流程可接收暫存資料流程的內容，您必須使用 [**ReplaceFile**](/windows/win32/api/winbase/nf-winbase-replacefilea) 來執行原始程式檔的不可部分完成取代。</span><span class="sxs-lookup"><span data-stu-id="9844e-277">Without an original stream to receive the contents of the temporary stream, you must use [**ReplaceFile**](/windows/win32/api/winbase/nf-winbase-replacefilea) to perform an atomic replacement of the source file.</span></span>

<span data-ttu-id="9844e-278">會以產生大於 1 MB 之檔案的方式使用的大型檔案格式應可支援就地寫入屬性的支援;否則，效能行為不符合屬性系統用戶端的期望。</span><span class="sxs-lookup"><span data-stu-id="9844e-278">Large file formats that will be used in a way that produces files greater than 1 MB should implement support for in-place property writing; otherwise, the performance behavior does not meet the expectations of clients of the property system.</span></span> <span data-ttu-id="9844e-279">在此案例中，寫入屬性所需的時間應該不會受到檔案大小的影響。</span><span class="sxs-lookup"><span data-stu-id="9844e-279">In this scenario, the time required to write properties should not be affected by the file size.</span></span>

<span data-ttu-id="9844e-280">針對非常大型的檔案，例如 1 GB 或更多的影片檔案，則需要不同的解決方案。</span><span class="sxs-lookup"><span data-stu-id="9844e-280">For very large files, for example a video file of 1 GB or more, a different solution is required.</span></span> <span data-ttu-id="9844e-281">如果檔案中沒有足夠的空間可進行就地寫入，則如果保留給就地屬性寫入的空間量已用盡，則處理常式可能會失敗屬性更新。</span><span class="sxs-lookup"><span data-stu-id="9844e-281">If there is not enough space in the file to perform in-place writing, the handler may fail the property update if the amount of space reserved for in-place property writing has been exhausted.</span></span> <span data-ttu-id="9844e-282">發生此錯誤的原因是為了避免因 2 GB IO (1 而產生效能不佳的效能，1寫入) 。</span><span class="sxs-lookup"><span data-stu-id="9844e-282">This failure occurs to avoid poor performance arising from 2 GB of IO (1 to read, 1 to write).</span></span> <span data-ttu-id="9844e-283">因為這可能會造成失敗，所以這些檔案格式應保留足夠的空間供就地屬性寫入之用。</span><span class="sxs-lookup"><span data-stu-id="9844e-283">Because of this potential failure, these file formats should reserve enough space for in-place property writing.</span></span>

<span data-ttu-id="9844e-284">如果檔案的標頭中有足夠的空間來寫入中繼資料，而且寫入該中繼資料並不會導致檔案成長或壓縮，則可以安全地就地寫入。</span><span class="sxs-lookup"><span data-stu-id="9844e-284">If the file has enough space in its header to write metadata, and if the writing of that metadata does not cause the file to grow or shrink, it might be safe to write in-place.</span></span> <span data-ttu-id="9844e-285">建議您將 64 KB 作為起點。</span><span class="sxs-lookup"><span data-stu-id="9844e-285">We recommend 64 KB as a starting point.</span></span> <span data-ttu-id="9844e-286">就地寫入相當於要求在 [**IPropertyStore：： commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85))的實 ManualSafeSave 和呼叫 [**IStream：：**](/windows/win32/api/objidl/nf-objidl-istream-commit) commit 的處理常式，而且效能比寫入時複製的效能更佳。</span><span class="sxs-lookup"><span data-stu-id="9844e-286">Writing in-place is equivalent to the handler asking for ManualSafeSave and calling [**IStream::Commit**](/windows/win32/api/objidl/nf-objidl-istream-commit) in the implementation of [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)), and has much better performance than copy-on-write.</span></span> <span data-ttu-id="9844e-287">如果檔案大小因為屬性值變更而變更，則不應嘗試就地寫入，因為發生異常終止時可能會損毀檔案。</span><span class="sxs-lookup"><span data-stu-id="9844e-287">If the file size changes due to property value changes, writing in-place should not be attempted because of the potential for a corrupted file in the event of an abnormal termination.</span></span>

> [!Note]  
> <span data-ttu-id="9844e-288">基於效能考慮，我們建議使用 ManualSafeSave 選項搭配使用 100 KB 或更大檔案的屬性處理常式。</span><span class="sxs-lookup"><span data-stu-id="9844e-288">For performance reasons we recommend that the ManualSafeSave option be used with property handlers working with files that are 100 KB or larger.</span></span>

 

<span data-ttu-id="9844e-289">如下列 [**IPropertyStore：： Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85))範例所示，會註冊 ManualSafeSave 的處理常式，以說明「手動安全儲存」選項。</span><span class="sxs-lookup"><span data-stu-id="9844e-289">As illustrated in the following sample implementation of [**IPropertyStore::Commit**](/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)), the handler for ManualSafeSave is registered to illustrate the manual safe save option.</span></span> <span data-ttu-id="9844e-290">**\_ SaveCacheToDom** 方法會將儲存在記憶體中快取中的屬性值寫入至設定物件。</span><span class="sxs-lookup"><span data-stu-id="9844e-290">The **\_SaveCacheToDom** method writes the property values stored in the in-memory cache to the XMLdocument object.</span></span>


```
HRESULT CRecipePropertyStore::Commit()
{
    HRESULT hr = E_UNEXPECTED;
    if (_pCache)
    {
        // Check grfMode to ensure writes are allowed.
        hr = STG_E_ACCESSDENIED;
        if (_grfMode & STGM_READWRITE)
        {
            // Save the internal value cache to XML DOM object.
            hr = _SaveCacheToDom();
            if (SUCCEEDED(hr))
            {
                // Reset the output stream.
                LARGE_INTEGER liZero = {};
                hr = _pStream->Seek(liZero, STREAM_SEEK_SET, NULL);
```



<span data-ttu-id="9844e-291">接下來，詢問 p 是否支援 [**IDestinationStreamFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory)。</span><span class="sxs-lookup"><span data-stu-id="9844e-291">Next, ask whether the pecified supports [**IDestinationStreamFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory).</span></span>


```
                        if (SUCCEEDED(hr))
                        {
                            // Write the XML out to the temprorary stream and commit it.
                            VARIANT varStream = {};
                            varStream.vt = VT_UNKNOWN;
                            varStream.punkVal = pStreamCommit;
                            hr = _pDomDoc->save(varStream);
                            if (SUCCEEDED(hr))
                            {
                                hr = pStreamCommit->Commit(STGC_DEFAULT);_
```



<span data-ttu-id="9844e-292">接下來，認可原始資料流程，這會以安全的方式將資料寫回原始檔案。</span><span class="sxs-lookup"><span data-stu-id="9844e-292">Next, commit the original stream, which writes the data back to the original file in a safe manner.</span></span>


```
                        if (SUCCEEDED(hr))
                                {
                                    // Commit the real output stream.
                                    _pStream->Commit(STGC_DEFAULT);
                                }
                            }

                            pStreamCommit->Release();
                        }

                        pSafeCommit->Release();
                    }
                }
            }
        }
    }
```



<span data-ttu-id="9844e-293">然後檢查 **\_ SaveCacheToDom** 的執行。</span><span class="sxs-lookup"><span data-stu-id="9844e-293">Then examine the **\_SaveCacheToDom** implementation.</span></span>


```
// Saves the values in the internal cache back to the internal DOM object.
HRESULT CRecipePropertyStore::_SaveCacheToDom()
{
    // Iterate over each property in the internal value cache.
    DWORD cProps;  
```



<span data-ttu-id="9844e-294">接下來，取得儲存在記憶體中快取中的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="9844e-294">Next, get the number of properties stored in the in-memory cache.</span></span>


```
HRESULT hr = _pCache->GetCount(&cProps);          
            
```



<span data-ttu-id="9844e-295">現在逐一查看屬性，以判斷屬性的值在載入記憶體之後是否已變更。</span><span class="sxs-lookup"><span data-stu-id="9844e-295">Now iterate through the properties to determine whether the value of a property has been changed since it was loaded into memory.</span></span>


```
    for (UINT i = 0; SUCCEEDED(hr) && (i < cProps); ++i)
    {
        PROPERTYKEY key;
        hr = _pCache->GetAt(i, &key); 
```



<span data-ttu-id="9844e-296">[**IPropertyStoreCache：： >getstate**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-getstate)方法會取得快取中的屬性狀態。</span><span class="sxs-lookup"><span data-stu-id="9844e-296">The [**IPropertyStoreCache::GetState**](/windows/win32/api/propsys/nf-propsys-ipropertystorecache-getstate) method gets the state of the property in the cache.</span></span> <span data-ttu-id="9844e-297">PSC 中途 \_ 旗標是在 [**IPropertyStore：： SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) 實中設定的，會將屬性標示為已變更。</span><span class="sxs-lookup"><span data-stu-id="9844e-297">The PSC\_DIRTY flag, which was set in the [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) implementation, marks a property as changed.</span></span>


```
        if (SUCCEEDED(hr))
        {
            // check the cache state; only save dirty properties
            PSC_STATE psc;
            hr = _pCache->GetState(key, &psc);
            if (SUCCEEDED(hr) && psc == PSC_DIRTY)
            {
                // get the cached value
                PROPVARIANT propvar = {};
                hr = _pCache->GetValue(key, &propvar); 
```



<span data-ttu-id="9844e-298">將屬性對應至 XML 節點，如例如 **\_ rgPropertyMap** 陣列中所指定。</span><span class="sxs-lookup"><span data-stu-id="9844e-298">Map the property to the XML node as specified in the **eg\_rgPropertyMap** array.</span></span>


```
if (SUCCEEDED(hr))
                {
                    // save as a native property if the key is in the property map
                    BOOL fIsNativeProperty = FALSE;
                    for (UINT i = 0; i < ARRAYSIZE(g_rgPROPERTYMAP); ++i)
                    {
                        if (IsEqualPropertyKey(key, *g_rgPROPERTYMAP[i].pkey))
                        {
                            fIsNativeProperty = TRUE;
                            hr = _SaveProperty(propvar, g_rgPROPERTYMAP[i]);
                            break;
                        }     
```



<span data-ttu-id="9844e-299">如果屬性不在對應中，則為 Windows 檔案總管所設定的新屬性。</span><span class="sxs-lookup"><span data-stu-id="9844e-299">If a property is not in the map, it is a new property that was set by Windows Explorer.</span></span> <span data-ttu-id="9844e-300">因為支援開放中繼資料，請將新的屬性儲存在 XML 的 **ExtendedProperties** 區段中。</span><span class="sxs-lookup"><span data-stu-id="9844e-300">Because open metadata is supported, save the new property in the **ExtendedProperties** section of the XML.</span></span>


```
                    
                    // Otherwise, save as an extended property.
                    if (!fIsNativeProperty)
                    {
                        hr = _SaveExtendedProperty(key, propvar);
                    }

                    PropVariantClear(&propvar);
                }
            }
        }
    }

    return hr;    
```



## <a name="implementing-ipropertystorecapabilities"></a><span data-ttu-id="9844e-301">執行 IPropertyStoreCapabilities</span><span class="sxs-lookup"><span data-stu-id="9844e-301">Implementing IPropertyStoreCapabilities</span></span>

<span data-ttu-id="9844e-302">[**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) 會通知 shell ui 是否可在 shell ui 中編輯特定屬性。</span><span class="sxs-lookup"><span data-stu-id="9844e-302">[**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) informs the Shell UI whether a particular property can be edited in the Shell UI.</span></span> <span data-ttu-id="9844e-303">請務必注意，這只與編輯 UI 中屬性的功能有關，而不是您是否可以在屬性上成功呼叫 [**IPropertyStore：： SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) 。</span><span class="sxs-lookup"><span data-stu-id="9844e-303">It is important to note that this relates only to the ability to edit the property in the UI, not whether you can successfully call [**IPropertyStore::SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)) on the property.</span></span> <span data-ttu-id="9844e-304">\_從 [**IPropertyStoreCapabilities：： IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) provokes 傳回值 FALSE 的屬性，可能仍可以透過應用程式進行設定。</span><span class="sxs-lookup"><span data-stu-id="9844e-304">A property that provokes a return value of S\_FALSE from [**IPropertyStoreCapabilities::IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) might still be capable of being set through an application.</span></span>


```
interface IPropertyStoreCapabilities : IUnknown
{
    HRESULT IsPropertyWritable([in] REFPROPERTYKEY key);
}
```



<span data-ttu-id="9844e-305">[**IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) 會 **傳回 \_ [確定]** ，表示應該允許使用者直接編輯屬性;\_FALSE 表示不應如此。</span><span class="sxs-lookup"><span data-stu-id="9844e-305">[**IsPropertyWritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) returns **S\_OK** to indicate that end users should be allowed to edit the property directly; S\_FALSE indicates that they should not.</span></span> <span data-ttu-id="9844e-306">\_FALSE 可能表示應用程式會負責寫入屬性，而不是使用者。</span><span class="sxs-lookup"><span data-stu-id="9844e-306">S\_FALSE can mean that applications are responsible for writing the property, not users.</span></span> <span data-ttu-id="9844e-307">Shell 會根據呼叫這個方法的結果，適當地停用編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="9844e-307">The Shell disables editing controls as appropriate based on the results of calls to this method.</span></span> <span data-ttu-id="9844e-308">會假設不會執行 [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) 的處理常式會透過支援寫入任何屬性來支援開啟的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="9844e-308">A handler that does not implement [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) is assumed to support open metadata through support for the writing of any property.</span></span>

<span data-ttu-id="9844e-309">如果您要建立處理唯讀屬性的處理常式，則應該將 **Initialize** 方法 ([**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)、 [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)或 [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)) ，以便在 \_ \_ 使用 ACCESSDENIED READWRITE 旗標呼叫時傳回 stg. E STGM \_ 。</span><span class="sxs-lookup"><span data-stu-id="9844e-309">If you are building a handler that handles only read-only properties, then you should implement your **Initialize** method ([**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem), or [**IInitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)) so that it returns STG\_E\_ACCESSDENIED when called with the STGM\_READWRITE flag.</span></span>

<span data-ttu-id="9844e-310">某些屬性的 [isInnate](./propdesc-schema-typeinfo.md) 屬性設定為 **true**。</span><span class="sxs-lookup"><span data-stu-id="9844e-310">Some properties have their [isInnate](./propdesc-schema-typeinfo.md) attribute set to **true**.</span></span> <span data-ttu-id="9844e-311">固有屬性具有下列特性：</span><span class="sxs-lookup"><span data-stu-id="9844e-311">Innate properties have the following characteristics:</span></span>

-   <span data-ttu-id="9844e-312">屬性通常會以某種方式計算。</span><span class="sxs-lookup"><span data-stu-id="9844e-312">The property is usually calculated in some way.</span></span> <span data-ttu-id="9844e-313">例如， `System.Image.BitDepth` 是從影像本身計算而來。</span><span class="sxs-lookup"><span data-stu-id="9844e-313">For instance, `System.Image.BitDepth` is calculated from the image itself.</span></span>
-   <span data-ttu-id="9844e-314">變更屬性不會有任何意義，而不需要變更檔案。</span><span class="sxs-lookup"><span data-stu-id="9844e-314">Changing the property would not make sense without changing the file.</span></span> <span data-ttu-id="9844e-315">比方說，變更 `System.Image.Dimensions` 並不會調整影像大小，所以允許使用者進行變更並不合理。</span><span class="sxs-lookup"><span data-stu-id="9844e-315">For instance, changing `System.Image.Dimensions` would not resize the image, so it does not make sense to allow the user to change it.</span></span>
-   <span data-ttu-id="9844e-316">在某些情況下，系統會自動提供這些屬性。</span><span class="sxs-lookup"><span data-stu-id="9844e-316">In some cases, these properties are provided automatically by the system.</span></span> <span data-ttu-id="9844e-317">範例包括 `System.DateModified` 檔案系統所提供的，以及以使用者共用檔案的使用者為基礎的範例 `System.SharedWith` 。</span><span class="sxs-lookup"><span data-stu-id="9844e-317">Examples include `System.DateModified`, which is provided by the file system, and `System.SharedWith`, which is based on who the user is sharing the file with.</span></span>

<span data-ttu-id="9844e-318">由於這些特性，標記為 *IsInnate* 的屬性只會在 Shell UI 中提供給使用者，以做為唯讀屬性。</span><span class="sxs-lookup"><span data-stu-id="9844e-318">Due to these characteristics, properties marked as *IsInnate* are provided to the user in the Shell UI only as read-only properties.</span></span> <span data-ttu-id="9844e-319">如果屬性標示為 *IsInnate*，屬性系統不會將該屬性儲存在屬性處理常式中。</span><span class="sxs-lookup"><span data-stu-id="9844e-319">If a property is marked as *IsInnate*, the property system does not store that property in the property handler.</span></span> <span data-ttu-id="9844e-320">因此，屬性處理常式不需要特殊的程式碼，就能在其實作為中考慮這些屬性。</span><span class="sxs-lookup"><span data-stu-id="9844e-320">Therefore, property handlers do not need special code to account for these properties in their implementations.</span></span> <span data-ttu-id="9844e-321">如果未針對特定屬性明確陳述 *IsInnate* 屬性的值，則預設值為 **false**。</span><span class="sxs-lookup"><span data-stu-id="9844e-321">If the value of the *IsInnate* attribute is not explicitly stated for a particular property, the default value is **false**.</span></span>

## <a name="registering-and-distributing-property-handlers"></a><span data-ttu-id="9844e-322">註冊和散發屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="9844e-322">Registering and Distributing Property Handlers</span></span>

<span data-ttu-id="9844e-323">在實作為屬性處理常式的情況下，必須註冊它以及與處理常式相關聯的副檔名。</span><span class="sxs-lookup"><span data-stu-id="9844e-323">With the property handler implemented, it must be registered and its file name extension associated with the handler.</span></span> <span data-ttu-id="9844e-324">如需詳細資訊，請參閱 [註冊和散發屬性處理常式](./prophand-reg-dist.md)。</span><span class="sxs-lookup"><span data-stu-id="9844e-324">For more information, see [Registering and Distributing Property Handlers](./prophand-reg-dist.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9844e-325">相關主題</span><span class="sxs-lookup"><span data-stu-id="9844e-325">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9844e-326">瞭解屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="9844e-326">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
</dt> <dt>

[<span data-ttu-id="9844e-327">使用種類名稱</span><span class="sxs-lookup"><span data-stu-id="9844e-327">Using Kind Names</span></span>](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[<span data-ttu-id="9844e-328">使用屬性清單</span><span class="sxs-lookup"><span data-stu-id="9844e-328">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
</dt> <dt>

[<span data-ttu-id="9844e-329">註冊和散發屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="9844e-329">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
</dt> <dt>

[<span data-ttu-id="9844e-330">屬性處理常式的最佳作法和常見問題</span><span class="sxs-lookup"><span data-stu-id="9844e-330">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.yml)
</dt> </dl>

 

 
