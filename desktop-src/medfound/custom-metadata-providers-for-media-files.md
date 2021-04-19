---
description: 本主題說明如何撰寫 Microsoft 媒體基礎媒體來源的自訂 Shell 屬性處理常式。
ms.assetid: f8cf70ff-8324-4308-8adf-a145aa351ca9
title: 媒體檔案的自訂中繼資料提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2ded77492d03f7b802f6b2f9c25e1009ef97f50
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106986673"
---
# <a name="custom-metadata-providers-for-media-files"></a><span data-ttu-id="a39c6-103">媒體檔案的自訂中繼資料提供者</span><span class="sxs-lookup"><span data-stu-id="a39c6-103">Custom Metadata Providers for Media Files</span></span>

<span data-ttu-id="a39c6-104">本主題說明如何撰寫 Microsoft 媒體基礎媒體來源的自訂 Shell 屬性處理常式。</span><span class="sxs-lookup"><span data-stu-id="a39c6-104">This topic describes how to write a custom Shell property handler for a Microsoft Media Foundation media source.</span></span>

> [!Note]  
> <span data-ttu-id="a39c6-105">如需媒體基礎中中繼資料提供者的背景資訊，請參閱 [媒體中繼資料](media-metadata.md)。</span><span class="sxs-lookup"><span data-stu-id="a39c6-105">For background information about metadata providers in Media Foundation, see [Media Metadata](media-metadata.md).</span></span> <span data-ttu-id="a39c6-106">本主題討論 Shell 屬性處理常式;它不會描述第1版的中繼資料介面 [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)。</span><span class="sxs-lookup"><span data-stu-id="a39c6-106">This topic discusses Shell property handlers; it does not describe the version 1 metadata interface, [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata).</span></span>

 

<span data-ttu-id="a39c6-107">中繼資料會緊密地系結至檔案的格式。</span><span class="sxs-lookup"><span data-stu-id="a39c6-107">Metadata is closely tied to the format of the file.</span></span> <span data-ttu-id="a39c6-108">在媒體基礎中，檔案格式會以媒體來源表示。</span><span class="sxs-lookup"><span data-stu-id="a39c6-108">In Media Foundation, file formats are represented by media sources.</span></span> <span data-ttu-id="a39c6-109">如果您想要支援媒體基礎中原生不支援的格式中繼資料，則必須使用屬性處理常式來執行自訂媒體來源。</span><span class="sxs-lookup"><span data-stu-id="a39c6-109">If you want to support metadata for a format that is not supported natively in Media Foundation, you must implement a custom media source with a property handler.</span></span> <span data-ttu-id="a39c6-110">屬性處理常式可讓 Shell 屬性系統有效率地讀取和寫入中繼資料。</span><span class="sxs-lookup"><span data-stu-id="a39c6-110">The property handler enables the Shell property system to read and write metadata efficiently.</span></span>

<span data-ttu-id="a39c6-111">屬性處理常式是一個 COM 物件，它會執行下列介面：</span><span class="sxs-lookup"><span data-stu-id="a39c6-111">A property handler is a COM object that implements the following interfaces:</span></span>

-   [<span data-ttu-id="a39c6-112">**IInitializeWithStream**</span><span class="sxs-lookup"><span data-stu-id="a39c6-112">**IInitializeWithStream**</span></span>](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)
-   [<span data-ttu-id="a39c6-113">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="a39c6-113">**IPropertyStore**</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystore)

<span data-ttu-id="a39c6-114">也可以選擇公開下列介面：</span><span class="sxs-lookup"><span data-stu-id="a39c6-114">Optionally, it can also expose the following interface:</span></span>

-   [<span data-ttu-id="a39c6-115">**IPropertyStoreCapabilities**</span><span class="sxs-lookup"><span data-stu-id="a39c6-115">**IPropertyStoreCapabilities**</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities)

