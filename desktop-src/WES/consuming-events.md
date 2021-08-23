---
title: '使用事件 (Windows 事件記錄) '
description: 您可以使用通道或記錄檔中的事件。
ms.assetid: 17204d3f-0875-42c5-9af4-caca6349a67d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f131f0f3b02485c3c838e9180ea1daaebb4121b8846e5a124f36cfdb6bf377f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119620378"
---
# <a name="consuming-events-windows-event-log"></a>使用事件 (Windows 事件記錄) 

您可以使用通道或記錄檔中的事件。 若要取用事件，您可以使用所有事件，也可以指定 XPath 運算式來識別您想要取用的事件。 若要判斷您可以在 XPath 運算式中使用之事件的元素和屬性，請參閱 [事件架構](eventschema-schema.md)。

Windows事件記錄檔支援 XPath 1.0 的子集。 如需限制的詳細資訊，請參閱 [XPath 1.0 限制](#xpath-10-limitations)。

下列範例顯示簡單的 XPath 運算式。


```XML
// The following query selects all events from the channel or log file
XPath Query: *

// The following query selects all the LowOnMemory events from the channel or log file
XPath Query: *[UserData/LowOnMemory]

// The following query selects all events with a severity level of 1 (Critical) from the channel or log file
XPath Query: *[System/Level=1]

// The following query shows a compound expression that selects all events from the channel or log file
// where the printer's name is MyPrinter and severity level is 1.
XPath Query: *[UserData/*/PrinterName="MyPrinter" and System/Level=1]

// The following query selects all events from the channel or log file where the severity level is
// less than or equal to 3 and the event occurred in the last 24 hour period.
XPath Query: *[System[(Level <= 3) and TimeCreated[timediff(@SystemTime) <= 86400000]]]
```



您可以直接在呼叫 [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) 或 [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) 函數時使用 XPath 運算式，也可以使用包含 XPath 運算式的結構化 XML 查詢。 針對從單一來源查詢事件的簡單查詢，使用 XPath 運算式是正常的。 如果 XPath 運算式是包含20個以上運算式的複合運算式，或您要查詢來自多個來源的事件，則您必須使用結構化 XML 查詢。 如需結構化 XML 查詢之元素的詳細資訊，請參閱 [查詢架構](queryschema-schema.md)。

結構化查詢會識別事件的來源，以及一或多個選取器或 suppressors。 選取器包含從來源選取事件的 XPath 運算式，而抑制器包含可防止選取事件的 XPath 運算式。 您可以從一個以上的來源選取事件。 如果選取器和抑制器識別相同的事件，則事件不會包含在結果中。

下圖顯示指定一組選取器和 suppressors 的結構化 XML 查詢。


```XML
<QueryList>
  <Query Id="0">
    <Select Path="Application">
        *[System[(Level <= 3) and 
        TimeCreated[timediff(@SystemTime) <= 86400000]]]
    </Select>
    <Suppress Path="Application">
        *[System[(Level = 2)]]
    </Suppress>
    <Select Path="System">
        *[System[(Level=1  or Level=2 or Level=3) and 
        TimeCreated[timediff(@SystemTime) <= 86400000]]]
    </Select>
  </Query>
</QueryList>
```



查詢的結果集不包含查詢時的事件快照集。 相反地，結果集會包含在查詢時所產生的事件，而且也會包含在您列舉結果時所引發符合查詢準則的所有新事件。

> [!Note]  
> 事件的順序會保留給相同執行緒所寫入的事件。 不過，在多處理器電腦的不同處理器上，由個別執行緒所撰寫的事件可能不會出現順序。

 

如需使用事件的詳細資訊，請參閱下列主題：

-   [查詢事件](querying-for-events.md)
-   [訂閱事件](subscribing-to-events.md)
-   [轉譯事件](rendering-events.md)
-   [格式化事件訊息](formatting-event-messages.md)
-   [將事件加上書簽](bookmarking-events.md)

使用事件的標準終端使用者工具組括：

-   [事件檢視器](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11))
-   Windows PowerShell [new-winevent](/previous-versions//dd367894(v=technet.10))指令 Cmdlet
-   [**WevtUtil**](windows-event-log-tools.md)

## <a name="xpath-10-limitations"></a>XPath 1.0 限制

Windows事件記錄檔支援 XPath 1.0 的子集。 主要限制是，事件選取器只可以選取代表事件的 XML 元素。 未選取事件的 XPath 查詢無效。 所有有效的選取器路徑都以 \* 或 "Event" 開頭。 所有位置路徑都是在事件節點上運作，並且由一系列步驟組成。 每個步驟都是三個部分的結構：軸、節點測試與述詞。 如需有關這些元件以及 XPath 1.0 的詳細資訊，請參閱 [XML 路徑語言 (XPath) ](https://www.w3.org/TR/xpath)。 Windows事件記錄檔會在運算式上放置下列限制：

-   軸：僅支援子 (預設) 和屬性 (以及其速記 "@" ) 軸。
-   節點測試：僅支援節點名稱和 NCName 測試。 支援 " \* " 字元（可選取任何字元）。
-   述詞：如果位置路徑符合下列限制，則可接受任何有效的 XPath 運算式：
    -   支援標準運算子 **或**、 **AND**、=、！ =、<=、<、>=、> 和括弧。
    -   不支援產生節點名稱的字串值。
    -   不支援以反向順序進行評估。
    -   不支援節點集。
    -   不支援命名空間範圍設定。
    -   不支援命名空間、處理和批註節點。
    -   不支援內容大小。
    -   不支援變數系結。
    -   只有) 才支援 position 函式和其速記陣列參考 (于分葉節點上。
    -   支援頻外函數。 函數會針對兩個整數數位引數執行位 AND。 如果位 AND 的結果為非零值，則函數會評估為 true;否則，函數會評估為 false。
    -   支援 timediff 函數。 函數會計算第二個引數與第一個引數之間的差異。 其中一個引數必須是常值。 引數必須使用 FILETIME 標記法。 結果是兩次之間的毫秒數。 如果第二個引數代表較晚的時間，則結果為正數;否則，它會是負數。 如果未提供第二個引數，則會使用目前的系統時間。

 

 
