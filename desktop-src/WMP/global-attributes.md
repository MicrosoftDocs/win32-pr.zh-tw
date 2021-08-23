---
title: '全域屬性 (Windows Media Player SDK) '
description: 全域屬性
ms.assetid: 2ed09506-990e-4da2-89d6-6ff77dc43eb2
keywords:
- Windows Media Player 的外觀、全域屬性
- 外觀，全域屬性
- 外觀、全域屬性的參考
- 全域屬性
- 屬性，全域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69c2d52b6489a28eff20e3a7e5c7180fc9e2db9309c0fe42880bfc779a23f563
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648078"
---
# <a name="global-attributes"></a>全域屬性

全域屬性是一種屬性，可讓您輕鬆存取面板內任何位置的特定播放機元素或物件。

**Player** global 屬性是 [player](player-object.md)物件的參考，可用來存取 Windows Media Player 的主要功能。 下列範例會使用 **player** 開始播放數位媒體播放。


```C++
<BUTTON
  onclick="jscript:player.controls.play();"
/>

```



**主題** 全域屬性是 [主題](theme-element.md)元素的參考。 這是存取 **主題** 屬性的適當方式，而不是在 **主題** 元素內指定識別碼。 下列範例會使用 **主題** 來開啟新的視圖。


```C++
<TEXT 
  value="open" 
  onclick="jscript:theme.openView('newView');"
/>

```



**View** global 屬性是目前 [視圖](view-element.md)的參考。 這可以用來取代在不同 **VIEW** 元素內指定的識別碼。 下列範例會使用 **view** 來關閉目前的視圖。


```C++
<BUTTON 
  id="quitbutton"
  onclick="jscript:view.close();"
/>

```



**事件** 全域屬性是用來從事件處理常式記憶體取環境事件屬性。 下列範例會使用 **事件** ，判斷按一下按鈕時是否按下 ALT 鍵。


```C++
<BUTTON
  onclick="jscript:if (event.altKey == true) myText.value='ALT';"
/>

```



**PlayerApplication** global 屬性是 [playerApplication](playerapplication-object.md)物件的參考，而且會由提供作為遠端播放機控制項之自訂使用者介面的外觀檔案使用。 只有在執行 **IWMPRemoteMediaServices** 介面的 c + + 程式中，才能將 Player 控制項內嵌在遠端模式中。 下列範例會使用 **playerApplication** 切換到播放程式的完整模式。


```C++
<BUTTON
  onclick="jscript:playerApplication.switchToPlayerApplication();"
/>

```



如需詳細資訊，請參閱 [環境事件屬性](ambient-event-attributes.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**其他**](miscellaneous.md)
</dt> </dl>

 

 