<span data-ttu-id="a39c6-116">如果 Shell 屬性系統需要取得檔案的中繼資料，它會呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 來建立屬性處理常式，然後在 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面上呼叫適當的讀取和寫入方法。</span><span class="sxs-lookup"><span data-stu-id="a39c6-116">If the Shell property system needs to get metadata for a file, it calls [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create the property handler and then calls the appropriate read and write methods on the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface.</span></span>

<span data-ttu-id="a39c6-117">媒體基礎管線會使用稍微不同的機制，因為管線會直接從媒體來源取得屬性處理常式。</span><span class="sxs-lookup"><span data-stu-id="a39c6-117">The Media Foundation pipeline uses a slightly different mechanism, because the pipeline gets the property handler directly from the media source.</span></span> <span data-ttu-id="a39c6-118">管線會呼叫媒體來源上的 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) ，而不是呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)來建立屬性處理常式，如 [Shell 中繼資料提供者](shell-metadata-providers.md)的主題所述。</span><span class="sxs-lookup"><span data-stu-id="a39c6-118">Instead of calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create the property handler, the pipeline calls [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the media source, as described in the topic [Shell Metadata Providers](shell-metadata-providers.md).</span></span>

<span data-ttu-id="a39c6-119">若要建立自訂屬性處理常式，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="a39c6-119">To create a custom property handler, do the following:</span></span>

-   <span data-ttu-id="a39c6-120">執行 [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) 介面以公開 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="a39c6-120">Implement the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface to expose [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span> <span data-ttu-id="a39c6-121">服務 GUID 是 **MF \_ 屬性 \_ 處理常式 \_ 服務**。</span><span class="sxs-lookup"><span data-stu-id="a39c6-121">The service GUID is **MF\_PROPERTY\_HANDLER\_SERVICE**.</span></span>
-   <span data-ttu-id="a39c6-122">如果將從遠端使用媒體來源，則除了 [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)以外，它也必須透過媒體來源的 **QueryInterface** 方法公開 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)介面。</span><span class="sxs-lookup"><span data-stu-id="a39c6-122">If the media source will be used remotely, it must also expose the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface through the media source's **QueryInterface** method, in addition to [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice).</span></span>
-   <span data-ttu-id="a39c6-123">若要將屬性處理常式提供給 Shell 屬性系統，請如 [註冊和散發屬性處理常式](../properties/prophand-reg-dist.md)中所述，註冊屬性處理常式的 DLL。</span><span class="sxs-lookup"><span data-stu-id="a39c6-123">To make the property handler available to the Shell property system, register the DLL for the property handler as described in [Registering and Distributing Property Handlers](../properties/prophand-reg-dist.md).</span></span>
-   <span data-ttu-id="a39c6-124">媒體來源會分開註冊，如 [配置處理常式和 Byte-Stream 處理常式](scheme-handlers-and-byte-stream-handlers.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="a39c6-124">The media source is registered separately, as described in [Scheme Handlers and Byte-Stream Handlers](scheme-handlers-and-byte-stream-handlers.md).</span></span>

### <a name="implementation-tips"></a><span data-ttu-id="a39c6-125">執行秘訣</span><span class="sxs-lookup"><span data-stu-id="a39c6-125">Implementation Tips</span></span>

<span data-ttu-id="a39c6-126">如需中繼資料屬性索引鍵的清單，請參閱媒體檔案的 [中繼資料屬性](metadata-properties-for-media-files.md)。</span><span class="sxs-lookup"><span data-stu-id="a39c6-126">For a list of metadata property keys, see [Metadata Properties for Media Files](metadata-properties-for-media-files.md).</span></span>

<span data-ttu-id="a39c6-127">屬性處理常式必須快速;它們必須提供對中繼資料的有效讀取和寫入存取權。</span><span class="sxs-lookup"><span data-stu-id="a39c6-127">Property handlers must be fast; they must provide efficient read and write access to the metadata.</span></span> <span data-ttu-id="a39c6-128"> (考慮到 Shell 可能會從數百個檔案取出中繼資料 ) 。因此，請不要從您的屬性處理常式呼叫 [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) 。</span><span class="sxs-lookup"><span data-stu-id="a39c6-128">(Consider that the Shell may retrieve metadata from hundreds of files.) Therefore, do not call [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) from your property handler.</span></span> <span data-ttu-id="a39c6-129">**MFStartup** 函式會引進啟動延遲，因為它會建立多個工作佇列執行緒，並配置全域記憶體。</span><span class="sxs-lookup"><span data-stu-id="a39c6-129">The **MFStartup** function introduces startup latency, because it creates multiple work-queue threads and allocates global memory.</span></span>

<span data-ttu-id="a39c6-130">在一般的執行中，屬性處理常式和媒體來源會共用部分相同的剖析程式碼。</span><span class="sxs-lookup"><span data-stu-id="a39c6-130">In a typical implementation, the property handler and the media source will share some of the same parsing code.</span></span> <span data-ttu-id="a39c6-131">不過，媒體來源會針對 i/o 使用非同步 [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) 呼叫，而屬性處理常式會使用 [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) 介面。</span><span class="sxs-lookup"><span data-stu-id="a39c6-131">However, a media source uses asynchronous [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) calls for I/O, whereas the property handler uses the [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) interface.</span></span> <span data-ttu-id="a39c6-132">媒體基礎提供可包裝 **IStream** 型資料流程，並將其公開為 **IMFByteStream** 資料流程的 helper 物件。</span><span class="sxs-lookup"><span data-stu-id="a39c6-132">Media Foundation provides a helper object that wraps an **IStream**-based stream and exposes it as an **IMFByteStream** stream.</span></span> <span data-ttu-id="a39c6-133">若要建立包裝函式，請呼叫 [**MFCreateMFByteStreamOnStream**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemfbytestreamonstream)。</span><span class="sxs-lookup"><span data-stu-id="a39c6-133">To create the wrapper, call [**MFCreateMFByteStreamOnStream**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemfbytestreamonstream).</span></span>

<span data-ttu-id="a39c6-134">更新中繼資料時，建議您將資料直接寫入原始資料流程。</span><span class="sxs-lookup"><span data-stu-id="a39c6-134">When updating metadata, it is recommended to write the data directly to the original stream.</span></span> <span data-ttu-id="a39c6-135">這項建議與大部分屬性處理常式的 *複製寫入* 行為不同，後者會修改資料的複本。</span><span class="sxs-lookup"><span data-stu-id="a39c6-135">This recommendation differs from the *copy-on-write* behavior of most property handlers, in which a copy of the data is modified.</span></span> <span data-ttu-id="a39c6-136">媒體檔案可能很大，所以寫入時複製通常太慢，無法進行有效率的執行。</span><span class="sxs-lookup"><span data-stu-id="a39c6-136">Media files can be very large, so copy-on-write is typically too slow for an efficient implementation.</span></span> <span data-ttu-id="a39c6-137">若要停用寫入時複製，請設定 **ManualSafeSave** 登錄設定，如 [註冊和散發屬性處理常式](../properties/prophand-reg-dist.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="a39c6-137">To disable copy-on-write, set the **ManualSafeSave** registry setting, as described in [Registering and Distributing Property Handlers](../properties/prophand-reg-dist.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a39c6-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="a39c6-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a39c6-139">媒體中繼資料</span><span class="sxs-lookup"><span data-stu-id="a39c6-139">Media Metadata</span></span>](media-metadata.md)
</dt> <dt>

[<span data-ttu-id="a39c6-140">媒體來源</span><span class="sxs-lookup"><span data-stu-id="a39c6-140">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="a39c6-141">撰寫自訂媒體來源</span><span class="sxs-lookup"><span data-stu-id="a39c6-141">Writing a Custom Media Source</span></span>](writing-a-custom-media-source.md)
</dt> </dl>

 

 
