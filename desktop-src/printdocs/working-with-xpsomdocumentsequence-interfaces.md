---
description: 本主題說明如何使用提供 FixedDocumentSequence 存取權的介面，這是 XPS OM 中檔階層的最上層。
ms.assetid: e7d01f21-0b5d-4385-89e8-14021800e234
title: 使用 IXpsOMDocumentSequence 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f108cbadf735b334f758102915abbda239a4e974
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986986"
---
# <a name="working-with-ixpsomdocumentsequence-interfaces"></a>使用 IXpsOMDocumentSequence 介面

本主題說明如何使用提供 FixedDocumentSequence 存取權的介面，這是 XPS OM 中檔階層的最上層。



| 介面名稱                                                          | 邏輯子介面                            | Description                                                              |
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



 

 




