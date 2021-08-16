---
title: 消費者介面自動化如何公開内嵌物件
description: 本主題說明 Microsoft 消費者介面自動化如何在文字檔或容器中公開内嵌物件或子項目。
ms.assetid: 5ecf5e94-5329-4abb-aedb-4e303688e5f7
keywords:
- 消費者介面自動化，文字模式總覽
- 消費者介面自動化，文字控制項總覽
- 消費者介面自動化，文字控制項模式
- 消費者介面自動化，内嵌物件總覽
- 消費者介面自動化，公開内嵌物件
- 消費者介面自動化，内嵌物件的案例
- 文字模式，關於
- 文字控制項，關於
- 文字控制項模式
- 控制項模式、文字
- 內嵌物件
- 公開内嵌物件
ms.topic: article
ms.date: 08/31/2019
ms.openlocfilehash: 2cb5a571d61353d2c8458b42fb65eac19eab0fb228f1e157539470075e392b8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899315"
---
# <a name="how-ui-automation-exposes-embedded-objects"></a>消費者介面自動化如何公開内嵌物件

本主題說明 Microsoft 消費者介面自動化如何使用 Text 和 TextRange 控制項模式，在文字檔或容器中) 的子系/子代元素 (公開内嵌物件。

針對消費者介面自動化，内嵌物件是任何具有非文字界限的元素，例如影像、超連結、表格或檔案類型 (Microsoft Excel 試算表、Microsoft Windows 媒體檔案，依此類推) 。

> [!NOTE]
> 這與元件物件模型不同 (COM) OLE 定義 (請參閱 [内嵌物件](../com/embedded-objects.md)) ，也就是在一個應用程式中建立專案，並在另一個應用程式中內嵌或連結的專案。 是否可以在它的原始應用程式中編輯物件，與消費者介面自動化的內容無關。

## <a name="embedded-objects-and-the-ui-automation-tree"></a>內嵌物件和 UI 自動化樹狀目錄

内嵌物件在消費者介面自動化樹狀結構的控制項視圖中會被視為個別的元素。 它們會公開成為文字容器的子系，以便透過與消費者介面自動化中其他控制項相同的物件模型來存取它們。

下表列出容器和非容器元素的範例。

:::row:::
   :::column span="2":::

      **容器元素**

   :::column-end:::
   :::column span="":::

      **非容器元素**

   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::

- Calendar
- Combobox
- DataGrid
- 文件
- 編輯
- Group
- 標頭
- HeaderItem
- List
- 功能表

   :::column-end:::
   :::column span="":::

- MenuBar
- 窗格
- SplitButton
- 索引標籤
- 資料表
- 工具列
- 樹狀結構
- TreeItem
- 時間範圍

   :::column-end:::
   :::column span="":::

- 連結
- Cpl
- Button

  :::column-end:::
:::row-end:::

下圖顯示使用內嵌資料表和影像)  (檔的文字容器。

![顯示具有內嵌資料表和影像之檔的圖例](images/embeddedtable.jpg)

上述檔的消費者介面自動化內容視圖如下圖所示。

![具有内嵌物件之檔的 ui 自動化內容視圖圖](images/contenttree.jpg)

### <a name="compatible-and-non-compatible-embedded-objects"></a>「相容」和「不相容」的内嵌物件

某些消費者介面自動化提供者會針對其所包含的每個 TextPattern 物件使用相同的文字存放區。  與容器相同的文字存放區所支援的物件稱為「相容」的内嵌物件。 這些物件可以是 TextPattern 物件，在此情況下，其文字範圍可與從其容器取得的文字範圍相當。 這可讓提供者公開個別 TextPattern 物件的用戶端資訊，就像是一個大型文字提供者一樣。

但是，提供者可以針對內嵌于 TextPattern 容器內的不同 TextPattern 物件使用不同的文字存放區。 容器的文字存放區不支援的物件稱為「不相容」的内嵌物件。 這些類型的内嵌物件不一定是以 TextPattern 為基礎的物件。  

下表列出一些相容和不相容的内嵌物件範例。

| 物件  | 相容的内嵌物件 | 不相容的内嵌物件 |
| --- | --- | --- |
| 非 TextPattern 的内嵌物件 | 按鈕 Microsoft Edge<br>Microsoft Edge 中的資料表 | Microsoft XAML 架構 k 中的按鈕<br>Microsoft Edge 中具有 alt 文字的影像<br>Microsoft XAML 架構中 k 的 ListView with ListItems |
| TextPattern 内嵌物件 | Microsoft Edge 中 "text" 類型的輸入控制項<br>Word 檔中的表格 | Microsoft Word 檔中的 TextBox 元素 |

## <a name="exposing-embedded-objects"></a>公開内嵌物件

[Text 和 TextRange](uiauto-implementingtextandtextrange.md)控制項模式會公開屬性和方法，以方便流覽和查詢內嵌物件。

文字內容 (或文字容器的內部文字) 和内嵌物件（例如超連結或資料表單元格）會在控制項視圖和消費者介面自動化樹狀結構的內容視圖中公開為單一的連續文字資料流程;系統會忽略物件界限。 如果消費者介面自動化用戶端正在以某種方式來朗誦、解讀或分析文字，則應檢查特殊案例（例如具有文字內容或其他內嵌物件的表格）的文字範圍。 呼叫 [**IUIAutomationTextRange：： GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) ，以取得每個內嵌物件的 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 介面，然後呼叫 [**IUIAutomationTextPattern：： RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) 來取得每個元素的文字範圍。 這會以遞迴方式進行，直到擷取所有的文字內容為止。

> [!NOTE]
> 退化 (或折迭的) 範圍是開始端點和結束端點相同的位置。 退化範圍通常用來指出文字游標在 [ITextProvider](/windows/win32/api/uiautomationcore/nn-uiautomationcore-itextprovider) [GetSelection](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextprovider-getselection) 和 [GetCaretRange](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextprovider2-getcaretrange) 方法中的位置。

下圖顯示具有内嵌物件和其範圍範圍的文字資料流程。

![顯示具有内嵌物件及其範圍範圍之文字資料流程的圖表](images/rangespans.jpg)

## <a name="embedded-objects-and-textunit"></a>内嵌物件和 TextUnit

[ITextProvider](/windows/win32/api/uiautomationcore/nn-uiautomationcore-itextprovider)物件可以由指定的[TextUnit](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textunit)進行往返。 包含内嵌物件的提供者可以用很多方式來進行處理，但内嵌物件會影響到遍歷。 以下是一些要注意的事項：

- 任何不相容的内嵌物件都會以容器元素 TextPattern 的文字存放區中的取代字元 U + FFFC 來表示。 它也會同時視為字元單位和單字單位。
- 相容的内嵌物件可能包含多個字元和單字。
- 封入元素是橫跨整個文字範圍的最底層元素。
- 範圍的子專案也是在範圍內部分或完全封閉之容器元素的子項目。
- 在理想的情況下 (特別是如果是資料表之類的容器元素) 單字界限不會超出物件界限。 在下列範例中，文字單位 "Bar" 不包含標記 (的任何文字位置，而不是 `</td>` `<br \>` "Bar" ) 的一部分。

```Xaml
<table style="width:100%">
  <tr>
    <th>Name</th>
    <th>Notes</th>
  </tr>
  <tr>
    <td>Eve Jackson</td>
    <td>Foo Bar</td>
  </tr>
</table>
<br/>
```

- 一般而言， `<br \>` 會將視為個別的單字，使其不會超過行界限。
- 上述規則的例外狀況是文字文字單位在本身內包含完整物件的位置。 例如， `<p>Hello <a href="#">link</a> here.</p>` 包含內嵌容器的 "Hello"、"link" 和 "here" 等字。 其中 "link" 具有 TextPattern 物件做為封入專案，以及連結化物件做為子系。
- 在字元單位的案例中，物件是封入元素 (文字單位，這就不應該有子系) 。
- 注釋物件不應該以内嵌物件表示。 例如，在共同撰寫的檔中有其他作者規範存在。
- 内嵌物件至少需要一個資料指標位置，注釋只是中繼資料。
- 每個物件界限 (開始與結束) 會以 TextPattern 檔範圍中的格式分隔符號表示。
- 若是 HTML，每個 html 標記不一定會產生消費者介面自動化物件。 例如， <em></em> 強調標記內的內容不需要表示為元素，而是 UIA_IsItalicAttributeId 傳回 TRUE 的文字資料流程。
- 啟動端點是內含的，且為端點專用時的慣用端點。 當範圍為退化，且開始和結束端點屬於該範圍的相同位置時，這非常有用。

## <a name="comparing-embedded-objects"></a>比較内嵌物件

在類似的子關聯性中，並共用相同的支援文字存放區的嵌套 TextPattern 物件稱為可比較。 在此情況下，可以使用 [ITextRangeProvider：： Compare](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-compare) 和 [ITextRangeProvider：： CompareEndpoints](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-compareendpoints)來比較 TextPattern 物件的範圍。 兩者都會產生有效的數值，以指定其相對位置。

如果物件在 TextPattern ([ITextProvider：： RangeFromChild](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextprovider-rangefromchild)) 中的有效範圍，且文字範圍背後的內容不是空的，而且不是取代字元，則內嵌于 TextPattern 物件中的非 TextPattern 物件可與 TextPattern 比較。

## <a name="embedded-textpattern-objects-and-the-document-textunit"></a>內嵌 TextPattern 物件和檔 TextUnit

針對內嵌的 TextPattern 物件， [檔](/windows/win32/api/uiautomationcore/ne-uiautomationcore-textunit) 單位只會辨識該元素內所包含的內容。

### <a name="word-textpattern-element-hierarchy"></a>Word TextPattern 元素階層

- Document 元素會執行 TextPattern 和 [document](/windows/win32/api/uiautomationcore/ne-uiautomationcore-textunit) ，以傳回整個 Word 檔範圍。
- 檔的個別頁面會執行 TextPattern，而且 [檔](/windows/win32/api/uiautomationcore/ne-uiautomationcore-textunit) 會傳回這些個別頁面的內容 (即使頁面與整個檔 TextPattern) 共用相同的文字存放區也一樣。

### <a name="webpage-and-text-input-controls-in-edge"></a>Edge 中的網頁和文字輸入控制項

- 主要網頁窗格元素會執行 TextPattern，並公開整個網頁內容。
- 個別的文字輸入控制項支援 TextPattern，其中檔範圍代表每個輸入欄位中包含的文字 (即使它們與整個網頁) 共用相同的文字存放區也一樣。

## <a name="common-scenarios"></a>常見案例

本章節提供包含内嵌物件之常見案例的範例：超連結、影像和資料表。 在下列範例中，左大括弧 ( {) 表示文字範圍的起始端點，右邊的大括弧 (} ) 代表結束端點。

### <a name="hyperlink-example-1-a-text-range-that-contains-an-embedded-text-hyperlink"></a>HyperLink 範例1：包含內嵌文字超連結的文字範圍

下列文字範圍包含內嵌文字超連結。

  {URL https://www.microsoft.com 內嵌在文字中}。

呼叫 [**IUIAutomationTextRange：： GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)、 [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)、 [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)和 [**IUIAutomationTextPattern：： RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) 方法會產生下表所述的行為。

| 呼叫的方法                                                                                                                                                                                                                                                     | 結果                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange：： GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                                                                                                                                                                                  | 傳回字串「URL https://www.microsoft.com 內嵌在文字中」。                                                                               |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)                                                                                                                                                          | 傳回包含文字範圍的最內層消費者介面自動化專案，在此案例中，表示文字提供者本身的 Automation 元素。 |
| [**IUIAutomationTextRange：： GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)                                                                                                                                                                          | 傳回代表超連結控制項的消費者介面自動化元素。                                                                                      |
| [**IUIAutomationTextPattern：： RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild)，其中消費者介面自動化元素是由先前的 [**IUIAutomationTextRange：： GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) 方法所傳回。 | 傳回表示 "" 的範圍 https://www.microsoft.com 。                                                                                            |
### <a name="hyperlink-example-2-a-text-range-that-partially-spans-an-embedded-text-hyperlink"></a>HyperLink 範例2：部分跨越內嵌文字超連結的文字範圍

下列文字範圍部分跨越內嵌文字超連結。

  URL HTTPs：//{www} 內嵌于文字中。

呼叫 [**IUIAutomationTextRange：： GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)、 [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)和 [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) 方法會產生下表所述的行為。

| 呼叫的方法                                                                                            | 結果                                                                                                         |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange：： GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                         | 傳回字串 "www"。                                                                                      |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) | 傳回括住文字範圍的最內層消費者介面自動化元素;在此案例中為超連結控制項。 |
| [**IUIAutomationTextRange：： GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)                 | 會傳回 **Null** ，因為文字範圍不會跨越整個 URL 字串。                                   |

### <a name="hyperlink-example-3-a-text-range-that-partially-spans-the-content-of-a-text-container"></a>超連結範例3：部分跨越文字容器內容的文字範圍

下列文字範圍部分跨越文字容器的內容。 此文字容器有不屬於此文字範圍的內嵌文字超連結。

  {URL} https://www.microsoft.com 內嵌于文字中。

呼叫 [**IUIAutomationTextRange：： GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)、 [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)和 [**Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) 方法會產生下表所述的行為。

| 呼叫的方法                                                                                            | 結果                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange：： GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                         | 傳回字串 "The URL"。                                                                                                                                                                                                     |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) | 傳回括住文字範圍的最內層消費者介面自動化專案，在此案例中為代表文字提供者本身的元素。                                                                                     |
| [**IUIAutomationTextRange：： Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move)                               | 將文字範圍範圍移至 "HTTPs://"，因為超連結的文字是由個別單字所組成。 在此情況下，並未將超連結視為單一物件。<br/> The URL {http} is embedded in text.<br/> |

