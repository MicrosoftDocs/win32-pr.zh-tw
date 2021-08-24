---
description: 本主題說明如何使用提供 FixedDocumentSequence 存取權的介面，這是 XPS OM 中檔階層的最上層。
ms.assetid: e7d01f21-0b5d-4385-89e8-14021800e234
title: 使用 IXpsOMDocumentSequence 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edac74809de63c1ae4e688bb99214d11b091ee4e877c921e9280abc9c6868121
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119098660"
---
# <a name="working-with-ixpsomdocumentsequence-interfaces"></a>使用 IXpsOMDocumentSequence 介面

本主題說明如何使用提供 FixedDocumentSequence 存取權的介面，這是 XPS OM 中檔階層的最上層。



| 介面名稱                                                          | 邏輯子介面                            | 描述                                                              |
|-------------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------------------------------------------|
| [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/>     | [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/> | 將一組 FixedDocuments 分組為已排序的清單。<br/>          |
| [**IXpsOMDocumentCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)<br/> | 無<br/>                                     | XPS 檔順序中的 FixedDocuments 集合。<br/> |



 

## <a name="code-example"></a>程式碼範例

下列程式碼範例會取得 [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) 介面的指標，其中包含 *xpsPackage* 所代表之 XPS OM 的檔順序。 然後，此範例會列舉集合中的檔。


```C++
    HRESULT                         hr = S_OK;

    IXpsOMDocumentSequence          *docSeq;
    IXpsOMDocumentCollection        *docs;
    IXpsOMDocument                  *doc;

    UINT32  numDocs = 0;
    UINT32  thisDoc = 0;

    // get the fixed document sequence of the package
    hr = xpsPackage->GetDocumentSequence(&docSeq);

    // get the collection of fixed documents in 
    //  the fixed document sequence
    hr = docSeq->GetDocuments(&docs);

    // walk the collection of documents;
    hr = docs->GetCount(&numDocs);
    thisDoc = 0;
    while (thisDoc < numDocs) {
        hr = docs->GetAt(thisDoc, &doc);
 
        // use this doc for something

        // release this doc and then go to the next one
        doc->Release();
        thisDoc++;
    }
    // release the document collection and
    // the document sequence
    docs->Release();
    docSeq->Release();
```



 

 




