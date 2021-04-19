---
description: 檔介面可讓您存取 XPS 封裝元件，以在 XPS OM 中判斷檔的結構。
ms.assetid: 3302d164-81ad-4198-a116-f967e7a14147
title: XPS OM 檔介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc191c4c0b8ec5571331022321a8ae829587022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996668"
---
# <a name="xps-om-document-interfaces"></a>XPS OM 檔介面

檔介面可讓您存取 XPS 封裝元件，以在 XPS OM 中判斷檔的結構。 下表列出檔介面。



| 介面名稱                                                      | 邏輯子介面                                      | Description                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> | [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/>           | 代表在已排序清單中系結在一起的一組檔。<br/> 子介面會收集在 [**IXpsOMDocumentCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection) 介面中。<br/>                                                                                                                                                                                                  |
| [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/>                 | [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/> | 代表單一 FixedDocument 元件，並將檔中頁面的頁面參考集合系結在一起。<br/> 子介面會收集在 [**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) 介面中。<br/> 檔結構會公開在 [**IXpsOMDocumentStructureResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource) 介面中。<br/> |
| [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/>       | [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/>                   | 檔中頁面的輕量虛擬化版本。 頁面參考描述頁面的核心特性 (例如其維度) 但不包含任何頁面的內容。<br/>                                                                                                                                                                                             |
| [**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)<br/>     | 無<br/>                                               | 以超連結為目標的頁面物件集合。<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**IXpsOMPartResources**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)<br/>       | 無<br/>                                               | 與頁面相關聯之部分資源的集合。<br/>                                                                                                                                                                                                                                                                                                                                |



 

## <a name="contents"></a>目錄

-   使用[IXpsOMDocumentSequence 介面](working-with-xpsomdocumentsequence-interfaces.md)包含使用下列介面的相關資訊：
    -   [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
    -   [**IXpsOMDocumentCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)
-   使用[IXpsOMDocument 介面](working-with-xpsomdocument-interfaces.md)包含使用下列介面的相關資訊：
    -   [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)
    -   [**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)
    -   [**IXpsOMDocumentStructureResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource)
-   使用[IXpsOMPageReference 介面](working-with-xpsompagereference-interfaces.md)包含使用下列介面的相關資訊：
    -   [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
    -   [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
    -   [**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)
    -   [**IXpsOMPartResources**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)

 

 