### <a name="image-example-1-a-text-range-that-contains-an-embedded-image"></a>影像範例1：包含內嵌影像的文字範圍

下列文字範圍包含往復的內嵌影像。

 {影像 ![快速導航圖](images/shuttle.jpg) 內嵌于文字} 中。

呼叫 [**IUIAutomationTextRange：： GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)、 [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)、 [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)和 [**IUIAutomationTextPattern：： RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) 方法會產生下表所述的行為。

| 呼叫的方法                                                                                                                                                                                                                                                    | 結果                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange：： GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                                                                                                                                                                                 | 傳回字串「影像內嵌在文字中」。 任何與影像相關聯的替代文字都不會包含在文字資料流程中。                |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)                                                                                                                                                         | 傳回括住文字範圍的最內層消費者介面自動化專案，在此案例中為代表文字提供者本身的元素。 |
| [**IUIAutomationTextRange：： GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)                                                                                                                                                                         | 傳回代表影像控制項的消費者介面自動化元素。                                                                               |
| [**IUIAutomationTextPattern：： RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) ，其中消費者介面自動化元素是由先前的 [**IUIAutomationTextRange：： GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) 方法所傳回。 | 傳回退化範圍。                                                                                                                 |

### <a name="image-example-2-a-text-range-that-partially-spans-the-content-of-a-text-container"></a>影像範例2：部分跨越文字容器內容的文字範圍

