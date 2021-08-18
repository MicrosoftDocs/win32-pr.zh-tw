---
description: IXpsOMPackageWriter 介面會建立 XPS 檔檔，應用程式可以在其中寫入 XPS OM 的 IXpsOMPage 介面內容。
ms.assetid: eff1ab1e-2205-4f5c-9e32-199e073f5dbf
title: 使用 IXpsOMPackageWriter 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a4437f939821b826fa0d5c30407777b7d44c5d03c236f4ef850d52145b4f8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119098700"
---
# <a name="using-the-ixpsompackagewriter-interface"></a>使用 IXpsOMPackageWriter 介面

[**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)介面會建立 xps 檔檔，應用程式可以在其中寫入 xps OM 的 [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)介面內容。 當檔內容是依序處理或建立時， [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) 介面最有用。 與 [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)介面的 [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile)和 [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream)方法不同的是，若要使用 **IXpsOMPackageWriter** 介面，則整個 FixedDocument 或 FixedDocumentSequence 都不需要完成。

## <a name="overview"></a>概觀

[**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)介面會一次寫入一頁，從 XPS 檔的第一頁到最後一個頁面。 介面可以用來建立簡單的 XPS 檔檔案，以及在 FixedDocumentSequence 中包含多個 FixedDocument 的複雜 XPS 檔檔案。 在複雜的 XPS 檔檔中，FixedDocuments 也會依序建立，從 FixedDocumentSequence 中的第一個 FixedDocument 開始。 **IXpsOMPackageWriter** 介面不支援以隨機順序建立檔內容。 例如，您可以使用它來建立連續報告，或在設備磁碟機篩選器中執行處理，以依序將檔內容送入驅動程式。

## <a name="terminology-review"></a>術語審查

*XPS 檔* 檔是符合 XML 檔規格的開放式封裝慣例 (OPC) 套件。 因此，技術上來說， [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) 介面會建立 *opc 封裝*，但它是符合 XML 檔規格的 opc 套件。 基於這個理由，在有關 XPS 檔的討論中， *xps 檔* 和 *套件* 的條款通常會交替使用。

[**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)介面所建立的 *封裝* 將包含所需的 XPS 檔元件： FixedDocumentSequence、至少一個 FixedDocument，以及至少一個 FixedPage。 當 **IXpsOMPackageWriter** 介面具現化時，就會建立 FixedDocumentSequence。 每次呼叫 [**IXpsOMPackageWriter：： StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument) 時會建立一個 FixedDocument，每次呼叫 [**IXpsOMPackageWriter：： AddPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage) 時，就會建立一個 FixedPage。 因為介面會依序寫入檔內容，所以 **AddPage** 方法會將頁面新增至最近建立的 FixedDocument。

## <a name="using-the-ixpsompackagewriter-interface"></a>使用 IXpsOMPackageWriter 介面

下列程式描述如何使用 [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) 介面建立 XPS 檔檔。 此程式不會說明如何具現化 [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) 介面及其內容。 For more information about **IXpsOMPage** and adding content to a page, see [XPS OM Page Interfaces](xps-object-model-page-interfaces.md) and the topics listed in the See Also section.

 **建立檔**

1.  具現化 [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) 介面。

    這會在封裝中建立空的 FixedDocumentSequence。

    -   若要在檔案中建立 XPS 檔，請呼叫 [**IXpsOMObjectFactory：： CreatePackageWriterOnFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronfile)。
    -   若要在資料流程中建立 XPS 檔，請呼叫 [**IXpsOMObjectFactory：： CreatePackageWriterOnStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronstream)。

2.  藉由呼叫 [**IXpsOMPackageWriter：： StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument)，在封裝中啟動新檔。

    新增頁面之前，請呼叫 [**IXpsOMPackageWriter：： StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument) ，將 FixedDocument 新增至步驟1中建立的 FixedDocumentSequence。

3.  加入內容。
    -   若要在檔中加入新的 FixedPage，請呼叫 [**IXpsOMPackageWriter：： AddPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage)，並將指標傳遞至 [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) 介面，該介面具有您想要新增的 fixedpage 內容。
    -   若要在 FixedDocumentSequence 中建立新的 FixedDocument，請呼叫 [**IXpsOMPackageWriter：： StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument)。
4.  藉由呼叫 [**IXpsOMPackageWriter：： close**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-close)，關閉封裝和其內容。

## <a name="advanced-features"></a>進階功能

[**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)介面的方法也支援新增資源、縮圖和列印票證。 這些檔元件可以在套件、FixedDocumentSequence、FixedDocument 和 FixedPage 層級加入。 如需使用此介面進行列印的詳細資訊，請參閱 [列印 XPS OM](print-an-xps-om.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 XPS 數位簽章 API](using-digital-signatures-in-xps-documents.md)
</dt> <dt>

[XPS OM 頁面介面](xps-object-model-page-interfaces.md)
</dt> <dt>

[流覽 XPS OM](navigate-the-xps-om.md)
</dt> <dt>

[使用 XPS OM 畫布和視覺化介面](working-with-xpsomcanvas-interfaces.md)
</dt> <dt>

[使用 XPS OM 路徑介面](working-with-xps-object-model-path-interfaces.md)
</dt> <dt>

[使用 XPS OM 文字、圖形和影像介面](working-with-xps-object-model-text-and-image-interfaces.md)
</dt> <dt>

[XPS OM 列印票證介面](xps-object-model-print-ticket-interfaces.md)
</dt> <dt>

[**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator)
</dt> <dt>

[XPS 檔 API 參考](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



