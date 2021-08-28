---
title: 關於 Rich Edit 控制項
description: 本節介紹 rich edit 控制項。
ms.assetid: ab9dcdf4-a311-4159-8f37-e67e144f31f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 314e41747ae0d55ca1010df31dee1522527eadb3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470195"
---
# <a name="about-rich-edit-controls"></a>關於 Rich Edit 控制項

本節將討論下列主題。

-   [Rich Edit 的版本](#versions-of-rich-edit)
    -   [Rich Edit 1.0 版](#rich-edit-version-10)
    -   [Rich Edit 2.0 版](#rich-edit-version-20)
    -   [Rich Edit 3.0 版](#rich-edit-version-30)
    -   [Rich Edit 4.1 版](#rich-edit-version-41)
-   [不支援的編輯控制項功能](#unsupported-edit-control-functionality)
-   [Rich Edit 快速鍵](#rich-edit-shortcut-keys)
-   [相關主題](#related-topics)

## <a name="versions-of-rich-edit"></a>Rich Edit 的版本

Rich edit 控制項的原始規格是 Microsoft Rich Edit 1.0;目前的規格是 Microsoft Rich Edit 4.1。 Rich edit 的每個版本都是前一個版本的超集合，但只有 Microsoft Rich Edit 1.0 的亞洲組建具有垂直文字選項。 在建立 rich edit 控制項之前，您應該呼叫 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 函式來確認已安裝的 Microsoft rich edit 版本。

下表顯示哪個 DLL 對應到哪個版本的 Rich Edit。 請注意，檔案的名稱不會從2.0 版變更為3.0 版。 這可讓版本2.0 升級為3.0 版，而不會中斷現有的程式碼。



| Rich Edit 版本 | DLL          | 視窗類別    |
|-------------------|--------------|-----------------|
| 1.0               | Riched32.dll | RICHEDIT \_ 類別 |
| 2.0               | Riched20.dll | RICHEDIT \_ 類別 |
| 3.0               | Riched20.dll | RICHEDIT \_ 類別 |
| 4.1               | Msftedit.dll | MSFTEDIT.DLL \_ 類別 |



 

### <a name="rich-edit-version-10"></a>Rich Edit 1.0 版

Microsoft Rich Edit 1.0 包含下列功能。



|    功能   | 描述   |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 文字輸入和選取                                                           | 大部分是標準 (系統編輯控制項) 選取專案和文字專案。 選取列支援 (選取專案列是每個段落左邊的未標記區域，當按下時，會選取該行) 。 自動換行和自動單字選取選項。 單一、雙和三次的選取專案。 |
| ANSI (單一位元組字元集 (SBCS) 和多位元組字元集 (MBCS) ) 編輯 | 但是，並沒有 Unicode 編輯。                                                                                                                                                                                                                                                     |
| 一組基本的字元/段落格式化屬性                             | 請參閱 [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) 和 [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat)。                                                                                                                                                                                                                |
| 字元格式屬性                                                    | 字型名稱和大小、粗體、斜體、實線、刪除線、受保護、連結、位移和文字色彩。                                                                                                                                                                                   |
| 段落格式化屬性                                                    | 開始縮排、靠右縮排、後續的行位移、專案符號、對齊 (左、置中、靠右) 和索引標籤。                                                                                                                                                                                    |
| 向前尋找                                                                       | 包含不區分大小寫且符合全字的選項。                                                                                                                                                                                                                                   |
| 以訊息為基礎的介面                                                            | 幾乎是系統編輯控制訊息集的超集合，還有兩個介面： [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) 和 [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback)。                                                                                                              |
| 內嵌物件                                                                   | 需要以 [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) 和 [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) 介面為基礎的用戶端協同作業。                                                                                                                                          |
| 右鍵按鈕功能表支援                                                          | 使用 [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) 介面。                                                                                                                                                                                                                      |
| 拖放編輯                                                              | 支援拖放編輯。                                                                                                                                                                                                                                                       |
| 通知                                                                      | [**WM \_**](/windows/desktop/menurc/wm-command)傳送給用戶端的命令訊息加上其他數。 這是一般控制項通知的超集合。                                                                                                                                                 |
| 單一層級的復原/重做                                                             | 行為類似于系統編輯控制項。 選取 [ **復原** ] 會反轉最後一個動作，然後該動作就會變成新的 **重做** 動作。                                                                                                                                          |
| 簡單的垂直文字                                                               |  (亞洲組建僅) 。                                                                                                                                                                                                                                                                      |
| 輸入法編輯器 (IME) 支援                                                  |  (亞洲組建僅) 。                                                                                                                                                                                                                                                                      |
| 使用印表機計量進行 WYSIWYG 編輯                                              | 尤其是 Microsoft WordPad 需要這項功能。                                                                                                                                                                                                                              |
| 剪下/複製/貼上/StreamIn/StreamOut                                                  | 純文字 (**CF \_ Text**) 或 RTF 格式 (rtf) with 和不包含物件。                                                                                                                                                                                                        |
| C 程式碼基底                                                                        | 程式碼是以 C 撰寫，可提供穩固且多功能的基礎。                                                                                                                                                                                                                |
| 不同腳本的不同組建                                             | Microsoft Rich Edit 1.0 解決了不同組建的當地語系化問題。                                                                                                                                                                                                              |



 

### <a name="rich-edit-version-20"></a>Rich Edit 2.0 版

Microsoft Rich Edit 2.0 併入了幾項額外的功能，例如支援 Unicode 和亞洲語言、多層復原、元件物件模型 (COM) 介面，以及許多 UI 增強功能。

除了 [Microsoft Rich edit 1.0](#rich-edit-version-10)提供的功能之外，Microsoft rich edit 2.0 還包含下列功能。



|    功能                                           |    描述                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unicode                                       | Unicode 能簡化處理國際文字的工作。 不過，為了維持與現有非 Unicode 檔的相容性，您也需要投入精力，也就是轉換成非 Unicode 純文字和 rtf 文字的能力。                                                                                                                                                             |
| 一般國際支援                 | 一般分行符號演算法 (延伸的避避規則) 、簡單字型連結、鍵盤字型切換。                                                                                                                                                                                                                                                                          |
| 亞洲支援                                 | [層級 2 (] 對話方塊) 和 (3 個 [Ime] 支援內嵌) 。                                                                                                                                                                                                                                                                                                                            |
| 尋找/找出支援                     | 支援向前及向後搜尋。                                                                                                                                                                                                                                                                                                                                         |
| 雙向支援                         | 這包含在 Microsoft Rich Edit 2.1 中                                                                                                                                                                                                                                                                                                                                          |
| 多層次復原                               | 可延伸的復原架構可讓用戶端參與整個應用程式的復原模型。                                                                                                                                                                                                                                                                                         |
| Magellan 滑鼠支援                        | 這是具有捲軸以供滾動的滑鼠。                                                                                                                                                                                                                                                                                                                                       |
| 雙重字型支援                             | 當現用字型不適用於目前的鍵盤時，鍵盤可以自動切換字型，例如，新羅馬的中文字元。                                                                                                                                                                                                                            |
| 智慧型字型適用                              | 字型變更要求不會將西方字型套用到亞洲字元。                                                                                                                                                                                                                                                                                                                |
| 改善顯示                              | 當有多個字型出現在同一行時，就會使用螢幕點陣圖。 例如，這可讓您無法切碎單字的最後一個字母。                                                                                                                                                                                                                           |
| 透明度支援                          | 也可在無視窗模式中進行。                                                                                                                                                                                                                                                                                                                                                             |
| 系統選取色彩                       | 用來選取文字。                                                                                                                                                                                                                                                                                                                                                             |
| 自動 URL 辨識                     | 可以檢查數個 URL 格式 (例如，HTTP： )                                                                                                                                                                                                                                                                                                                            |
| Microsoft Word 編輯 UI 相容性          | 選取範圍，方向鍵的語義。                                                                                                                                                                                                                                                                                                                                                  |
| 單字標準 EOP                             | 段落結束記號 (CR) 也可以處理換行字元/換行字元 (CR/LF)  (換行字元、換行字元) 。                                                                                                                                                                                                                                                                       |
| 純文字及豐富文字功能 | 單一字元格式和單一段落格式。                                                                                                                                                                                                                                                                                                                                 |
| 單行和多行控制項            | 在第一段結束時截斷，不 wordwrap。                                                                                                                                                                                                                                                                                                                                  |
| 快速鍵                              | 支援快速鍵。                                                                                                                                                                                                                                                                                                                                                      |
| 密碼視窗樣式                         | 密碼編輯控制項是透過 [**em \_ GETPASSWORDCHAR**](em-getpasswordchar.md) 和 [**em \_ SETPASSWORDCHAR**](em-setpasswordchar.md)提供。                                                                                                                                                                                                                                 |
| 可擴充的架構                         | 以減少實例大小。                                                                                                                                                                                                                                                                                                                                                             |
| 無視窗操作和介面           | 這是透過 [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) 和 [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) 介面提供。                                                                                                                                                                                                                                                                   |
| COM 雙重介面                           |  (TOM) 介面的文字物件模型。                                                                                                                                                                                                                                                                                                                                                  |
| CHARFORMAT2                                   | 新增字型粗細、背景色彩、地區設定識別碼、底線類型、上標和下標 (除了位移) 、停用效果之外。 僅限 RTF roundtripping，在字母之間新增空間、在上方調整字元配對的 twip 大小、動畫文字類型、各種效果：字型陰影/外框、所有大寫字母、小型大寫字母、隱藏、浮凸、粗體和修訂。 |
| PARAFORMAT2                                   | 在前後加入空格和文字行間距。 僅適用于 RTF roundtripping，新增陰影粗細/樣式、編號開始/樣式/索引標籤、框線空間/寬度/側邊、定位對齊/領導人、各種單欄位落效果： RTL 段落、保留、保留下、分頁符號之前、無行號、非孤行控制、不使用斷字、並存。                                         |
| 更多 RTF roundtripping                        | 所有 Word FormatFont 和 FormatParagraph 屬性。                                                                                                                                                                                                                                                                                                                           |
| 程式碼穩定性和穩定              | 範例：參數和物件驗證、函式不變數、重新進入防護、物件穩定。                                                                                                                                                                                                                                                                             |
| 強大的測試基礎結構                 | 包括廣泛的迴歸測試。                                                                                                                                                                                                                                                                                                                                               |
| 提升效能                          | 較小的工作集、更快速的載入和重新顯示時間等等。                                                                                                                                                                                                                                                                                                                     |
| C + + 程式碼基底                                 | 這段程式碼是以 c + + 撰寫，可提供建立 Microsoft Rich Edit 3.0 的穩固基礎。                                                                                                                                                                                                                                                                             |



 

但有一些例外狀況，Microsoft Rich Edit 2.0 會使用與 Microsoft Rich Edit 1.0 相同的功能、結構和訊息。 不過，請注意下列差異：

-   Microsoft Rich Edit 1.0 視窗類別的名稱是 **RichEdit**。 Microsoft Rich Edit 2.0 分別具有 **RichEdit20A** 和 **RichEdit20W** 的 ANSI 和 Unicode 視窗類別。 若要指定適當的 rich edit 視窗類別，請使用 RICHEDIT \_ 類別常數，RICHEDIT .h 檔案會根據 UNICODE 編譯旗標的定義來定義。
-   在 Microsoft Rich Edit 2.0 中，如果您建立 Unicode rich edit 控制項 (需要 Unicode 文字訊息的) ，您必須在傳送至控制項的任何視窗訊息中只指定 Unicode 資料。 同樣地，如果您建立 ANSI rich edit 控制項，請只將 ANSI 或雙位元組字元集 (DBCS) 資料。 您可以使用 [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) 函數來判斷 rich edit 控制項是否使用 Unicode 文字訊息。 請注意，rich edit COM 介面會使用 Unicode 文字，除非它們遇到字碼頁引數。
-   Microsoft Rich Edit 1.0 針對段落標記使用了 CR/LF 字元組合。 Microsoft Rich Edit 2.0 只使用換行字元 ( ' \\ r ' ) 。 Microsoft Rich Edit 3.0 只使用換行字元，但在這方面可以模擬 Microsoft Rich Edit 1.0。
-   Microsoft Rich Edit 2.0 引進了下列新訊息。 

    | 訊息                                           | 描述                                                             |
    |---------------------------------------------------|-------------------------------------------------------------------------|
    | [**EM \_ AUTOURLDETECT**](em-autourldetect.md)     | 啟用或停用自動偵測 URL。                            |
    | [**EM \_ CANREDO**](em-canredo.md)                 | 判斷重做佇列中是否有任何動作。             |
    | [**EM \_ GETIMECOMPMODE**](em-getimecompmode.md)   | 抓取目前的輸入方法編輯器 (IME) 模式。                   |
    | [**EM \_ GETLANGOPTIONS**](em-getlangoptions.md)   | 抓取 IME 和亞洲語言支援的選項。                   |
    | [**EM \_ GETREDONAME**](em-getredoname.md)         | 抓取重做佇列中下一個動作的型別名稱。           |
    | [**EM \_ GETTEXTMODE**](em-gettextmode.md)         | 抓取文字模式或復原層級。                                  |
    | [**EM \_ GETUNDONAME**](em-getundoname.md)         | 捕獲復原佇列中下一個動作的型別名稱。           |
    | [**EM \_ 重做**](em-redo.md)                       | 重新執行重做佇列中的下一個動作。                               |
    | [**EM \_ SETLANGOPTIONS**](em-setlangoptions.md)   | 設定輸入法和亞洲語言支援的選項。                        |
    | [**EM \_ SETTEXTMODE**](em-settextmode.md)         | 設定文字模式或復原層級。                                       |
    | [**EM \_ SETUNDOLIMIT**](em-setundolimit.md)       | 設定復原佇列中的動作數目上限。                   |
    | [**EM \_ STOPGROUPTYPING**](em-stopgrouptyping.md) | 停止將連續的輸入動作分組為目前的復原動作。 |

    

     

-   Microsoft Rich Edit 2.0 引進了下列新結構。 

    | 結構                          | Description                                      |
    |------------------------------------|--------------------------------------------------|
    | [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) | 包含有關字元格式的資訊。 |
    | [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) | 包含段落格式設定的相關資訊。 |

    

     

-   只有 Microsoft Rich Edit 1.0 的亞洲語言版本才支援下列訊息。 任何較新版本的 Rich Edit 都不支援這些功能。

    [**EM \_ CONVPOSITION**](em-convposition.md)

    [**EM \_ GETIMECOLOR**](em-getimecolor.md)

    [**EM \_ GETIMEOPTIONS**](em-getimeoptions.md)

    [**EM \_ GETPUNCTUATION**](em-getpunctuation.md)

    [**EM \_ GETWORDWRAPMODE**](em-getwordwrapmode.md)

    [**EM \_ SETIMECOLOR**](em-setimecolor.md)

    [**EM \_ SETIMEOPTIONS**](em-setimeoptions.md)

    [**EM \_ SETPUNCTUATION**](em-setpunctuation.md)

    [**EM \_ SETWORDWRAPMODE**](em-setwordwrapmode.md)

### <a name="rich-edit-version-30"></a>Rich Edit 3.0 版

Microsoft Rich Edit 3.0 是單一、可擴充的全全球 DLL，可在小型封裝中提供與 Word 之間的高效能和相容性。 Microsoft Rich Edit 3.0 的新功能包括更豐富的文字、縮放、字型系結、功能更強大的輸入支援，以及豐富的複雜字集支援， (雙向、印度文和泰文) 。

除了 [Rich edit 2.0 版](#rich-edit-version-20)提供的功能之外，Microsoft Rich edit 3.0 還包含下列功能。




| | |Zoom |縮放因數是以比例提供。 | | (單一層級) 的段落編號 |數值、大寫和小寫字母或羅馬數字。 | |簡單資料表 |您可以刪除和插入資料列，但無法調整大小或在儲存格內換行。 開啟 advanced rtf (請參閱 <a href="em-gettypographyoptions.md"><strong>EM_GETTYPOGRAPHYOPTIONS</strong></a>) 、Microsoft Rich Edit 3.0 可以讓資料行以中央或向右對齊，並包含小數。 資料格是依索引標籤來模擬，因此文字索引標籤和換行字元會以空白取代。 | |一般和標題樣式 | <a href="em-setparaformat.md"><strong>EM_SETPARAFORMAT</strong></a> 和 <a href="text-object-model.md">Text 物件模型</a> 都支援內建的標準樣式和標題樣式1到9， (TOM) 介面。 | |更多底線類型 |已新增虛線、虛線、虛線、虛線-點、點加底線。 | |底線著色 |加底線的文字可以使用15個檔選項的其中一個來標記底線色彩。 | |隱藏文字 |以 CHARFORMAT2 屬性標記。 方便 roundtripping (寫出檔案) 的資訊，通常不應該顯示。 | |更多預設快速鍵 |這些快速鍵的運作方式與 Word 中的相同。 例如，歐洲輔色的「無效按鍵」 (美式鍵盤) 。 數位熱鍵 (CTRL + L) 迴圈可用的編號選項，以專案符號開頭。 | |HexToUnicode IME |允許使用者使用快速鍵在十六進位和 Unicode 之間進行轉換。 | |彎引號 |這項功能是由 CTRL + ALT + ' 針對美國鍵盤開啟和關閉。 | |軟連字號 |若為純文字，請使用0xAD。 若為 RTF，請使用 \- 。 | |斜體游標 |此外，當您透過 Url 時，滑鼠游標會變更為手。 | |Advanced 印刷樣式選項 |Microsoft Rich Edit 3.0 可以使用先進的印刷樣式選項來換行和顯示 (請參閱 <a href="em-gettypographyoptions.md"><strong>EM_GETTYPOGRAPHYOPTIONS</strong></a>) 。 這個簡潔的選項主要是為了協助處理複雜的腳本 (雙向、印度文和泰文) 。 此外，簡單的腳本也會進行一些改善。 範例包括：<ul><li>置中、靠右、十進位索引標籤</li><li>完全對齊的文字</li><li>底線平均，可提供統一的底線，即使連續的文字執行具有不同的字型大小也是如此。</li></ul> | |複雜字集支援 |Microsoft Rich Edit 3.0 支援以阿拉伯文和/或希伯來文混合的雙向 (文字與其他腳本) 、印度文 (印度文的印度文，例如 Devangari) 和泰文文字。 為了支援這些複雜的腳本，會使用 advanced 印刷樣式和 Uniscribe 元件。 | |字型系結 |Microsoft Rich Edit 3.0 會針對清楚不屬於目前字元集戳記的字元，自動選擇適當的字型。 這是藉由將字元集指派給文字執行，並將字型與這些字元集產生關聯來完成。 如需詳細資訊，請參閱 <a href="using-rich-edit-controls.md">字型</a>系結。 | |字元集專用的純文字讀取/寫入選項 |這可讓您使用一組字元集來讀取檔案，並使用不同的字元集進行寫入。 | |UTF-8 RTF |這建議用於剪下、複製和貼上作業。 這種檔案格式比一般 RTF 更精簡、更快速且與 Unicode 相容。 | |Microsoft Office 9 IME 支援 (IME98) |這項功能更強大的 IME 功能已分成獨立的模組。 功能包括：<ul><li>在較早的版本中重新封漢字，使用者必須先刪除最後一個字串，然後輸入新字串以取得正確的候選。 這項新功能可讓使用者將最終字串轉換回撰寫模式，進而方便您選擇不同的候選字串。<br /></li><li>檔摘要：這項功能會使用目前段落的文字提供 IME98，協助 IME98 在輸入期間執行更精確的轉換。<br /></li><li>滑鼠操作：這項功能可讓您在輸入期間更妥善地控制候選和 UI 視窗。<br /></li><li>插入號位置這項功能會提供目前的插入號和行資訊，IME98 會使用此資訊來定位 UI 視窗 (例如) 的候選清單。<br /></li></ul> | |Active Input Method Manager (IMM) 支援 |使用者可以叫用作用中的 IMM 物件，讓使用者在美國系統上輸入亞洲字元。 | |HexToUnicode 支援 |使用者可以使用快速鍵，在十六進位標記法和 Unicode 之間進行轉換。 | |更多 RTF roundtripping |從檔案讀取的 RTF 文字將會原封不動地寫回。 | |改良的1.0 相容性模式 |Microsoft Rich Edit 3.0 可模擬 Microsoft Rich Edit 1.0 行為。 例如，您可以在 MBCS 和 Unicode 字元位置 (cp) 對應之間變更。 | |增加凍結控制項 |您可以透過多個 API 呼叫來凍結顯示，然後解除凍結以顯示更新。 | |增強的復原控制項 |復原可以 (IME 需求) 來暫停和繼續。 | |增加/減少字型大小 |將字型大小增加或減少為六個標準值的其中一個 (12、28、36、48、72和80點) 。 | 




 

### <a name="rich-edit-version-41"></a>Rich Edit 4.1 版

Microsoft Rich Edit 4.1 的視窗類別是 MSFTEDIT.DLL \_ 類別。 Microsoft Rich Edit 4.1 的新功能包括斷字、頁面旋轉和文字服務架構 (TSF) 支援。

除了 [Rich edit 3.0 版](#rich-edit-version-30)提供的功能之外，Microsoft Rich edit 4.1 還包含下列功能。




| | |斷字 |您可以透過下列 Api 來支援斷字： <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a>、 <a href="em-sethyphenateinfo.md"><strong>EM_SETHYPHENATEINFO</strong></a>和 <a href="em-gethyphenateinfo.md"><strong>EM_GETHYPHENATEINFO</strong></a>。 | |頁面旋轉 |透過 <a href="em-setpagerotate.md"><strong>EM_SETPAGEROTATE</strong></a> 和 <a href="em-getpagerotate.md"><strong>EM_GETPAGEROTATE</strong></a>，可支援從上到下和自下而上的版面配置。 | |文字服務架構支援 | <ul><li>若要開啟 TSF 和特定的 TSF 功能，請在 <a href="em-seteditstyle.md"><strong>EM_SETEDITSTYLE</strong></a>中使用下列樣式： SES_USECTF、SES_CTFALLOWEMBED、SES_CTFALLOWPROOFING 和 SES_CTFALLOWSMARTTAG。</li><li>若要設定和取得 TSF 模式偏差，請使用 <a href="em-setctfmodebias.md"><strong>EM_SETCTFMODEBIAS</strong></a> 和 <a href="em-getctfmodebias.md"><strong>EM_GETCTFMODEBIAS</strong></a>。</li><li>若要設定並取得 TSF 鍵盤狀態，請使用 <a href="em-setctfopenstatus.md"><strong>EM_SETCTFOPENSTATUS</strong></a> 和 <a href="em-getctfopenstatus.md"><strong>EM_GETCTFOPENSTATUS</strong></a>。</li></ul> | |其他 IME 支援 | <ul><li>若要設定和取得 IME 模式偏差，請使用 <a href="em-setimemodebias.md"><strong>EM_SETIMEMODEBIAS</strong></a> 和 <a href="em-getimemodebias.md"><strong>EM_GETIMEMODEBIAS</strong></a>。</li><li>若要取得輸入法的屬性和功能，請使用 <a href="em-getimeproperty.md"><strong>EM_GETIMEPROPERTY</strong></a>。</li><li>若要取得 IME 組合文字，請使用 <a href="em-getimecomptext.md"><strong>EM_GETIMECOMPTEXT</strong></a>。</li><li>若要判斷地區設定是否為東亞地區設定，請使用 <a href="em-isime.md"><strong>EM_ISIME</strong></a>。</li></ul> | |其他 <a href="em-seteditstyle.md"><strong>EM_SETEDITSTYLE</strong></a> 設定 |除了 TSF 設定之外，還有新的設定會排除 Ime、設定雙向文字流程、使用 draftmode 字型等等。 | |其他 <a href="em-setcharformat.md"><strong>EM_SETCHARFORMAT</strong></a> 設定 |新的旗標可讓用戶端設定指定之 LCID 或字元集的預設字型和字型大小，以設定控制項的預設字型，以防止鍵盤切換為符合字型等等。 | |將輸入限制為 ANSI 文字 |使用<a href="em-settextmode.md"><strong>EM_SETTEXTMODE</strong></a>中的<a href="/windows/win32/api/richedit/ne-richedit-textmode"><strong>TM_SINGLECODEPAGE</strong></a>可防止 Unicode 輸入輸入 Rich Edit 控制項。 | |不支援的 RTF 關鍵字通知 | <a href="en-lowfirtf.md">EN_LOWFIRTF</a> 會在有不支援的 RTF 關鍵字時警告應用程式。 | |其他語言支援 |其他語言包括亞美尼亞文、迪維、泰泰和其他語言。 | |改進的資料表支援 |功能包括：在儲存格內換行、透過 RTF 改進處理，以及改進的導覽。 | |ES_VERTICAL |支援 <a href="rich-edit-control-styles.md"><strong>ES_VERTICAL</strong></a> 視窗樣式。 | | <a href="/windows/desktop/inputdev/wm-unichar"><strong>WM_UNICHAR</strong></a> 支援 |若要將 Unicode 字元傳送或張貼至 ANSI 視窗，請使用 <a href="/windows/desktop/inputdev/wm-unichar"><strong>WM_UNICHAR</strong></a>。 它相當於 <a href="/windows/desktop/inputdev/wm-char"><strong>WM_CHAR</strong></a>，但它使用 (utf-16) -32。 | 




 

## <a name="unsupported-edit-control-functionality"></a>不支援的編輯控制項功能

Rich edit 控制項支援多行編輯控制項的大部分但並非所有功能。 此區段會列出 rich edit 控制項 *不* 支援的編輯控制項訊息和視窗樣式。

下列訊息是由編輯控制項處理，而 *不* 是由 rich edit 控制項處理。



| 不支援的訊息                         | 註解                                                                                                                    |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**EM \_ FMTLINES**](em-fmtlines.md)         | 不支援。                                                                                                              |
| [**EM \_ GETHANDLE**](em-gethandle.md)       | Rich edit 控制項不會將文字儲存為簡單字元陣列。                                                       |
| [**EM \_ GETIMESTATUS**](em-getimestatus.md) | 不支援。                                                                                                              |
| [**EM \_ GETMARGINS**](em-getmargins.md)     | 不支援。                                                                                                              |
| [**EM \_ SETHANDLE**](em-sethandle.md)       | Rich edit 控制項不會將文字儲存為簡單字元陣列。                                                       |
| [**EM \_ SETIMESTATUS**](em-setimestatus.md) | 不支援。                                                                                                              |
| [**EM \_ SETMARGINS**](em-setmargins.md)     | Microsoft Rich Edit 3.0 支援。                                                                                       |
| [**EM \_ SETRECTNP**](em-setrectnp.md)       | 不支援。                                                                                                              |
| [**EM \_ SETTABSTOPS**](em-settabstops.md)   | 改為使用 [**EM \_ SETPARAFORMAT**](em-setparaformat.md) 訊息。 Microsoft Rich Edit 3.0 支援。<br/> |
| [**WM \_ CTLCOLOR**](/windows/desktop/DevNotes/wm-ctlcolor-)    | 改為使用 [**EM \_ SETBKGNDCOLOR**](em-setbkgndcolor.md) 訊息。                                                  |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)        | 改為使用 [**EM \_ GETCHARFORMAT**](em-getcharformat.md) 訊息。                                                  |



 

下列視窗樣式適用于多行編輯控制項，但不含 rich edit 控制項： [**es \_ 小寫**](edit-control-styles.md)、 [**es \_ 大寫**](edit-control-styles.md)和 [**ES \_ OEMCONVERT**](edit-control-styles.md)。

## <a name="rich-edit-shortcut-keys"></a>Rich Edit 快速鍵

Rich edit 控制項支援下列快速鍵。



| 索引鍵                      | Operations                                                                                                                               | 註解                                                                                                                                                                                                                       |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Shift + 倒退鍵           | 在雙向鍵盤上產生 LRM/LRM                                                                                                    | 雙向特定                                                                                                                                                                                                                  |
| Ctrl+Tab                  | 索引標籤                                                                                                                                      |                                                                                                                                                                                                                                |
| Ctrl + Clear                | 全選                                                                                                                               |                                                                                                                                                                                                                                |
| Ctrl + 數位板5         | 全選                                                                                                                               |                                                                                                                                                                                                                                |
| Ctrl+A                    | 全選                                                                                                                               |                                                                                                                                                                                                                                |
| Ctrl+E                    | 置中對齊                                                                                                                         |                                                                                                                                                                                                                                |
| Ctrl+J                    | 對齊對齊                                                                                                                        |                                                                                                                                                                                                                                |
| Ctrl+R                    | 靠右對齊                                                                                                                          |                                                                                                                                                                                                                                |
| Ctrl+L                    | 靠左對齊                                                                                                                           |                                                                                                                                                                                                                                |
| Ctrl+C                    | 複製                                                                                                                                     |                                                                                                                                                                                                                                |
| Ctrl+V                    | 貼上                                                                                                                                    |                                                                                                                                                                                                                                |
| Ctrl+X                    | 剪下                                                                                                                                      |                                                                                                                                                                                                                                |
| Ctrl+Z                    | 復原                                                                                                                                     |                                                                                                                                                                                                                                |
| Ctrl+Y                    | 取消復原                                                                                                                                     |                                                                                                                                                                                                                                |
| Ctrl + ' + ' (Ctrl + Shift + ' = ' )  | 標                                                                                                                              |                                                                                                                                                                                                                                |
| Ctrl + ' = '                  | 標                                                                                                                                |                                                                                                                                                                                                                                |
| Ctrl+1                    | 行間距 = 1 行。                                                                                                                   |                                                                                                                                                                                                                                |
| Ctrl+2                    | 行距 = 2 行。                                                                                                                  |                                                                                                                                                                                                                                |
| Ctrl+5                    | 行間距 = 1.5 行。                                                                                                                |                                                                                                                                                                                                                                |
| Ctrl + ' (單引號)        | 強調銳角                                                                                                                             | 按下簡短的按鍵之後，請按下適當的字母 (例如 a、e 或 u) 。 這僅適用于英文、法文、德文、義大利文和西班牙文鍵盤。                                                         |
| Ctrl + \` (抑)            | 輔音符號                                                                                                                             | 請參閱 Ctrl + ' 批註。                                                                                                                                                                                                           |
| Ctrl + ~ (波狀符號)             | 輔色波浪線                                                                                                                             | 請參閱 Ctrl + ' 批註。                                                                                                                                                                                                           |
| Ctrl +; (分號)         | 重音變音符                                                                                                                            | 請參閱 Ctrl + ' 批註。                                                                                                                                                                                                           |
| Ctrl + Shift + 6              | 重音插入號 (揚)                                                                                                                 | 請參閱 Ctrl + ' 批註。                                                                                                                                                                                                           |
| Ctrl +、 (逗點)             | 強調符號加符                                                                                                                           | 請參閱 Ctrl + ' 批註。                                                                                                                                                                                                           |
| Ctrl + Shift + ' (單引號)  | 啟用智慧引號                                                                                                                    |                                                                                                                                                                                                                                |
| 退格鍵                 | 如果文字受到保護，則會發出嗶聲，且不會將其刪除。 否則，請刪除先前的字元。                                                   |                                                                                                                                                                                                                                |
| Ctrl+退格鍵            | 刪除上一個字組。 這會產生 VK \_ F16 程式碼。                                                                                     |                                                                                                                                                                                                                                |
| F16                       | 與倒退鍵相同。                                                                                                                       |                                                                                                                                                                                                                                |
| Ctrl+Insert               | 複製                                                                                                                                     |                                                                                                                                                                                                                                |
| Shift+Insert              | 貼上                                                                                                                                    |                                                                                                                                                                                                                                |
| 插入                    | Overwrite                                                                                                                                | DBCS 不會覆寫。                                                                                                                                                                                                       |
| Ctrl+向左鍵           | 將游標向左移動一個單字。                                                                                                        | 在雙向鍵盤上，這取決於文字的方向。                                                                                                                                                                   |
| Ctrl+向右鍵          | 將游標向右移動一個單字。                                                                                                       | 請參閱 Ctrl + 向左箭號批註。                                                                                                                                                                                                  |
| Ctrl + 左 Shift           | 靠左對齊                                                                                                                           | 在雙向檔中，這是由左到右的讀取順序。                                                                                                                                                                    |
| Ctrl + 右移          | 靠右對齊                                                                                                                          | 在雙向檔中，這是由右至左的讀取順序。                                                                                                                                                                    |
| Ctrl+向上鍵             | 移至上方的行。                                                                                                                  |                                                                                                                                                                                                                                |
| Ctrl+向下鍵           | 移到下一行。                                                                                                                  |                                                                                                                                                                                                                                |
| Ctrl+Home                 | 移至檔的開頭。                                                                                                   |                                                                                                                                                                                                                                |
| Ctrl+End                  | 移至文件結尾。                                                                                                         |                                                                                                                                                                                                                                |
| Ctrl + Page Up              | 向上移動一個頁面。                                                                                                                        | 如果在 SystemEditMode 和單行控制項中，不執行任何動作。                                                                                                                                                                      |
| Ctrl + Page Down            | 向下移動一個頁面。                                                                                                                      | 請參閱 Ctrl + Page Up 批註。                                                                                                                                                                                                     |
| Ctrl+Delete               | 刪除下一個單字或選取的字元。                                                                                             |                                                                                                                                                                                                                                |
| Shift+Delete              | 剪下選取的字元。                                                                                                             |                                                                                                                                                                                                                                |
| Esc                       | 停止拖放。                                                                                                                          | 拖放文字時。                                                                                                                                                                                               |
| Alt + Esc                   | 變更使用中的應用程式。                                                                                                           |                                                                                                                                                                                                                                |
| Alt+X                     | 將插入點前面的 Unicode 十六進位值轉換成對應的 Unicode 字元。                             |                                                                                                                                                                                                                                |
| Alt + Shift + X               | 將插入點前面的 Unicode 字元轉換為對應的 Unicode 十六進位值。                             |                                                                                                                                                                                                                                |
| Alt + 0xxx (數位板)      | 如果 xxx 大於255，則插入 Unicode 值。 當 xxx 小於256時，會根據目前的鍵盤插入 ASCI 範圍的文字。 | 必須輸入小數值。                                                                                                                                                                                                     |
| Alt + Shift + Ctrl + F12        | 十六進位至 Unicode。                                                                                                                          | 如果已使用 Alt + X 作為其他用途。                                                                                                                                                                                |
| Alt + Shift + Ctrl + F11        | 選取的文字將會輸出到偵錯工具視窗，並儲存至% temp% \\DumpFontInfo.txt。                                               | 僅限 Debug (需要在 Win.ini 中設定旗標 = 8)                                                                                                                                                                                  |
| Ctrl+Shift+A              | 設定全部的 caps。                                                                                                                            |                                                                                                                                                                                                                                |
| Ctrl+Shift+L              | 把玩專案符號樣式。                                                                                                                     |                                                                                                                                                                                                                                |
| Ctrl+Shift+向右鍵    | 增加字型大小。                                                                                                                      | 4pt-11pt; 範圍內的字型大小變更1個點2points for 12pt-28pt;其變更自 28pt-> 36pt-> 48pt-> 72pt-> 80pt;其變更範圍為 80pt-1630pt; 中的10點。最大值為1638。 |
| Ctrl+Shift+向左鍵     | 減少字型大小。                                                                                                                      | 請參閱 Ctrl + Shift + 向右箭號批註。                                                                                                                                                                                           |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[使用 Rich Edit 控制項](using-rich-edit-controls.md)
</dt> <dt>

[無視窗的 Rich Edit 控制項](windowless-rich-edit-controls.md)
</dt> </dl>

