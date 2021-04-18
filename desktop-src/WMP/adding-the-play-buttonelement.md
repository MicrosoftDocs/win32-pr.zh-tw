---
title: 新增播放 BUTTONELEMENT
description: 新增播放 BUTTONELEMENT
ms.assetid: 895850a7-7538-4581-8348-41cbb3bc9717
keywords:
- 建立外觀，BUTTONELEMENT 元素
- Windows Media Player 的 BUTTONELEMENT 元素
- 外觀，BUTTONELEMENT 元素
- 外觀定義檔，BUTTONELEMENT 元素
- BUTTONELEMENT 元素
- 元素，BUTTONELEMENT
- 建立外觀、播放按鈕
- Windows Media Player 的外觀、播放按鈕
- 外觀、播放按鈕
- 外觀定義檔，播放按鈕
- 播放按鈕
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a92b5416adf2e323043eb563ec08e1e4d2525733
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507248"
---
# <a name="adding-the-play-buttonelement"></a>新增播放 BUTTONELEMENT

最後，您可以加入 **BUTTONELEMENT** 元素，以連接螢幕上的視覺效果按鈕來 Windows Media Player 動作。 這是您面板的核心，而您可以將其視為將面板表面連接到 Windows Media Player 的內部機械。

**BUTTONELEMENT** 會包含在 **BUTTONGROUP** 中。 每個 **BUTTONGROUP** 內都必須至少有一個 **BUTTONELEMENT** 。

將 Play **BUTTONELEMENT** 程式碼放在 **BUTTONGROUP** 的右角括弧之後。


```C++
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Play"
            onClick = "JScript: player.URL='https://proseware.com/laure.wma';" />

```



下列屬性是用來定義 [播放] 按鈕的 **BUTTONELEMENT** ：

**mappingColor**

這是您先前建立之地圖藝術檔案中區域的色彩值。 在這種情況下，它是純色的綠色色彩。 任何 **BUTTONELEMENT** 都需要這個屬性。 藉由定義此色彩，您會告訴 Windows Media Player 將此色彩區域與此按鈕的 XML 程式碼產生關聯。

**upToolTip**

這會定義當使用者將滑鼠停留在按鈕上時所要顯示的文字。 請勿將它與將會顯示的暫留圖片混淆。 工具提示是很小的氣球標題，需要一些時間才會出現。 不過，「暫止」圖片會以您選擇的任何色彩和圖形立即出現。

**onClick**

這會定義滑鼠按一下按鈕時所發生的事件。 這個事件屬性的值稱為「事件處理常式」（event handler），它會是 Microsoft JScript 程式碼的行，或是由 **視圖** 的 **loadScript** 屬性所載入之外部文字檔中的 jscript 函數。 在此情況下，JScript 程式碼會呼叫 Windows Media Player 的 **URL** 方法，這個方法會載入並開始播放名為 "laure" 的檔案。 請注意，在引號內以分號結尾的行，這是良好的 JScript 編碼作法。 也請注意，在雙引號內使用單引號來設定檔案名。 如需 JScript 的詳細資訊，請參閱此 SDK 的「關於面板」一節中的「 [使用 jscript](using-jscript.md) 」。

請注意，沒有結束的 **BUTTONELEMENT** 標記。 如果專案未括住另一個元素，您可以在右角括弧前面加上正斜線來關閉它。 這會告訴 XML 您已完成該元素。 例如，


```C++
<BUTTONELEMENT></BUTTONELEMENT>
```



及


```C++
<BUTTONELEMENT/>
```



以 XML 傳達相同的資訊。

面板的威力來自于使用事件處理常式。 如果使用者使用滑鼠來執行某項工作，您可以使用 JScript 來處理該事件。 您的程式碼可以是單一行，讓 Windows Media Player 執行簡單的作業，例如播放，或者可以是以 JScript 撰寫的完整應用程式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立外觀定義檔**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




