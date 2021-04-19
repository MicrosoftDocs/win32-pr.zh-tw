---
description: 本主題說明如何流覽 XPS OM，以及存取記憶體中檔的不同部分。
ms.assetid: 90b726aa-29da-4cfb-9c69-f471c2acb678
title: 流覽 XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0ec33543867f66dd4da65ef95aab0cdfd8cfe0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980587"
---
# <a name="navigate-the-xps-om"></a><span data-ttu-id="4ef67-103">流覽 XPS OM</span><span class="sxs-lookup"><span data-stu-id="4ef67-103">Navigate the XPS OM</span></span>

<span data-ttu-id="4ef67-104">本主題說明如何流覽 XPS OM，以及存取記憶體中檔的不同部分。</span><span class="sxs-lookup"><span data-stu-id="4ef67-104">This topic describes how to navigate an XPS OM and to access different parts of the in-memory document.</span></span>

<span data-ttu-id="4ef67-105">XPS 檔 API 的組織會鏡像 XPS 檔的組織。</span><span class="sxs-lookup"><span data-stu-id="4ef67-105">The organization of the XPS Document API mirrors the organization of an XPS document.</span></span> <span data-ttu-id="4ef67-106">下表說明 XPS 檔 API 介面與 XPS 檔元件的關聯性。</span><span class="sxs-lookup"><span data-stu-id="4ef67-106">The following table illustrates how the interfaces of the XPS Document API relate to the components of an XPS document.</span></span>



