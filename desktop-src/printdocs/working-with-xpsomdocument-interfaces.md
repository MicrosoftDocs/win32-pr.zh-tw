---
description: 本主題說明提供 XPS OM 檔層級元件存取權的介面。
ms.assetid: 96b92480-cc28-4a57-a184-c52d3ddc9b05
title: 使用 IXpsOMDocument 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad7e8c0908382a731532f2697f03c8d67cb732ddf902f0c1ea181fe221d075fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033756"
---
# <a name="working-with-ixpsomdocument-interfaces"></a>使用 IXpsOMDocument 介面

本主題說明提供 XPS OM 檔層級元件存取權的介面。



| 介面名稱                                                                        | 邏輯子介面                                      | 描述                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/>                                   | [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/> | 代表單一 FixedDocument 元件，並系結頁面參考的集合。<br/> [**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) 是用來逐一查看檔中 [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) 介面的集合介面。<br/> |
| [**IXpsOMDocumentStructureResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource)<br/> | 無<br/>                                               | 代表 DocumentStructure 元件。<br/>                                                                                                                                                                                                                                                                           |



 

## <a name="code-examples"></a>程式碼範例

本章節中的程式碼範例說明如何在程式中使用一些檔介面。

### <a name="get-the-page-references-of-a-document"></a>取得檔的頁面參考

下列程式碼範例會取得 [**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)的指標，其中包含 *doc* 參數所參考檔的 [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)介面清單。


```C++
    HRESULT                               hr = S_OK;


    IXpsOMPageReferenceCollection         *pages;
    IXpsOMPageReference                   *pageRef;
    IXpsOMPage                            *page;

    UINT32  numPageRefs = 0;
    UINT32  thisPageRef = 0;

    // get the doc contents
    hr = doc->GetPageReferences(&pages);
        
    // walk the collection of page references
    hr = pages->GetCount(&numPageRefs);
    thisPageRef = 0;
    while (thisPageRef < numPageRefs) {
        // get this page reference
        hr = pages->GetAt(thisPageRef, &pageRef);

        // get the page content of this page reference
        hr = pageRef->GetPage (&page);

        // use the page

        // free this page & page reference and go to next
        page->Release();
        pageRef->Release();
        thisPageRef++;
    }

    pages->Release();
```



### <a name="get-the-document-structure-of-a-document"></a>取得檔的檔結構

下列程式碼範例會取得包含檔結構的資源。


```C++
    HRESULT                             hr = S_OK;
    
    IXpsOMDocumentStructureResource     *docStruct;
    IStream                             *docStructResStream;

    // doc is passed in as an argument
    // get the doc contents
    hr = doc->GetDocumentStructureResource(&docStruct);
   
    hr = docStruct->GetStream ( &docStructResStream );

    // access the document structure resource 
    //  contents by reading from the stream

    docStructResStream->Release();
    docStruct->Release();

```



 

 




