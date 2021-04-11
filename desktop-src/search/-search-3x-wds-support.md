---
description: .
ms.assetid: 378e346b-2067-484f-85e9-76673a35550b
title: Windows Search 中的通知處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c7dd37979eab7ef32a5a8917ba6a3589e976105
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112469"
---
# <a name="notifications-process-in-windows-search"></a>Windows Search 中的通知處理

本主題的組織方式如下：

-   [通知流程的總覽](#overview-of-the-notifications-process)
-   [爬](#crawls)
-   [索引子管理的通知](#indexer-managed-notifications)
-   [提供者管理的通知](#provider-managed-notifications)
-   [資料列集的通知](#notifications-on-rowsets)
-   [相關主題](#related-topics)

## <a name="overview-of-the-notifications-process"></a>通知流程的總覽

有三種方法可將資料存放區中的資料編制索引：

-   爬
-   索引子管理的通知
-   提供者管理的通知

下列各節將說明每個方法的優點。

## <a name="crawls"></a>爬

啟用通知的來源會在啟動時進行累加式編目，然後依賴通知或明確的命令來再次編目。 這會在 Windows Vista 和更新版本上自動發生。 在 Windows Vista 之前的作業系統上，您必須在 [工作排程器](../taskschd/task-scheduler-start-page.md) 中設定已排程的事件，以呼叫您的程式碼，以起始 (s) 的起始頁編目。 您不需要執行任何形式的通知。 在背景進程中，索引子會取得其編目範圍、尋找變更和更新目錄。 在幾乎所有情況下，建議使用這個選項。

## <a name="indexer-managed-notifications"></a>Indexer-Managed 通知

利用索引子管理的通知，您可以執行通知策略，以在資料存放區中的資料已變更時通知索引子，而索引子會管理追蹤通知和編制資料索引。 在這種情況下，您的元件 (我們將呼叫通知提供者) 監視資料存放區、收集儲存變更的相關資訊，然後使用需要編制索引的專案清單定期通知索引子。 索引子會負責復原和解決失敗時的通知。 這個選項（您可以將它視為「傳送它並忘記密碼」策略）可減少索引子編目的頻率。

## <a name="provider-managed-notifications"></a>Provider-Managed 通知

透過提供者管理的通知，您可以執行類似于第二個方法的通知策略，不同之處在于您的通知提供者必須追蹤通知，並負責在發生失敗時復原和解決通知。 在此情況下，您的通知提供者會監視資料存放區、收集和維護存放區變更的相關資訊、定期通知索引子，其中包含需要編制索引的專案清單、接收來自索引子的狀態更新，並在發生失敗時重新傳送通知。

> [!Note]  
> 除非您預期資料存放區的累加式編目會大幅降低效能，而且您需要更細微地控制或深入瞭解索引狀態，否則 **不建議使用** 此選項。

 

## <a name="notifications-on-rowsets"></a>資料列集的通知

在 Windows 7 和更新版本中，索引編制事件可讓提供者接收其資料列集的通知。 使用索引編制事件的提供者可以用類似實際檔案系統位置行為的方式來維護其資料列集。 程式庫和搜尋是 Windows 7 中非檔案系統位置的主要範例。 索引子事件就是程式庫視圖，因為通知是檔案資料夾的視圖。 必須執行 [**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents) 介面，才能接收事件的通知。 資料層是索引子事件的主要用戶端，並決定要如何處理 Items View UI 中的事件。 如需詳細資訊，請參閱 [在 Windows 7 中編制優先順序和資料列集事件的索引](indexing-prioritization-and-rowset-events.md)。

相反地，在 Windows Vista 中，以查詢為基礎的視圖沒有相關聯的事件，但檔案屬性編輯的 Shell 快取除外。 當您執行搜尋時，傳回的結果是靜態的。 因此，如果您的系統中新增了與搜尋字詞相符的另一份檔，則您的 view 不會更新為包含新的新增專案。 這是靜態 web 型結果的標準行為。 但是，當您嘗試在儲存位置上提供以查詢為基礎的視圖時，靜態結果較不容易接受。 使用者預期索引子的內容是最新的。 如需詳細資訊，請參閱 [通知索引的變更](-search-3x-wds-notifyingofchanges.md)。 如需參考檔，請參閱 [通知介面](-search-notifications-interfaces-entry-page.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Search 中的編制索引、查詢和通知](-search-3x-wds-included-in-index.md)
</dt> <dt>

[索引中包含的內容](-search-indexing-process-overview.md)
</dt> <dt>

[Windows Search 中的編制索引進程](-search-indexing-process-overview.md)
</dt> <dt>

[在 Windows Search 中查詢進程](querying-process--windows-search-.md)
</dt> <dt>

[URL 格式設定需求](url-formatting-requirements.md)
</dt> </dl>

 

 
