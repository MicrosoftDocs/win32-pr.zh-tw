---
title: 關於動態資料交換
description: 本主題討論如何在應用程式之間傳輸資料。
ms.assetid: 0bcd8de4-a6f0-4f2a-8b9d-0b1b638925fb
keywords:
- 動態資料交換 (的 DDE) ，關於
- DDE (動態資料交換) ，關於
- '資料交換、動態資料交換 (DDE) '
- 動態資料交換 (DDE) ，連結至即時資料
- DDE (動態資料交換) ，連結至即時資料
- 動態資料交換 (DDE) ，建立複合檔案
- DDE (動態資料交換) ，建立複合檔案
- 動態資料交換 (DDE) 、資料查詢
- DDE (動態資料交換) 、資料查詢
- 動態資料交換 (DDE) ，範例
- DDE (動態資料交換) ，範例
- 動態資料交換 (DDE) 、模擬
- DDE (動態資料交換) ，模擬
- 動態資料交換 (的 DDE) 、訊息
- DDE (動態資料交換) 、訊息
- 動態資料交換 (DDE) 、原子
- DDE (動態資料交換) 、原子
- 動態資料交換 (DDE) 、shared memory 物件
- " (動態資料交換) 、共用記憶體物件的 DDE"
- 動態資料交換 (DDE) 、參數封裝函數
- DDE (動態資料交換) ，參數封裝函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50331a69fac11dbc6f49acdc6f3245f4a8f1da4434774ae8b2931d50f8921e1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118811977"
---
# <a name="about-dynamic-data-exchange"></a>關於動態資料交換

Windows 提供數種方法來在應用程式之間傳輸資料。 其中一個方法是使用動態資料交換 (DDE) 通訊協定。 DDE 通訊協定是一組訊息與指導方針。 它會在共用資料的應用程式之間傳送訊息，並使用共用記憶體來交換應用程式之間的資料。 應用程式可以使用 DDE 通訊協定進行單次資料傳輸，以及在有新的資料可供使用時，讓應用程式將更新傳送到另一個應用程式的連續交換。

Windows 也支援動態資料交換管理程式庫 (DDEML) 。 DDEML 是動態連結程式庫 (DLL) ，可讓應用程式用來共用資料。 DDEML 會提供函式和訊息，以簡化將 DDE 功能新增至應用程式的工作。 應用程式會使用 DDEML 函式來管理 DDE 交談，而不是直接傳送、張貼和處理 DDE 訊息。  (DDE 交談是用戶端與伺服器應用程式之間的互動。 ) 

DDEML 也提供管理 DDE 應用程式共用之字串與資料的功能。 DDE 應用程式不會使用原子和指向共用記憶體物件的指標，而是會建立和交換字串控制碼，以識別字串和資料控制碼，以識別記憶體物件。 DDEML 也可讓伺服器應用程式註冊它所支援的服務名稱。 這些名稱會廣播到系統中的其他應用程式，而這些應用程式可以使用名稱連接到伺服器。 此外，DDEML 會強制它們以一致的方式執行 DDE 通訊協定，以確保 DDE 應用程式之間的相容性。

使用以訊息為基礎之 DDE 通訊協定的現有應用程式，與使用 DDEML 的應用程式完全相容。 也就是說，使用訊息型 DDE 的應用程式可以建立交談，以及使用 DDEML 的應用程式來執行交易。 由於 DDEML 有許多優點，因此新的應用程式應該使用它，而不是使用 DDE 訊息。 若要使用 DDEML 的 API 元素，您必須在原始程式檔中包含 DDEML 標頭檔，並連結 DDEML 程式庫，並確定 DDEML 動態連結程式庫位於系統的搜尋路徑中。

本節將討論下列主題。

