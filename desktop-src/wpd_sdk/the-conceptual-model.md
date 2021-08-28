---
description: 概念模型
ms.assetid: f906466e-acdc-4d0f-bf27-c5a25dc56c01
title: 概念模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a653d3658e0785fcc729be335fc4d648ea9bc91af676678aece0c43ce046f419
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806544"
---
# <a name="the-conceptual-model"></a>概念模型

本節說明構成 WPD 概念模型的物件、屬性和資源。

### <a name="objects"></a>物件

在 WPD 中，裝置上的邏輯實體稱為物件。 通常（但不一定）表示裝置上的資料。 物件具有屬性，並由物件識別碼參考。 物件的範例包括相機上的圖片和資料夾、媒體播放機上的歌曲和播放清單、行動電話上的連絡人等等。

物件也可以代表裝置的功能或資訊部分。 這些範例包括 player 控制項 (播放/錄製/暫停) 、攝影機設定、行動電話的 SMS 功能等等。

下列兩個主題提供兩種物件類型的範例和圖例： Image 物件和 Mediacast 物件。

### <a name="image-object"></a>Image 物件

影像物件代表靜止影像。 下圖顯示影像物件、其屬性和其資源之間的關聯性。

![顯示 wpd 物件及其屬性和資源關聯性的圖表](images/wpd-overview-figure2.gif)

如需影像物件和其屬性的詳細資訊，請參閱 [**WPD \_ 內容 \_ 類型 \_ 影像**](wpd-content-type-image.md) 主題。

### <a name="mediacast-object"></a>Mediacast 物件

Mediacast 物件可以視為將相關內容分組的容器物件，就像播放清單群組音樂一樣。 通常，Mediacast 物件是用來將線上發佈的媒體內容分組。 例如，RSS 通道可以表示為 Mediacast 物件，其物件參考指向代表通道中每個專案的內容物件。 下圖顯示 Mediacast 物件與其包含的三個音訊物件之間的關聯性。

![顯示 medicast 物件的階層式結構以及其中包含的三個物件的圖表](images/mediacast1.gif)

音訊物件的參考是在 Mediacast 物件的 [WPD \_ 物件 \_ 參考](object-properties.md) 屬性中指定。 如需有關 Mediacast 物件所支援之屬性的詳細資訊，請參閱 [**WPD \_ 內容 \_ 類型 \_ 媒體 \_ 轉換**](wpd-content-type-media-cast.md) 主題。

### <a name="properties"></a>屬性

物件屬性提供交換物件描述中繼資料的機制。 例如，影像物件可能會包含描述其檔案名、大小、格式、寬度（以圖元為單位）的屬性。

屬性具有目前的值和屬性。 WPD 會定義一組組成 API 和 DDI 定義的標準屬性。 廠商不限於預先定義的 WPD 屬性，而且可以自由新增自己的屬性。

### <a name="property-attributes"></a>Property 屬性

屬性屬性描述存取權限、有效值，以及與屬性相關的其他資訊。 例如，代表位元速率的屬性可以是每秒 8 kb 的範圍 (Kbps) 20 Kbps，且步驟值為 1 Kbps。

存取權限會指出呼叫端是否可以讀取、寫入及/或刪除屬性。 有效的值表示屬性值的限制。 有效的值會被視為特定的表單。 有效的值表單包括範圍 (也就是，屬性可以從最小到最大值使用指定的步驟) 、列舉 (也就是，屬性值是指定清單) 中的其中一個值，而無 (表示沒有任何特定的有效值) 。

### <a name="resources"></a>資源

資源是二進位資料的預留位置。 物件可以有一個以上的資源。 例如，如果物件代表具有音訊注釋的影像檔案，則此物件的資源可能如下所示：

-   預設資源。 此資源代表整個影像檔案。  (這包括任何內嵌資料，例如音訊注釋、縮圖等) 
-   縮圖資源。 此資源代表影像的縮圖資料。
-   音訊注釋資源。 此資源代表與影像相關聯的音訊資料。

### <a name="resource-attributes"></a>資源屬性

與屬性屬性類似，資源屬性會描述與資源相關的存取權限、大小、格式和其他資訊。 例如，影像物件上之音訊注釋資源的屬性，可能會指定音訊的位元速率、通道計數和資料格式。

### <a name="rendering-profiles-and-resource-attributes"></a>轉譯設定檔和資源屬性

轉譯設定檔是應用程式用來探索指定資源之有效屬性的一種方法。 例如，行動電話可能會支援點陣圖具有最小和最大寬度和高度值的特定限制。 藉由查詢 bitmap 物件的轉譯設定檔，應用程式可以取出這些確切的值。

下列範例輸出會識別裝置在支援點陣圖（最小高度為10圖元、最大寬度為20圖元、最大高度為1000圖元、最大寬度為2000圖元）時所傳回的轉譯設定檔資訊。


```C++
WPD_OBJECT_FORMAT = WPD_OBJECT_FORMAT_BMP
WPD_MEDIA_HEIGHT:
        WPD_PROPERTY_ATTRIBUTE_FORM = WPD_PROPERTY_ATTRIBUTE_FORM_RANGE
        WPD_PROPERTY_ATTRIBUTE_DEFAULT_VALUE =  10
        WPD_PROPERTY_ATTRIBUTE_RANGE_MIN =  10 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MAX = 1000
        WPD_PROPERTY_ATTRIBUTE_RANGE_STEP = 1
WPD_MEDIA_WIDTH:
        WPD_PROPERTY_ATTRIBUTE_FORM = WPD_PROPERTY_ATTRIBUTE_FORM_RANGE
        WPD_PROPERTY_ATTRIBUTE_DEFAULT_VALUE =  20 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MIN =  20 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MAX =  2000
        WPD_PROPERTY_ATTRIBUTE_RANGE_STEP = 1
WPD_RESOURCE_ATTRIBUTE_TOTAL_SIZE:
        WPD_PROPERTY_ATTRIBUTE_FORM = WPD_PROPERTY_ATTRIBUTE_FORM_RANGE
        WPD_PROPERTY_ATTRIBUTE_DEFAULT_VALUE = 0
        WPD_PROPERTY_ATTRIBUTE_RANGE_MIN =  2000 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MAX = 1000000
        WPD_PROPERTY_ATTRIBUTE_RANGE_STEP = 1
```



如需應用程式如何取得轉譯配置 (檔的說明，以及相關聯的資源屬性) 的說明，請參閱程式設計指南中的如何抓取 [裝置所支援的轉譯功能](retrieving-the-rendering-capabilities-supported-by-a-device.md) 主題。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**應用程式總覽**](application-overview.md)
</dt> </dl>

 

 



