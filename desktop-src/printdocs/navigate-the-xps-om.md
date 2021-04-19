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
# <a name="navigate-the-xps-om"></a>流覽 XPS OM

本主題說明如何流覽 XPS OM，以及存取記憶體中檔的不同部分。

XPS 檔 API 的組織會鏡像 XPS 檔的組織。 下表說明 XPS 檔 API 介面與 XPS 檔元件的關聯性。



| XPS 檔元件                                         | XPS 檔 API 介面                                          | 要在階層中的下一個層級下呼叫的方法                                                                                       |
|----------------------------------------------------------------|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| XPS 檔檔 (包含 OPC 套件) <br/>            | [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)<br/>                   | [**GetDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-getdocumentsequence)<br/>                                                                   |
| FixedDocumentSequence 元件<br/>                          | [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> | [**GetDocuments**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocumentsequence-getdocuments)<br/>                                                                        |
| FixedDocument 元件<br/>                                  | [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/>                 | [**GetPageReferences**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocument-getpagereferences)<br/>                                                                      |
| FixedDocument 標記中的 **PageContent** 元素<br/> | [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/>       | [**GetPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage)<br/> [**CollectPartResources**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectpartresources)<br/> |
| FixedPage 部分<br/>                                      | [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/>                         | [**GetVisuals**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-getvisuals)<br/>                                                                                        |
| FixedPage 標記中的 **Canvas** 元素<br/>          | [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/>                     | [**GetVisuals**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcanvas-getvisuals)<br/>                                                                                      |
| FixedPage 標記中的 **Path** 元素<br/>            | [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/>                         | 檔階層的結尾。<br/>                                                                                                         |
| FixedPage 標記中的 **字型** 元素<br/>          | [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/>                     | 檔階層的結尾。<br/>                                                                                                         |
| 字型部分<br/>                                           | [**IXpsOMFontResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource)<br/>         | 檔階層的結尾。<br/>                                                                                                         |
| 影像元件<br/>                                          | [**IXpsOMImageResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource)<br/>       | 檔階層的結尾。<br/>                                                                                                         |



 

在您的程式中使用下列程式碼範例之前，請閱讀 [一般 XPS 檔程式設計](common-xps-document-tasks.md)工作中的免責聲明。

## <a name="code-example"></a>程式碼範例

下列程式碼範例假設已初始化的 XPS OM 存在，而且 *套件* 指向代表該 xps Om 的 [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) 介面。 如需有關建立 XPS OM 的詳細資訊，請參閱 [將 Xps 檔讀入 XPS om](read-an-xps-document-into-an-xps-om.md) 或 [建立空白的 xps om](create-a-blank-xps-om.md)。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

**後續步驟**
</dt> <dt>

[將文字寫入至 XPS OM](write-text-to-an-xps-om.md)
</dt> <dt>

[在 XPS OM 中繪製圖形](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[以 XPS OM 放置影像](place-images-in-an-xps-om.md)
</dt> <dt>

**用於此頁面**
</dt> <dt>

[**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)
</dt> <dt>

[**IXpsOMDocumentCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)
</dt> <dt>

[**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[**IXpsOMFontResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource)
</dt> <dt>

[**IXpsOMFontResourceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresourcecollection)
</dt> <dt>

[**IXpsOMImageResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource)
</dt> <dt>

[**IXpsOMImageResourceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresourcecollection)
</dt> <dt>

[**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)
</dt> <dt>

[**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)
</dt> <dt>

[**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)
</dt> <dt>

**詳細資訊**
</dt> <dt>

[初始化 XPS OM](xps-object-model-initialization.md)
</dt> <dt>

[將 XPS 檔讀入 XPS OM](read-an-xps-document-into-an-xps-om.md)
</dt> <dt>

[建立空白的 XPS OM](create-a-blank-xps-om.md)
</dt> <dt>

[封裝 API](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[XPS 檔 API 參考](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

