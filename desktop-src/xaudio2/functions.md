---
title: XAudio2 函式
description: 本章節包含 Microsoft XAudio2 API 所提供的函式相關資訊。
ms.assetid: 870a0425-3226-7848-bcc0-0ba7145135cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bcd8bcfdb00565d6f8bbc31ae0ee6a24f106dee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000293"
---
# <a name="xaudio2-functions"></a>XAudio2 函式

本章節包含 Microsoft XAudio2 API 所提供的函式相關資訊。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                       | 描述                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx)<br/>                                                                     | 建立要求之 [XAPOFX](xapofx-overview.md) 效果的實例。<br/>                                                                                                                                                         |
| [**CreateHrtfApo**](/windows/desktop/api/HrtfApoApi/nf-hrtfapoapi-createhrtfapo)<br/>                                                           |  (HRTF) 處理，建立與 head 相關的傳送函式之 [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) 介面的實例。<br/>                                                                                                                  |
| [**ReverbConvertI3DL2ToNative**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-reverbconverti3dl2tonative)<br/>                                 | 將 I3DL2 (互動式3D 音訊轉譯指導方針層級 2.0) 參數轉換為原生 XAudio2 參數的內嵌函式。<br/>                                                                                                 |
| [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate)<br/>                                                   | 計算與3D 參數相關的 DSP 設定。<br/>                                                                                                                                                                             |
| [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize)<br/>                                                 | 設定所有全域3D 音訊常數。<br/>                                                                                                                                                                                                |
| [**XAudio2AmplitudeRatioToDecibels**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2amplituderatiotodecibels)<br/>                       | 將波幅比率值轉換為分貝值的內嵌函數。<br/>                                                                                                                                                         |
| [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create)<br/>                                                           | 建立新的 **XAudio2** 物件，並將指標傳回至其 [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) 介面。<br/>                                                                                                                              |
| [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb)<br/>                                               |  (APO) 建立新的「回音」音訊處理物件，並傳回其指標。<br/>                                                                                                                                                   |
| [**XAudio2CreateVolumeMeter**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createvolumemeter)<br/>                                     |  (APO) 建立新的磁片區計量音訊處理物件，並傳回其指標。<br/>                                                                                                                                              |
| [**XAudio2CutoffFrequencyToOnePoleCoefficient**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2cutofffrequencytoonepolecoefficient)<br/> | 內嵌函式，可從以赫茲表示的篩選器截止頻率轉換成與 [**XAUDIO2 \_ 篩選 \_ 參數**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters)結構的 **Frequency** 成員搭配使用的篩選係數。<br/>   |
| [**XAudio2CutoffFrequencyToRadians**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2cutofffrequencytoradians)<br/>                       | 內嵌函式，可從以赫茲表示的篩選截止頻率轉換為 [**XAUDIO2 \_ 篩選 \_ 參數**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters)結構的 **frequency** 成員所使用的弧度頻率值。<br/> |
| [**XAudio2DecibelsToAmplitudeRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2decibelstoamplituderatio)<br/>                       | 將分貝值轉換成波幅比率值的內嵌函數。<br/>                                                                                                                                                         |
| [**XAudio2FrequencyRatioToSemitones**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2frequencyratiotosemitones)<br/>                     | 將頻率比率值轉換成 semitone 值的內嵌函式。<br/>                                                                                                                                                         |
| [**XAudio2RadiansToCutoffFrequency**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2radianstocutofffrequency)<br/>                       | 內嵌函式，可從 [**XAUDIO2 \_ 篩選 \_ 參數**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters) 中使用的弧度頻率轉換回以赫茲為單位的絕對頻率。<br/>                                                          |
| [**XAudio2SemitonesToFrequencyRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2semitonestofrequencyratio)<br/>                     | 將 semitone 值轉換為頻率比率值的內嵌函式。<br/>                                                                                                                                                         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[XAudio2：:P rogramming 參考](programming-reference.md)
</dt> </dl>

 

 




