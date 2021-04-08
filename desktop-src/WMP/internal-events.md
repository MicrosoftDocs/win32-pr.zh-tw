---
title: 內部事件
description: 內部事件
ms.assetid: d99e84ec-41db-42e7-ab26-5ca6a3ba610b
keywords:
- Windows Media Player 的外觀、內部事件
- 外觀，內部事件
- 事件，內部
- 撰寫適用于面板、內部事件的程式碼
- 內部事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08ed2abca3f23a89ea6fe261a29639d671e0d58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931998"
---
# <a name="internal-events"></a>內部事件

您可以偵測 Windows Media Player 中發生的變更或您自己面板中的變更。 這些可以是 Windows Media Player 物件屬性或方法中的變更、面板屬性的變更等等。

## <a name="windows-media-player-property-changes"></a>Windows Media Player 屬性變更

您可以使用 wmpprop 接聽程式來處理 Windows Media Player 中的變更。 您必須將接聽程式設定為屬性的值。 以雙引號括住值，並以 "wmpprop" 一字開頭，後面接著冒號。 然後，您會包含想要接聽的屬性。 當屬性變更時，屬性的值也會變更。 例如，每當 **currentPosition** 屬性的值變更時，若要讓滑杆元素值變更，請輸入下列內容：


```C++
<SLIDER id="mySlider" value="wmpprop:player.Controls.currentPosition" />
```



-   **重要** 請勿在 Windows Media Player 方法上使用 wmpprop。 可能會發生非預期的結果。

## <a name="windows-media-player-method-changes"></a>Windows Media Player 方法變更

您可以使用 wmpenabled 和 wmpdisabled，讓您的面板回應 Windows Media Player 上的方法可用性。 這些使用方式與 wmpprop 接聽程式類似，不同之處在于您只能在 **isAvailable** 方法所支援的 **控制項** 物件方法上使用這些方法。

例如，您可以只在啟用 **Play** 方法時啟用按鈕，使用如下的程式碼：


```C++
<BUTTON ... enabled="wmpenabled:player.Controls.Play();" />

```



-   **重要** 請勿在 Windows Media Player 屬性上使用 wmpenabled 或 wmpdisabled。 可能會發生非預期的結果。

## <a name="skin-attribute-changes"></a>外觀屬性變更

您可以使用 wmpprop 或 **\_ onchange** 事件，以兩種方式的其中一種來回應面板屬性中的變更。

您可以使用 wmpprop 來接聽您自己面板中的變更。 例如，若要在文字方塊中顯示滑杆值，您可以輸入下列內容：


```C++
<TEXT ... value="wmpprop:mySlider.value">

```



您可以使用 **\_ onchange** 事件來處理元素內的事件。 您必須將您要追蹤的屬性名稱附加至 **\_ onchange**。 例如，如果您想要追蹤文字方塊的值，請輸入：


```C++
value_onchange

```



然後，您將指派值變更時要執行的 JScript 字串。 例如，若要回應可用來調整 Windows Media Player 音量之文字方塊值的變更，請在您的 **text** 元素內部輸入下列內容做為屬性：


```C++
value_onchange = "JScript: player.Settings.Volume = myText.value"

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**處理事件**](handling-events.md)
</dt> </dl>

 

 




