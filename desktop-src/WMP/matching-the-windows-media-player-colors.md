---
title: 符合 Windows Media Player 色彩
description: 符合 Windows Media Player 色彩
ms.assetid: b4d1da08-a4cf-46dd-82a5-40562bb3c049
keywords:
- Windows Media Player 線上商店，符合 Windows Media Player 色彩
- 線上商店，符合 Windows Media Player 色彩
- 輸入1個線上商店，符合 Windows Media Player 色彩
- 輸入2個線上商店，符合 Windows Media Player 色彩
- Windows Media Player 線上商店，Windows Media Player 色彩比對
- 線上商店、Windows Media Player 色彩比對
- 輸入1個線上商店，Windows Media Player 色彩比對
- 輸入2個線上商店，Windows Media Player 色彩比對
- Windows Media Player 線上商店、Windows Media Player 的色彩比對
- 線上商店、Windows Media Player 的色彩對應
- 輸入1個線上商店、Windows Media Player 的色彩對應
- 輸入2個線上商店、Windows Media Player 的色彩對應
- Windows Media Player 的色彩比對
- 符合 Windows Media Player 色彩
- Windows Media Player，相符的色彩
- Windows Media Player，色彩比對
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eedf3e5df7c02f498c0dc21aeeed16c99452003c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965996"
---
# <a name="matching-the-windows-media-player-colors"></a>符合 Windows Media Player 色彩

讓您的線上商店網頁符合 Windows Media Player 色彩配置很簡單。 只要處理 **OnColorChange** 事件即可。 若要指定函式來處理事件，請在您的網頁載入時使用如下的程式碼：


```C++
// Set up the color change event.
external.OnColorChange = OnAppColor;
```



每次使用者變更 Windows Media Player 的色彩配置時，播放程式就會呼叫您的函式。 下列範例顯示一個簡單的函式，它會將網頁背景設定為符合 **appColorLight** 屬性：


```C++
// Match the current color.
function OnAppColor()
{
    window.document.bgColor = external.appColorLight;
}
```



您也可以使用其他的色彩屬性。 請參閱 [類型2線上商店的外部物件](external-object-for-type-2-online-stores.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**AppColorLight**](external-appcolorlight.md)
</dt> <dt>

[**OnColorChange 事件**](external-oncolorchange-event.md)
</dt> <dt>

[**Type 1 和 Type 2 線上商店的一般資訊**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




