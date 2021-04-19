---
title: 語音命令視窗
description: 語音命令視窗
ms.assetid: vs|msagent|~\guidlin_12gn.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c4ad0a1521e8dacc941ba5b2ce5f6c264c65a31
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106967259"
---
# <a name="voice-commands-window"></a>語音命令視窗

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

[語音命令] 視窗會顯示字元目前可用的語音命令。 當您選擇 [開啟命令視窗] 命令或 [**CommandsWindow**](/windows/desktop/lwef/the-commandswindow-object)物件的 [**Visible**](visible-property.md)屬性設定為 **True** 時，會出現此視窗。 如果語音引擎尚未載入，則查詢或設定這個屬性會導致 Microsoft Agent 嘗試初始化引擎。 如果使用者停用語音，視窗仍然可以顯示;但是，它會包含文字訊息，通知使用者語音目前已停用。

輸入-主動用戶端的命令會根據其 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合的 [**VoiceCaption**](voicecaption-property.md)下所列的 [**語音**](voice-property.md)[**字幕**](caption-property.md)和 **語音** 屬性設定，出現在 [語音命令] 視窗中。

**圖1。語音命令視窗**

選擇 [開啟命令視窗] 命令時，會出現 [語音命令] 視窗。 輸入-主動用戶端的命令會根據 [[**命令**](/windows/desktop/lwef/the-commands-collection-object)集合的 **聲音**] 下所列的 [[**語音**](voice-property.md)[**] 和 [**](caption-property.md) **語音**] 屬性設定，出現在 [語音命令] 視窗中。

[語音命令] 視窗也會列出其他字元用戶端的 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合 [**VoiceCaption**](voicecaption-property.md) ，以及下列全域命令專案下一般互動的伺服器產生的語音命令：



| 語音標題                       | 語音文法                                                                                                                                            |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 開啟 [ \| 關閉語音命令] 視窗 |  (開啟 \| [顯示 \[ ]) [ \] 命令 \[ ] 視窗 \] \| 我現在可以說什麼 \[\] <br/> 切換為： <br/> 關閉 \[ \] 命令 \[ 視窗\] <br/> |
| 隱藏                                | 隱藏 \*                                                                                                                                                  |
| *CharacterName*                     | *CharacterName*\*\*                                                                                                                                      |
| 全域命令                     | \[顯示 \] \[ \] 全域命令                                                                                                                          |



 

\* 只有當字元目前可見時，才會列出該字元。

\*\* 所有載入的字元都會列出。

說到另一個用戶端 [**命令**](/windows/desktop/lwef/the-commands-collection-object) 集合的 voice 命令會切換到該用戶端，而 [語音命令] 視窗則會顯示該用戶端的命令。 不會展開其他專案。 同樣地，如果使用者切換字元，[語音命令] 視窗就會變更，以顯示其輸入-主動用戶端的命令。 如果用戶端已經輸入-主動，說出其中一個語音命令沒有任何作用。  (不過，如果使用者使用滑鼠來折迭作用中用戶端的子樹狀結構，則說出用戶端名稱會重新出現用戶端的子樹。 ) 

如果用戶端有語音命令，但沒有 [**命令**](/windows/desktop/lwef/the-commands-collection-object)物件的 [**聲音**](voice-property.md)設定 (或沒有 **語音**[**標題**](caption-property.md)) ，則樹狀結構會顯示「 (命令未定義) 」作為父專案--但只有在該用戶端為輸入-主動且用戶端在其集合中具有 **標題** 和 **語音** 設定的命令時才會顯示。

伺服器會自動顯示目前輸入-主動用戶端的命令，並視需要滾動視窗，以根據視窗的大小，盡可能顯示用戶端的命令數目。 如果字元沒有用戶端專案，則會展開全域命令專案。

如果使用者說「全域命令」，[語音命令] 視窗一律會顯示其相關聯的子樹狀目錄專案。 如果已顯示，則命令沒有任何作用。

雖然您也可以使用 [**Visible**](visible-property.md) 屬性，從應用程式的程式碼顯示或隱藏 [語音命令] 視窗，但無法變更語音命令視窗大小或位置。 伺服器會根據使用者與視窗的互動，來維護 [語音命令] 視窗的屬性。 它的初始位置會緊接在字元的工作列圖示的旁邊。

[語音命令] 視窗會包含在 ALT + TAB 視窗順序中。 這可讓使用者切換至視窗，以使用鍵盤來滾動、調整大小或重新調整視窗的大小。

-   [接聽秘訣](the-listening-tip.md)
-   [[先進的字元選項] 視窗](https://www.bing.com/search?q=The+Advanced+Character+Options+Window)

 

