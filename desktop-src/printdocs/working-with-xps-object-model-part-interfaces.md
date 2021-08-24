---
description: 本主題說明如何使用提供 XPS OM 中 XPS 檔元件存取權的介面。
ms.assetid: c52f7044-890d-47d1-83f8-bae1f8d83139
title: XPS OM 元件介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc93023f251d96f557dfc351949b58f7b9a0b67d308903d83b182de8f710e110
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823898"
---
# <a name="xps-om-part-interfaces"></a>XPS OM 元件介面

本主題說明如何使用提供 XPS OM 中 XPS 檔元件存取權的介面。



| 介面名稱                                                                                                    | 邏輯子介面                                                                                                                                                                                                                                                                                     | 描述                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**IXpsOMPart**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompart)<br/>                                                                       | [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/> [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/> [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> [**IXpsOMResource**](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomresource)<br/>    | 記錄組成檔結構的元件。<br/>                                          |
| [**IXpsOMResource**](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomresource)<br/> [**IXpsOMPartResources**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)<br/> | IXpsOMFontResource<br/> IXpsOMImageResource<br/> IXpsOMColorProfileResource<br/> IXpsOMPrintTicketResource<br/> IXpsOMRemoteDictionaryResource<br/> IXpsOMDocumentStructureResource<br/> IXpsOMStoryFragmentsResource<br/> IXpsOMSignatureBlockResource<br/> | 檔元件，其中包含在頁面或檔所使用或參考的元素。<br/> |
| [**IXpsOMPartUriCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomparturicollection)<br/>                                             | 無<br/>                                                                                                                                                                                                                                                                                              | 元件 Uri 的集合。<br/>                                                                        |



 

## <a name="code-examples"></a>程式碼範例

接下來的程式碼範例會示範兩個範例，說明如何使用元件介面來存取 XPS OM 內容。

### <a name="get-the-name-of-a-document-part"></a>取得檔元件的名稱

下列程式碼範例會導覽至檔元件，並取得元件的名稱。


```C++
    HRESULT                         hr = S_OK;
    
    IXpsOMDocumentSequence          *docSeq;
    IXpsOMDocumentCollection        *docs;
    IXpsOMDocument                  *doc;
    IXpsOMPageReferenceCollection   *pages;
    IXpsOMPageReference             *pageRef;
    IXpsOMPage                      *page;

    IOpcPartUri                     *thisDocPartUri;
    IOpcPartUri                     *thisPagePartUri;

    UINT32  numDocs = 0;
    UINT32  thisDoc = 0;

    UINT32  numPageRefs = 0;
    UINT32  thisPageRef = 0;

    // package points to the IXpsOMPackage interface to walk.

    // get the fixed document sequence of the package
    hr = package->GetDocumentSequence(&docSeq);

    // get the fixed documents in the fixed document sequence
    hr = docSeq->GetDocuments(&docs);

    // walk the collection of documents;
    hr = docs->GetCount(&numDocs);
    thisDoc = 0;
    while (thisDoc < numDocs) {
        hr = docs->GetAt(thisDoc, &doc);
        
        // get the part name (URI) of this document
        hr = doc->GetPartName ( &thisDocPartUri );

        // get the doc contents
        hr = doc->GetPageReferences(&pages);
        
        // walk the collection of page references
        hr = pages->GetCount(&numPageRefs);
        thisPageRef = 0;
        while (thisPageRef < numPageRefs) {
            // get this page reference
            hr = pages->GetAt(thisPageRef, &pageRef );

            // get the part name (URI) of this page
            hr = pageRef->GetPage (&page);
            hr = page->GetPartName ( &thisPagePartUri );

            // do something with the part name
 
            thisPagePartUri->Release();
            page->Release();
            pageRef->Release();

            thisPageRef++;
        }
        pages->Release();
        thisDocPartUri->Release();
        doc->Release();
        thisDoc++;
    }

    docs->Release();
    docSeq->Release();

```



### <a name="get-the-part-resources-that-are-associated-with-this-page"></a>取得與此頁面相關聯的元件資源

下列程式碼範例會取得此頁面所使用之不同資源的清單。


```C++
    HRESULT                                   hr = S_OK;
    IXpsOMPartResources                       *resources;

    IXpsOMColorProfileResourceCollection      *colorProfileResources;
    IXpsOMFontResourceCollection              *fontResources;
    IXpsOMImageResourceCollection             *imageResources;
    IXpsOMRemoteDictionaryResourceCollection  *dictionaryResources; 

    // pageRef contains the current page reference 
    hr = pageRef->CollectPartResources ( &resources );

    // Get pointers to each type of resource
    hr = resources->GetColorProfileResources( &colorProfileResources );
    hr = resources->GetFontResources( &fontResources );
    hr = resources->GetImageResources( &imageResources );
    hr = resources->GetRemoteDictionaryResources( &dictionaryResources );

    // use resources

    dictionaryResources->Release();
    imageResources->Release();
    fontResources->Release();
    colorProfileResources->Release();
    resources->Release();
```



 