-   [動態資料交換通訊協定](#dynamic-data-exchange-protocol)
-   [使用 Windows 動態資料交換](#uses-for-windows-dynamic-data-exchange)
-   [從使用者的觀點來動態資料交換](#dynamic-data-exchange-from-the-users-point-of-view)
-   [動態資料交換概念](#dynamic-data-exchange-concepts)
    -   [用戶端、伺服器和對話](#client-server-and-conversation)
    -   [應用程式、主題和專案名稱](#application-topic-and-item-names)
    -   [系統主題](#the-system-topic)
    -   [永久資料連結](#permanent-data-links)
    -   [原子和共用記憶體物件](#atoms-and-shared-memory-objects)
-   [動態資料交換訊息總覽](#dynamic-data-exchange-messages-overview)
-   [動態資料交換訊息 Flow](#dynamic-data-exchange-message-flow)
-   [參數封裝函數](#parameter-packing-functions)
-   [動態資料交換和模擬](#dynamic-data-exchange-and-impersonation)

## <a name="dynamic-data-exchange-protocol"></a>動態資料交換通訊協定

因為 Windows 有以訊息為基礎的架構，所以傳遞訊息是在應用程式之間自動傳送資訊最適當的方法。 不過，訊息只會包含兩個參數 (*wParam* 和 *lParam*) 來傳遞資料。 如此一來，當應用程式之間傳遞的資訊超過幾個字組時，這些參數必須間接參考其他資料片段。 DDE 通訊協定會明確定義應用程式應該如何使用 *wParam* 和 *lParam* 參數，透過全域原子和共用記憶體控制碼來傳遞較大的資料片段。 DDE 通訊協定具有配置和刪除全域原子和共用記憶體物件的特定規則。

全域 atom 是字元字串的參考。 在 DDE 通訊協定中，原子會識別應用程式交換資料、所交換資料的本質，以及資料項目目本身。 如需原子的詳細資訊，請參閱 [關於原子](about-atom-tables.md)。

## <a name="uses-for-windows-dynamic-data-exchange"></a>使用 Windows 動態資料交換

DDE 最適合不需要進行使用者互動的資料交換。 通常，應用程式會提供方法，讓使用者在應用程式交換資料之間建立連結。 不過，一旦建立該連結，應用程式就可以交換資料，而不需要進一步的使用者介入。

您可以使用 DDE 來執行廣泛的應用程式功能，例如：

-   連結至即時資料，例如股票市場更新、科學儀器或流程式控制制。
-   建立複合檔案，例如文字處理檔，其中包含圖形應用程式所產生的圖表。 使用 DDE 時，圖表會在來源資料變更時變更，而檔的其餘部分則保持不變。
-   在應用程式之間執行資料查詢，例如試算表查詢資料庫是否有過期的帳戶。

## <a name="dynamic-data-exchange-from-the-users-point-of-view"></a>從使用者的觀點來動態資料交換

下列範例說明兩個 DDE 應用程式如何共同合作，如同從使用者的觀點來看。

試算表使用者想要使用 Microsoft Excel 來追蹤紐約股票 Exchange 上特定股票的價格。 使用者有一個稱為「報價」的應用程式，該應用程式接著可以存取 NYSE 資料。 Excel 和引號之間的 DDE 交談如下所示：

-   使用者會藉由提供應用程式的名稱 (報價) ，以提供資料和感興趣的特定主題 (NYSE) ，來起始交談。 產生的 DDE 交談會用來要求特定股票的引號。
-   Excel 將應用程式和主題名稱廣播給目前在系統中執行的所有 DDE 應用程式。 報價回應，與 NYSE 主題的相關 Excel 建立交談。
-   然後，使用者可以在資料格中建立試算表公式，要求試算表會在特定股票報價變更時自動更新。 例如，使用者可以藉由指定下列 Excel 公式： = ' Quote ' ' NYSE '，在 ZAXX 庫存的銷售價格中進行變更時，要求自動更新 \| ！ZAXX
-   使用者可以隨時終止 ZAXX 股票報價的自動更新。 另外建立的其他資料連結 (例如針對其他股票的報價) 仍會在相同的 NYSE 交談下維持使用中狀態。
-   使用者也可以終止 NYSE 主題上 Excel 和引述之間的整個交談，如此就不能在不需要起始新對話的情況下，建立該主題上的任何特定資料連結。

## <a name="dynamic-data-exchange-concepts"></a>動態資料交換概念

下列各節說明瞭解動態資料交換的重要概念和術語。

-   [用戶端、伺服器和對話](#client-server-and-conversation)
-   [應用程式、主題和專案名稱](#application-topic-and-item-names)
-   [系統主題](#the-system-topic)
-   [永久資料連結](#permanent-data-links)
-   [原子和共用記憶體物件](#atoms-and-shared-memory-objects)

### <a name="client-server-and-conversation"></a>用戶端、伺服器和對話

參與 DDE 的兩個應用程式被視為參與 DDE 交談。 起始交談的應用程式是 DDE 用戶端應用程式;回應用戶端的應用程式是 DDE 伺服器應用程式。 應用程式可以同時參與數個交談，作為某些和其他伺服器中的用戶端。

DDE 交談會在兩個視窗之間進行，每個參與的應用程式各一個視窗。 視窗可以是應用程式的主視窗;與特定檔相關聯的視窗，如同在多重文件介面中 (MDI) 應用程式;或隱藏的 (不可見的) 視窗，其唯一目的是處理 DDE 訊息。

由於 DDE 交談是由參與交談之視窗的控制碼配對所識別，因此不應該在多個視窗中與另一個視窗參與多個交談。 用戶端應用程式或伺服器應用程式必須針對每個與特定伺服器或用戶端應用程式的交談，提供不同的視窗。

應用程式可以藉由建立每個交談的隱藏視窗，來確保一組用戶端和伺服器視窗永遠不會參與多個交談。 此視窗的唯一目的是處理 DDE 訊息。

### <a name="application-topic-and-item-names"></a>應用程式、主題和專案名稱

DDE 通訊協定會識別用戶端與伺服器之間傳遞的資料單位，這些資料單位為應用程式、主題和專案名稱的三層階層。

每個 DDE 交談都是由應用程式名稱和主題唯一定義。 在 DDE 交談的開頭，用戶端和伺服器會決定應用程式名稱和主題。 應用程式名稱通常是伺服器應用程式的名稱。 例如，當 Excel 作為交談中的伺服器時，會 Excel 應用程式名稱。

DDE 主題是資料的一般分類，在交談期間 (交換) 多個資料項目。 針對在以檔案為基礎的檔上操作的應用程式，此主題通常是檔案名。 針對其他應用程式，主題是應用程式特定的名稱。

由於用戶端和伺服器視窗會一起識別 DDE 交談，因此在對話過程中，無法變更定義交談的應用程式名稱和主題。

DDE 資料項目是與應用程式之間交換的交談主旨相關的資訊。 資料項目的值可以從伺服器傳遞到用戶端，或是從用戶端傳遞至伺服器。 您可以使用任何標準剪貼簿格式或已註冊的剪貼簿格式來傳遞資料。 名為 Link 的特殊、註冊格式會識別 DDE 交談中的專案。 如需剪貼簿格式的詳細資訊，請參閱 [剪貼](clipboard.md)簿。

### <a name="the-system-topic"></a>系統主題

應用程式應該隨時都支援系統主題。 本主題提供另一個應用程式一般感興趣的資訊內容。

資料項目目值必須以 [**CF \_ 文字**](standard-clipboard-formats.md) 剪貼簿格式轉譯。 系統主題之專案值的個別元素必須以定位字元分隔。 下表建議系統主題的部分專案。



| 項目          | 描述                                                                                                                                                                                                                                                                                             |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 格式       | 應用程式可轉譯的剪貼簿格式清單（以 Tab 分隔）。 一般而言， **cf \_** 格式會列出已移除名稱的 "**CF \_**" 部分 (例如， **cf \_ 文字** 會列為「**文字**」 ) 。                                                                                        |
| 說明          | 簡短說明如何使用 DDE 伺服器的文字。                                                                                                                                                                                                                                                   |
| ReturnMessage | 最近使用之 [**WM \_ DDE \_ ACK**](wm-dde-ack.md) 訊息的支援詳細資料。 當需要超過8個位的應用程式特定傳回資料時，此專案很有用。                                                                                                                |
| 狀態        | 應用程式目前狀態的指示。 當伺服器收到這個系統主題專案的 [**wm \_ dde \_ 要求**](wm-dde-request.md) 訊息時，它應該會以適當的方式，使用包含忙碌或就緒的字串張貼一個 [**wm \_ dde \_ 資料**](wm-dde-data.md) 訊息來回應。 |
| SysItems      | 應用程式支援的系統主題專案清單。                                                                                                                                                                                                                                                    |
| TopicItemList | 類似于 SysItems 專案，除了系統主題以外的每個主題都應支援 TopicItemList。 這可讓您流覽任何主題下支援的專案。 如果無法列舉專案，此專案只應包含 "TopicItemList"。                                  |
| 主題        | 應用程式目前支援的主題清單;這份清單可能會有不同的時間。                                                                                                                                                                                                  |



 

### <a name="permanent-data-links"></a>永久資料連結

一旦開始 DDE 交談之後，用戶端就可以建立一或多個與伺服器之間的永久資料連結。 資料連結是一種通訊機制，當指定資料項目的值變更時，伺服器會通知用戶端。 資料連結是永久性的，這表示此通知程式會繼續進行，直到資料連結或 DDE 交談本身結束為止。

永久的 DDE 資料連結有兩種：暖和經常性存取。 在暖資料連結中，伺服器會通知用戶端資料項目的值已變更，但伺服器不會將資料值傳送給用戶端，直到用戶端要求為止。 在經常性存取資料連結中，伺服器會立即將變更的資料值傳送給用戶端。

支援暖或經常性資料連結的應用程式通常會在其 [**編輯**] 功能表中提供 [**複製**] 或 [**貼上連結**] 命令，讓使用者能夠建立應用程式之間的連結。

### <a name="atoms-and-shared-memory-objects"></a>原子和共用記憶體物件

某些 DDE 訊息的引數是全域原子或共用記憶體物件。 使用這些引數的應用程式必須遵循明確的規則，以瞭解何時配置和刪除這些引數。 在所有情況下，訊息寄件者都必須刪除預期接收者將不會收到的任何 atom 或共用記憶體物件，因為發生錯誤狀況，例如 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) 函式失敗。

DDE 使用共用記憶體物件的三個用途：

-   包含要交換的資料項目目值。 這是在 [**wm \_ dde \_ 資料**](wm-dde-data.md)和 [**Wm \_ dde \_**](wm-dde-poke.md)訊息中， *hData* 參數所參考的專案。
-   在訊息中攜帶選項。 這是在 [**WM \_ DDE \_ 建議**](wm-dde-advise.md)訊息中，由 *hOptions* 參數所參考的專案。
-   以執行命令執行字串。 這是在 [**wm \_ dde \_ 執行**](wm-dde-execute.md)訊息及其對應的 [**WM \_ Dde \_ ACK**](wm-dde-ack.md)訊息中，由 *hCommands* 參數所參考的專案。

接收 DDE 共用記憶體物件的應用程式必須將它視為唯讀。 應用程式不能使用物件作為免費交換資料的相互讀寫區域。

就像使用 DDE atom 一樣，應用程式應該釋放共用記憶體物件，才能有效地管理記憶體。 應用程式也應該鎖定和解除鎖定記憶體物件。

## <a name="dynamic-data-exchange-messages-overview"></a>動態資料交換訊息總覽

因為 DDE 是以訊息為基礎的通訊協定，所以它不會採用任何函式或程式庫。 在用戶端與伺服器視窗之間傳遞某些已定義的 DDE 訊息，即可進行所有 DDE 交易。

有九個 DDE 訊息;這些訊息的符號常數定義于 DDE 標頭檔中。 您也可以在此標頭檔中定義各種 DDE 訊息的特定結構。

下表匯總了 DDE 訊息。



| 訊息                                        | 描述                                                                                                                                      |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ DDE \_ ACK**](wm-dde-ack.md)             | 認可接收或未接收訊息。                                                                                               |
| [**WM \_ DDE \_ 建議**](wm-dde-advise.md)       | 要求伺服器應用程式在每次變更時，提供資料項目目的更新或通知。 這會建立永久的資料連結。 |
| [**WM \_ DDE \_ 資料**](wm-dde-data.md)           | 將資料項目目值傳送至用戶端應用程式。                                                                                               |
| [**WM \_ DDE \_ 執行**](wm-dde-execute.md)     | 將字串傳送至伺服器應用程式，此應用程式預期會將字串處理為一連串的命令。                                       |
| [**WM \_ DDE \_ 起始**](wm-dde-initiate.md)   | 起始用戶端與伺服器應用程式之間的交談。                                                                             |
| [**WM \_ DDE 的進行 \_**](wm-dde-poke.md)           | 將資料項目目值傳送至伺服器應用程式。                                                                                               |
| [**WM \_ DDE \_ 要求**](wm-dde-request.md)     | 要求伺服器應用程式提供資料項目目的值。                                                                             |
| [**WM \_ DDE \_ 終止**](wm-dde-terminate.md) | 終止交談。                                                                                                                       |
| [**WM \_ DDE \_ UNADVISE**](wm-dde-unadvise.md)   | 終止永久資料連結。                                                                                                                |



 

應用程式會呼叫 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 來發出 [**wm \_ dde \_ 起始**](wm-dde-initiate.md) 訊息或傳送的 [**Wm \_ dde \_**](wm-dde-ack.md) 通知訊息，以回應 **WM \_ dde \_ 起始**。 所有其他訊息都是由 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)傳送。 這些呼叫的第一個參數是接收視窗的控制碼;第二個參數包含要傳送的訊息;第三個參數會識別傳送視窗;第四個參數包含訊息特定的引數。

## <a name="dynamic-data-exchange-message-flow"></a>動態資料交換訊息 Flow

一般的 DDE 交談包含下列事件：

1.  用戶端應用程式會起始交談，而伺服器應用程式會回應。
2.  應用程式會透過下列任何或所有方法來交換資料：
    -   -   伺服器應用程式會在用戶端的要求中，將資料傳送給用戶端。
        -   用戶端應用程式會將未經要求的資料傳送至伺服器應用程式。
        -   用戶端應用程式會要求伺服器應用程式在每次資料項目變更時通知用戶端 (暖資料連結) 。
        -   用戶端應用程式會要求伺服器應用程式在資料變更時，傳送資料 (熱資料連結) 。
        -   伺服器應用程式會在用戶端的要求中執行命令。

3.  用戶端或伺服器應用程式會終止交談。

處理來自用戶端或伺服器之要求的應用程式視窗，必須嚴格地以其收到的順序進行處理。

用戶端可以與一部以上的伺服器建立交談;伺服器可以有多個用戶端的交談。 處理來自多個來源的訊息時，用戶端或伺服器必須同步處理交談的訊息，但不需要同步處理所有訊息。 換句話說，它可以視需要從一個交談移至另一個。

如果應用程式無法處理傳入的要求，因為它正在等候 DDE 回應，它必須將具有設定為1之 [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack)結構的 **fBusy** 成員張貼的 [**WM \_ DDE \_ ACK**](wm-dde-ack.md)訊息，以防止鎖死。 如果基於任何原因，應用程式無法在合理的時間內處理傳入的要求，也可以傳送忙碌的 **WM \_ DDE \_ ACK** 訊息。

應用程式應該能夠處理用戶端或伺服器在特定時間內回應訊息的失敗。 由於逾時間隔可能會根據應用程式的本質和使用者的系統設定而有所不同 (包括是否連接到網路) ，因此應用程式應該提供方法讓使用者指定間隔。

## <a name="parameter-packing-functions"></a>參數封裝函數

許多 DDE 訊息的 *lParam* 參數包含兩個數據片段。 例如， [**WM \_ DDE \_ 資料**](wm-dde-data.md)訊息的 *lParam* 包含資料處理程式和 atom。 應用程式必須使用 [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) 函式，將控制碼和 atom 封裝至 *lParam* 參數，並使用 [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) 函數來移除值。 DDE 應用程式必須針對在 DDE 交談期間張貼的所有訊息，使用 **PackDDElParam** 和 **UnpackDDElParam** 。

應用程式也可以使用 [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) 和 [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) 函數。 **ReuseDDElParam** 可讓 DDE 應用程式重複使用壓縮的 *lParam* 參數，以協助減少應用程式在交談期間必須執行的記憶體重新配置數目。 應用程式可以使用 **FreeDDElParam** 來釋放與在 DDE 交談期間收到的資料控制碼相關聯的記憶體。

## <a name="dynamic-data-exchange-and-impersonation"></a>動態資料交換和模擬

若要允許伺服器模擬用戶端，用戶端會呼叫 [**DdeSetQualityOfService**](/windows/desktop/api/Dde/nf-dde-ddesetqualityofservice) 函數。 [**安全性模擬 \_ \_ 等級**](/windows/win32/api/winnt/ne-winnt-security_impersonation_level)結構是用來控制伺服器可能執行的模擬層級。

DDE 伺服器可以藉由呼叫 [**ImpersonateDdeClientWindow**](/windows/desktop/api/Dde/nf-dde-impersonateddeclientwindow) 函數來模擬 dde 用戶端。 DDEML 伺服器應使用 [**DdeImpersonateClient**](/windows/desktop/api/Ddeml/nf-ddeml-ddeimpersonateclient) 函數。

 

 