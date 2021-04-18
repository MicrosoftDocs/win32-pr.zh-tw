---
title: 類型2線上商店的外部物件
description: 類型2線上商店的外部物件
ms.assetid: d12e7480-39ec-4d32-9cf9-5555d0f92d80
keywords:
- Windows Media Player 線上商店、外部物件
- 線上商店、外部物件
- 類型2線上商店，外部物件
- 外部物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c412cac301d61aeb791131e85bb8bc60f390201d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507304"
---
# <a name="external-object-for-type-2-online-stores"></a>類型2線上商店的外部物件

> [!Note]  
> 本章節描述專為線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**外部** 物件可以為類型2線上商店提供並裝載于 Windows Media Player 中的網頁提供功能。

**外部** 物件會公開下列屬性。



| 屬性                                                        | 描述                                                                               |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [appColorButtonHighlight](external-appcolorbuttonhighlight.md) | 抓取 Windows Media Player 使用者介面目前的按鈕反白顯示色彩。 |
| [appColorButtonHoverFace](external-appcolorbuttonhoverface.md) | 抓取 Windows Media Player 使用者介面目前的按鈕停留色彩。     |
| [appColorButtonShadow](external-appcolorbuttonshadow.md)       | 抓取 Windows Media Player 使用者介面目前的按鈕陰影色彩。    |
| [appColorDark](external-appcolordark.md)                       | 抓取 Windows Media Player 使用者介面目前的深色陰影色彩。       |
| [appColorLight](external-appcolorlight.md)                     | 抓取 Windows Media Player 使用者介面目前的淺色陰影色彩。      |
| [appColorMedium](external-appcolormedium.md)                   | 抓取 Windows Media Player 使用者介面目前的中陰影色彩。     |
| [DownloadManager](external-downloadmanager.md)                 | 抓取 **DownloadManager** 物件。                                                 |
| [SelectedTaskPane](external-selectedtaskpane.md)               | 指定或抓取目前選取的工作窗格。                                  |
| [version](external-version.md)                                 | 抓取 Windows Media Player 的目前版本。                                    |



 

**外部** 物件會公開下列方法。



| 方法                                                  | 描述                                                                          |
|---------------------------------------------------------|--------------------------------------------------------------------------------------|
| [NavigateTaskPaneURL](external-navigatetaskpaneurl.md) | 在指定的工作窗格中開啟網頁，並將焦點變更為指定的窗格。 |
| [playMedia (已淘汰) ](external-playmedia.md)        | 指定要播放之數位媒體專案的 URL。                                   |



 

**外部** 物件會公開下列事件。



| 事件                                             | 描述                                                               |
|---------------------------------------------------|---------------------------------------------------------------------------|
| [OnColorChange](external-oncolorchange-event.md) | 當 Windows Media Player 使用者介面的色彩變更時發生。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**類型 2 線上商店的參考**](reference-for-type-2-online-stores.md)
</dt> <dt>

[**遠端處理 Windows Media Player 控制項**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




