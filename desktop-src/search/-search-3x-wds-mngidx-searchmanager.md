---
description: ISearchManager 介面提供在目錄之間進行變更的方法。
ms.assetid: e6f4432b-03bf-4711-a79e-1bf9242c5683
title: 使用搜尋管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3e8c52211c7d69ba7a50c9a9925dad8bb84f848
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943285"
---
# <a name="using-the-search-manager"></a>使用搜尋管理員

[**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)介面提供在目錄之間進行變更的方法。 在 **ISearchManager** 層級所做的變更會全域套用至索引子所使用的所有目錄，而在 [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) 層級所做的變更則適用于特定的目錄。 不過，Windows Search 目前只使用一個目錄 SystemIndex。 您可以使用 [搜尋管理員] 執行下列動作：

- 取得搜尋目錄的目錄管理員實例。
- 取得 Windows Search 引擎的版本資訊。

[**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)介面的下列方法可協助您管理搜尋目錄 (s) ：

| 方法                                                                      | 描述                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog)                     | 依名稱取得目錄，並傳回該目錄的 [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) 實例。 這可讓您管理個別的搜尋目錄。                                          |
| [**GetIndexerVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getindexerversion)       | 以兩個整數傳回索引子的版本：主要版本和次要版本。 例如，Windows 10 搜尋的主要版本號碼為「10」，而次要版本號碼為「0」。 在 Windows XP 上的 Windows Vista 搜尋和 Windows Search 3.0 的主要版本號碼為 "3"，而次要版本號碼為 "0"。 |
| [**GetIndexerVersionStr**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getindexerversionstr) | 以字串形式傳回索引子的完整版本號碼：例如，"10.0.18309.1000"。 針對 Windows 10 這通常會符合作業系統版本號碼。 若是 Windows XP、Vista 和7，則會不同。                                                                                                                                        |


如需這些方法的詳細資訊，請參閱 [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) 檔。

下列 [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) 方法會保留供日後使用。 不過，它們會實並不會影響索引子或目錄，因為目前只有一個目錄用於 Windows Search。

- **取得 \_ BypassList**
- **取得 \_ LocalBypass**
- **取得 \_ PortNumber**
- **取得 \_ ProxyName**
- **取得 \_ UseProxy**
- **取得 \_ UserAgent**
- **put \_ UserAgent**
- **SetProxy**

**GetParameter** 和 **SetParameter** 也保留供日後使用，但不會執行。

## <a name="related-topics"></a>相關主題

[管理索引](-search-3x-wds-mngidx-overview.md)

[用於管理索引的介面](interfaces-for-managing-the-index.md)

[使用目錄管理員](-search-3x-wds-mngidx-catalog-manager.md)

[使用編目範圍管理員](-search-3x-wds-extidx-csm.md)
