---
title: 建立外觀定義檔
description: 建立外觀定義檔
ms.assetid: ea7f8e7c-a505-478d-80c3-cb3a3f67859d
keywords:
- Windows Media Player行動外觀、面板定義檔
- 外觀、面板定義檔
- 面板的檔案、外觀定義
- 外觀定義檔，建立
- 建立外觀，關於
- 建立外觀 Windows Media Player 行動裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0bb18289a8ed124c820e983c37ccc9fff60c5c1c2b0794e4964a8e170c84909
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341598"
---
# <a name="creating-a-skin-definition-file"></a>建立外觀定義檔

面板定義檔是用來定義面板及其所有複合元件的文字檔。 副檔名必須是. skn。

每個面板定義檔的開頭都必須是下列程式程式碼，以指定面板檔案版本號碼。 下表顯示 Windows Media Player 版本以及應用來在面板定義檔中識別每個版本的程式程式碼。 雖然程式程式碼中的一些數位不是您預期的，但它們是正確的，如下表所示。



| Windows Media Player 版本 | 外觀定義檔案的第一行 |
|------------------------------|------------------------------------|
| 1.01.1<br/>            | \[Pocket WMP 皮檔1.0 版\]      |
| 1.2                          | \[Pocket WMP 面板檔案 v 1。2\]      |
| 7.0                          | \[Pocket WMP 皮檔 v2。0\]      |
| 7.1                          | \[Pocket WMP 皮檔8.0 版\]      |
| 9系列                     | \[Pocket WMP 皮檔9.0。1\]    |
| 10 行動裝置版                    | \[Pocket WMP 皮檔9.0。1\]    |
| 10.1 行動裝置                  | \[Pocket WMP 皮檔9.0。1\]    |



 

版本號碼9.0.1 適用于特別針對 Windows Media Player 9 系列或更新版本所建立的外觀。 具有舊版號碼的面板會以 Windows Media Player 9 系列或更新版本的形式開啟為直向模式，每英寸96點 (DPI) 的外觀。

外觀定義檔包含數個區段。 每個區段都會定義外觀的特定區域。 這些區段必須以下列順序放置：

1.  Description
2.  點陣圖
3.  影片
4.  按鈕
5.  狀態
6.  Text
7.  Marquee
8.  Trackbars

每個區段的開頭都是以方括弧括住的區段名稱，例如：


```C++
[ Bitmaps ]

```



> [!Note]  
> 除非您在括弧和區段名稱之間包含空格，否則您的面板定義檔將不會正確剖析。

 

然後，一或多行定義個別的影像、按鈕等等。 例如，點陣圖區段可能包含下列各項：


```C++
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0

```



不需要對齊資料行中的值，但可協助您的程式碼更容易閱讀。 如需有關面板定義檔各區段的詳細資訊，請參閱面板 [參考](skin-reference.md)。

> [!Note]  
> 請勿在檔案中的任何位置使用 tab 鍵;請改用額外的空間。 這非常重要，因為在撰寫或編輯面板定義檔時按下 TAB 鍵會導致整個面板失敗。 每行都必須完成，而且無法繼續到第二行。 此外，與 Windows Media Player 10 行動裝置版或更新版本搭配使用的面板也會取代區域和超級值。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**外觀定義檔**](skin-definition-file-mobile.md)
</dt> </dl>

 

 





