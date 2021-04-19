---
description: 音訊效果是接受傳入音訊資料的物件，並在資料傳遞之前對資料執行某些作業。 您可以使用效果來執行各種不同的工作，包括將回音新增至音訊串流以及監視尖峰音量層級。
ms.assetid: 8c3fa4ca-dcff-bd23-7220-7d0aeb6c6068
title: XAudio2 音訊效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8de87a65ea4321b5e8d73a837f79a3e56e8e3a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974070"
---
# <a name="xaudio2-audio-effects"></a>XAudio2 音訊效果

音訊效果是接受傳入音訊資料的物件，並在資料傳遞之前對資料執行某些作業。 您可以使用效果來執行各種不同的工作，包括將回音新增至音訊串流以及監視尖峰音量層級。

## <a name="effect-chains"></a>效果鏈

任何 XAudio2 聲音都可以裝載一連串的音訊效果。 您可以使用 [**XAUDIO2 \_ 效果 \_ 描述**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) 項結構的陣列來指定效果鏈。 每個描述項都包含用戶端所提供之效果物件的指標。 這些物件必須 (APO) 介面來執行音訊處理物件。 如需 APO 模型的詳細資訊，請參閱 [XAPO 總覽](xapo-overview.md) 。

當 XAudio2 引擎執行時，用戶端可以動態地修改效果鏈 () 、可以個別啟用或停用效果，而效果參數也可以變更，而不會干擾音訊。 每當效果圖形的任何方面變更時，XAudio2 會再次優化圖形，以避免不必要的處理。 請參閱 [**IXAudio2Voice：： SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain)、 [**IXAudio2Voice：： EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect)和 [**IXAudio2Voice：： SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters)。

將效果附加至 XAudio2 聲音之後，XAudio2 會控制效果，而且用戶端不應該對其進行任何進一步的呼叫。 確保這一點最簡單的方式，就是釋放效果的所有指標。

給定 XAudio2 聲音效果鏈中的效果，必須以該語音的處理範例費率取用並產生浮點音訊。 其可變更之音訊格式的唯一層面是通道計數 (例如，將 mono 效果轉換成 5.1) 。 用戶端可以使用 [**XAUDIO2 \_ 效果 \_ 描述**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor)元。**OutputChannels** 欄位，指定每個效果應產生的通道數目。 如果有任何效果無法滿足這些需求，或如果效果產生了下一個效果無法處理的通道數目，效果鏈就會失敗。 任何 [**IXAudio2Voice：： EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect) 或 [**IXAudio2Voice：:D**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) 會導致效果鏈停止滿足這些需求的 isableeffect 呼叫都將會失敗。

XAudio2 中使用的 APO 介面必須是 *破壞性* 的。 這表示它們一律會覆寫他們在輸出緩衝區中找到的任何資料。 否則，產生的音訊可能會不正確，因為 XAudio2 無法保證這些緩衝區先前已使用無聲初始化。

## <a name="xaudio2-built-in-effects"></a>XAudio2 內建效果

下表列出 XAudio2 所提供的內建音訊效果及其建立方法。 

| 效果       | 建立方法                                              |
|--------------|--------------------------------------------------------------|
| 混響       | [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb)           |
| 磁片區計量 | [**XAudio2CreateVolumeMeter**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createvolumemeter) |



 

如需建立和使用音訊效果實例的範例，請參閱 [如何：建立效果鏈](how-to--create-an-effect-chain.md)。

## <a name="custom-effects-in-xaudio2"></a>XAudio2 中的自訂效果

[XAPO](xapo-overview.md) API 提供的架構可讓您建立可在 XAudio2 中使用的自訂音訊效果。 如需使用 XAPO 建立自訂效果的範例，請參閱 [如何：建立 XAPO](how-to--create-an-xapo.md)。

## <a name="xapo-effect-library-xapofx"></a>XAPO 效果程式庫 (XAPOFX) 

[XAPOFX](xapofx-overview.md) 提供額外的 XAPOs 程式庫，以及建立它們的常用機制。 如需搭配使用 XAPOFX 與 XAudio2 的範例，請參閱 [如何：使用 XAudio2 中的 XAPOFX](how-to--use-xapofx-in-xaudio2.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊效果](audio-effects.md)
</dt> <dt>

[XAudio2 程式設計指南](programming-guide.md)
</dt> </dl>

 

 
