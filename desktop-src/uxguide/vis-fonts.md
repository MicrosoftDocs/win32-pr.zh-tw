---
title: 字型
description: 使用者與文字的互動比 Microsoft Windows 中的任何其他元素更多。 Segoe UI (發音為 \ 0034;請參閱-go \ 0034; ) 是 Windows 系統字型。 標準字型大小已增加至9點。
ms.assetid: 6d4f669d-d28c-4585-9bc3-ecda44de6df5
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 7ac9f725349433f1cd5f2070b0c80d86acb9d8b3f4d9537cc14375d977283620
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119816479"
---
# <a name="fonts"></a>字型

> [!NOTE]
> 此設計指南是針對 Windows 7 所建立，而且尚未針對較新的 Windows 版本進行更新。 大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。

使用者與文字的互動比 Microsoft Windows 中的任何其他元素更多。 Segoe UI (發音為「看不到」 ) 是 Windows 系統字型。 標準字型大小已增加至9點。

![segoe ui 字型中的字母圖例 ](images/vis-fonts-image1.png)

Segoe UI 字型。

Segoe UI 和 Segoe 都不是相同的字型。 Segoe UI 是適用于使用者介面文字字串的 Windows 字型。 Segoe 是 Microsoft 和合作夥伴所使用的商標字型，可產生列印和廣告的材質。

Segoe UI 是平易近人、開放且易記的字型，因此其可讀性比 Tahoma、Microsoft Sans Serif 和 Arial 更好。 它具有 humanist sans serif 的特性：其大寫字母的變化寬度 (窄的 E 和 S，例如，相較于 Helvetica，寬度較大、相當大的) ;其小寫的壓力和 letterforms;而且它的真斜體 (而不是「傾斜」或傾斜的羅馬，像是許多產業上的大型雙襯線) 。 字樣的目的是要在螢幕上和列印中提供相同的視覺效果。 它是設計成 humanist 的 sans serif，沒有強字元或 quirkiness。

Segoe UI 已針對 ClearType 優化，在 Windows 中預設為開啟。 啟用 ClearType 之後，Segoe UI 是簡潔、可讀取的字型。 若未啟用 ClearType，Segoe UI 只會被接受。 此因素決定您應該使用 Segoe UI 的時機。

