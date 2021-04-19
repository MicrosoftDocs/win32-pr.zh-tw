---
description: IXpsOMPackageWriter 介面會建立 XPS 檔檔，應用程式可以在其中寫入 XPS OM 的 IXpsOMPage 介面內容。
ms.assetid: eff1ab1e-2205-4f5c-9e32-199e073f5dbf
title: 使用 IXpsOMPackageWriter 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1e8a34a0538ff09cc050ac287d5314be93f0da8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979826"
---
# <a name="using-the-ixpsompackagewriter-interface"></a><span data-ttu-id="f3c23-103">使用 IXpsOMPackageWriter 介面</span><span class="sxs-lookup"><span data-stu-id="f3c23-103">Using the IXpsOMPackageWriter Interface</span></span>

<span data-ttu-id="f3c23-104">[**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)介面會建立 xps 檔檔，應用程式可以在其中寫入 xps OM 的 [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)介面內容。</span><span class="sxs-lookup"><span data-stu-id="f3c23-104">The [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) interface creates an XPS document file into which applications can write the contents of the [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) interfaces of an XPS OM.</span></span> <span data-ttu-id="f3c23-105">當檔內容是依序處理或建立時， [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) 介面最有用。</span><span class="sxs-lookup"><span data-stu-id="f3c23-105">The [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) interface is most useful when document contents are being processed or created sequentially.</span></span> <span data-ttu-id="f3c23-106">與 [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)介面的 [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile)和 [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream)方法不同的是，若要使用 **IXpsOMPackageWriter** 介面，則整個 FixedDocument 或 FixedDocumentSequence 都不需要完成。</span><span class="sxs-lookup"><span data-stu-id="f3c23-106">Unlike the [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) and [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) methods of the [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) interface, for the **IXpsOMPackageWriter** interface to be used neither the entire FixedDocument nor the FixedDocumentSequence has to be finished.</span></span>

## <a name="overview"></a><span data-ttu-id="f3c23-107">概觀</span><span class="sxs-lookup"><span data-stu-id="f3c23-107">Overview</span></span>

<span data-ttu-id="f3c23-108">[**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)介面會一次寫入一頁，從 XPS 檔的第一頁到最後一個頁面。</span><span class="sxs-lookup"><span data-stu-id="f3c23-108">The [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) interface writes one page at a time, from the first page of an XPS document to the last.</span></span> <span data-ttu-id="f3c23-109">介面可以用來建立簡單的 XPS 檔檔案，以及在 FixedDocumentSequence 中包含多個 FixedDocument 的複雜 XPS 檔檔案。</span><span class="sxs-lookup"><span data-stu-id="f3c23-109">The interface can be used to create simple XPS document files and also complex XPS document files that contain more than one FixedDocument in the FixedDocumentSequence.</span></span> <span data-ttu-id="f3c23-110">在複雜的 XPS 檔檔中，FixedDocuments 也會依序建立，從 FixedDocumentSequence 中的第一個 FixedDocument 開始。</span><span class="sxs-lookup"><span data-stu-id="f3c23-110">In complex XPS document files, the FixedDocuments are also created in sequence, starting with the first FixedDocument in the FixedDocumentSequence.</span></span> <span data-ttu-id="f3c23-111">**IXpsOMPackageWriter** 介面不支援以隨機順序建立檔內容。</span><span class="sxs-lookup"><span data-stu-id="f3c23-111">The **IXpsOMPackageWriter** interface does not support the creation of document contents in random order.</span></span> <span data-ttu-id="f3c23-112">例如，您可以使用它來建立連續報告，或在設備磁碟機篩選器中執行處理，以依序將檔內容送入驅動程式。</span><span class="sxs-lookup"><span data-stu-id="f3c23-112">Use it, for example, to create a sequential report or to perform processing in a device driver filter where the document contents are fed to the driver in sequence.</span></span>

## <a name="terminology-review"></a><span data-ttu-id="f3c23-113">術語審查</span><span class="sxs-lookup"><span data-stu-id="f3c23-113">Terminology Review</span></span>

<span data-ttu-id="f3c23-114">*XPS 檔* 檔是符合 XML 檔規格的開放式封裝慣例 (OPC) 套件。</span><span class="sxs-lookup"><span data-stu-id="f3c23-114">An *XPS document file* is an Open Packaging Conventions (OPC) package that conforms to the XML Paper Specification.</span></span> <span data-ttu-id="f3c23-115">因此，技術上來說， [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) 介面會建立 *opc 封裝*，但它是符合 XML 檔規格的 opc 套件。</span><span class="sxs-lookup"><span data-stu-id="f3c23-115">So, technically, the [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) interface creates an *OPC package*, but it is an OPC package that conforms to the XML Paper Specification.</span></span> <span data-ttu-id="f3c23-116">基於這個理由，在有關 XPS 檔的討論中， *xps 檔* 和 *套件* 的條款通常會交替使用。</span><span class="sxs-lookup"><span data-stu-id="f3c23-116">For this reason, in discussions about XPS documents, the terms *XPS document* and *package* are often used interchangeably.</span></span>

