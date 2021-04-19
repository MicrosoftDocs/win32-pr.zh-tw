---
description: 本主題說明如何建立空白的 XPS OM。
ms.assetid: 5b6f12ba-9a41-4252-96c4-391bb8d75cd4
title: 建立空白的 XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0588fc11deb4b3d980e978dfe8a5370bc170d506
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988784"
---
# <a name="create-a-blank-xps-om"></a><span data-ttu-id="5c6ff-103">建立空白的 XPS OM</span><span class="sxs-lookup"><span data-stu-id="5c6ff-103">Create a Blank XPS OM</span></span>

<span data-ttu-id="5c6ff-104">本主題說明如何建立空白的 XPS OM。</span><span class="sxs-lookup"><span data-stu-id="5c6ff-104">This topic describes how to create a blank XPS OM.</span></span> <span data-ttu-id="5c6ff-105">本文提供程式碼範例，說明如何使用 XPS OM 來建立具有一個空白頁面的 XPS 檔檔結構。</span><span class="sxs-lookup"><span data-stu-id="5c6ff-105">It presents the code examples that illustrate how to use an XPS OM to build the document structure of an XPS document that has one blank page.</span></span>

<span data-ttu-id="5c6ff-106">若要儲存為 XPS 檔，XPS OM 至少需要下列元件：</span><span class="sxs-lookup"><span data-stu-id="5c6ff-106">To be saved as an XPS document, the XPS OM requires at least the following components:</span></span>

-   <span data-ttu-id="5c6ff-107">描述 XPS 檔套件的 [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)</span><span class="sxs-lookup"><span data-stu-id="5c6ff-107">An [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) that describes the XPS document package</span></span>
-   <span data-ttu-id="5c6ff-108">包含套件內容架構的 [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)</span><span class="sxs-lookup"><span data-stu-id="5c6ff-108">An [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) that contains the framework of the package contents</span></span>
-   <span data-ttu-id="5c6ff-109">[**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument) ，其中包含封裝內檔的架構</span><span class="sxs-lookup"><span data-stu-id="5c6ff-109">An [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument) that contains the framework of a document within the package</span></span>
-   <span data-ttu-id="5c6ff-110">包含檔中頁面集合的 [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)</span><span class="sxs-lookup"><span data-stu-id="5c6ff-110">An [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) that contains the collection of pages in the document</span></span>
-   <span data-ttu-id="5c6ff-111">包含空白頁面的 [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)</span><span class="sxs-lookup"><span data-stu-id="5c6ff-111">An [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) that contains a blank page</span></span>

<span data-ttu-id="5c6ff-112">使用這些介面時，XPS OM 將包含具有一個空白頁面的檔。</span><span class="sxs-lookup"><span data-stu-id="5c6ff-112">When these interfaces are used, the XPS OM will contain a document that has one blank page.</span></span> <span data-ttu-id="5c6ff-113">若要在 XPS OM 中建立這份檔，程式必須先建立個別的元件，然後將它們連結在一起。</span><span class="sxs-lookup"><span data-stu-id="5c6ff-113">To create this document in an XPS OM, the program must first create the individual components and then link them together.</span></span>

<span data-ttu-id="5c6ff-114">使用下列程式碼範例之前，請閱讀 [一般 XPS 檔程式設計](common-xps-document-tasks.md)工作中的免責聲明。</span><span class="sxs-lookup"><span data-stu-id="5c6ff-114">Before using the following code examples, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-examples"></a><span data-ttu-id="5c6ff-115">程式碼範例</span><span class="sxs-lookup"><span data-stu-id="5c6ff-115">Code Examples</span></span>

<span data-ttu-id="5c6ff-116">下列程式碼範例假設初始化 [XPS OM](xps-object-model-initialization.md)中所述的初始化成功。</span><span class="sxs-lookup"><span data-stu-id="5c6ff-116">The following code example assumes that the initialization, described in [Initialize an XPS OM](xps-object-model-initialization.md), has succeeded.</span></span>