下列文字範圍部分跨越文字容器的內容。 此文字容器有不屬於此文字範圍的內嵌影像。

 {映射} ![快速導航圖](images/shuttle.jpg) 內嵌于文字中。

呼叫 [**IUIAutomationTextRange：： GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)、 [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)和 [**Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) 方法會產生下表所述的行為。

| 呼叫的方法                                                                                                          | 結果                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange：： GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                                       | 傳回字串 "The image"。                                                                                                                                                                                                                                                 |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)               | 傳回括住文字範圍的最內層消費者介面自動化專案，在此案例中為代表文字提供者本身的元素。                                                                                                                                   |
| [**IUIAutomationTextRange：： Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) (**TextUnit \_ Word**，2) 的參數。 | 將文字範圍移至 "is"。 因為只有以文字為基礎的內嵌物件會被視為文字資料流程的一部分，所以此範例中的影像並不會影響 [**IUIAutomationTextRange：： Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) 或其傳回值，在此情況下為2。 |

### <a name="table"></a>資料表

### <a name="table-example-1-gets-the-text-container-from-the-content-of-a-cell"></a>表格範例1：從儲存格內容取得文字容器

下表從儲存格內容取得文字容器。

| 包含影像的儲存格                                            | 包含文字的儲存格 |
|------------------------------------------------------------|----------------|
| ![快速導航圖](images/shuttle.jpg)           | X              |
| ![空間和望遠鏡的圖解](images/space.jpg) | Y              |
| ![microscope 的圖例](images/microscope.jpg)     | Z              |

