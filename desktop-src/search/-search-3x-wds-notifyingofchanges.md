---
description: 藉由使用通知 Api 元件，可通知索引子已變更、移動或刪除專案，並可將搜尋範圍新增至需要編制索引之 Url 的 Windows Search 索引子佇列。
ms.assetid: 817550e2-a256-48d5-9fa6-1ea04f8b8589
title: '通知索引變更 (Windows Search) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a89112da20c4010e1fc23fab16778309195d20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112485"
---
# <a name="notifying-the-index-of-changes-windows-search"></a>通知索引變更 (Windows Search) 

藉由使用通知 Api 元件，可通知索引子已變更、移動或刪除專案，並可將搜尋範圍新增至需要編制索引之 Url 的 Windows Search 索引子佇列。

元件可以通知 Windows Search 索引子，其存放區中的資料已變更。 一般而言，您可以依賴索引子的排程編目。 不過，若要將通知提供給索引子，可以藉由確保索引子不會對增量索引的整個存放區進行編目，來改善效能。 例如，如果您預期您的資料存放區相當大且/或非常忙碌，例如電子郵件資料存放區，則建議您這樣做。

-   [執行索引子管理的通知](#implementing-indexer-managed-notifications)
    -   [通知佇列](#notifications-queue)
    -   [ISearchPersistentItemsChangedSink](#isearchpersistentitemschangedsink)
-   [執行提供者管理的通知](#implementing-provider-managed-notifications)
    -   [通知佇列](#notifications-queue)
    -   [ISearchItemsChangedSink](#isearchitemschangedsink)
    -   [ISearchNotifyInlineSite](#isearchnotifyinlinesite)
-   [其他資源](#additional-resources)
-   [相關主題](#related-topics)

## <a name="implementing-indexer-managed-notifications"></a>執行索引子管理的通知

索引子管理的通知可讓您控制資料存放區的存取權，同時讓您能夠在整個編制索引過程中維護通知佇列。 您的通知提供者必須監視對資料存放區所做的變更，並建立通知佇列。 您的提供者會定期將一批變更通知傳送至索引子。 當索引子收到您的通知時，它會傳回確認，而且您可以從佇列中移除 () 的專案。 如果您在一段時間後未收到通知，您可以重新傳送通知。 如果發生失敗，索引子會重建其內部佇列的專案，以編目或執行存放區的增量編目。

若要執行索引子管理的通知，您需要執行下列動作：

-   用於監視資料存放區中變更的機制。
-   用來將資訊排入佇列的資料結構 (多個 [**搜尋 \_ 專案 \_ 持續 \_ 變更**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_persistent_change) 結構) 這些變更。
-   [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink) 介面，將您的通知傳送至索引子，並從索引子取得通知通知。

### <a name="notifications-queue"></a>通知佇列

您必須監視並將資料存放區中的每個變更排入佇列，以傳送至索引子作為通知。 您要排入佇列的通知數目，以及將它們傳送至索引子的頻率，取決於您的情況。 您可能會針對每隔 *n* 次的變更或在某個 *t* 時間間隔之後，或在其中兩者的組合，傳送一批通知。

索引子預期通知會出現在 [**搜尋 \_ 專案 \_ 持續 \_ 變更**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_persistent_change) 結構的陣列中，因此您可以選擇以同樣的方式來執行您的佇列。

### <a name="isearchpersistentitemschangedsink"></a>ISearchPersistentItemsChangedSink

若要存取此介面，您必須先具現化 [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) 物件，以取得 [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) 物件的存取權。 從該 **ISearchCatalogManager** 物件，您可以具現化 [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink) 物件，並使用 **OnItemsChanged** 方法的呼叫來通知索引子資料變更。

在呼叫這個方法時，您會包含要報告的變更數目，以及 [**搜尋 \_ 專案 \_ 持續性 \_ 變更**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_persistent_change) 結構的陣列。 您會取得 HR 完成代碼的陣列，指出是否接受每個 URL 來編制索引。 這是您從索引子收到的確認。

## <a name="implementing-provider-managed-notifications"></a>執行提供者管理的通知

提供者管理的通知可讓您控制資料存放區的存取權，並在更新 Windows Search 目錄時監視索引子的進度。 您的提供者必須監視對資料存放區所做的變更，並建立通知佇列。 您的提供者會定期將一批變更通知傳送至索引子。 當索引子收到通知時，它會傳回確認。 如果您在一段時間後未收到通知，您可以重新傳送通知。 當索引子編目資料存放區，並更新 Windows Search 目錄時，它會通知您每個目錄更新的提供者，而且您可以從佇列中移除 (s) 的專案。 您的提供者會在此程式中維護其通知佇列，如果發生失敗，您可以重新傳送通知給索引子。

若要執行提供者管理的通知，您需要執行下列動作：

-   用於監視資料存放區中變更的機制。
-   用來將資訊排入佇列的資料結構 (多個 [**搜尋 \_ 專案 \_ 變更**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_change) 結構) 這些變更的相關資訊。
-   [**ISearchItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchitemschangedsink) 介面，將您的通知傳送至索引子，並從索引子取得通知通知。
-   [**ISearchNotifyInlineSite**](/windows/desktop/api/Searchapi/nn-searchapi-isearchnotifyinlinesite) 介面，以接收有關索引狀態的更新。

### <a name="notifications-queue"></a>通知佇列

您必須監視並將資料存放區中的每個變更排入佇列，以傳送至索引子作為通知。 您要排入佇列的通知數目，以及將它們傳送至索引子的頻率，取決於您的情況。 您可能會針對每隔 *n* 次的變更或在某個 *t* 時間間隔之後，或在其中兩者的組合，傳送一批通知。

索引子預期通知會出現在 [**搜尋 \_ 專案 \_ 變更**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_change) 結構的陣列中，因此您可以選擇以類似的方式儲存變更資訊。 不過，您也必須能夠比對您傳送的通知和索引子所傳回的更新。 您可能也想要能夠偵測取得通知所需的時間，以便您可以決定是否要重新傳送通知。

### <a name="isearchitemschangedsink"></a>ISearchItemsChangedSink

若要存取此介面，您必須先具現化 [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) 物件，以取得 [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) 物件的存取權。 從該 **ISearchCatalogManager** 物件，您可以具現化 [**ISearchItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchitemschangedsink) 物件，並使用 **OnItemsChanged** 方法的呼叫來通知索引子資料變更。

在呼叫這個方法時，您會包含要報告的變更數目，以及 [**搜尋 \_ 專案 \_ 變更**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_change) 結構的陣列。 您會取得代表每個變更的索引子指派 Docid 陣列，以及一組 HR 完成代碼陣列，指出是否接受每個 URL 來編制索引。 這是來自索引子的通知，指出它已收到您的通知，且正在準備索引項目目。

從這個位置開始，索引子會使用 [**ISearchNotifyInlineSite**](/windows/desktop/api/Searchapi/nn-searchapi-isearchnotifyinlinesite) 介面來傳送更新。

### <a name="isearchnotifyinlinesite"></a>ISearchNotifyInlineSite

若要取得您的專案和目錄之狀態的更新，您必須向索引子註冊 [**ISearchNotifyInlineSite**](/windows/desktop/api/Searchapi/nn-searchapi-isearchnotifyinlinesite) 介面，讓它可以將您的回呼傳送給您。 使用 [**ISearchNotifyInlineSite：： OnItemIndexedStatusChange**](/windows/desktop/api/Searchapi/nf-searchapi-isearchnotifyinlinesite-onitemindexedstatuschange) 所傳送的每個更新都會依 DocId 來識別專案，每個專案的狀態 ([**搜尋 \_ 專案 \_ 編制索引 \_ 狀態**](/windows/desktop/api/Searchapi/ns-searchapi-search_item_indexing_status)) 和編制索引階段 ([**搜尋 \_ 索引 \_ 階段**](/windows/desktop/api/Searchapi/ne-searchapi-search_indexing_phase)) 專案所在。

您不只會收到每個專案狀態的更新，如先前所述，您也會取得有關目錄本身狀態的重要資訊。 終端使用者、協力廠商應用程式或其他失敗可能會中斷或重新開機 Windows Search 服務。 發生這種情況時，您需要一種方式來判斷要 repush 至索引子的通知。

Windows Search 服務所呼叫的 [**ISearchNotifyInlineSite：： OnCatalogStatusChange**](/windows/desktop/api/Searchapi/nf-searchapi-isearchnotifyinlinesite-oncatalogstatuschange) 方法會使用下表所述的參數，通知用戶端有關目錄的狀態。



| 參數                 | Description                                                                                                                                           |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| guidCatalogResetSignature | 代表目錄重設的 GUID。 如果此 GUID 有所變更，則必須重新傳送所有的通知。                                                        |
| guidCheckPointSignature   | GUID，表示最後還原的檢查點。 如果此 GUID 有所變更，則必須重新傳送上次儲存的檢查點之後累積的所有通知。 |
| dwLastCheckPointNumber    | 表示已儲存最後一個檢查點的數位。                                                                                                        |



 

 

當發生類別目錄檢查點時，搜尋服務會更新 *dwLastCheckPointNumber*，而在該檢查點之前傳送的所有通知都是安全且可在發生服務失敗時復原的。 通知提供者只需要追蹤在類別目錄還原或重設時，檢查點和 repush 之間傳送的通知。

如果發生目錄還原，搜尋服務會將目錄回復到最後儲存的檢查點，並更新 *guidCheckPointSignature*。 在這種情況下，通知提供者必須 repush 由 *dwLastCheckPointNumber* 所識別的最新儲存檢查點以來累積的所有通知。

如果應該重設目錄，搜尋服務會重設整個目錄，並更新 *guidCatalogResetSignature*。 通知提供者必須再次 repush 其整個編目範圍。

## <a name="additional-resources"></a>其他資源

-   如需索引編制程式的總覽，請參閱 [索引](-search-indexing-process-overview.md)程式。
-   如需目錄管理員和目錄搜尋管理員 (CSM) 的總覽，請參閱 [使用目錄管理員](-search-3x-wds-mngidx-catalog-manager.md) 以及 [使用編目範圍管理員](-search-3x-wds-extidx-csm.md)。
-   如需建立 Shell 資料存放區的詳細資訊，請參閱 [執行基本資料夾物件介面](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85))。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[開發通訊協定處理常式](-search-3x-wds-phaddins.md)
</dt> <dt>

[瞭解通訊協定處理常式](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[新增圖示和快顯功能表](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[程式碼範例：通訊協定處理常式的 Shell 擴充功能](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[安裝和註冊通訊協定處理常式](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[建立通訊協定處理常式的搜尋連接器](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[偵錯工具通訊協定處理常式](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