| <span data-ttu-id="4ef67-107">XPS 檔元件</span><span class="sxs-lookup"><span data-stu-id="4ef67-107">XPS document component</span></span>                                         | <span data-ttu-id="4ef67-108">XPS 檔 API 介面</span><span class="sxs-lookup"><span data-stu-id="4ef67-108">XPS Document API interface</span></span>                                          | <span data-ttu-id="4ef67-109">要在階層中的下一個層級下呼叫的方法</span><span class="sxs-lookup"><span data-stu-id="4ef67-109">Method to call for the next level down in the hierarchy</span></span>                                                                                       |
|----------------------------------------------------------------|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ef67-110">XPS 檔檔 (包含 OPC 套件) </span><span class="sxs-lookup"><span data-stu-id="4ef67-110">XPS document file (contains OPC package)</span></span><br/>            | [<span data-ttu-id="4ef67-111">**IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="4ef67-111">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)<br/>                   | [<span data-ttu-id="4ef67-112">**GetDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="4ef67-112">**GetDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-getdocumentsequence)<br/>                                                                   |
| <span data-ttu-id="4ef67-113">FixedDocumentSequence 元件</span><span class="sxs-lookup"><span data-stu-id="4ef67-113">FixedDocumentSequence part</span></span><br/>                          | [<span data-ttu-id="4ef67-114">**IXpsOMDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="4ef67-114">**IXpsOMDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> | [<span data-ttu-id="4ef67-115">**GetDocuments**</span><span class="sxs-lookup"><span data-stu-id="4ef67-115">**GetDocuments**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocumentsequence-getdocuments)<br/>                                                                        |
| <span data-ttu-id="4ef67-116">FixedDocument 元件</span><span class="sxs-lookup"><span data-stu-id="4ef67-116">FixedDocument part</span></span><br/>                                  | [<span data-ttu-id="4ef67-117">**IXpsOMDocument**</span><span class="sxs-lookup"><span data-stu-id="4ef67-117">**IXpsOMDocument**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/>                 | [<span data-ttu-id="4ef67-118">**GetPageReferences**</span><span class="sxs-lookup"><span data-stu-id="4ef67-118">**GetPageReferences**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocument-getpagereferences)<br/>                                                                      |
| <span data-ttu-id="4ef67-119">FixedDocument 標記中的 **PageContent** 元素</span><span class="sxs-lookup"><span data-stu-id="4ef67-119">**PageContent** element in the FixedDocument markup</span></span><br/> | [<span data-ttu-id="4ef67-120">**IXpsOMPageReference**</span><span class="sxs-lookup"><span data-stu-id="4ef67-120">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/>       | [<span data-ttu-id="4ef67-121">**GetPage**</span><span class="sxs-lookup"><span data-stu-id="4ef67-121">**GetPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage)<br/> [<span data-ttu-id="4ef67-122">**CollectPartResources**</span><span class="sxs-lookup"><span data-stu-id="4ef67-122">**CollectPartResources**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectpartresources)<br/> |
| <span data-ttu-id="4ef67-123">FixedPage 部分</span><span class="sxs-lookup"><span data-stu-id="4ef67-123">FixedPage part</span></span><br/>                                      | [<span data-ttu-id="4ef67-124">**IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="4ef67-124">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/>                         | [<span data-ttu-id="4ef67-125">**GetVisuals**</span><span class="sxs-lookup"><span data-stu-id="4ef67-125">**GetVisuals**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-getvisuals)<br/>                                                                                        |
| <span data-ttu-id="4ef67-126">FixedPage 標記中的 **Canvas** 元素</span><span class="sxs-lookup"><span data-stu-id="4ef67-126">**Canvas** element in the FixedPage markup</span></span><br/>          | [<span data-ttu-id="4ef67-127">**IXpsOMCanvas**</span><span class="sxs-lookup"><span data-stu-id="4ef67-127">**IXpsOMCanvas**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/>                     | [<span data-ttu-id="4ef67-128">**GetVisuals**</span><span class="sxs-lookup"><span data-stu-id="4ef67-128">**GetVisuals**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcanvas-getvisuals)<br/>                                                                                      |
| <span data-ttu-id="4ef67-129">FixedPage 標記中的 **Path** 元素</span><span class="sxs-lookup"><span data-stu-id="4ef67-129">**Path** element in the FixedPage markup</span></span><br/>            | [<span data-ttu-id="4ef67-130">**IXpsOMPath**</span><span class="sxs-lookup"><span data-stu-id="4ef67-130">**IXpsOMPath**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/>                         | <span data-ttu-id="4ef67-131">檔階層的結尾。</span><span class="sxs-lookup"><span data-stu-id="4ef67-131">End of document hierarchy.</span></span><br/>                                                                                                         |
| <span data-ttu-id="4ef67-132">FixedPage 標記中的 **字型** 元素</span><span class="sxs-lookup"><span data-stu-id="4ef67-132">**Glyphs** element in the FixedPage markup</span></span><br/>          | [<span data-ttu-id="4ef67-133">**IXpsOMGlyphs**</span><span class="sxs-lookup"><span data-stu-id="4ef67-133">**IXpsOMGlyphs**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/>                     | <span data-ttu-id="4ef67-134">檔階層的結尾。</span><span class="sxs-lookup"><span data-stu-id="4ef67-134">End of document hierarchy.</span></span><br/>                                                                                                         |
| <span data-ttu-id="4ef67-135">字型部分</span><span class="sxs-lookup"><span data-stu-id="4ef67-135">Font part</span></span><br/>                                           | [<span data-ttu-id="4ef67-136">**IXpsOMFontResource**</span><span class="sxs-lookup"><span data-stu-id="4ef67-136">**IXpsOMFontResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource)<br/>         | <span data-ttu-id="4ef67-137">檔階層的結尾。</span><span class="sxs-lookup"><span data-stu-id="4ef67-137">End of document hierarchy.</span></span><br/>                                                                                                         |
| <span data-ttu-id="4ef67-138">影像元件</span><span class="sxs-lookup"><span data-stu-id="4ef67-138">Image part</span></span><br/>                                          | [<span data-ttu-id="4ef67-139">**IXpsOMImageResource**</span><span class="sxs-lookup"><span data-stu-id="4ef67-139">**IXpsOMImageResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource)<br/>       | <span data-ttu-id="4ef67-140">檔階層的結尾。</span><span class="sxs-lookup"><span data-stu-id="4ef67-140">End of document hierarchy.</span></span><br/>                                                                                                         |



 

<span data-ttu-id="4ef67-141">在您的程式中使用下列程式碼範例之前，請閱讀 [一般 XPS 檔程式設計](common-xps-document-tasks.md)工作中的免責聲明。</span><span class="sxs-lookup"><span data-stu-id="4ef67-141">Before using the following code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-example"></a><span data-ttu-id="4ef67-142">程式碼範例</span><span class="sxs-lookup"><span data-stu-id="4ef67-142">Code Example</span></span>

<span data-ttu-id="4ef67-143">下列程式碼範例假設已初始化的 XPS OM 存在，而且 *套件* 指向代表該 xps Om 的 [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) 介面。</span><span class="sxs-lookup"><span data-stu-id="4ef67-143">The following code example assumes the existence of an initialized XPS OM, and *package* points to an [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) interface that represents that XPS OM.</span></span> <span data-ttu-id="4ef67-144">如需有關建立 XPS OM 的詳細資訊，請參閱 [將 Xps 檔讀入 XPS om](read-an-xps-document-into-an-xps-om.md) 或 [建立空白的 xps om](create-a-blank-xps-om.md)。</span><span class="sxs-lookup"><span data-stu-id="4ef67-144">For information about creating an XPS OM, see [Read an XPS Document into an XPS OM](read-an-xps-document-into-an-xps-om.md) or [Create a Blank XPS OM](create-a-blank-xps-om.md).</span></span>


```C++
    HRESULT                        hr = S_OK;

    IXpsOMDocumentSequence         *docSeq = NULL;
    IXpsOMDocumentCollection       *docs = NULL;
    IXpsOMDocument                 *doc = NULL;
    IXpsOMPageReferenceCollection  *pages = NULL;
    IXpsOMPageReference            *pageRef = NULL;
    IXpsOMPage                     *page = NULL;
    IXpsOMCanvas                   *canvas = NULL;
    IXpsOMPath                     *path = NULL;
    IXpsOMPartResources            *pageParts = NULL;
    IXpsOMGlyphs                   *glyphs = NULL;
    IXpsOMFontResourceCollection   *fonts = NULL; 
    IXpsOMFontResource             *font = NULL;
    IXpsOMImageResourceCollection  *images = NULL;
    IXpsOMImageResource            *image = NULL;
    IXpsOMVisualCollection         *visuals = NULL;
    IXpsOMVisual                   *visual = NULL;

    UINT32  numDocs = 0;
    UINT32  thisDoc = 0;

    UINT32  numPageRefs = 0;
    UINT32  thisPageRef = 0;

    UINT32  numVisuals = 0;
    UINT32  thisVisual = 0;

    UINT32  numFonts = 0;
    UINT32  thisFont = 0;

    UINT32  numImages = 0;
    UINT32  thisImage = 0;

    XPS_OBJECT_TYPE  visualType;
 
    // package points to the IXpsOMPackage interface to walk.

    // Get the fixed document sequence of the package.
    hr = package->GetDocumentSequence(&docSeq);

    // Get the fixed documents in the fixed document sequence.
    hr = docSeq->GetDocuments(&docs);

    // Walk the collection of documents.
    hr = docs->GetCount(&numDocs);
    thisDoc = 0;
    while (thisDoc < numDocs) {
        hr = docs->GetAt(thisDoc, &doc);
        
        // Get the doc contents.
        hr = doc->GetPageReferences(&pages);
        
        // Walk the collection of page references
        hr = pages->GetCount(&numPageRefs);
        thisPageRef = 0;
        while (thisPageRef < numPageRefs) {
            // Get this page reference.
            hr = pages->GetAt(thisPageRef, &pageRef);

            // Get the page content of this page reference.
            {
                hr = pageRef->GetPage (&page);

                // Get the visual tree of this page.
                hr = page->GetVisuals (&visuals);
                
                // Walk the visuals.
                hr = visuals->GetCount (&numVisuals);
                thisVisual = 0;
                while (thisVisual < numVisuals) {
                    hr = visuals->GetAt (thisVisual, &visual);
                    // Get visual type.
                    hr = visual->GetType( &visualType );
                    
                    // Do other stuff with the visual.

                    // Release the visual.
                    if (NULL != visual) {visual->Release(); visual = NULL;}
                    thisVisual++; // Get next visual in collection.
                }
                if (NULL != visuals) {visuals->Release(); visuals = NULL;}
                if (NULL != page) {page->Release(); page = NULL;}
            }
            // Get the part resources used by this page.
            hr = pageRef->CollectPartResources (&pageParts);

            // Get the font resources.
            {
                hr = pageParts->GetFontResources (&fonts);
                
                // Walk the fonts.
                hr = fonts->GetCount (&numFonts);
                thisFont = 0;
                while (thisFont < numFonts) {
                    hr = fonts->GetAt(thisFont, &font);
                    if (NULL != font) {font->Release(); font = NULL;}

                    thisFont++; // Get the next font in collection.
                }
                if (NULL != fonts) {fonts->Release(); fonts = NULL;}
            }

            // Get the image resources.
            {
                hr = pageParts->GetImageResources (&images);

                // walk the images
                hr = images->GetCount (&numImages);
                thisImage = 0;
                while (thisImage < numImages) {
                    hr = images->GetAt(thisImage, &image);
                    thisImage++;
                    if (NULL != image) {image->Release(); image = NULL;}
                }
                if (NULL != images) {images->Release(); images = NULL;}
            }
            if (NULL != pageRef) {pageRef->Release(); pageRef = NULL;}
            thisPageRef++; // Get next page in doc.
        }
        if (NULL != pages) {pages->Release(); pages = NULL;}
        if (NULL != doc) {doc->Release(); doc = NULL;}
        thisDoc++; // Get next doc in collection.
    }

    // Release interface pointers.
    if (NULL != docs) docs->Release();
    if (NULL != docSeq) docSeq->Release();

```



## <a name="related-topics"></a><span data-ttu-id="4ef67-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="4ef67-145">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4ef67-146">**後續步驟**</span><span class="sxs-lookup"><span data-stu-id="4ef67-146">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="4ef67-147">將文字寫入至 XPS OM</span><span class="sxs-lookup"><span data-stu-id="4ef67-147">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="4ef67-148">在 XPS OM 中繪製圖形</span><span class="sxs-lookup"><span data-stu-id="4ef67-148">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="4ef67-149">以 XPS OM 放置影像</span><span class="sxs-lookup"><span data-stu-id="4ef67-149">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="4ef67-150">**用於此頁面**</span><span class="sxs-lookup"><span data-stu-id="4ef67-150">**Used in This Page**</span></span>
</dt> <dt>

[<span data-ttu-id="4ef67-151">**IXpsOMDocument**</span><span class="sxs-lookup"><span data-stu-id="4ef67-151">**IXpsOMDocument**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)
</dt> <dt>

[<span data-ttu-id="4ef67-152">**IXpsOMDocumentCollection**</span><span class="sxs-lookup"><span data-stu-id="4ef67-152">**IXpsOMDocumentCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)
</dt> <dt>

[<span data-ttu-id="4ef67-153">**IXpsOMDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="4ef67-153">**IXpsOMDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[<span data-ttu-id="4ef67-154">**IXpsOMFontResource**</span><span class="sxs-lookup"><span data-stu-id="4ef67-154">**IXpsOMFontResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource)
</dt> <dt>

[<span data-ttu-id="4ef67-155">**IXpsOMFontResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="4ef67-155">**IXpsOMFontResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresourcecollection)
</dt> <dt>

[<span data-ttu-id="4ef67-156">**IXpsOMImageResource**</span><span class="sxs-lookup"><span data-stu-id="4ef67-156">**IXpsOMImageResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource)
</dt> <dt>

[<span data-ttu-id="4ef67-157">**IXpsOMImageResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="4ef67-157">**IXpsOMImageResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresourcecollection)
</dt> <dt>

[<span data-ttu-id="4ef67-158">**IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="4ef67-158">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[<span data-ttu-id="4ef67-159">**IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="4ef67-159">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="4ef67-160">**IXpsOMPageReference**</span><span class="sxs-lookup"><span data-stu-id="4ef67-160">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[<span data-ttu-id="4ef67-161">**IXpsOMPageReferenceCollection**</span><span class="sxs-lookup"><span data-stu-id="4ef67-161">**IXpsOMPageReferenceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)
</dt> <dt>

[<span data-ttu-id="4ef67-162">**IXpsOMVisual**</span><span class="sxs-lookup"><span data-stu-id="4ef67-162">**IXpsOMVisual**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)
</dt> <dt>

[<span data-ttu-id="4ef67-163">**IXpsOMVisualCollection**</span><span class="sxs-lookup"><span data-stu-id="4ef67-163">**IXpsOMVisualCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)
</dt> <dt>

<span data-ttu-id="4ef67-164">**詳細資訊**</span><span class="sxs-lookup"><span data-stu-id="4ef67-164">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="4ef67-165">初始化 XPS OM</span><span class="sxs-lookup"><span data-stu-id="4ef67-165">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="4ef67-166">將 XPS 檔讀入 XPS OM</span><span class="sxs-lookup"><span data-stu-id="4ef67-166">Read an XPS Document into an XPS OM</span></span>](read-an-xps-document-into-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="4ef67-167">建立空白的 XPS OM</span><span class="sxs-lookup"><span data-stu-id="4ef67-167">Create a Blank XPS OM</span></span>](create-a-blank-xps-om.md)
</dt> <dt>

[<span data-ttu-id="4ef67-168">封裝 API</span><span class="sxs-lookup"><span data-stu-id="4ef67-168">Packaging API</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="4ef67-169">XPS 檔 API 參考</span><span class="sxs-lookup"><span data-stu-id="4ef67-169">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="4ef67-170">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="4ef67-170">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

