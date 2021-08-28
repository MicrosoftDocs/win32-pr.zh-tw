---
title: 開始使用主題和視圖
description: 開始使用主題和視圖
ms.assetid: 1ac92f3a-463a-4343-a269-5230c644b57f
keywords:
- 建立外觀，主題元素
- Windows Media Player 的外觀，主題元素
- 外觀，主題元素
- 外觀定義檔，主題元素
- 主題元素
- 建立外觀、VIEW 元素
- Windows Media Player 的外觀、VIEW 元素
- 外觀，VIEW 元素
- 外觀定義檔，VIEW 元素
- VIEW 元素
- 元素、VIEW
- 元素，主題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51bcb18a9d56a8780e56d81d6de60ca269036c72
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883716"
---
# <a name="start-with-theme-and-view"></a>開始使用主題和視圖

每個面板都必須只有一個 **主題** 元素，以及至少一個 **VIEW** 元素。

使用文字編輯器，建立下列文字：


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "False">


    </VIEW>
</THEME>

```



在關閉 **視圖** 標記之前保留一些空白行，因為稍後會在此新增更多程式碼。

使用您想要的任何檔案名來儲存您的檔案，但請確定副檔名為 wms。 例如，一般的檔案名可能是 skinone。

每個外觀都必須以 &lt; 主題開頭 &gt; ，並以結尾 </THEME> 。 您的面板中只能有一個 **主題** 元素，但您必須有一個。

您也必須有至少一個 **VIEW** 元素。 您可以有一個以上的 **視圖**，但這個範例只有一個。 您必須有開啟的 &lt; 視圖 &gt; 和關閉 &lt; 視圖 &gt; 。 請注意，開頭 &lt; /VIEW &gt; 標記不會立即關閉標記，但會在右角括弧 (>) 之前包含數個屬性。 下列屬性用於此範例中的 **主題** 元素：

**clippingColor**

如果您的面板邊緣是矩形，您就不一定需要 **clippingColor** 屬性。 此範例中的面板是橢圓形的，因此您需要您想要查看桌面的面板部分的裁剪色彩;基本上是 oval 以外的所有部分。 在此範例面板中，我們將使用以 Web 格式指定為 " \# CCCC00" 的深黃色。 這項選擇的原因是為了 [建立主要藝術](creating-the-primary-art-file.md)檔案而提供。 基本上，這個值一律是您從藝術節目中取得的數位。

**backgroundImage**

這是主要藝術檔案的名稱。 它應該是您的主要圖片檔案的確切檔案名和路徑。 僅支援 BMP、JPG、GIF 和 PNG 檔案，建議使用 BMP。

**標題列**

此面板沒有 **標題列**，因此值會是 "false"。 如果您想要讓面板具有背景色彩且為矩形，您只需要標題列。

確定您將結尾角括弧放 (>) **標題** 值之後，表示您已完成定義此 **視圖**。 在關閉 **視圖** 和 **主題** 標記之前留下幾行空白行。 您將需要稍後將加入的程式程式碼。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立外觀定義檔**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




