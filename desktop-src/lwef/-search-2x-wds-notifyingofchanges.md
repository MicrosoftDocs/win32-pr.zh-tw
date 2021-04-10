---
title: '通知 (舊版 Windows 環境功能的變更索引) '
description: 使用 Microsoft Windows 桌面搜尋 (WDS) 2.6，指定資料存放區的通訊協定處理常式可以在其存放區中的資料變更時，告訴 WDS 索引子。
ms.assetid: 700b1707-dd11-4a30-8f00-5c4aae1173ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6021cfe5cd7061a3d3255e56d08e665a6caedf03
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104187269"
---
# <a name="notifying-the-index-of-changes-legacy-windows-environment-features"></a>通知 (舊版 Windows 環境功能的變更索引) 

> [!NOTE]
> Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。 在之後的版本中，請改用 [Windows Search](../search/-search-3x-wds-overview.md) 。

使用 Microsoft Windows 桌面搜尋 (WDS) 2.6，指定資料存放區的通訊協定處理常式可以在其存放區中的資料變更時，告訴 WDS 索引子。 這可確保索引子不會在累加式索引上編目整個存放區，以改善效能。 使用通知 Api 時，通訊協定處理常式可以通知索引子已移動或刪除專案，而且可以將範圍新增至需要編制索引之 Url 的 WDS 索引子編目佇列。 通知對電子郵件之類的應用程式很有説明，因為通訊協定處理常式會監視存放區，並通知索引子該專案已變更且需要編制索引。

## <a name="isearchitemschangedsink"></a>ISearchItemsChangedSink

通訊協定處理常式會透過 [**ISearchItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchitemschangedsink) 介面通知索引子的變更。 您應該在搜尋 \_ 專案變更結構和搜尋類型的變更列舉型別中收集資料變更的相關資訊 \_ ，然後 \_ \_ \_ 透過 **ISearchItemsChangedSink** 介面的 **OnItemsChanged** 方法，傳達給索引子。

若要存取此介面，自訂通訊協定處理常式必須先具現化 [**ISearchManager**](/windows/desktop/api/searchapi/nn-searchapi-isearchmanager) 物件，以取得 [**ISearchCatalogManager**](/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager) 物件的存取權。 從該處，您可以具現化 [**ISearchItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchitemschangedsink) 物件，並通知索引子資料變更。

OnItemsChanged 方法可讓您收集資料變更並與客戶資料存放區進行通訊，以起始索引。



| 方向 | 變數              | 描述                                                              |
|-----------|-----------------------|--------------------------------------------------------------------------|
| 位於        | dwNumberofChanges     | 通知中的變更總數。                             |
| 位於        | DataChangeEntries\[\] | 搜尋專案的陣列中的所有變更通知都會 \_ \_ 變更結構。 |
| 外       | dwBatchId             | 將傳回錯誤的批次識別碼。                       |
| 外       | hrCompletionCodes\[\] | 指出是否接受每個 URL 來編制索引。                    |



 

搜尋 \_ 專案 \_ 變更結構會識別發生的變更種類，以及專案目前的 url 和先前的 url （如果適用）。 結構的定義如下：



| 屬性名稱 | 屬性類型                  | Description                                                                |
|---------------|--------------------------------|----------------------------------------------------------------------------|
| 變更        | 搜尋 \_ \_ 變更種類 \_       | 要通知的變更類型。                                 |
| URL           | LPWSTR                         | 已變更之物件的 URL。                                   |
| OldURL        | LPWSTR                         | 如果通知是移動，則會提供舊的 URL，而且必須是唯一的。 |
| 優先順序      | 搜尋 \_ 通知 \_ 優先順序 | 變更的優先順序。                                                |



 

\_變更列舉的搜尋種類 \_ 定義如下 \_ ：



| 列舉值                           | 值   | 描述                                                                                     |
|--------------------------------------|---------|-------------------------------------------------------------------------------------------------|
| 搜尋 \_ 變更 \_ 新增                  | 0       | 通知是針對額外的 URL。                                                      |
| 搜尋 \_ 變更 \_ 刪除               | 1       | 通知是用來刪除 URL。                                                  |
| 搜尋 \_ 變更 \_ 修改               | 2       | 通知是 URL 已經修改過了。                                               |
| 搜尋 \_ 變更 \_ 移動 \_ 重新命名         | 3       | 通知是用來將物件的移動和重新命名為新的 URL。                          |
| 搜尋 \_ 變更 \_ 語義 \_ 目錄 | 0x10000 | 通知適用于容器 URL。                                                        |
| 搜尋 \_ 變更 \_ 語義 \_ 淺層   | 0x20000 | 這項通知適用于應只將其容器屬性編制索引的容器 URL。 |
| 搜尋 \_ 變更 \_ 語義 \_ 安全性  | 0x40000 | 通知是針對已變更其安全性屬性的 URL 或容器 URL。    |



 

搜尋 \_ 通知 \_ 優先順序列舉定義如下：



| 列舉值               | 值 | 描述                                                                                                                                                                    |
|--------------------------|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 搜尋 \_ 正常 \_ 優先順序 | 0     | 索引 URL 時，應該只使用一般的優先權。 這些通知會在使用者的檔案和存放區的一般背景累加式編制索引之前進行處理。 |



 

 

 
