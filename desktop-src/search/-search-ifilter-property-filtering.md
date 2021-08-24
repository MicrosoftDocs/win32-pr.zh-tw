---
description: 您可以使用已註冊的屬性處理常式，或使用針對特定檔案類型註冊的篩選，從專案中解壓縮屬性。 篩選處理常式 (IFilter 介面的執行) 可以用任意數量的方式解讀檔案類型的內容。
ms.assetid: 6701d151-c36f-43e5-929b-9831c5ce5823
title: 從篩選處理常式傳回屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b1842710af65e22f5a730891ea6e7f32053b92212f8c3ad4c5f0f68f23578d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594850"
---
# <a name="returning-properties-from-a-filter-handler"></a>從篩選處理常式傳回屬性

您可以使用已註冊的屬性處理常式，或使用針對特定檔案類型註冊的篩選，從專案中解壓縮屬性。 篩選處理常式 ([**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面的執行) 可以用任意數量的方式解讀檔案類型的內容。

本主題的組織方式如下：

- [屬性篩選](#returning-properties-from-a-filter-handler)
  - [屬性大小限制](#property-size-limitations)
- [其他資源](#additional-resources)
- [相關主題](#related-topics)

## <a name="property-filtering"></a>屬性篩選

下表列出屬性篩選的最佳作法。

| 方法                                                | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IFilter：： Init**](/windows/win32/api/filter/nf-filter-ifilter-init)      | 傳回 [**IFILTER \_ 旗標**](/windows/win32/api/filter/ne-filter-ifilter_flags) 列舉。 如果此列舉的 *IFILTER \_ 旗標 \_ OLE \_ 屬性* 成員設定為一個，則 Windows Search 會使用 [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage)和 [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage)介面介面來列舉和存取外部數值型別屬性。 |
| [**IFilter：： GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) | 從具有區塊類型 (文字或值) 、名稱和地區設定的「區塊」中的檔傳回信息。 區塊包含一個 document 屬性。                                                                                                                                                                                                                                                                                                      |
| [**IFilter：： GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext)   | 從區塊取得文字型別屬性。                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**IFilter：： GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) | 從區塊取得數值型別屬性。                                                                                                                                                                                                                                                                                                                                                                                                        |

下圖顯示範例檔。 外部實數值型別屬性 `DocTitle` (使用 [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) 和 [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) 介面的方法取得) 和內部實數值型別屬性 `Book` (取得作為自訂 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 執行的結果，) 描述整份檔。 文字類型屬性 `Contents` 和 `Chapter` 描述檔的內容。 處理此檔時，篩選處理常式 (**IFilter** 介面的執行) 識別和解壓縮這些屬性。

![顯示一般檔元素的圖表](images/ifilterpropertyextraction.png)

### <a name="property-size-limitations"></a>屬性大小限制

屬性大小有兩個可能的限制：

- Windows Search 接受每個檔案的資料大小上限。
- 屬性描述檔案中定義之每個屬性的大小上限。

目前，Windows Search 在計算從專案接受的資料量時，不會使用已定義的屬性大小。 相反地，Windows Search 使用的限制是檔案大小的產品，而 (的檔案 `MaxGrowFactor` 大小 N \* MaxGrowFactor) 從登錄中讀取。 預設值 `MaxGrowFactor` 為四。

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Gathering Manager
            MaxGrowFactor
```

因此，如果您的檔案類型通常較小，但具有較大的屬性，Windows Search 可能不會接受您要發出的所有屬性資料。 不過，您可以增加 `MaxGrowFactor` 以符合您的需求。

## <a name="additional-resources"></a>其他資源

- [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)上提供的 [IFilterSample](-search-sample-ifiltersample.md)程式碼範例，示範如何建立用來執行 [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter)介面的 ifilter 基礎類別。
- 如需索引編制程式的總覽，請參閱 [索引](-search-indexing-process-overview.md)程式。
- 如需檔案類型的總覽，請參閱 [檔案類型](../shell/fa-file-types.md)。
- 若要查詢檔案類型的檔案關聯屬性，請參閱 [PerceivedTypes、SystemFileAssociations 和應用程式註冊](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))。
- 如需屬性和屬性處理常式的總覽，以及可用於檔案格式的系統屬性清單，請參閱[開發 Windows Search 的屬性處理常式](-search-3x-wds-extidx-propertyhandlers.md)。

## <a name="related-topics"></a>相關主題

[開發篩選處理常式](-search-ifilter-conceptual.md)

[關於 Windows Search 中的篩選處理常式](-search-ifilter-about.md)

[在 Windows Search 中建立篩選處理常式的最佳作法](-search-3x-wds-extidx-filters.md)

[Windows 隨附的篩選處理常式](-search-ifilter-implementations.md)

[在 Windows Search 中執行篩選處理常式](-search-ifilter-constructing-filters.md)

[註冊篩選處理常式](-search-ifilter-registering-filters.md)

[測試篩選處理常式](-search-ifilter-testing-filters.md)
