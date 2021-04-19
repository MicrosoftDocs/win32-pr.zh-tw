---
description: X3DAudio 是與 XAudio2 搭配使用的 API，可在3D 空間中放置音效，以從空間中的點（相對於相機的位置）建立音效的假像。
ms.assetid: 1638e848-4186-5dea-18e8-5369eee544ae
title: X3DAudio 總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff509b16556ee1932d2a2543ad5008ddcbaa5b92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985134"
---
# <a name="x3daudio-overview"></a>X3DAudio 總覽

X3DAudio 是與 [XAudio2](programming-guide.md) 搭配使用的 API，可在3d 空間中放置音效，以從空間中的點（相對於相機的位置）建立音效的假像。尤其是，功能3D 場景的標題會想要使用 X3DAudio。 不需要3D 定位的音效（例如 soundtracks 或非定位的環境音效）可能會完全略過 X3DAudio。

## <a name="listeners-and-emitters"></a>接聽程式和發射器

為了管理3D 空間 *中的音效* ，X3DAudio 採用接聽程式和 *發射器* 的概念。 接聽程式和發射器代表任何發音為3D 音效的位置，以及這些音效源自的點。

-   接聽程式會定義為空間和方向的點。 這是 *聽到* 音效的位置。 接聽程式的位置和方向通常與相機的位置和方向相同。 無論標題使用的是第一個人或協力廠商的觀點觀點，都是如此。 接聽程式的位置是以全局座標表示。 請務必注意，它是接聽程式 *相對* 于發射器的位置，可決定如何計算最終的喇叭磁片區。
-   發射器定義為一個 (或多個) 點 *在音效來源* 的空間中。 發射器的位置可以是3D 空間中的任何位置。 如同接聽程式，發射器的位置是以全局座標表示。 它是 *相對* 于接聽程式的發射器位置，可決定最終的喇叭磁片區的計算方式。
-   X3DAudio 使用左手型座標。 若要使用右手座標，開發人員必須將 X3DAUDIO 接聽程式 \_ 和 X3DAUDIO 發射器的 OrientTop、OrientFront、Position 和 Velocity 成員的 z 元素否定。 \_

除了位置，接聽程式和發射器也可以包含速度。 與3D 轉譯引擎不同的是，X3DAudio 只會使用速度計算 Doppler 效果 (不會用來計算位置) 。

如需接聽程式和發射器的詳細資訊，請參閱 [**X3DAUDIO \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) 接聽程式和 [**X3DAUDIO \_ 發射器**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) 結構參考主題。

## <a name="using-x3daudio-with-xaudio2"></a>使用 X3DAudio 搭配 XAudio2

針對 X3DAudio 與 XAudio2 之間的所有互動，請使用下列 X3DAudio 函數。

-   [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize)

    呼叫 [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) 函數來初始化 X3DAudio。 一般而言，您只需要在遊戲的存留期內呼叫 **X3DAudioInitialize** 一次，除非說話者設定有所變更。

-   [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate)

    初始化 X3DAudio 之後，您可以將音效的發射器和接聽程式傳遞至 [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) 函式，以判斷指定音效的音量和其他值。 然後，您可以針對傳遞給函式的旗標，將 **X3DAudioCalculate** 所計算的值套用至 XAudio2 聲音或效果。 您可以使用 [**IXAudio2Voice：： SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) 和 [**IXAudio2SourceVoice：： SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) 方法，將 X3DAudio 所計算的音量和音調值套用至語音。 使用 [**IXAudio2Voice：： SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters)方法時，必須將 X3DAudio 所計算的其他值套用至「[**回音」效果**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb)。

如需搭配使用 X3DAudio 與 XAudio2 的逐步範例，請參閱 how [to：整合 X3DAudio 與 XAudio](how-to--integrate-x3daudio-with-xaudio2.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[X3DAudio](x3daudio.md)
</dt> </dl>

 

 
