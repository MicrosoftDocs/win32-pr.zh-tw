---
description: 描述 WsdCodeGen 設定檔。
ms.assetid: 6dc340db-221e-4389-ba76-9f189f91866b
title: WsdCodeGen 設定檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8c252c5361fda411e2b7eca4f906ba92085a552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114836"
---
# <a name="wsdcodegen-configuration-file"></a>WsdCodeGen 設定檔

WsdCodeGen 設定檔通常是由 WsdCodeGen 工具所產生。 您可以手動建立設定檔，但是檔案的複雜度和長度通常會無法手動編碼。 我們強烈建議使用 WsdCodeGen 來產生檔案。 如需產生設定檔的詳細資訊，請參閱 [使用 WsdCodeGen](using-wsdcodegen.md) 和 [WsdCodeGen 命令列語法](wsdcodegen-command-line-syntax.md)。

您應該檢查產生的設定檔，並視需要加以修改，然後再使用它來建立原始程式碼。 WsdCodeGen 產生的設定檔通常已足以進行大部分的用戶端開發。

若要使用設定檔進行伺服器開發，需要進行一些修改。 如果已啟用裝載 (亦即，如果選取了 [全部] 或 [主機] 模式) ，請視需要修改 [**ThisModelMetadata**](thismodelmetadata.md) 元素和其子項目的內容。 此外，請視需要 [**修改或移除 ThisModelMetadata 元素或裝載**](hosted.md)專案內的 [**PnPXDeviceCategory**](/windows/desktop/WsdApi/pnpxdevicecategory)、 [**PnPXHardwareId**](pnpxhardwareid.md)和 [**PnPXCompatibleId**](/windows/desktop/WsdApi/pnpxcompatibleid)元素。

設定檔是由一系列的元素所組成，這些專案會提供產生程式碼的輸入資料，後面接著任意數量的 [**檔案元素，**](file.md) 以描述要產生的檔案。 輸入資料包含一些全域屬性，以及以 WSDL、XSD 和 managed 元件表示之類型的參考。 **File** 元素中的 TEXT 和 CDATA 會寫入產生的檔案，而不需要修改。 在產生的 **檔案中，** 會使用產生的程式碼來取代檔案元素中的其他元素。

XML 設定檔必須遵循一些一般規則，才能正確地格式化以搭配程式碼產生器公用程式使用。 這些警告是：

-   任何設定檔的根項目都是 [**wsdCodeGen**](wsdcodegen.md)。

-   包含單一資料型別的元素可與屬性交換。 例如：

    ``` syntax
    <wsdCodeGen>
        <layerNumber>1</layerNumber>
    </wsdCodeGen>
    ```

    相當於：

    ``` syntax
    <wsdCodeGen layerNumber="1"/>
    ```

-   一般情況下，專案的順序沒有限制。 例如：

    ``` syntax
    <wsdCodeGen>
        <layerNumber>1</layerNumber>
        <layerPrefix>MEDIA_</layerPrefix>
    </wsdCodeGen>
    ```

    相當於：

    ``` syntax
    <wsdCodeGen>
        <layerPrefix>MEDIA_</layerPrefix>
        <layerNumber>1</layerNumber>
    </wsdCodeGen>
    ```

    不過，程式碼產生器會處理單一階段中的設定檔，而排序的確有一些相關性。 例如，產生與特定埠類型相關之程式碼的檔案 [**元素，必須**](file.md) 出現在指示程式碼產生器讀取埠類型合約的元素之後。

如需 WsdCodeGen 設定檔中使用之元素的完整清單，請參閱 [WsdCodeGen 設定檔 XML 參考](wsdcodegen-configuration-file-xml-reference.md)。

範例設定檔包含在 Windows SDK 中。 如需詳細資訊，請參閱 [WSDAPI 範例](wsdapi-samples.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 WsdCodeGen](about-wsdcodegen.md)
</dt> <dt>

[WSDAPI 範例](wsdapi-samples.md)
</dt> </dl>

 

 
