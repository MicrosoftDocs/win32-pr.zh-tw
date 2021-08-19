---
description: 封裝介面代表 XPS OM 的最上層，其對應于 XPS 檔檔。
ms.assetid: 9e269b18-e5b1-4801-b8e7-473750443c6d
title: XPS OM 封裝介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6732531e3874046bbd174c363db24e304da95b9596b810014abb52a795e720c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886138"
---
# <a name="xps-om-package-interfaces"></a>XPS OM 封裝介面

封裝介面代表 XPS OM 的最上層，其對應于 XPS 檔檔。 這些介面包含將 XPS OM 序列化為 XPS 檔或資料流程的方法，並將 XPS 封裝還原序列化以建立 XPS OM，讓程式能夠存取檔的內容。



| 介面名稱                                                  | 邏輯子介面                                                                                                            | 描述                                                                                    |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)<br/>               | [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> | 與包含 XPS 檔的封裝對應的完整 XPS OM。<br/> |
| [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)<br/>   | 無<br/>                                                                                                                     | 啟用檔頁面至封裝的累加式序列化。<br/>                   |
| [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> | 無<br/>                                                                                                                     | 存取檔中繼資料。 <br/>                                                    |



 

## <a name="code-examples"></a>程式碼範例

接下來的程式碼範例將說明程式如何使用某些套件介面。 除非另有說明，否則所有的斜體專案都是參數名稱。

-   [將 XPS 檔讀入 XPS OM](#read-an-xps-document-into-an-xps-om)
-   [將 XPS OM 寫入 XPS 檔檔](#write-an-xps-om-to-an-xps-document-file)
-   [存取 XPS OM 的檔順序](#access-the-document-sequence-of-the-xps-om)
-   [存取檔的 CoreProperties](#access-the-documents-coreproperties)

### <a name="read-an-xps-document-into-an-xps-om"></a>將 XPS 檔讀入 XPS OM

從檔案名稱儲存在 *xpsDocumentFilename* 中的現有 xps 檔中，此程式碼範例會建立 *xpsPackage* 所參考的 xps OM。


```C++
    HRESULT                 hr = S_OK;
    IXpsOMPackage           *xpsPackage;

    hr = xpsFactory->CreatePackageFromFile(
        xpsDocumentFilename,
        FALSE,
        &xpsPackage);

    // xpsPackage now contains a pointer to the IXpsOMPackage
    // object that has been populated with the contents
    // of the XPS document in xpsDocumentFilename.
```



### <a name="write-an-xps-om-to-an-xps-document-file"></a>將 XPS OM 寫入 XPS 檔檔

下列程式碼範例會寫入 *xpsPackage* 所參考的 XPS OM。 此範例會在檔案中建立一份 XPS 檔，其名稱會儲存在 *檔案名* 中。


```C++
    HRESULT hr = S_OK;

    hr = xpsPackage->WriteToFile(
        xpsDocumentFilename,
        NULL,                    // LPSECURITY_ATTRIBUTES
        FILE_ATTRIBUTE_NORMAL,
        FALSE);                  // optimizeMarkupSize
```



### <a name="access-the-document-sequence-of-the-xps-om"></a>存取 XPS OM 的檔順序

下列程式碼範例會取得 [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) 介面的指標，其中包含 *xpsPackage* 所代表之 XPS OM 的檔順序。


```C++
    HRESULT                         hr = S_OK;
    IXpsOMDocumentSequence          *docSeq;
    IXpsOMDocumentCollection        *docs;

    // get the fixed document sequence of the package
    hr = xpsPackage->GetDocumentSequence(&docSeq);

    // get the collection of fixed documents in 
    //  the fixed document sequence
    hr = docSeq->GetDocuments(&docs);
```



### <a name="access-the-documents-coreproperties"></a>存取檔的 CoreProperties

下列程式碼範例會取得 [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties) 介面的指標，讓程式能夠存取 CoreProperties 元件的內容。 在此範例中，會假設檔已讀入 *xpsPackage* 所代表的 XPS OM。


```C++
    HRESULT                         hr = S_OK;
    IXpsOMCoreProperties            *coreProps;
    LPWSTR                          title;

    // get the fixed document sequence of the package
    hr = xpsPackage->GetCoreProperties(&coreProps);

    // get the title property 
    hr = coreProps->GetTitle(&title);

    // do something with the title property here...

    // free the string when finished with it
    CoTaskMemFree ( title );
    coreProps->Release();
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 IXpsOMPackageWriter 介面](using-the-ixpsompackagewriter-interface.md)
</dt> <dt>

[流覽 XPS OM](navigate-the-xps-om.md)
</dt> <dt>

[**IXpsOMDocumentSequence 介面**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[**IXpsOMPackage 介面**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[**IXpsOMPackageWriter 介面**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)
</dt> <dt>

[**IXpsOMCoreProperties 介面**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)
</dt> </dl>

 

 