呼叫 [**IUIAutomationGridPattern：： GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem)、 [**IUIAutomationTextPattern：： RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild)和 [**IUIAutomationTextRange：： GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) 方法會產生下表所述的行為。

| 呼叫的方法                                                                                                                                                                                                                       | 結果                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationGridPattern：： GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) 參數 (0，0) 。                                                                                                                        | 傳回代表資料表單元格內容的消費者介面自動化專案，在此案例中，元素是文字控制項。                                                               |
| [**iuiautomatioNtextpattern::rangefromchild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild)                                                                                                                                  | 傳回影像的範圍。 ![快速導航圖](images/shuttle.jpg).                                                                                                            |
| [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) ，用於先前的 [**IUIAutomationTextPattern：： RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) 方法所傳回的物件。 | 傳回代表資料表單元格的消費者介面自動化元素。 在此情況下，元素是支援 [TableItem](uiauto-implementingtableitem.md) 控制項模式的文字控制項。 |
| [**IUIAutomationTextRange：： GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) ，適用于前一個 **GetEnclosingElement** 方法所傳回的物件。                                                    | 傳回代表資料表的消費者介面自動化元素。                                                                                                                                   |
| [**IUIAutomationTextRange：： GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) ，適用于前一個 **GetEnclosingElement** 方法所傳回的物件。                                                    | 傳回表示文字提供者本身的消費者介面自動化元素。                                                                                                                 |

