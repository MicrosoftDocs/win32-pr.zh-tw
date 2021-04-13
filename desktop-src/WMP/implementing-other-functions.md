---
title: 執行其他函數
description: 執行其他函數
ms.assetid: 274ba948-b954-4e9e-a384-dee5b3befbcb
keywords:
- 視覺效果，IWMPEffects 介面
- 自訂視覺效果，IWMPEffects 介面
- 視覺效果，轉譯函數
- 自訂視覺效果，轉譯函數
- 轉譯函數，其他函式
- IWMPEffects 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ed6efa5cc9a0697653e558f27165b66d5f230fd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374486"
---
# <a name="implementing-other-functions"></a>執行其他函數

您一定會想要撰寫自己的 **轉譯函數實作為。** 另外還有數個也是 **IWMPEffects** 介面成員函式的其他函數。 有些會提供您可選擇使用的額外資訊，而其他資訊則會自動 Windows Media Player 提供由 wizard 產生的資訊，例如您的視覺效果名稱。

除了轉譯之外， **IWMPEffects** 介面還支援下列函 **式：**



| 函式                                                   | 描述                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DisplayPropertyPage](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-displaypropertypage) | Wizard 未提供預設的執行。                                                                                                                                                                                                                                                           |
| [GetCapabilities](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getcapabilities)         | 取得視覺效果的功能，並將其傳遞至 Windows Media Player。                                                                                                                                                                                                                     |
| [GetCurrentPreset](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getcurrentpreset)       | 當您產生視覺效果的程式碼時，嚮導會建立兩個預設。 當面板開發人員想要取得目前預設值的索引時，就會呼叫這個函式。 您不會想要變更此函數的執行，因為它只會使用其他函數所設定的資訊。 |
| [GetPresetCount](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getpresetcount)           | 當您產生視覺效果的程式碼時，嚮導會建立兩個預設。 您可以藉由變更 **GetPresetCount** 的執行來變更計數。 如需變更預設值 [的詳細資訊](presets.md) ，請參閱預設值。                                                             |
| [GetPresetTitle](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getpresettitle)           | 當您產生視覺效果的程式碼時，嚮導會建立兩個預設。 您可以變更 **GetPresetTitle** 的實作者所使用的標題。 如需變更預設值 [的詳細資訊](presets.md) ，請參閱預設值。                                                       |
| [GetTitle](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-gettitle)                       | 取得視覺效果的標題，並將其傳遞至 Windows Media Player。 Wizard 使用您專案的名稱來產生傳回的名稱。                                                                                                                                           |
| [GoFullscreen](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-gofullscreen)               | Wizard 未提供預設的執行。                                                                                                                                                                                                                                                           |
| [Mediainfo.xml](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-mediainfo)                     | 抓取音訊頻道數目和目前播放音訊的取樣率。                                                                                                                                                                                                               |
| [RenderFullScreen](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-renderfullscreen)       | Wizard 未提供預設的執行。                                                                                                                                                                                                                                                           |
| [SetCurrentPreset](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-setcurrentpreset)       | 當您產生視覺效果的程式碼時，嚮導會建立兩個預設。 當 Windows Media Player 想要變更為已命名的預設值時，會呼叫此函式。                                                                                                                                   |



 

**IWMPEffects2** 介面支援下列其他功能：



| 函式                                            | 描述                                                                                                                                      |
|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [建立](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-create)                   | 在視窗中轉譯時，Windows Media Player 會呼叫這個函式，讓您建立新的視窗以供轉譯。                          |
| [摧毀](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-destroy)                 | 在視窗中轉譯時，Windows Media Player 會呼叫這個函式，以允許您終結在呼叫 **建立** 時所建立的視窗。 |
| [NotifyNewMedia](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-notifynewmedia)   | 當播放程式載入新媒體專案時，此功能可讓您的視覺效果回應。                                          |
| [OnWindowMessage](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-onwindowmessage) | 當以無視窗模式轉譯時，此函式會從播放玩家接收 windows 訊息。                                                       |
| [RenderWindowed](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-renderwindowed)   | 播放程式以視窗模式轉譯時，播放程式會呼叫這個函式，而不是 **IWMPEffects：： Render** 。                          |
| [SetCore](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-setcore)                 | 此函式會接收 **IWMPCore** 介面的指標。                                                                                  |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**執行您的程式碼**](implementing-your-code.md)
</dt> </dl>

 

 




