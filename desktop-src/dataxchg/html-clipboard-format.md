---
title: HTML 剪貼簿格式
description: 本節討論 HTML 剪貼簿格式。
ms.assetid: e891393f-234f-4c94-b581-c4e5f885d2ab
keywords:
- Windows 消費者介面，剪貼簿
- 剪貼簿，資料剪下
- 剪貼簿，複製資料
- 剪貼簿，貼上資料
- 剪貼簿，格式
- 剪貼簿、HTML 格式
- 剪貼簿、剪切的 HTML 文字
- 剪貼簿，貼上 HTML 文字
- CF_HTML 剪貼簿格式
- 剪貼簿，CF_HTML 格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75cdcd9c2fc982a7cbde38bba4b7dec6738f1793
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021621"
---
# <a name="html-clipboard-format"></a>HTML 剪貼簿格式

根據案例，透過剪貼簿傳輸 HTML 文字的需求會有所不同。 本文將說明如何剪下和貼上 HTML 檔案的片段。 可能需要透過剪貼簿傳送整個 HTML 檔案;不過，這篇文章是由傳送所選 HTML 文字片段的需求所驅動。 因此，需要將整個 HTML 檔案複製到剪貼簿的方法會被視為過於重量級。

CF \_ html 剪貼簿格式允許原始 HTML 文字和其內容的片段以 ASCII 的形式儲存在剪貼簿上。 這可讓應用程式檢查 HTML 片段的內容（由所有前面加上標籤組成），讓 HTML 片段的周圍標記可以用其屬性來注明。 雖然應用程式是由決定如何解讀這類片段的應用程式所決定，但根據 IE4/MSHTML 的執行，這裡有一些基本的指導方針。

剪貼簿的官方名稱 (RegisterClipboardFormat) 使用的字串是 HTML 格式。

