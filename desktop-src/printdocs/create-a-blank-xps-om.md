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
# <a name="create-a-blank-xps-om"></a>建立空白的 XPS OM

本主題說明如何建立空白的 XPS OM。 本文提供程式碼範例，說明如何使用 XPS OM 來建立具有一個空白頁面的 XPS 檔檔結構。

若要儲存為 XPS 檔，XPS OM 至少需要下列元件：

-   描述 XPS 檔套件的 [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
-   包含套件內容架構的 [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
-   [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument) ，其中包含封裝內檔的架構
-   包含檔中頁面集合的 [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
-   包含空白頁面的 [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)

使用這些介面時，XPS OM 將包含具有一個空白頁面的檔。 若要在 XPS OM 中建立這份檔，程式必須先建立個別的元件，然後將它們連結在一起。

使用下列程式碼範例之前，請閱讀 [一般 XPS 檔程式設計](common-xps-document-tasks.md)工作中的免責聲明。

## <a name="code-examples"></a>程式碼範例

下列程式碼範例假設初始化 [XPS OM](xps-object-model-initialization.md)中所述的初始化成功。


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



## <a name="best-practices"></a>最佳做法

使用 [**IOpcPartUri**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi) 介面建立元件之後 (例如在程式碼範例) 中呼叫 **CreateDocument** 方法之後，請釋放該介面的指標，除非您需要它來進行另一個呼叫。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**後續步驟**
</dt> <dt>

[流覽 XPS OM](navigate-the-xps-om.md)
</dt> <dt>

[將文字寫入至 XPS OM](write-text-to-an-xps-om.md)
</dt> <dt>

[在 XPS OM 中繪製圖形](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[以 XPS OM 放置影像](place-images-in-an-xps-om.md)
</dt> <dt>

**用於此頁面**
</dt> <dt>

[**IOpcPartUri**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[**IXpsOMDocumentCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)
</dt> <dt>

[**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)
</dt> <dt>

[**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)
</dt> <dt>

[**XPS \_ 大小**](/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_size)
</dt> <dt>

**詳細資訊**
</dt> <dt>

[初始化 XPS OM](xps-object-model-initialization.md)
</dt> <dt>

[封裝 API](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[XPS 檔 API 參考](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
