---
title: 關於 Text 物件模型
description: 本主題提供 TOM 的概要說明。
ms.assetid: e304ec18-ec2e-4ea7-91c6-6f6ab63b72ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b934aab1cbd3dca932b58e4aa99498843cb8cc97
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024206"
---
# <a name="about-text-object-model"></a>關於 Text 物件模型

 (TOM) 的 Text 物件模型會定義一組文字操作介面，這些介面會依數個 Microsoft 文字解決方案的不同程度來支援，包括 rich edit 控制項。 本主題提供 TOM 的概要說明。 本主題將討論下列主題。

-   [TOM 第2版物件](#tom-version-2-objects)
-   [TOM 介面慣例](#tom-interface-conventions)
-   [TomBool 類型](#the-tombool-type)
-   [數學堆積和建立](#math-buildup-and-build-down)
-   [TOM RTF](#tom-rtf)
-   [尋找 Rich Text](#finding-rich-text)
-   [TOM 協助工具](#tom-accessibility)
    -   [從執行中的物件資料表執行的介面](#interface-from-running-object-table)
    -   [來自視窗訊息的介面](#interface-from-window-messages)
    -   [協助工具導向的方法](#accessibility-oriented-methods)
-   [字元相符集](#character-match-sets)

## <a name="tom-version-2-objects"></a>TOM 第2版物件

TOM 第2版 (TOM 2) 擴充原始的文字物件模型;新介面衍生自舊介面。 更新的 TOM API 包括支援新的字元和段落格式屬性、資料表模型、多重選取，以及數學和 ruby 的内嵌物件支援。

最上層 TOM 2 物件是由 [**ITextDocument2**](/windows/desktop/api/Tom/nn-tom-itextdocument2) 介面所定義，這個介面具有在物件階層中較低層級建立和取得物件的方法。 針對簡單的純文字處理，您可以從 **ITextDocument2** 物件取得 [**ITextRange2**](/windows/desktop/api/Tom/nn-tom-itextrange2)物件，並利用該物件來進行大部分的作業。 如果您需要新增 rich text 格式，您可以從 **ITextRange2** 物件取得 [**ITextFont2**](/windows/desktop/api/Tom/nn-tom-itextfont2)和 [**ITextPara2**](/windows/desktop/api/Tom/nn-tom-itextpara2)物件。 **ITextFont2** 提供與 Microsoft word 格式（字型）對話方塊相同的程式設計，而 **ITextPara2** 則提供相當於單字格式段落對話方塊的專案。

除了這三個較低層級的物件之外，TOM 2 還有一個選取專案物件 ([**ITextSelection2**](/windows/win32/api/tom/nn-tom-itextselection2)) ，也就是具有反白顯示和某些 UI 導向方法的 [**ITextRange2**](/windows/desktop/api/Tom/nn-tom-itextrange2) 物件。

範圍和選取專案物件包含螢幕導向的方法，可讓程式檢查螢幕上的文字或可滾動到螢幕上的文字。 例如，這些功能有助於讓視力受損的人員能夠存取文字。

具有2個尾碼的每個介面都會繼承自對應的介面，但不含2個尾碼。 例如， [**ITextDocument2**](/windows/desktop/api/Tom/nn-tom-itextdocument2) 繼承自 [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument)。

TOM 2 物件具有下列階層。

``` syntax
ITextDocument2         Top-level editing object
    ITextRange2        Primary text interface: a range of text
        ITextFont2     Character-attribute interface
        ITextPara2     Paragraph-attribute interface
        ITextRow       Table interface
    ITextSelection2    Screen highlighted text range
        ITextRange2    Selection inherits all range methods
    ITextDisplays      Displays collection (not yet defined)
    ITextStrings       Rich-text strings collection
    ITextStoryRanges2  Enumerator for stories in document
```

[**ITextDocument2**](/windows/desktop/api/Tom/nn-tom-itextdocument2)物件描述一或多個連續的文字範圍，稱為「*故事*」。 故事代表檔的各個部分，例如檔的主要文字、頁首和頁尾、註腳、注釋和 rich text 臨時板。 在以線性格式的數學運算式和內建表單之間轉譯時，會使用臨時板的故事。 當內容即將變更時，當您儲存目前複製來源範圍的內容時，也會使用臨時板故事。

[**ITextRange2**](/windows/desktop/api/Tom/nn-tom-itextrange2)物件是由其開始和結束字元位置位移和故事物件所定義。 雖然它的文字可以複製到剪貼簿或其他目標，但它並不會獨立存在於其父案例物件中。 文字範圍物件不同于試算表和其他範圍物件，這些物件是由其他類型的位移所定義;例如，資料列/資料行或圖形位置 (x，y) 。 文字範圍物件可以透過各種方式自行修改，可以傳回本身的複本，並可將其開始和結束字元位置及其故事指標複製到目前的選取範圍。

不需要明確的故事物件，因為一律可以建立 [**ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange) 物件來代表任何指定的情節。 尤其是， [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) 物件可以建立 [**ITextStoryRanges**](/windows/desktop/api/Tom/nn-tom-itextstoryranges) 物件來列舉檔中的故事，其範圍具有開始和結束字元位置值，這些值會描述完整的故事 (例如，0和 **tomForward**) 。

使用 [**ITextStoryRanges2**](/windows/desktop/api/Tom/nn-tom-itextstoryranges2) 物件時，不需要明確的故事物件，因為每個案例都是由 [**ITextRange2**](/windows/desktop/api/Tom/nn-tom-itextrange2) 物件描述。 尤其是， [**ITextDocument2**](/windows/desktop/api/tom/nn-tom-itextdocument2) 物件可以建立 [**ITextStoryRanges2**](/windows/desktop/api/tom/nn-tom-itextstoryranges2) 物件來列舉檔中的故事，其範圍具有開始和結束字元位置值，這些值會描述完整的故事 (例如，0和 **tomForward**) 。

[**ITextRow**](/windows/desktop/api/Tom/nn-tom-itextrow)介面以及 [**ITextRange：： Move**](/windows/desktop/api/Tom/nf-tom-itextrange-move)和 [**ITextRange：： Expand**](/windows/desktop/api/Tom/nf-tom-itextrange-expand)方法可讓您插入、查詢及變更資料表。

## <a name="tom-interface-conventions"></a>TOM 介面慣例

所有 TOM 方法都會傳回 **HRESULT** 值。 一般而言，TOM 方法會傳回下列標準值。

-   E \_ OUTOFMEMORY
-   E \_ INVALIDARG
-   E \_ >NOTIMPL
-   E \_ FILENOTFOUND
-   E \_ ACCESSDENIED
-   E \_ 失敗
-   聯合 \_ E \_ 發行
-   >AAD-USERREADUSINGALTERNATIVESECURITYID-NOERROR (與 S \_ 正常) 
-   S \_ FALSE

請注意，如果刪除與 TOM 物件（例如 [**ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange) ）相關聯的編輯實例，tom 物件就會變成無用，而且其所有方法都會傳回已 \_ 發行的 E \_ 。

除了 **HRESULT** 傳回值之外，許多方法都包含 out 參數，這些參數是用來傳回值的指標。 針對所有介面，您應該檢查所有指標參數，以確保它們在使用之前都是非零。 如果您傳遞 null 值給需要有效指標的方法，此方法會傳回 E \_ INVALIDARG。 有 null 值的選擇性 out 指標會被忽略。

使用具有 Get 和 Set 首碼的方法來取得和設定屬性。 布林值變數會使用 **tomFalse** (0) 用於 **FALSE**，而 **tomTrue** (-1) 表示 **TRUE**。

TOM 常數定義于 [**tomConstants**](/windows/win32/api/tom/ne-tom-tomconstants) 列舉型別中，並以首碼 *tom* 開頭，例如 **tomWord**。

## <a name="the-tombool-type"></a>TomBool 類型

許多 TOM 方法會使用一種特殊類型的變數，稱為 "tomBool"，適用于具有二進位狀態的 rich text 屬性。 TomBool 類型與 **布林** 類型不同，因為它可以採用四個值： **tomTrue**、 **tomFalse**、 **tomToggle** 和 **tomUndefined**。 **TomTrue** 和 **tomFalse** 值表示 true 和 false。 **TomToggle** 值是用來切換屬性。 **TomUndefined** 值（通常稱為 NINCH）是一種特殊的無輸入、無變更的值，可搭配長、浮點數和 **COLORREF** s 使用。 若為字串， **tomUndefined** (或 NINCH) 會以 null 字串表示。 若為屬性設定作業，使用 **tomUndefined** 並不會變更目標屬性。 針對屬性取得作業， **tomUndefined** 表示範圍中的字元具有不同的值 (它會在屬性對話方塊中提供灰色的核取方塊) 。

## <a name="math-buildup-and-build-down"></a>數學堆積和建立

您可以使用 [**ITextRange2：： BuildUpMath**](/windows/desktop/api/Tom/nf-tom-itextrange2-buildupmath) 方法，將線性格式的數學運算式轉換成內建版本。 [**ITextRange2：： Linearize**](/windows/desktop/api/Tom/nf-tom-itextrange2-linearize)方法會執行相反的轉換（稱為 linearization 或建立），將數學運算式的內建版本轉換回線性格式。 當您需要匯出純文字或啟用特定類型的編輯時，數學組建關閉功能會很有用。

## <a name="tom-rtf"></a>TOM RTF

在 TOM 中，rich text 交換可透過一組明確的方法呼叫來完成，或藉由將 rtf 格式的 rtf 文字傳輸 (RTF) 來完成。 本節提供段落屬性和字元屬性的 RTF 控制字組表格。

**TOM RTF 段落控制字組**

| 控制字組   | 意義                                                                                                                                                                                                                                                                        |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \\ fi *n*      | 第一行縮排 (預設值為零) 。                                                                                                                                                                                                                                       |
| \\ 保持        | 保持段落不變。                                                                                                                                                                                                                                                         |
| \\ keepn       | 繼續進行下一個段落。                                                                                                                                                                                                                                                  |
| \\ li *n*      | 左邊縮排 (預設值為零) 。                                                                                                                                                                                                                                             |
| \\ noline      | 無行號。                                                                                                                                                                                                                                                             |
| \\ nowidctlpar | 關閉孤行控制。                                                                                                                                                                                                                                                 |
| \\ pagebb      | 段落前中斷頁面。                                                                                                                                                                                                                                                   |
| \\ 面值         | 新段落。                                                                                                                                                                                                                                                                 |
| \\ pard        | 重設為預設段落屬性。                                                                                                                                                                                                                                        |
| \\ Ql          | 靠左對齊 (預設) 。                                                                                                                                                                                                                                                    |
| \\ Qr          | 靠右對齊。                                                                                                                                                                                                                                                                 |
| \\ qj          | 左右對齊。                                                                                                                                                                                                                                                                     |
| \\ Qc          | 置中。                                                                                                                                                                                                                                                                      |
| \\ ri *n*      | 靠右縮排 (預設值為零) 。                                                                                                                                                                                                                                            |
| \\ s *n*       | 樣式 *n*。                                                                                                                                                                                                                                                                     |
| \\ sa *n*      |  (預設值之後的空間為零) 。                                                                                                                                                                                                                                             |
| \\ sb *n*      |  (預設值之前的空間為零) 。                                                                                                                                                                                                                                            |
| \\ sl *n*      | 如果遺失或 *n*= 1000，行間距是由一行中最高的字元所決定 (單行間距) ;如果 *n*> 零，則至少使用此大小;如果 *n* 是 < 零， \|  \| 則會使用剛好 n。 如果 slmult 1 如下，則行距為多行間距 \\ 。 |
| \\ slmult *m*  | 後面接著 \\ sl。 *m* = 零：至少或確切的行間距（如 \\ sl *n* 所述）。 *m* = 1：行距 = *n*/240 倍單一行間距。                                                                                                                              |
| \\ tb *n*      | 左邊界中的橫條定位鍵位置（以緹為單位）。                                                                                                                                                                                                                              |
| \\ tldot       | Tab 前置字元點。                                                                                                                                                                                                                                                               |
| \\ tleq        | Tab 前導前導等號。                                                                                                                                                                                                                                                         |
| \\ tlhyph      | Tab 鍵前導連字號。                                                                                                                                                                                                                                                            |
| \\ tlth        | Tab 前置字元粗線。                                                                                                                                                                                                                                                         |
| \\ tlul        | Tab 前置字元。                                                                                                                                                                                                                                                          |
| \\ Tqc         | 中央索引標籤。                                                                                                                                                                                                                                                                  |
| \\ tqdec       | [小數] 索引標籤。                                                                                                                                                                                                                                                                   |
| \\ tqr         | 向右對齊索引標籤。                                                                                                                                                                                                                                                               |
| \\ tx *n*      | 左邊界中的索引標籤位置（以緹為單位）。                                                                                                                                                                                                                                  |



 

**TOM RTF 字元格式控制字組**

| 控制字組     | 意義                                                                                                                                                                                                                                  |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \\ 動畫 *n* | 將動畫類型設定為 *n*。                                                                                                                                                                                                              |
| \\ B             | 大膽。                                                                                                                                                                                                                                    |
| \\ 帽          | 全部大寫。                                                                                                                                                                                                                            |
| \\ cf *n*        | 前景色彩 (預設值為 **tomAutocolor**) 。                                                                                                                                                                                      |
| \\ cs *n*        | 字元樣式 *n*。                                                                                                                                                                                                                     |
| \\ dn *n*        | 以半點分隔的注標位置 (預設值為 6) 。                                                                                                                                                                                    |
| \\ embo          | 浮凸。                                                                                                                                                                                                                                |
| \\ f *n*         | 字型大小， *n* 是指字型資料表中的專案。                                                                                                                                                                                   |
| \\ fs *n*        | 以半點為單位的字型大小 (預設值為 24) 。                                                                                                                                                                                            |
| \\ 醒目提示 *n* | 預設值為 **tomAutocolor**) 的背景色彩 (。                                                                                                                                                                                      |
| \\ 我             | 斜。                                                                                                                                                                                                                                  |
| \\ impr          | 印記。                                                                                                                                                                                                                                 |
| \\ lang *n*      | 將語言套用至字元。 *n* 是對應至語言的數位。 純文字控制字組會將 \\ 語言屬性重設為 \\ 檔案屬性中 deflang *n* 所定義的語言。                             |
| \\ nosupersub    | 關閉上標或注標。                                                                                                                                                                                                      |
| \\ outl          | 大綱。                                                                                                                                                                                                                                 |
| \\ 平原         | 將字元格式設定屬性重設為應用程式所定義的預設值。 您也可以重設 RTF 規格) 中相關聯之字元屬性 (一節中所述的相關聯字元格式屬性。 |
| \\ scaps         | 小型大寫字母。                                                                                                                                                                                                                          |
| \\ shad          | 陰影。                                                                                                                                                                                                                                  |
| \\ 罷工        | 雙.                                                                                                                                                                                                                           |
| \\ 子           | 將注標套用至文字，並根據字型資訊減少點大小。                                                                                                                                                          |
| \\ 超級         | 將上標套用至文字，並根據字型資訊減少點大小。                                                                                                                                                        |
| \\ Ul            | 連續的底線。 \\ ul0 會關閉所有底線。                                                                                                                                                                                  |
| \\ uld           | 虛線底線。                                                                                                                                                                                                                        |
| \\ uldb          | 雙底線。                                                                                                                                                                                                                        |
| \\ ulnone        | 停止所有底線。                                                                                                                                                                                                                   |
| \\ ulw           | 文字加底線。                                                                                                                                                                                                                          |
| \\ 向上 *n*        | 以半點分隔的上標位置 (預設值為 6) 。                                                                                                                                                                                  |
| \\ V             | 隱藏文字。                                                                                                                                                                                                                             |



 

## <a name="finding-rich-text"></a>尋找 Rich Text

您可以使用 TOM 方法來尋找文字範圍所定義的 rtf 文字。 在文書處理中通常需要尋找這類豐富的文字，但在「您所看到的內容」 (WYSIWYG) 字處理器中，這種情況並不是必要的。 有一個較大的豐富文字比對網域，可讓您忽略某些字元格式屬性 (或包含段落格式和/或物件內容) ，但這類一般化已超出本節的範圍。

這項功能的其中一個用途是使用 rtf [ **尋找** ] 對話方塊，來定義您想要在檔中尋找的 rtf 文字。 此對話方塊會使用 rich edit 控制項來執行，並使用 TOM 方法來執行檔的搜尋。 您可以將所需的 rtf 文字從檔案複製到 [ **尋找** ] 對話方塊，或直接在 [ **尋找** ] 對話方塊中輸入並格式化。

下列範例顯示如何使用 TOM 方法來尋找包含正確字元格式組合的文字。 此演算法會在比對範圍中搜尋純文字（名稱為） `pr1` 。 如果找到純文字，則會由名為的試用範圍指向 `pr2` 。 然後，會使用兩個插入點範圍 (和) ，來逐步解說與的 `prip1` `prip2` 字元格式比較的試用範圍 `pr1` 。 如果兩者完全相符，則) 所提供的輸入範圍 (`ppr` 會更新以指向試用版範圍的文字，而函式會傳回相符範圍中的字元計數。 [](/windows/desktop/api/Tom/nn-tom-itextfont) `pf1` `pf2` 在字元格式比較中，會使用兩個 ITextFont 物件和。 它們會附加至插入點範圍 `prip1` 和 `prip2` 。


```
LONG FindRichText (
    ITextRange **ppr,             // Ptr to range to search
    ITextRange *pr1)              // Range with rich text to find
{
    BSTR        bstr;             // pr1 plain-text to search for
    LONG        cch;              // Text string count
    LONG        cch1, cch2;       // tomCharFormat run char counts
    LONG        cchMatch = 0;     // Nothing matched yet
    LONG        cp;               // Handy char position
    LONG        cpFirst1;         // pr1 cpFirst
    LONG        cpFirst2;         // pr2 cpFirst
    ITextFont  *    pf1, *pf      // Fonts corresponding to IPs prip1 and prip2
    ITextRange *pr2;              // Range duplicate to search with
    ITextRange *prip1, *prip      // Insertion points to walk pr1, pr2

    if (!ppr || !*ppr || !pr1)
        return E_INVALIDARG;

    // Initialize range and font objects used in search
    if ((*ppr)->GetDuplicate(&pr2)    != NOERROR ||
        pr1->GetDuplicate(&prip1)     != NOERROR ||
        pr2->GetDuplicate(&prip2)     != NOERROR ||
        prip1->GetFont(&pf1)          != NOERROR ||
        prip2->GetFont(&pf2)          != NOERROR ||
        pr1->GetText(&bstr)           != NOERROR )
    {
        return E_OUTOFMEMORY;
    }

    pr1->GetStart(&cpFirst1);

    // Keep searching till rich text is matched or no more plain-text hits
    while(!cchMatch && pr2->FindText(bstr, tomForward, 0, &cch) == NOERROR)
    {
        pr2->GetStart(&cpFirst2);                 // pr2 is a new trial range
        prip1->SetRange(cpFirst1, cpFirst1);      // Set up IPs to scan match
        prip2->SetRange(cpFirst2, cpFirst2);      //  and trial ranges

        while(cch > 0 &&
            pf1->IsEqual(pf2, NULL) == NOERROR)   // Walk match & trial ranges
        {                                         //  together comparing font
            prip1->GetStart(&cch1);               //  properties
            prip1->Move(tomCharFormat, 1, NULL);
            prip1->GetStart(&cp);
            cch1 = cp - cch1;                     // cch of next match font run

            prip2->GetStart(&cch2);
            prip2->Move(tomCharFormat, 1, NULL);
            prip2->GetStart(&cp);
            cch2 = cp - cch2;                      // cch of next trial font run

            if(cch1 < cch)                         // There is more to compare
            {
                if(cch1 != cch2)                   // Different run lengths:
                    break;                         //  no formatting match
                cch = cch - cch1;                  // Matched format run
            }
            else if(cch2 < cch)                    // Trial range format run too
                break;                             //  short

            else                                   // Both match and trial runs
            {                                      //  reach at least to match
                pr2->GetEnd(&cp);                  //  text end: rich-text match
                (*ppr)->SetRange(cpFirst2, cp)     // Set input range to hit
                cchMatch = cp - cpFirst2;          //  coordinates and return
                break;                             //  length of matched string
            }
        }
    }
    pr2->Release();
    prip1->Release();
    prip2->Release();
    pf1->Release();
    pf2->Release();
    SysFreeString(bstr);

    return cchMatch;
}
```



## <a name="tom-accessibility"></a>TOM 協助工具

TOM 透過 [**ITextSelection**](/windows/desktop/api/Tom/nn-tom-itextselection) 和 [**ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange) 介面提供協助工具支援。 本節描述可用於存取範圍的方法，以及程式如何判斷物件的 *x*， *y* 螢幕位置。

由於以 UI 為基礎的協助工具程式通常適用于畫面和滑鼠，因此常見的問題是尋找目前滑鼠位置的對應 [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) 介面 (在螢幕座標) 。 下列各節提供兩種方式來判斷適當的介面：

-   [透過正在執行的物件資料表](#interface-from-running-object-table)
-   透過 [**EM \_ GETOLEINTERFACE**](em-getoleinterface.md) 訊息（適用于視窗化的 rich edit 實例），前提是用戶端位於相同的進程空間 (不需要 *封送處理*) 

如需詳細資訊，請參閱 Microsoft Active Accessibility 規格。 從螢幕位置取得物件之後，您可以使用做為 [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) 介面，並呼叫 [**RangeFromPoint**](/windows/desktop/api/Tom/nf-tom-itextdocument-rangefrompoint) 方法，以在與螢幕位置對應的 cp 上取得空的範圍物件。

### <a name="interface-from-running-object-table"></a>從執行中的物件資料表執行的介面

執行中的物件資料表 (的 ROT) 指出哪些物件實例為使用中狀態。 藉由查詢此資料表，您可以在物件已在執行時，加速將用戶端連接到物件的程式。 在程式可以透過執行中的物件表存取 TOM 介面之前，具有視窗的 TOM 實例必須使用標記在 ROT 中註冊。 您可以從包含其 [**HWND**](/windows/desktop/WinProg/windows-data-types)之十六進位值的字串來建立標記。 下列程式碼範例示範如何執行這項作業。


```
// This TOM implementation code is executed when a new windowed 
// instance starts up. 
// Variables with leading underscores are members of this class.

HRESULT hr;
OLECHAR szBuf[10];            // Place to put moniker
MONIKER *pmk;

hr = StringCchPrintf(szBuff, 10, "%x", _hwnd);
if (FAILED(hr))
{
    //
    // TODO: write error handler
    //
}
CreateFileMoniker(szBuf, &pmk);
OleStdRegisterAsRunning(this, pmk, &_dwROTcookie);
....................
 
// Accessibility Client: 
//    Find hwnd for window pointed to by mouse cursor.

GetCursorPos(&pt);
hwnd = WindowFromPoint(pt);

// Look in ROT (running object table) for an object attached to hwnd

hr = StringCchPrintf(szBuff, 10, "%x", hwnd);
if (FAILED(hr))
{
    //
    // TODO: write error handler
    //
}
CreateFileMoniker(szBuf, &pmk);
CreateBindContext(0, &pbc);
pmk->BindToObject(pbc, NULL, IID_ITextDocument, &pDoc);
pbc->Release();

if( pDoc )
{
    pDoc->RangeFromPoint(pt.x, pt.y, &pRange);
    // ...now do whatever with the range pRange
}
```



### <a name="interface-from-window-messages"></a>來自視窗訊息的介面

[**EM \_ GETOLEINTERFACE**](em-getoleinterface.md)訊息提供另一種方式，在指定的螢幕位置取得物件的 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 如執行 [物件表的介面](#interface-from-running-object-table)中所述，您會取得螢幕位置的 [**HWND**](/windows/desktop/WinProg/windows-data-types) ，然後將此訊息傳送至該 **hwnd**。 **EM \_ GETOLEINTERFACE** 訊息是 rich edit 專屬的，而且會將指標傳回給 *lParam* 所定址之變數中的 [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole)介面。

**秘訣** 如果傳回指標 (請務必先將 *lParam* 指向 null 的物件設定為 null，然後再將訊息傳送) ，您可以呼叫其 [**IUnknown：： QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 方法來取得 [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) 介面。 下列程式碼範例說明此方法。


```
    HWND    hwnd;
    ITextDocument *pDoc;
    ITextRange *pRange;
    POINT    pt;
    IUnknown *pUnk = NULL;
    
    GetCursorPos(&pt);
    hwnd = WindowFromPoint(pt);
    SendMessage(hwnd, EM_GETOLEINTERFACE, 0, (LPARAM)&pUnk);
    if(pUnk && 
        pUnk->QueryInterface(IID_ITextDocument, &pDoc) == NOERROR)
    {
        pDoc->RangeFromPoint(pt.x, pt.y, &pRange);
        //  ... continue with rest of program
    }
```



### <a name="accessibility-oriented-methods"></a>協助工具導向的方法

有些 TOM 方法特別適用于在螢幕上流覽，而其他 TOM 方法則可在您抵達感興趣的地方時，增強您可以做的事。 下表說明最有用的方法。



| 方法                                                 | 如何提升協助工具                                                                                                                                                                 |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSelection**](/windows/desktop/api/Tom/nf-tom-itextdocument-getselection)     | 這個方法會取得可用的選取範圍，以供各種面向視圖用途使用，例如反白顯示文字和滾動。                                                      |
| [**RangeFromPoint**](/windows/desktop/api/Tom/nf-tom-itextdocument-rangefrompoint) | 使用於作用中的選取範圍時，這個方法一定會取得與特定視圖相關聯的範圍。                                                                                 |
| [**展開**](/windows/desktop/api/Tom/nf-tom-itextrange-expand)                    | 將文字範圍放大，讓它包含的任何部分單元都完全包含在其中。 例如， `Expand(tomWindow)` 展開範圍，以包含範圍案例的可見部分。 |
| [**GetDuplicate**](/windows/desktop/api/Tom/nf-tom-itextrange-getduplicate)        | 使用於作用中的選取範圍時，這個方法一定會取得與特定視圖相關聯的範圍。 請參閱 [**RangeFromPoint**](/windows/desktop/api/Tom/nf-tom-itextdocument-rangefrompoint)的描述。  |
| [**GetPoint**](/windows/desktop/api/Tom/nf-tom-itextrange-getpoint)                | 取得文字範圍中開始或結束字元位置的螢幕座標。                                                                                                        |
| [**ScrollIntoView**](/windows/desktop/api/Tom/nf-tom-itextrange-scrollintoview)    | 將文字範圍滾動到視野中。                                                                                                                                                               |
| [**SetPoint**](/windows/desktop/api/Tom/nf-tom-itextrange-setpoint)                | 選取一或多個指定點上的文字。                                                                                                                                              |



 

## <a name="character-match-sets"></a>字元相符集

ITextRange 中各種 **移動** \* 方法（例如 [**MoveWhile**](/windows/desktop/api/Tom/nf-tom-itextrange-movewhile)和 [](/windows/desktop/api/Tom/nn-tom-itextrange) [**MoveUntil**](/windows/desktop/api/Tom/nf-tom-itextrange-moveuntil)）的 variant 參數可以採用明確字串或字元相符設定32位索引。 索引是由 Unicode 範圍或 [**GetStringTypeEx**](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw) 字元集所定義。 開頭為 *n* 且長度為 *l* (< 32768) 的 Unicode 範圍是由索引 *n* + (*l <*< 16) + 0x80000000 提供。 例如，基本希臘字元是由 CR \_ 希臘文 = 0x805f0370 所定義，且可列印的 ASCII 字元是由 cr \_ ASCIIPrint = 0x805e0020 所定義。 此外， **MoveWhile** 和 **MoveUntil** 方法可讓您快速略過任何 **GetStringTypeEx** 字元集中的字元範圍，或在不屬於任何這些字元集的字元範圍中。

[**GetStringTypeEx**](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw)集是由 *Ctype1*、 *Ctype2* 和 *Ctype3* 的值所指定，並定義如下。



| Cset                 | 意義                          |
|----------------------|----------------------------------|
| *Ctype1*             | CT \_ CTYPE1 類型的組合。 |
| *Ctype2* + tomCType2 | 任何 \_ 的 CT CTYPE2 類型。             |
| *Ctype3* + tomCType3 | CT \_ CTYPE3 類型的組合。 |



 

具體而言， *Ctype1* 可以是下列各項的任何組合。



| Ctype1 名稱 | 值  | 意義                                                           |
|-------------|--------|-------------------------------------------------------------------|
| C1 \_ 上層   | 0x0001 | 大寫。                                                        |
| C1 \_ 較低   | 0x0002 | 小寫。                                                        |
| C1 \_ 位數   | 0x0004 | 十進位數。                                                   |
| C1 \_ 空間   | 0x0008 | 空白字元。                                                 |
| C1 \_ PUNCT   | 0x0010 | 標點符號。                                                      |
| C1 \_ 控制項   | 0x0020 | 控制字元。                                               |
| C1 \_ 空白   | 0x0040 | 空白字元。                                                 |
| C1 \_ XDIGIT  | 0x0080 | 十六進位數位。                                               |
| C1 \_ ALPHA   | 0x0100 | 任何語言字元 (字母、音節或象形) 。 |
| \_定義 C1 | 0x0200 | 定義的字元，但不是其他任何 C1 類型的其中一個 \_ \* 。       |



 

*Ctype2* 類型支援 Unicode 文字的適當版面配置。 指派 direction 屬性，讓以 Unicode 標準化的雙向配置演算法產生精確的結果。 這兩種類型是互斥的。 如需有關使用這些屬性的詳細資訊，請參閱 *Unicode 標準：全球字元編碼、磁片區1和 2*，Addison-Wesley 發佈公司：1991、1992。



| CType2 名稱          | 值 | 意義                          |
|----------------------|-------|----------------------------------|
| 強：              |       |                                  |
| C2 \_ LEFTTORIGHT      | 0x1   | 由左至右。                   |
| C2 \_ RIGHTTOLEFT      | 0x2   | 由右至左。                   |
| 弱：                |       |                                  |
| C2 \_ EUROPENUMBER     | 0x3   | 歐洲數位、歐洲數位。 |
| C2 \_ EUROPESEPARATOR  | 0x4   | 歐洲數位分隔符號。      |
| C2 \_ EUROPETERMINATOR | 0x5   | 歐洲數值結束字元。     |
| C2 \_ ARABICNUMBER     | 0x6   | 阿拉伯文數位。                   |
| C2 \_ COMMONSEPARATOR  | 0x7   | 一般數值分隔符號。        |
| 中性：             |       |                                  |
| C2 \_ BLOCKSEPARATOR   | 0x8   | 區塊分隔符號。                 |
| C2 \_ SEGMENTSEPARATOR | 0x9   | 區段分隔符號。               |
| C2 \_ 空白字元       | 0xA   | 空白字元。                     |
| C2 \_ OTHERNEUTRAL     | 0xB   | 其他 neutrals。                  |
| 不適用：      |       |                                  |
| C2 \_ NOTAPPLICABLE    | 0x0   | 無隱含方向。           |



 

*Ctype3* 型別旨在做為一般文字處理或標準 C 程式庫函式所需的 POSIX 類型之擴充功能的預留位置。



| CType3 名稱       | 值  | 意義                                                             |
|-------------------|--------|---------------------------------------------------------------------|
| C3 非 \_ 間距    | 0x1    | 非間距標記。                                                    |
| C3 \_ 變音符號     | 0x2    | 變音符號非間距標記。                                          |
| C3 \_ VOWELMARK     | 0x4    | 母音非間距標記。                                              |
| C3 \_ 符號        | 0x8    | 象徵。                                                             |
| C3 \_ 片假名      | 0x10   | 片假名字元。                                                 |
| C3 \_ 平假名      | 0x20   | 平假名字元。                                                 |
| C3 \_ 半形     | 0x40   | 半形字元。                                               |
| C3 \_ 全形     | 0x80   | 全形字元。                                               |
| C3 \_ 表意文字     | 0x100  | 表意字元。                                              |
| C3 \_ KASHIDA       | 0x200  | 阿拉伯文 Kashida 字元。                                           |
| C3 \_ ALPHA         | 0x8000 | 所有語言字元都 (字母、音節和象形) 。 |
| C3 \_ NOTAPPLICABLE | 0x0    | 不適用。                                                     |



 

編輯開發工具組 (EDK) 可能包含 Unicode 標準所述之下列範圍的 *pVar* 索引定義。



| 字元集         | Unicode 範圍 | 字元集             | Unicode 範圍 |
|-----------------------|---------------|---------------------------|---------------|
| ASCII                 | 0x0-0x7f      | ANSI                      | 0x0-0xff      |
| ASCIIPrint            | 0x20-0x7e     | 採用 latin1-general                    | 0x20-0xff     |
| Latin1Supp            | 0xa0-0xff     | LatinXA                   | 0x100-0x17f   |
| LatinXB               | 0x180—0x24f   | IPAX                      | 0x250—0x2af   |
| SpaceMod              | 0x2b0—0x2ff   | 結合                 | 0x300—0x36f   |
| 希臘文                 | 0x370—0x3ff   | BasicGreek                | 0x370—0x3cf   |
| GreekSymbols          | 0x3d0—0x3ff   | 古斯拉夫文                  | 0x400-0x4ff   |
| 亞美尼亞文              | 0x530—0x58f   | Hebrew                    | 0x590—0x5ff   |
| BasicHebrew           | 0x5d0—0x5ea   | HebrewXA                  | 0x590—0x5cf   |
| HebrewXB              | 0x5eb—0x5ff   | 阿拉伯文                    | 0x600—0x6ff   |
| BasicArabic           | 0x600—0x652   | ArabicX                   | 0x653—0x6ff   |
| Devangari             | 0x900—0x97f   | 孟加拉國文 (先前為孟加拉國文)  | 0x980—0x9ff   |
| 古木基文              | 0xa00—0xa7f   | 古吉拉特文                  | 0xa80—0xaff   |
|  (以前的奧裡亞文)  | 0xb00—0xb7f   | 坦米爾文                     | 0xb80—0xbff   |
| Teluga                | 0xc00—0xc7f   | 坎那達文                   | 0xc80—0xcff   |
| 馬來亞拉姆文             | 0xd00—0xd7f   | 泰文                      | 0xe00—0xe7f   |
| 寮文                   | 0xe80—0xeff   | GeorgianX                 | 0x10a0—0xa0cf |
| BascGeorgian          | 0x10d0—0x10ff | 拼音字母                      | 0x1100—0x11ff |
| LatinXAdd             | 0x1e00—0x1eff | GreekX                    | 0x1f00—0x1fff |
| GenPunct              | 0x2000 —0x206f | 標               | 0x2070—0x207f |
| 標             | 0x2080—0x208f | SuperSubscript            | 0x2070—0x209f |
| 貨幣              | 0x20a0—0x20cf | CombMarkSym               | 0x20d0—0x20ff |
| 字母            | 0x2100—0x214f | NumberForms               | 0x2150—0x218f |
| 箭頭                | 0x2190—0x21ff | MathOps                   | 0x2200—0x22ff |
| MiscTech              | 0x2300—0x23ff | CtrlPictures              | 0x2400—0x243f |
| OptCharRecog          | 0x2440—0x245f | EnclAlphaNum              | 0x2460—x24ff  |
| BoxDrawing            | 0x2500—0x257f | BlockElement              | 0x2580—0x259f |
| GeometShapes          | 0x25a0—0x25ff | MiscSymbols               | 0x2600—0x26ff |
| Dingbats              | 0x2700—0x27bf | CJKSymPunct               | 0x3000—0x303f |
| 平假名              | 0x3040—0x309f | 片假名                  | 0x30a0—0x30ff |
| 符號              | 0x3100—0x312f | HangulJamo                | 0x3130—0x318f |
| CJLMisc               | 0x3190—0x319f | EnclCJK                   | 0x3200—0x32ff |
| CJKCompatibl          | 0x3300—0x33ff | 漢                       | 0x3400—0xabff |
| 韓文                | 0xac00—0xd7ff | UTF16Lead                 | 0xd800-0xdbff |
| UTF16Trail            | 0xdc00-0xdfff | PrivateUse                | 0xe000—0xf800 |
| CJKCompIdeog          | 0xf900—0xfaff | AlphaPres                 | 0xfb00—0xfb4f |
| ArabicPresA           | 0xfb50—0xfdff | CombHalfMark              | 0xfe20—0xfe2f |
| CJKCompForm           | 0xfe30—0xfe4f | SmallFormVar              | 0xfe50—0xfe6f |
| ArabicPresB           | 0xfe70—0xfefe | HalfFullForm              | 0xff00—0xffef |
| 特價              | 0xfff0—0xfffd |                           |               |



 

 

 