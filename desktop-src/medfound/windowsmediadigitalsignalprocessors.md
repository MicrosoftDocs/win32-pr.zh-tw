---
description: 數位訊號處理器
ms.assetid: cd3952ca-3958-4944-8fde-f0163a47bff9
title: 數位訊號處理器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f5c9aa0ee3c4cc2a8c7f725b3a8444f4852c8c5b52ee3713b533ec435f4a3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100940"
---
# <a name="digital-signal-processors"></a>數位訊號處理器

本節說明 Windows 提供的 (DSP) 物件的數位訊號處理器。

Microsoft 使用「 *數位訊號處理器* 」一詞來指定一組 COM 物件，這些物件會在未壓縮的音訊和影片資料上執行轉換。 此 SDK 中所述的 Dsp 會以各種未壓縮的格式轉換音訊和影片。

Dsp 可以單獨使用，或結合音訊和視頻編解碼器。 除了語音捕獲 DSP 之外，此處所列的每個 DSP 都有兩個不同但類似的介面。



| 介面                              | 描述                                 |
|----------------------------------------|---------------------------------------------|
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)   | 與 Microsoft 媒體基礎相容。 |
| [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) | 與 DirectShow 相容。                 |



 

您可以使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面設定屬性，以設定 dsp。 某些 Dsp 具有可設定屬性的額外介面。 若要使用這些介面，請呼叫 DSP 之任何其他介面的 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 方法。 每個 DSP 的參考主題都會列出支援的屬性、介面和其他功能。

此章節包含下列主題。



| DSP                                                      | 描述                                          |
|----------------------------------------------------------|------------------------------------------------------|
| [音訊 Resampler DSP](audioresampler.md)                | 轉換音訊串流的取樣率。       |
| [色彩控制轉換 DSP](colorcontroltransform.md) | 調整影片資料流程的色彩特性。 |
| [色彩轉換器 DSP](colorconverter.md)                | 在色彩格式之間轉換影片串流。       |
| [畫面播放速率轉換器 DSP](framerateconverter.md)       | 變更影片串流的畫面播放速率。            |
| [影片尺寸調整 DSP](videoresizer.md)                    | 調整影片資料流程的大小。                              |
| [語音捕獲 DSP](voicecapturedmo.md)                 | 封裝與語音捕捉相關的數個 Dsp。  |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎程式設計參考](media-foundation-programming-reference.md)
</dt> </dl>

 

 
