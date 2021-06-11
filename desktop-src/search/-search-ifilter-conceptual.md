---
description: 瞭解如何在 Windows Search 中開發篩選處理常式。 搜尋會使用篩選來將專案解壓縮，以包含在全文檢索索引中。
ms.assetid: 7b24986b-972d-4674-846b-f856b908edf4
title: 針對 Windows Search 開發篩選處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa86c0a1e41ababf6f00db72a26784beb93e1879
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988857"
---
# <a name="developing-filter-handlers-for-windows-search"></a>針對 Windows Search 開發篩選處理常式

Microsoft Windows Search 會使用篩選器來解壓縮專案的內容，以包含在全文檢索索引中。 您可以藉由撰寫篩選器來解壓縮內容，並使用屬性處理常式來解壓縮檔案的屬性，藉此擴充 Windows Search 來編制新的或專屬檔案類型的索引。

本節提供在 () 的 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面上執行篩選處理常式所需的概念架構。

- [瞭解 Windows Search 中的篩選處理常式](-search-ifilter-about.md)
- [在 Windows Search 中建立篩選處理常式的最佳作法](-search-3x-wds-extidx-filters.md)
- [從篩選處理常式傳回屬性](-search-ifilter-property-filtering.md)
- [Windows 隨附的篩選處理常式](-search-ifilter-implementations.md)
- [在 Windows Search 中執行篩選處理常式](-search-ifilter-constructing-filters.md)
- [註冊篩選處理常式](-search-ifilter-registering-filters.md)
- [測試篩選處理常式](-search-ifilter-testing-filters.md)

## <a name="additional-resources"></a>其他資源

- [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)上提供的 [IFilterSample](-search-sample-ifiltersample.md)程式碼範例會示範如何建立用來執行 [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter)介面的 ifilter 基礎類別。
- 如需索引編制程式的總覽，請參閱 [索引](-search-indexing-process-overview.md)程式。
- 如需檔案類型的總覽，請參閱 [檔案類型](../shell/fa-file-types.md)。
- 若要查詢檔案類型的檔案關聯屬性，請參閱 [PerceivedTypes、SystemFileAssociations 和應用程式註冊](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))。