Segoe UI 包括拉丁、希臘文、斯拉夫文和阿拉伯文字元。 針對其他字元集和使用所建立的新字型，也有最適合 ClearType 的設定。 這些包括 Meiryo for 日文、Malgun Mt for 韓文、Microsoft)  (JhengHei （繁體中文）、Microsoft YaHei for 中文 (簡體) 、Gisha for 希伯來文和 Leelawadee for 泰文，以及為檔使用而設計的 ClearType 集合字型。

Meiryo 包含以 Verdana 為基礎的拉丁字元。 Malgun Mt、Microsoft JhengHei 和 Microsoft YaHei 使用自訂的 Segoe UI。 不建議使用這些字型的斜體版本。 Malgun Mt、Microsoft JhengHei 和 Microsoft YaHei 僅以一般和粗體樣式提供，表示斜體字元是透過斜指直立的樣式來合成。 雖然 Meiryo 包含 true 斜體和粗體斜體，但這些樣式只適用于套用斜體樣式時，日文字元保持直立的拉丁字元。

[功能區](cmd-ribbons.md)命令使用者介面中偏好 Meiryo 的變化，稱為 Meiryo UI。

為了支援使用這些字元集的地區設定，Segoe UI 會根據 [當地語系化](glossary.md) 程式期間的每個地區設定，以正確的字型取代。

若要使用以 Windows 為基礎的程式散發授權 Segoe UI 及其他 Microsoft 字型，請聯絡[Monotype](https://www.monotype.com/)。

**注意：** 與 [樣式和語氣](text-style-tone.md) 和 [使用者介面文字](text-ui.md) 相關的指導方針會顯示在不同的文章中。

## <a name="design-concepts"></a>設計概念

### <a name="fonts-typefaces-point-sizes-and-attributes"></a>字型、字體、點大小和屬性

在傳統印刷樣式中，字型會描述字型、點大小和屬性的組合。 字型是字型的外觀。 Segoe UI、Tahoma、Verdana 和 Arial 都是字體。 「點大小」是指字型的大小，從 ascenders 的頂端算起到下行底部，減去內部間距 (稱為「前置) 」。 點大約是1/72 英寸。 最後，字型可以有粗體或斜體的屬性。

非正式地說，人們通常會使用字型來取代在本文中完成的字型，但是在技術上，Segoe UI 是一種字型，而非字型。 每個屬性的組合都是唯一的字型 (例如9點 Segoe UI 一般、10點 Segoe UI 粗體等) ）。

### <a name="serif-and-sans-serif"></a>Serif 和 sans serif

字體是 serif 或 sans serif。 Serif 是指通常會在字型中完成字母筆劃的小回合。 「Sans serif」字樣沒有襯線。

讀者通常會偏好使用在檔中當做內文文字使用的 serif 字型。 襯線可讓您感受到檔的俗套和優雅。 針對 UI 文字，乾淨外觀的需求和較低的電腦監視器解析度，讓 san serif 成為更好的選擇。

### <a name="contrast"></a>這個

當文字與背景的亮度之間有很大的差異時，最容易閱讀文字。 白色背景上的黑色文字會在非常淺的背景提供最高對比深色文字，也可以提供高對比。 這種組合最適合主要的 UI 表面。

深色背景的淺色文字提供良好的對比，但不像淺色背景上的深色文字一樣。 此組合適用于您想要特別強調主要 UI 介面的次要 UI 介面，例如 Explorer 工作窗格。

**如果您想要確保使用者閱讀您的文字，請在淺色背景使用深色文字。**

### <a name="affordances"></a>Affordances

文字可以使用下列 [affordances](glossary.md) 來指出其使用方式：

-   **指標。** I-bar ( 「文字選取」 ) 指標表示可以選取文字，而左方箭號 ( 「一般 select」 ) 指標則表示文字不是。
-   **字.** 當文字具有輸入焦點時，插入點會是閃爍的垂直線，表示可選取或可編輯文字中的插入/選取點。
-   **箱。** 文字周圍的方塊，表示它是可編輯的。 若要減少簡報的權數，只有在選取了可編輯的文字時，方塊才會動態顯示。
-   **前景色彩。** 淺灰色表示文字已停用。 非灰色色彩（特別是藍色和紫色）表示文字是連結。
-   **背景色彩。** 淺灰色背景弱表示文字是唯讀的，但實際上唯讀文字可以具有任何色彩背景。

這些 affordances 會結合下列意義：

-   **編輯。** 顯示在方塊中的文字，其中包含文字選取指標、輸入焦點 (輸入焦點) ，而且通常會在白色背景上。
-   **唯讀，可選取。** 具有選取指標的文字，以及輸入焦點)  (插入號。
-   **唯讀、不可選取。** 具有箭號指標的文字。
-   **已停用。** 具有箭號指標的淺灰色文字，有時會在灰色背景上。

唯讀文字通常會有灰色背景，但不需要灰色背景。 事實上，灰色背景可能不需要，尤其是針對大型文字區塊，因為這表示文字已停用且不鼓勵閱讀。

### <a name="accessibility-and-the-system-font-sizes-and-colors"></a>存取範圍和系統字型、大小和色彩

讓殘障人士或殘障人士存取文字的指導方針，可以爆發到一個簡單的規則：一律使用系統字型、大小和色彩，以尊重使用者的設定。

**如果您只做一件事 .。。**

一律使用系統字型、大小和色彩，以尊重使用者的設定。

**開發人員：** 您可以從程式碼判斷系統字型屬性 (包括其大小) 使用 GetThemeFont API 函數。 您可以使用 GetThemeSysColor API 函數來判斷系統色彩。

因為您無法對使用者的系統主題設定做出任何假設，所以您應該：

-   一律以系統主題色彩作為字型色彩和背景。 切勿根據固定 RGB (紅色、綠色、藍色) 值來建立您自己的色彩。
-   一律符合系統文字色彩與其對應的背景色彩。 例如，如果您選擇 [色彩 \_ STATICTEXT] 做為文字色彩，您也必須選擇 [色彩靜態] 做 \_ 為背景色彩。
-   一律根據系統字型的比例大小變化來建立新字型。 由於系統字型的度量，您可以建立粗體、斜體、更大和較小的變化。

**有一個簡單的方法可確保您的程式遵循使用者的設定，就是使用不同的字型大小和高對比色彩配置來進行測試。** 所有文字都應該調整大小，並在選擇的色彩配置中正確顯示。

## <a name="usage-patterns"></a>使用模式

文字有數種使用模式：



|    使用量                                         |    描述                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| **標題列文字**<br/> 標題列上用來識別視窗的文字。<br/>                                                                                                                                                                | ![標題列文字字型的範例 ](images/vis-fonts-image2.png)<br/>                                                                            |
| **主要指示**<br/> 說明要在頁面、視窗或對話方塊上做些什麼的文字。 <br/>                                                                                                                                              | ![主要指示文字字型的範例 ](images/vis-fonts-image3.png)<br/>                                                                    |
| **次要指示**<br/> 說明如何在頁面、視窗或對話方塊上進行的補充文字。 <br/>                                                                                                                            | ![次要指示文字字型的範例 ](images/vis-fonts-image4.png)<br/>                                                               |
| **一般文字**<br/> 一般 (唯讀) 使用者介面中顯示的文字。 <br/>                                                                                                                                                           | ![一般文字字型的範例 ](images/vis-fonts-image5.png)<br/>                                                                               |
| **強調文字**<br/> 粗體文字是用來讓文字更容易剖析，並且吸引使用者必須閱讀的文字。 斜體文字用來說出文字 (而非引號) 和強調特定字組。 <br/> | ![強調文字字型的範例 ](images/vis-fonts-image6.png)<br/>                                                                           |
| **可編輯的文字**<br/> 使用者可以編輯的文字會顯示在方塊中。 若要減少簡報的權數，只有在選取了可編輯的文字時，才會顯示方塊。 <br/>                                                          | ![可編輯文字字型的範例 ](images/vis-fonts-image7.png)<br/>                                                                             |
| **停用的文字**<br/> 未套用至目前內容的文字，例如停用控制項的標籤。 停用的文字表示使用者 (正常) 不應擔心讀取文字。 <br/>                                           | ![停用文字字型的範例 ](images/vis-fonts-image8.png)<br/>                                                                             |
| **連結**<br/> 用來流覽至另一個頁面、視窗或說明主題，或起始命令的文字。 <br/>                                                                                                                                     | ![連結文字字型的範例 ](images/vis-fonts-image9.png)<br/> ![ (將滑鼠停留) 文字字型的連結範例 ](images/vis-fonts-image10.png)<br/> |
| **群組標頭**<br/> 用來在清單視圖中群組專案的文字。 <br/>                                                                                                                                                                          | ![群組標頭文字字型的範例 ](images/vis-fonts-image11.png)<br/>                                                                        |
| **檔案名稱**<br/> 只有) ，才 (內容視圖中的檔案名文字。 <br/>                                                                                                                                                                               | ![內容視圖中的檔案名 (範例) 文字字型 ](images/vis-fonts-image12.png)<br/>                                                         |
| **檔文字**<br/> 檔中使用的文字 (與 ui 文字) 相反。 <br/>                                                                                                                                                                  | ![檔文字字型的範例 ](images/vis-fonts-image13.png)<br/>                                                                            |
| **檔標題**<br/> 在檔中當做標題使用的文字。 <br/>                                                                                                                                                                    | ![檔標題文字字型的範例 ](images/vis-fonts-image14.png)<br/>                                                                   |



 

## <a name="guidelines"></a>指導方針

### <a name="fonts-and-colors"></a>字型和色彩

-   **下列字型和色彩是 Windows Vista 和 Windows 7 的預設值。**



| 模式 | 主題符號 | 字型、色彩 |
|-----------------------------------------------------------------------------------------------|-----------------------------|------------------------------------------------------------|
| ![標題列文字字型的範例 ](images/vis-fonts-image2.png)<br/>                    | CaptionFont<br/>      | 9 pt。 黑色 (\# 000000) Segoe UI<br/>                 |
| ![主要指示文字字型的範例 ](images/vis-fonts-image3.png)<br/>            | MainInstruction<br/>  | 12 pt。 藍色 (\# 003399) Segoe UI<br/>                 |
| ![次要指示文字字型的範例 ](images/vis-fonts-image4.png)<br/>       | 指令<br/>      | 9 pt。 黑色 (\# 000000) Segoe UI<br/>                 |
| ![一般文字字型的範例 ](images/vis-fonts-image5.png)<br/>                       | BodyText<br/>         | 9 pt。 黑色 (\# 000000) Segoe UI<br/>                 |
| ![強調文字字型的範例 ](images/vis-fonts-image6.png)<br/>                   | BodyText<br/>         | 9 pt。 黑色 (\# 000000) Segoe UI、粗體或斜體<br/> |
| ![可編輯文字字型的範例 ](images/vis-fonts-image7.png)<br/>                     | BodyText<br/>         | 9 pt。 \#box 中的黑色 (000000) Segoe UI<br/>       |
| ![停用文字字型的範例 ](images/vis-fonts-image8.png)<br/>                     | 已停用<br/>         | 9 pt。 暗灰色 (\# 323232) Segoe UI<br/>             |
| ![連結文字字型的範例 ](images/vis-fonts-image9.png)<br/>                         | HyperLinkText<br/>    | 9 pt。 blue (\# 0066CC) Segoe UI<br/>                  |
| ![ (將滑鼠停留) 文字字型的連結範例 ](images/vis-fonts-image10.png)<br/>               | 經常性存取層<br/>              | 9 pt。 淺藍色 (\# 3399FF) Segoe UI<br/>            |
| ![群組標頭文字字型的範例 ](images/vis-fonts-image11.png)<br/>                |                             | 11 pt。 藍色 (\# 003399) Segoe UI<br/>                 |
| ![內容視圖中的檔案名 (範例) 文字字型 ](images/vis-fonts-image12.png)<br/> |                             | 11 pt。 黑色 (\# 000000) Segoe UI<br/>                |
| ![檔文字字型的範例 ](images/vis-fonts-image13.png)<br/>                    | (無)<br/>           | 9 pt。 黑色 (\# 000000) Calibri<br/>                  |
| ![檔標題文字字型的範例 ](images/vis-fonts-image14.png)<br/>           | (無)<br/>           | 17 pt。 黑色 (\# 000000) Calibri<br/>                 |



 

-   **根據 UI 技術和目標版本的 Windows，選擇 [字型] 和 [優化視窗版面配置]：**



| UI 技術 | 目標 Windows 版本 | 使用和優化的字型 |
|--------------------------------------------|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Presentation Foundation<br/> | 全部<br/>                                        | 使用 WPF 主題元件。<br/>                                                                                                                                                                                                                                                                                                                                  |
| Win32 或 WinForms<br/>               | Windows Vista 或更新版本<br/>                     | 使用適當的 Segoe UI 字型。<br/>                                                                                                                                                                                                                                                                                                                    |
|                                            | 可擴充元件或預先 Windows Vista<br/> | 若要以 Windows XP 和 Windows 2000 為目標，請使用8點 MS Shell Dlg 2 虛擬字型，其會對應至 Tahoma。<br/> 若要以舊版的 Windows 為目標，請使用8點 MS Shell Dlg 虛擬字型，其對應至 Windows 2000 和 Windows XP 上的 Tahoma，以及 Windows 95、Windows 98、Windows Millennium Edition 和 Windows NT 4.0 的 MS Sans Serif。<br/> |



 

-   **開發 人員：**
    -   針對使用固定配置 (例如 Windows 對話方塊範本和 WinForms) 的元素，請將上表中的適當字型硬編碼。
    -   針對使用動態配置 (例如 Windows Presentation Foundation) 的元素，請使用主題字型。 使用主題 Api （例如 DrawThemeText），根據主題符號來繪製文字。 如果主題服務未執行，請務必根據系統計量進行替代。
-   **針對 Segoe UI，請使用9個點或更大的字型大小。** Segoe UI 字型已針對這些大小進行優化，因此請避免使用較小的大小。
-   **一律符合系統文字色彩與其對應的背景色彩。** 例如，如果您選擇 [色彩 \_ STATICTEXT] 做為文字色彩，您也必須選擇 [色彩靜態] 做 \_ 為背景色彩。
-   **一律根據系統字型的比例大小變化來建立新字型。** 由於系統字型的度量，您可以建立粗體、斜體、更大和較小的變化。
-   顯示較長的唯讀文字區塊 (例如針對淺色背景的授權) 條款，而非灰色背景。 灰色背景建議將文字停用並防止閱讀。
-   **請考慮使用65個字元的最大行長度** ，讓文字更容易閱讀。  (字元包含字母、標點符號和空格。 ) 

### <a name="attributes"></a>屬性

-   大部分的 UI 文字都應該是純文字，而不含任何屬性。 您可以使用屬性，如下所示：
    -   **大膽。** 使用控制標籤可讓您更輕鬆地剖析文字。 請謹慎使用，以吸引使用者必須閱讀的文字。 使用太多粗體會減少其影響。
    -   **斜。** 用來說出文字，而非引號。 請謹慎使用以強調特定字組。 用於[文字方塊](ctrl-text-boxes.md)中的[提示](glossary.md)和[可編輯的下拉式清單](/windows/desktop/uxguide/ctrl-drop)。
    -   **粗體斜體。** 請勿使用。
    -   **強調。** 請勿使用連結以外的。 請改用斜體來強調。
-   並非所有字型都支援粗體和斜體，因此對於瞭解文字來說絕對不重要。