```C++
    // Declare the variables used in this section.
    HRESULT                       hr = S_OK;
    IOpcPartUri                   *opcPartUri = NULL;
    IXpsOMPackage                 *xpsPackage = NULL;
    IXpsOMDocumentSequence        *xpsFDS = NULL;
    IXpsOMDocumentCollection      *fixedDocuments = NULL;
    IXpsOMDocument                *xpsFD = NULL;
    IXpsOMPage                    *xpsPage = NULL;
    IXpsOMPageReferenceCollection *pageRefs = NULL;
    IXpsOMPageReference           *xpsPageRef = NULL;
    // These values are set outside of this code example.
    XPS_SIZE pageSize = {width, height}; 
    
    // Create the package.
    hr = xpsFactory->CreatePackage( &xpsPackage );

    // Create the URI for the fixed document sequence part and then  
    //  create the fixed document sequence
    hr = xpsFactory->CreatePartUri( 
        L"/FixedDocumentSequence.fdseq", &opcPartUri );
    hr = xpsFactory->CreateDocumentSequence( opcPartUri, &xpsFDS );
    // Release this URI to reuse the interface pointer.
    if (NULL != opcPartUri) {opcPartUri->Release(); opcPartUri = NULL;}

    // Create the URI for the document part and then create the document.
    hr = xpsFactory->CreatePartUri( 
        L"/Documents/1/FixedDocument.fdoc", &opcPartUri );
    hr = xpsFactory->CreateDocument( opcPartUri, &xpsFD );
    // Release this URI to reuse the interface pointer.
    if (NULL != opcPartUri) {opcPartUri->Release(); opcPartUri = NULL;}

    // Create a blank page.
    hr = xpsFactory->CreatePartUri( 
        L"/Documents/1/Pages/1.fpage", &opcPartUri );
    hr = xpsFactory->CreatePage(
        &pageSize,                  // Page size
        L"en-US",                   // Page language
        opcPartUri,                 // Page part name
        &xpsPage);                
    // Release this URI to reuse the interface pointer.
    if (NULL != opcPartUri) {opcPartUri->Release(); opcPartUri = NULL;}

    // Create a page reference for the page.
    hr = xpsFactory->CreatePageReference( &pageSize, &xpsPageRef );

    // Add the fixed document sequence to the package.
    hr = xpsPackage->SetDocumentSequence( xpsFDS );

    // Get the document collection of the fixed document sequence
    //  and then add the document to the collection.
    hr = xpsFDS->GetDocuments( &fixedDocuments );
    hr = fixedDocuments->Append( xpsFD );

    // Get the page reference collection from the document
    //  and add the page reference and blank page.
    hr = xpsFD->GetPageReferences( &pageRefs );
    hr = pageRefs->Append( xpsPageRef );
    hr = xpsPageRef->SetPage( xpsPage );

    // Release interface pointer
    if (NULL != xpsPage) xpsPage->Release();
    if (NULL != pageRefs) pageRefs->Release();
    if (NULL != fixedDocuments) fixedDocuments->Release();
    if (NULL != xpsPageRef) xpsPageRef->Release();
    if (NULL != xpsFD) xpsFD->Release();
    if (NULL != xpsFDS) xpsFDS->Release();
    if (NULL != xpsPackage) xpsPackage->Release();

```



## <a name="best-practices"></a><span data-ttu-id="5c6ff-117">最佳做法</span><span class="sxs-lookup"><span data-stu-id="5c6ff-117">Best Practices</span></span>

<span data-ttu-id="5c6ff-118">使用 [**IOpcPartUri**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi) 介面建立元件之後 (例如在程式碼範例) 中呼叫 **CreateDocument** 方法之後，請釋放該介面的指標，除非您需要它來進行另一個呼叫。</span><span class="sxs-lookup"><span data-stu-id="5c6ff-118">After you have used an [**IOpcPartUri**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi) interface to create a component (such as after calling the **CreateDocument** method in the code example), release the pointer to that interface—unless you need it for another call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c6ff-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="5c6ff-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5c6ff-120">**後續步驟**</span><span class="sxs-lookup"><span data-stu-id="5c6ff-120">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="5c6ff-121">流覽 XPS OM</span><span class="sxs-lookup"><span data-stu-id="5c6ff-121">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="5c6ff-122">將文字寫入至 XPS OM</span><span class="sxs-lookup"><span data-stu-id="5c6ff-122">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="5c6ff-123">在 XPS OM 中繪製圖形</span><span class="sxs-lookup"><span data-stu-id="5c6ff-123">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="5c6ff-124">以 XPS OM 放置影像</span><span class="sxs-lookup"><span data-stu-id="5c6ff-124">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="5c6ff-125">**用於此頁面**</span><span class="sxs-lookup"><span data-stu-id="5c6ff-125">**Used in This Page**</span></span>
</dt> <dt>

[<span data-ttu-id="5c6ff-126">**IOpcPartUri**</span><span class="sxs-lookup"><span data-stu-id="5c6ff-126">**IOpcPartUri**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[<span data-ttu-id="5c6ff-127">**IXpsOMObjectFactory**</span><span class="sxs-lookup"><span data-stu-id="5c6ff-127">**IXpsOMObjectFactory**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[<span data-ttu-id="5c6ff-128">**IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="5c6ff-128">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[<span data-ttu-id="5c6ff-129">**IXpsOMDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="5c6ff-129">**IXpsOMDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[<span data-ttu-id="5c6ff-130">**IXpsOMDocumentCollection**</span><span class="sxs-lookup"><span data-stu-id="5c6ff-130">**IXpsOMDocumentCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)
</dt> <dt>

[<span data-ttu-id="5c6ff-131">**IXpsOMDocument**</span><span class="sxs-lookup"><span data-stu-id="5c6ff-131">**IXpsOMDocument**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)
</dt> <dt>

[<span data-ttu-id="5c6ff-132">**IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="5c6ff-132">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="5c6ff-133">**IXpsOMPageReference**</span><span class="sxs-lookup"><span data-stu-id="5c6ff-133">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[<span data-ttu-id="5c6ff-134">**IXpsOMPageReferenceCollection**</span><span class="sxs-lookup"><span data-stu-id="5c6ff-134">**IXpsOMPageReferenceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)
</dt> <dt>

[<span data-ttu-id="5c6ff-135">**XPS \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="5c6ff-135">**XPS\_SIZE**</span></span>](/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_size)
</dt> <dt>

<span data-ttu-id="5c6ff-136">**詳細資訊**</span><span class="sxs-lookup"><span data-stu-id="5c6ff-136">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="5c6ff-137">初始化 XPS OM</span><span class="sxs-lookup"><span data-stu-id="5c6ff-137">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="5c6ff-138">封裝 API</span><span class="sxs-lookup"><span data-stu-id="5c6ff-138">Packaging API</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="5c6ff-139">XPS 檔 API 參考</span><span class="sxs-lookup"><span data-stu-id="5c6ff-139">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="5c6ff-140">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="5c6ff-140">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
