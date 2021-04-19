---
description: OpenXPS 是檔的開放 XML 檔規格格式，而且是以 (ECMA) 標準規格的歐洲貨箱 maker 關聯為基礎。
ms.assetid: 52FB5B3F-BEBF-4851-8BE9-5DC7AE535313
title: OpenXPS 列印的應用程式支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914d8c365209ea3486bedd5e0352e63a8e31086f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983477"
---
# <a name="app-support-for-openxps-printing"></a>OpenXPS 列印的應用程式支援

OpenXPS 是檔的開放 XML 檔規格格式，它是以 (ECMA) 標準規格的歐洲電腦製造商關聯為基礎。

Windows 8 透過 v4 列印驅動程式模型提供完整的 OpenXPS 列印支援，並持續支援 Microsoft XPS 格式。 本主題的重點在於與 Windows 應用程式開發人員相關的這項支援的部分。 如需 OpenXPS 支援之驅動程式需求的詳細資訊，請參閱 [OpenXPS 的驅動程式支援](/windows-hardware/drivers/print/printer-driver-overview)。

## <a name="sending-xps-data-to-the-print-system"></a>將 XPS 資料傳送至列印系統

建議您使用 [**IPrintDocumentPackageTarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) 將所有 XPS 列印工作傳送至列印系統。 **IPrintDocumentPackageTarget** 可在沒有序列化的情況下，接受 XPS 物件模型 (OM) ，這有助於改善整體效能。

以下是 **IPrintDocumentPackageTarget** 介面的簡短摘要：

-   此介面支援從量身打造的解決方案和桌面應用程式進行列印。

-   針對桌面應用程式，這可以用來取代 [**StartXpsPrintJob1**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob1)。

-   適用于 Windows 7 Service Pack 1 (SP1) + Platform Update 和 Windows 8。

-   在專案中包含 *DocumentTarget* ，以使用這些 api。

使用 OpenXPS 檔的應用程式應該注意，OpenXPS 的 MIME 類型如下所示：

<dl> 應用程式 \\ .oxps  
</dl>

## <a name="sending-openxps-data-to-the-xps-print-api"></a>將 OpenXPS 資料傳送至 XPS 列印 API

在 OpenXPS 的特定情況下，XPS OM 接受 MSXPS 和 OpenXPS，並提供轉換和序列化為任一格式的方法。 這可讓應用程式開發人員在需要的情況下，與目標驅動程式無關。 這也表示應用程式開發人員可以一律將列印工作以 XPS OM 的形式提交至 StartXpsPrintJob1 或 IDocumentPackageTarget，並知道列印系統將會處理任何必要的轉換。

當然，防止 XPS 格式之間的轉換將會改善端對端的效能。 從應用程式中，開發人員可以檢查下列登錄機碼，以判斷目標列印驅動程式慣用的 XPS 格式：

``` syntax
HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Print\Printers\[PrintDriverName]\PrintDriverData\XpsFormat
```

一旦決定了慣用的 XPS 格式之後，應用程式就可以提供不需要轉換的 XPS OM 物件。 特別注意的是，在 OpenXPS 的 MSXPS 和 JPEGXR 中使用 HD 相片。 從 JPEGXR 轉換到 HD 相片相當輕量，因為這項轉換的主要差異在於，HD 相片會忽略 JPEGXR 所需的4個控制位。 不過，從 HD 相片轉換成 JPEGXR 需要重新編碼整個映射，才能產生必要的控制項位。 因此，提供高解析度映射的 JPEGXR 映射可確保與 OpenXPS 的相容性，並將 MSXPS 映射的轉換成本降至最低。

*Xpsobjectmodel \_ 1. h* 標頭會定義 OpenXPS 的其他 api 和物件。 和 IXpsOMObjectFactory1 介面會提供其他方法來進行映射轉換。 語法如下：


```C++
IXpsOMObjectFactory1->ConvertHDPhotoToJpegXR(IXpsOMImageResource *imageResource);

IXpsOMObjectFactory1->ConvertJpegXRToHDPhoto(IXpsOMImageResource *imageResource);
```



Windows 8 提供下列新的和更新的列舉。

新列舉：

<dl>

[**XPS \_ 檔 \_ 類型**](/windows/win32/api/xpsobjectmodel_1/ne-xpsobjectmodel_1-xps_document_type)  
</dl>

已更新列舉

<dl>

[**XPS \_ 映射 \_ 類型**](/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type)  
</dl>

新的 GetDocumentType 方法可讓應用程式判斷檔的 XPS 格式。 這些都可在 [**IXpsOMObjectFactory1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsomobjectfactory1)、 [**IXpsOMPackage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompackage1)和 [**IXpsOMPage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompage1)中使用。 以下是一份方法清單。

<dl>

[**IXpsOMObjectFactory1::GetDocumentTypeFromFile**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromfile)  
[**IXpsOMObjectFactory1::GetDocumentTypeFromStream**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromstream)  
[**IXpsOMPackage1：： GetDocumentType**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompackage1-getdocumenttype)  
[**IXpsOMPage1：： GetDocumentType**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompage1-getdocumenttype)  
</dl>

Windows 8 提供下列新的錯誤碼以支援 OpenXPS：

<dl> XPS \_ E 不相符 \_ \_ 的命名空間。 <dl> 如果有不相符的命名空間，就會傳回此錯誤。  
</dl> </dd> XPS\_E\_ABSOLUTE\_REFERENCE. <dl> 如果 MSXPS 在內部參考中使用絕對 Uri，或嘗試使用內部參考來序列化資料流程中的，則會傳回此錯誤。 這是因為 XPS OM 會產生相對的 Uri。 而且，雖然 MSXPS 支援相對和絕對 Uri，但 OpenXPS 需要相對的 Uri。  
</dl> </dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[OpenXPS 的驅動程式支援](/windows-hardware/drivers/print/printer-driver-overview)
</dt> <dt>

[**IPrintDocumentPackageTarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget)
</dt> <dt>

[**IXpsOMObjectFactory1::GetDocumentTypeFromFile**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromfile)
</dt> <dt>

[**IXpsOMObjectFactory1::GetDocumentTypeFromStream**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromstream)
</dt> <dt>

[**IXpsOMPackage1：： GetDocumentType**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompackage1-getdocumenttype)
</dt> <dt>

[**IXpsOMPage1：： GetDocumentType**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompage1-getdocumenttype)
</dt> <dt>

[**XPS \_ 檔 \_ 類型**](/windows/win32/api/xpsobjectmodel_1/ne-xpsobjectmodel_1-xps_document_type)
</dt> <dt>

[**XPS \_ 映射 \_ 類型**](/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type)
</dt> </dl>

 

 