<span data-ttu-id="f3c23-117">[**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)介面所建立的 *封裝* 將包含所需的 XPS 檔元件： FixedDocumentSequence、至少一個 FixedDocument，以及至少一個 FixedPage。</span><span class="sxs-lookup"><span data-stu-id="f3c23-117">The *package* created by the [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) interface will contain the required XPS document components: a FixedDocumentSequence, at least one FixedDocument, and at least one FixedPage.</span></span> <span data-ttu-id="f3c23-118">當 **IXpsOMPackageWriter** 介面具現化時，就會建立 FixedDocumentSequence。</span><span class="sxs-lookup"><span data-stu-id="f3c23-118">The FixedDocumentSequence is created when the **IXpsOMPackageWriter** interface is instantiated.</span></span> <span data-ttu-id="f3c23-119">每次呼叫 [**IXpsOMPackageWriter：： StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument) 時會建立一個 FixedDocument，每次呼叫 [**IXpsOMPackageWriter：： AddPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage) 時，就會建立一個 FixedPage。</span><span class="sxs-lookup"><span data-stu-id="f3c23-119">A FixedDocument is created every time [**IXpsOMPackageWriter::StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument) is called, and a FixedPage is created every time [**IXpsOMPackageWriter::AddPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage) is called.</span></span> <span data-ttu-id="f3c23-120">因為介面會依序寫入檔內容，所以 **AddPage** 方法會將頁面新增至最近建立的 FixedDocument。</span><span class="sxs-lookup"><span data-stu-id="f3c23-120">Because the interface writes the document contents sequentially, the **AddPage** method adds the page to the most recently created FixedDocument.</span></span>

## <a name="using-the-ixpsompackagewriter-interface"></a><span data-ttu-id="f3c23-121">使用 IXpsOMPackageWriter 介面</span><span class="sxs-lookup"><span data-stu-id="f3c23-121">Using the IXpsOMPackageWriter Interface</span></span>

<span data-ttu-id="f3c23-122">下列程式描述如何使用 [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) 介面建立 XPS 檔檔。</span><span class="sxs-lookup"><span data-stu-id="f3c23-122">The following procedure describes how to create an XPS document file by using the [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) interface.</span></span> <span data-ttu-id="f3c23-123">此程式不會說明如何具現化 [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) 介面及其內容。</span><span class="sxs-lookup"><span data-stu-id="f3c23-123">The procedure does not describe how to instantiate an [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) interface and its contents.</span></span> <span data-ttu-id="f3c23-124">For more information about **IXpsOMPage** and adding content to a page, see [XPS OM Page Interfaces](xps-object-model-page-interfaces.md) and the topics listed in the See Also section.</span><span class="sxs-lookup"><span data-stu-id="f3c23-124">For more information about **IXpsOMPage** and adding content to a page, see [XPS OM Page Interfaces](xps-object-model-page-interfaces.md) and the topics listed in the See Also section.</span></span>

 <span data-ttu-id="f3c23-125">**建立檔**</span><span class="sxs-lookup"><span data-stu-id="f3c23-125">**Creating a document**</span></span>

1.  <span data-ttu-id="f3c23-126">具現化 [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) 介面。</span><span class="sxs-lookup"><span data-stu-id="f3c23-126">Instantiate an [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) interface.</span></span>

    <span data-ttu-id="f3c23-127">這會在封裝中建立空的 FixedDocumentSequence。</span><span class="sxs-lookup"><span data-stu-id="f3c23-127">This creates an empty FixedDocumentSequence in the package.</span></span>

    -   <span data-ttu-id="f3c23-128">若要在檔案中建立 XPS 檔，請呼叫 [**IXpsOMObjectFactory：： CreatePackageWriterOnFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronfile)。</span><span class="sxs-lookup"><span data-stu-id="f3c23-128">To create an XPS document in a file, call [**IXpsOMObjectFactory::CreatePackageWriterOnFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronfile).</span></span>
    -   <span data-ttu-id="f3c23-129">若要在資料流程中建立 XPS 檔，請呼叫 [**IXpsOMObjectFactory：： CreatePackageWriterOnStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronstream)。</span><span class="sxs-lookup"><span data-stu-id="f3c23-129">To create an XPS document in a stream, call [**IXpsOMObjectFactory::CreatePackageWriterOnStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronstream).</span></span>

2.  <span data-ttu-id="f3c23-130">藉由呼叫 [**IXpsOMPackageWriter：： StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument)，在封裝中啟動新檔。</span><span class="sxs-lookup"><span data-stu-id="f3c23-130">Start a new document in the package by calling [**IXpsOMPackageWriter::StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument).</span></span>

    <span data-ttu-id="f3c23-131">新增頁面之前，請呼叫 [**IXpsOMPackageWriter：： StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument) ，將 FixedDocument 新增至步驟1中建立的 FixedDocumentSequence。</span><span class="sxs-lookup"><span data-stu-id="f3c23-131">Before adding a page, call [**IXpsOMPackageWriter::StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument) to add a FixedDocument to the FixedDocumentSequence that was created in step 1.</span></span>

