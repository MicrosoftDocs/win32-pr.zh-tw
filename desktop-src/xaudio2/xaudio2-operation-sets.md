---
description: 本總覽導入了數個 XAudio2 方法，您可以呼叫這些方法作為作業集的一部分。
ms.assetid: 5bfd747d-af65-f619-e549-be8130748261
title: XAudio2 操作集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68a7f16edfa461d9944691bc4535debc05f820150dadf746caece85cb68c9f97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089408"
---
# <a name="xaudio2-operation-sets"></a>XAudio2 操作集

本總覽導入了數個 XAudio2 方法，您可以呼叫這些方法作為作業集的一部分。

有數個 XAudio2 方法會採用 *OperationSet* 引數，這可讓它們作為延遲群組的一部分來呼叫。 在特定時間，您可以藉由呼叫函式 [**IXAudio2：： CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) 與該群組的 *OperationSet* 識別碼，同時套用整個變更集。 識別碼為任意數目。 因此，它可讓用戶端程式代碼的個別部分在沒有任何衝突的情況下，將個別的不可部分完成變更套用到圖形。 建議的作法是讓用戶端在需要產生唯一的新 *OperationSet* 識別碼時，遞增全域計數器。 對圖形進行的一組變更（以不可部分完成的方式套用）保證會是正確的範例。 例如，語音將會開始同步。

如果您現在將 *OperationSet* 設定為 XAUDIO2 \_ COMMIT \_ ，則變更會立即套用。 它會在方法呼叫之後的第一個音訊處理階段中生效。 如果您呼叫 [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) with XAUDIO2 \_ COMMIT \_ ALL，則會執行所有擱置中作業集的變更，不論其 *OperationSet* 識別碼為何。

某些方法會在從 XAudio2 回呼以立即 *OperationSet* 的 XAudio2 認可呼叫時立即生效 \_ \_ 。 所有其他採用 *OperationSet* 引數的方法，只會在呼叫方法之後，才會影響下一次處理階段 (如果立即呼叫 with XAUDIO2 \_ COMMIT \_) ，或在使用相同 *OperationSet* 來呼叫 [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges)之後。 因此，某些方法呼叫不一定會依照呼叫的順序來進行。

呼叫 [**IXAudio2：： StopEngine**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) 時，會以不可部分完成的方式認可所有暫止的作業。 無論提供的 *OperationSet* 值為何，在引擎停止時呼叫的任何方法都會立即生效。 當您重新開機引擎時，XAudio2 會回到非同步模式。

作業集很有用的簡單案例包括下列範例。

-   同時啟動多個語音。
-   同時提交緩衝區至語音、設定語音參數，以及開始語音。
-   對圖形進行大規模變更，例如將所有來源語音連接到新的 submix 語音。

如需使用作業集的範例，請參閱 [如何：將音訊方法分組為作業集](how-to--group-audio-methods-as-an-operation-set.md) 。

## <a name="operation-set-methods"></a>Operation Set 方法

您可以呼叫下列方法作為作業集的一部分。

-   [**IXAudio2SourceVoice::ExitLoop**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-exitloop)
-   [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters)
-   [**IXAudio2SourceVoice::SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio)
-   [**IXAudio2Voice：:D isableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect)
-   [**IXAudio2Voice::EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect)
-   [**IXAudio2Voice::SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes)
-   [**IXAudio2Voice::SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters)
-   [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix)
-   [**IXAudio2Voice::SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume)
-   [**IXAudio2SourceVoice：： Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start)
-   [**IXAudio2SourceVoice：： Stop**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-stop)

如先前所述，用戶端程式代碼最後必須呼叫函式 [**IXAudio2：： CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) 來執行延遲的變更。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[操作集](operation-sets.md)
</dt> <dt>

[XAudio2 程式設計指南](programming-guide.md)
</dt> <dt>

[使用方法：將音訊方法群組為操作集](how-to--group-audio-methods-as-an-operation-set.md)
</dt> </dl>

 

 
