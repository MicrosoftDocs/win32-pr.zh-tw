---
description: 描述如何將程式中的 XPS OM 內容寫入 XPS 檔檔。
ms.assetid: 8bee8059-b901-4a99-a7e4-60dad831c239
title: 將 XPS OM 寫入 XPS 檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40f6ef79f592ad241e54e9a01fb5e4fe72cc41573e75c78f347109cdfb1c6f32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119098555"
---
# <a name="write-an-xps-om-to-an-xps-document"></a>將 XPS OM 寫入 XPS 檔

描述如何將程式中的 XPS OM 內容寫入 XPS 檔檔。

如果程式的 XPS OM 包含完整的檔，程式可以藉由呼叫 [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)介面的 [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile)方法，以 xps 檔的形式將 xps om 寫入檔案。

在程式中使用這些程式碼範例之前，請先閱讀 [一般 XPS 檔程式設計](common-xps-document-tasks.md)工作中的免責聲明。

## <a name="writing-a-complete-xps-om-to-an-xps-document"></a>將完整的 XPS OM 寫入 XPS 檔

設定 XPS OM 的內容之後，您可以藉由呼叫 [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)介面的 [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile)方法，將 XPS om 儲存為 xps 檔。


```C++
    HRESULT hr = S_OK;

    hr = xpsPackage->WriteToFile(
        fileName,
        NULL,                    // LPSECURITY_ATTRIBUTES
        FILE_ATTRIBUTE_NORMAL,
        FALSE                    // Optimize Markup Size
        );

```



> [!Note]  
> 將 XPS OM 寫入檔案或資料流程時，不會自動建立 XPS 檔的縮圖。 若要建立 XPS 檔的縮圖，請使用 [**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) 介面。

 

## <a name="incrementally-writing-an-xps-document"></a>以累加方式撰寫 XPS 檔

[**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)介面可以用來以累加方式寫入 XPS 檔的元件;例如，當檔元件依序建立或處理時。

> [!Note]  
> 將 XPS OM 寫入檔案或資料流程時，不會自動建立 XPS 檔的縮圖。 若要建立 XPS 檔的縮圖，請使用 [**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) 介面。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**後續步驟**
</dt> <dt>

[列印 XPS OM](print-an-xps-om.md)
</dt> <dt>

**在本節中使用**
</dt> <dt>

[**IOpcPartUri**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator)
</dt> <dt>

**詳細資訊**
</dt> <dt>

[初始化 XPS OM](xps-object-model-initialization.md)
</dt> <dt>

[XPS 檔 API 參考](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