-   [說明](#description)
-   [案例](#scenarios)

## <a name="description"></a>Description

CF \_ html 完全是文字格式 (是在 HTML 精神中的其他專案，而且會使用 utf-8) 並在內容中包含 `description` 、選擇性和 `context` `fragment` 。

以下是剪貼簿的範例：


```
Version:0.9
    StartHTML:71
    EndHTML:170
    StartFragment:140
    EndFragment:160
    StartSelection:140
    EndSelection:160
    <!DOCTYPE>
    <HTML>
    <HEAD>
    <TITLE> The HTML Clipboard</TITLE>
    <BASE HREF="https://sample/specs">
    </HEAD>
    <BODY>
    <UL>
    <!--StartFragment -->
    <LI> The Fragment </LI>
    <!--EndFragment -->
    </UL>
    </BODY>
    </HTML>
```



描述包括剪貼簿版本號碼和位移，指出內容和片段的開頭和結尾。 描述是 ASCII 文字關鍵字的清單， (min/maj 沒有意義) 後面接著字串，並以冒號 (： ) 分隔。

**版本**：剪貼簿的 >-vv 版本號碼。 起始版本為0.9。

**StartHTML**：從剪貼簿的開頭 bytecount 至內容的開頭; 如果沒有內容，則為-1。

**EndHTML**：從剪貼簿的開頭 bytecount 至內容的結尾，如果沒有內容，則為-1。

**StartFragment**：從剪貼簿開頭到片段開頭的 bytecount。

**EndFragment**：從剪貼簿開頭到片段結尾的 bytecount。

**StartSelection**：從剪貼簿的開頭 bytecount 至選取範圍的開頭。

**EndSelection**：從剪貼簿的開頭 bytecount 至選取範圍的結尾。

StartSelection 和 EndSelection 關鍵字是選擇性的，如果您不想讓應用程式產生這項資訊，則必須省略這兩者。

此類型的其他資訊可以在稍後加入，因為 HTML 是從 StartHTMLoffset 開始。 例如，您可以稍後新增多組 StartFragment/EndFragment，以支援連續選取的片段。

為了方便產生 bytecounts 的程式，bytecounts 可能會以零填補。 例如，產生 bytecounts 的程式可能會對每個關鍵字 (StartHTML： 0000000000)  (10 個) 零產生任意影響，然後，如果已知的 StartHTML bytecount 是已知的 bytecount （ (假設為 71) ），則程式可以將 StartHTML (： 0000000071) 取代為適當的零數目。

剪貼簿唯一支援的字元集是其 UTF-8 編碼中的 Unicode。 由於 UTF-8 和 ASCII 的第一個字元相符，因此描述一律為 ASCII，但是內容 (的位元組在 StartHTML) 可能會使用以 UTF-8 編碼的其他任何字元。

剪貼簿格式標頭中的行尾可以是 CR 或 CR/LF 或 LF。

片段包含純有效的 HTML，代表使用者選取 (複製的區域，例如) 。 這包含選取的文字加上在選取的文字中具有結束標記之任何專案的開頭標記和屬性，以及包含任何開始標記之片段結尾的結束記號。 這是基本貼上 HTML 片段所需的所有資訊。

片段前後都必須加上 HTML 批註 <!--StartFragment--> 及 <!--EndFragment-->  (!--和文字) 之間不允許空格，方便地指出片段的開頭和結尾。 因此，片段的開頭和結尾會以這些批註的存在，以及描述中的 StartFragment 和 EndFragment 位元組計數來表示。 預期工具會產生此資訊。 導入此冗余是為了能夠快速地從 [位元組計數]) 中找出片段 (的起點，並將片段的位置直接標示在 HTML 樹狀結構中。

選取範圍會在片段中指出使用者已選取 (複製的確切 HTML 區域，例如) 。 這會藉由指出確切選取的文字，而不使用已新增的開頭標記和結束標記，將更多資訊新增至片段，以確保片段是格式正確的 HTML。

選取範圍是選擇性的，因為包含在基本貼上的片段中包含足夠的資訊。 如果未儲存選取專案，StartSelection 和 EndSelection 都不會儲存在標頭中。

內容是有效、完整的 HTML 檔案。 本文包含片段和所有前面的標記 (開始和結束標記;這些先前周圍的標記代表片段的所有父節點，直到 HTML 節點) 為止。 本文也包含完整的標頭，並允許包含 BASE 和 TITLE 元素，因此可以取得此額外資訊。 將 HTML 片段複製到剪貼簿的應用程式可以選擇建立要包含在內容中的基底專案，如果這類元素不存在，就可以解析片段中的部分 Url。

內容是選擇性的，因為片段中包含足夠的資訊，可讓您進行基本的 HTML 片段貼上。 如果未儲存內容，則只會儲存片段，且 StartHTML = EndHTML =-1。

## <a name="scenarios"></a>案例

下列案例描述 IE4/MSHTML HTML 編輯器如何處理 HTML 剪下和貼上;其他應用程式不一定會遵循這些案例。 此處所述的剪貼簿格式，目的是要讓應用程式選擇運作的彈性更加靈活。  (這些案例只會顯示良好的 HTML，也就是沒有重迭的標記。 ) 

1.  HTML 的簡單片段。
    -   -   HTML 文字：

            <BODY>這是正常的，這是<B>粗體</B> <I><B>斜體</B>，這是斜體</I></BODY>

        -   顯示為：

            這是正常的，這是 **粗體**，此為    *    斜體 *

        -   選取的文字 \* \* 並複製到剪貼簿：

            這 **是正常的，這** 是粗體，這是 \* \*     * **粗體**   的 * \* \* *是斜體*

        -   這是剪貼簿 (注意這是 IE4/MSHTML 的解讀) ：

            版本：0。9

            StartHTML：71

            EndHTML：160

            StartFragment：130

            EndFragment：150

            **StartSelection：130**

            **EndSelection：150**

            <!DOCTYPE ...>

            <BODY>

            <!-- StartFragment -->>

            **<B>粗體</B><I><B>，這是以粗體顯示</B></I>**

            <!-- EndFragment -->

            </BODY>

            </HTML>

        -   在此案例中，只有內文標記和 HTML 標籤會出現在內容中，如同選取的片段之前。 請注意，開始標記和結束標記會包含在內容中。 選取範圍（以 StartSelection 和 EndSelection 分隔）會以粗體顯示。

2.  HTML 中資料表的片段。
    -   -   HTML 文字：

            <BODY><TABLE BORDER><TR><TH ROWSPAN=2>Head1</TH><TD>項目 1</TD><TD>項目 2</TD><TD>項目 3</TD><TD>專案4</TD></TR><TR><TD>專案5</TD><TD>專案6</TD><TD>專案7</TD><TD>專案8</TD></TR><TR><TH>Head2</TH><TD>專案9</TD><TD>項目 10</TD><TD>專案11</TD><TD>專案12</TD></TR></TABLE></BODY>

        -   顯示為： ><TABLE BORDER><TR><TH ROWSPAN=2>Head1</TH><TD>項目 1</TD><TD>項目 2</TD><TD>項目 3</TD><TD>專案4</TD></TR><TR><TD>專案5</TD><TD>專案6</TD><TD>專案7</TD><TD>專案8</TD></TR><TR><TH>Head2</TH><TD>專案9</TD><TD>項目 10</TD><TD>專案11</TD><TD>專案12</TD></TR></TABLE><！ \[Cdata\[\]\]>
        -   系統會選取資料表的專案6、Tuple.item7、專案10和專案11元素做為區塊，然後複製到剪貼簿。
        -   這是剪貼簿 (注意這是 IE4/MSHTML 的解讀) ：

            <!DOCTYPE ...>

            <HTML><BODY><TABLE BORDER>

            <!--StartFragment-->

            **<TR><TD>專案 6 </TD> <TD> 專案 7 </TD> </TR> <TR> <TD> 專案 10 </TD> <TD> 專案11</TD></TR>**

            <!--EndFragment-->

            </TABLE>

            </BODY></HTML>The selection, as delimited by StartSelection and EndSelection, is shown in bold.

3.  將已排序清單的片段貼入純文字中。
    -   -   HTML 文字：

            <BODY><OL TYPE = a><LI>項目 1<LI>項目 2<LI>項目 3<LI>專案4<LI>專案5<LI>專案6</OL></BODY>

        -   顯示為：
            1.  項目 1
            2.  項目 2
            3.  項目 3
            4.  專案4
            5.  專案5
            6.  專案6
        -   使用者選取並將專案3到5複製到剪貼簿。 下列 HTML 位於剪貼簿中：

            <DOCTYPE ... ><HTML><BODY><OL TYPE = a>

            <!-- StartFragment-->

            **<LI>專案 3 <LI> 專案 4 <LI> 專案5**

            <!-- EndFragment-->

            </OL></BODY></HTML>

            選取範圍（以 StartSelection 和 EndSelection 分隔）會以粗體顯示。

        -   如果此片段現在貼入空白檔，將會建立下列 HTML：

            <BODY><OL TYPE = a><LI>項目 3<LI>專案4<LI>專案5</OL></BODY>

        -   顯示為：
            1.  項目 3
            2.  專案4
            3.  專案5

4.  貼入部分選取的區域。
    -   -   HTML 文字：

            <P> IE4/MSHTML 是 WYSIWYG 編輯器，支援：<UL><LI>剪下<LI>複製<LI>貼上</UL><P>這是很棒的工具！

        -   顯示為： IE4/MSHTML 是 WYSIWYG 編輯器，支援：
            -   -   剪下
                -   複製
                -   貼上

        -   使用者從 "WYSIWYG" 開始選取，直到 "Cop" 為止。下列 HTML 位於剪貼簿中：

            <DOCTYPE ... ><HTML><BODY>

            <!-- StartFragment-->

            <P>

            **WYSIWYG 編輯器，支援**

            **<UL><LI>剪下 <LI> Cop**

            </UL>

            <!-- EndFragment-->

            </BODY></HTML>The selection, as delimited by StartSelection and EndSelection, is shown in bold.

     
    -   -   使用者選取 "複製"，直到「絕佳」。

            下列 HTML 位於剪貼簿中：

            <DOCTYPE ... ><HTML><BODY>

            <!-- StartFragment-->

            <UL><LI>

            **複製 <LI> 貼上很 </UL> <P> 棒**

            </P>

            <!-- EndFragment-->

            </BODY></HTML>

            選取範圍（以 StartSelection 和 EndSelection 分隔）會以粗體顯示。

 

 




