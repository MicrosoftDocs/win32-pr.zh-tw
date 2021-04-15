---
description: XAPOFX 是一組音訊效果，可執行 XAPO 介面以在 XAudio2 中使用。 XAPOFX 包含數個效果，以及用來建立效果實例的一般機制。
ms.assetid: 762062de-4e19-5e42-8059-e2f8741bd362
title: XAPOFX 總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb8979b5de50406d46bc472e18ca4a6479679e22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511909"
---
# <a name="xapofx-overview"></a>XAPOFX 總覽

XAPOFX 是一組音訊效果，可執行 [XAPO](xapo-overview.md) 介面以在 XAudio2 中使用。 XAPOFX 包含數個效果，以及用來建立效果實例的一般機制。

## <a name="included-effects"></a>包含的效果

下表說明 XAPOFX 所包含的效果。 

| 效果             | 描述                                                                                                                                                                                           | 參數結構                                                     | 參數常數                                              | 規格需求                                                                                                              |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| FXECHO             | Echo 效果。                                                                                                                                                                                       | [**FXECHO \_ 參數**](/windows/desktop/api/xapofx/ns-xapofx-fxecho_parameters)                         | [**FXECHO 常數**](fxecho-constants.md)                     | 僅支援 FLOAT32 音訊格式。                                                                                      |
| FXEQ               | 四個頻外的等化器。                                                                                                                                                                                | [**FXEQ \_ 參數**](/windows/desktop/api/xapofx/ns-xapofx-fxeq_parameters)                             | [**FXEQ 常數**](fxeq-constants.md)                         | 僅支援 FLOAT32 音訊格式。 取樣率必須介於 22000 Hz 到 48000 Hz 之間。                             |
| FXMasteringLimiter | 磁片區限制器。                                                                                                                                                                                     | [**FXMASTERINGLIMITER \_ 參數**](/windows/desktop/api/xapofx/ns-xapofx-fxmasteringlimiter_parameters) | [**FXMASTERINGLIMIT 常數**](fxmasteringlimit-constants.md) | 僅支援 FLOAT32 音訊格式。                                                                                      |
| FXReverb           | 簡單的回音效果。<br/> XAudio2 也會提供實普林斯頓數位回音（可利用 [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb)具現化）的效果。<br/> | [**FXREVERB \_ 參數**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters)                     | [**FXREVERB 常數**](fxreverb-constants.md)                 | 僅支援 FLOAT32 音訊格式。 此外，它只支援 mono 輸出的 mono 輸入，以及身歷聲輸出的身歷聲輸入。 |



 

## <a name="creating-an-instance-of-an-effect-included-in-xapofx"></a>建立包含在 XAPOFX 中之效果的實例

XAPOFX 會提供 [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) 函式，作為建立效果實例的一般機制。 **CreateFX** 會取得效果的 CLSID，並將 IUnknown 介面指標傳回給效果的實例。

## <a name="using-xapofx-in-xaudio2"></a>在 XAudio2 中使用 XAPOFX

使用 [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) 具現化的效果會在 XAudio2 中使用，方法是將它們附加至語音。 每個 XAudio2 voice 都有一個效果鏈，其中包含零或多個音訊效果。 傳送至語音的音訊資料會在傳送到語音輸出目標之前通過鏈中的每個效果。 語音會取得每個效果的輸出，然後將其送入鏈中的下一個效果，直到鏈中沒有任何效果。 若要將 XAPOFX 效果附加至 XAudio2 聲音，請以效果的資訊填妥 [**XAudio2 \_ 效果 \_ 鏈**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) 結構，並將它傳遞給 [**IXAudio2Voice：： SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain)。

如需 XAudio2 效果鏈的詳細資訊，請參閱 [XAudio2 音訊效果](xaudio2-audio-effects.md)。

如需在 XAudio2 中使用 XAPOFX 的範例，請參閱 [如何：使用 XAudio2 中的 XAPOFX](how-to--use-xapofx-in-xaudio2.md)。

## <a name="xaudio2-implicit-effects"></a>XAudio2 隱含效果

除了 XAPOFX 所提供的 XAPOs 程式庫之外，XAudio2 還有內建的「回音」和「成交量計量」音訊效果。 您可以使用 [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) 和 [**XAudio2CreateVolumeMeter**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createvolumemeter)來建立這些內建效果。 如需使用其中一個內建效果的範例，請參閱 [如何：建立效果鏈](how-to--create-an-effect-chain.md) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊效果](audio-effects.md)
</dt> </dl>

 

 