### <a name="table-example-2-gets-the-text-content-of-a-cell"></a>資料表範例2：取得儲存格的文字內容

上述範例中的資料表會取得儲存格的文字內容。

呼叫 [**IUIAutomationGridPattern：： GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) 和 [**IUIAutomationTextPattern：： RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) 方法會產生下表所述的行為。

| 呼叫的方法                                                                                                                                                                                                                                                          | 結果                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationGridPattern：： GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) 與參數 (1，1) 。                                                                                                                                                            | 傳回代表資料表單元格內容的消費者介面自動化元素。 在此情況下，元素是文字控制項。 |
| [**IUIAutomationTextPattern：： RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) ，其中消費者介面自動化專案是前一個 [**IUIAutomationGridPattern：： GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) 方法所傳回的物件。 | 傳回 "Y"。                                                                                                               |

當您透過 [**TextUnit \_ 線**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)移動檔時，如果文字範圍輸入了內嵌的表格，則資料格中的每一行文字都應該視為線條。

## <a name="related-topics"></a>相關主題

### <a name="conceptual"></a>概念

- [關於 Text 和 TextRange 控制項模式](uiauto-about-text-and-textrange-patterns.md)
- [消費者介面自動化 Text 屬性](uiauto-textattributes.md)
- [UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
- [消費者介面自動化文字內容的支援](uiauto-ui-automation-textpattern-overview.md)