3.  <span data-ttu-id="f3c23-132">加入內容。</span><span class="sxs-lookup"><span data-stu-id="f3c23-132">Add content.</span></span>
    -   <span data-ttu-id="f3c23-133">若要在檔中加入新的 FixedPage，請呼叫 [**IXpsOMPackageWriter：： AddPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage)，並將指標傳遞至 [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) 介面，該介面具有您想要新增的 fixedpage 內容。</span><span class="sxs-lookup"><span data-stu-id="f3c23-133">To add a new FixedPage to the document, call [**IXpsOMPackageWriter::AddPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage), passing it a pointer to the [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) interface that has the contents of the FixedPage that you want to add.</span></span>
    -   <span data-ttu-id="f3c23-134">若要在 FixedDocumentSequence 中建立新的 FixedDocument，請呼叫 [**IXpsOMPackageWriter：： StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument)。</span><span class="sxs-lookup"><span data-stu-id="f3c23-134">To create a new FixedDocument in the FixedDocumentSequence, call [**IXpsOMPackageWriter::StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument).</span></span>
4.  <span data-ttu-id="f3c23-135">藉由呼叫 [**IXpsOMPackageWriter：： close**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-close)，關閉封裝和其內容。</span><span class="sxs-lookup"><span data-stu-id="f3c23-135">Close the package and its contents by calling [**IXpsOMPackageWriter::Close**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-close).</span></span>

## <a name="advanced-features"></a><span data-ttu-id="f3c23-136">進階功能</span><span class="sxs-lookup"><span data-stu-id="f3c23-136">Advanced Features</span></span>

<span data-ttu-id="f3c23-137">[**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)介面的方法也支援新增資源、縮圖和列印票證。</span><span class="sxs-lookup"><span data-stu-id="f3c23-137">The methods of the [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) interface also support the adding of resources, thumbnails, and print tickets.</span></span> <span data-ttu-id="f3c23-138">這些檔元件可以在套件、FixedDocumentSequence、FixedDocument 和 FixedPage 層級加入。</span><span class="sxs-lookup"><span data-stu-id="f3c23-138">These document components can be added at the package, FixedDocumentSequence, FixedDocument, and FixedPage levels.</span></span> <span data-ttu-id="f3c23-139">如需使用此介面進行列印的詳細資訊，請參閱 [列印 XPS OM](print-an-xps-om.md)。</span><span class="sxs-lookup"><span data-stu-id="f3c23-139">For more information about using this interface for printing, see [Print an XPS OM](print-an-xps-om.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3c23-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="f3c23-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3c23-141">使用 XPS 數位簽章 API</span><span class="sxs-lookup"><span data-stu-id="f3c23-141">Using XPS Digital Signature API</span></span>](using-digital-signatures-in-xps-documents.md)
</dt> <dt>

[<span data-ttu-id="f3c23-142">XPS OM 頁面介面</span><span class="sxs-lookup"><span data-stu-id="f3c23-142">XPS OM Page Interfaces</span></span>](xps-object-model-page-interfaces.md)
</dt> <dt>

[<span data-ttu-id="f3c23-143">流覽 XPS OM</span><span class="sxs-lookup"><span data-stu-id="f3c23-143">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="f3c23-144">使用 XPS OM 畫布和視覺化介面</span><span class="sxs-lookup"><span data-stu-id="f3c23-144">Working with XPS OM Canvas and Visual Interfaces</span></span>](working-with-xpsomcanvas-interfaces.md)
</dt> <dt>

[<span data-ttu-id="f3c23-145">使用 XPS OM 路徑介面</span><span class="sxs-lookup"><span data-stu-id="f3c23-145">Working with XPS OM Path Interfaces</span></span>](working-with-xps-object-model-path-interfaces.md)
</dt> <dt>

[<span data-ttu-id="f3c23-146">使用 XPS OM 文字、圖形和影像介面</span><span class="sxs-lookup"><span data-stu-id="f3c23-146">Working with XPS OM Text, Graphics, and Image Interfaces</span></span>](working-with-xps-object-model-text-and-image-interfaces.md)
</dt> <dt>

[<span data-ttu-id="f3c23-147">XPS OM 列印票證介面</span><span class="sxs-lookup"><span data-stu-id="f3c23-147">XPS OM Print Ticket Interfaces</span></span>](xps-object-model-print-ticket-interfaces.md)
</dt> <dt>

[<span data-ttu-id="f3c23-148">**IXpsOMThumbnailGenerator**</span><span class="sxs-lookup"><span data-stu-id="f3c23-148">**IXpsOMThumbnailGenerator**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator)
</dt> <dt>

[<span data-ttu-id="f3c23-149">XPS 檔 API 參考</span><span class="sxs-lookup"><span data-stu-id="f3c23-149">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="f3c23-150">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="f3c23-150">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



