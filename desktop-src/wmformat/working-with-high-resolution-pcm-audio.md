---
title: 使用 High-Resolution PCM 音訊
description: 使用 High-Resolution PCM 音訊
ms.assetid: 422a78f9-0f43-4edb-acaf-7f6e3f4a1cb8
keywords:
- Advanced Systems Format (ASF) 、高解析度 PCM 音訊
- ASF (Advanced Systems Format) 、高解析度 PCM 音訊
- 設定檔，高解析度 PCM 音訊
- 編解碼器、高解析度 PCM 音訊
- Advanced Systems Format (ASF) 、PCM 音訊
- ASF (Advanced Systems Format) 、PCM 音訊
- 設定檔，PCM 音訊
- 編解碼器、PCM 音訊
- 高解析度 PCM 音訊
- PCM 音訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a76cfb8397cacd6d39f62ea3594c8be655f4543e0b48b60cafbf15b9783c7fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194853"
---
# <a name="working-with-high-resolution-pcm-audio"></a>使用 High-Resolution PCM 音訊

Windows Media 音訊 9 Professional 編解碼器的一些輸入格式和 Windows Media 音訊9無失真編解碼器是高解析度 PCM 格式。 這些 PCM 格式有兩個以上的通道，或每個樣本超過16個位 (音訊具有兩個以上的通道，也稱為多頻道音訊) 。

這些格式是使用 [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) 結構的結構化延伸來設定，稱為 [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85))。 **WAVEFORMATEXTENSIBLE** 結構包含音訊中所含通道的相關資訊。 使用高解析度 PCM 音訊時需要此結構，因為某些 Windows api 不會接受包含高解析度值的 **WAVEFORMATEX** 結構。

高解析度 PCM 格式有22個位元組的擴充資料，其指定于 **WAVEFORMATEX** 結構的 **cbSize** 成員中。 高解析度 Windows 媒體音訊格式不會使用 **WAVEFORMATEXTENSIBLE** 結構，但會將擴充的資料附加至 **WAVEFORMATEX** 結構。

Windows 媒體音訊編解碼器只支援在 Windows XP 或更新版本上執行應用程式時，對高解析度 PCM 格式進行解碼。 在舊版的 Microsoft Windows 中，編解碼器會解碼為格式，每個樣本最多16個位和2個通道。 此外，您必須 \_ 使用 [**IWMReaderAdvanced2：： SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting)方法，將 g wszEnableDiscreteOutput 輸出設定設為 **TRUE** ，以指定要將編解碼器解碼為高定義 PCM。 進行此呼叫之後，讀取器列舉的輸出會包含高定義格式。

多頻道音訊需要更多設定。 如需詳細資訊，請參閱 [讀取多頻道音訊](reading-multichannel-audio.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用輸入**](working-with-inputs.md)
</dt> </dl>

 

 