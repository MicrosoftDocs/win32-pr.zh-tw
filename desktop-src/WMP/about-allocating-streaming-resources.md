---
title: 關於配置串流資源
description: 關於配置串流資源
ms.assetid: b09633c4-58f7-4e3e-bb4d-007845baaccf
keywords:
- Windows Media Player 外掛程式、音訊 DSP
- 外掛程式、音訊 DSP
- 數位信號處理外掛程式，音訊串流資源
- DSP 外掛程式、音訊串流資源
- 音訊 DSP 外掛程式、串流資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f815fe9875f2e93e140b577da6e00dd7c684c1fedbad13234ecfbf87ca84ddb9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903728"
---
# <a name="about-allocating-streaming-resources"></a>關於配置串流資源

Windows Media Player 外掛程式 Wizard 產生的範例 DSP 外掛程式不需要任何額外的串流緩衝區。 不過，您可能會想要為您的 DSP 外掛程式配置記憶體資源。 例如，產生 echo 效果的外掛程式需要次要緩衝區來建立必要的時間延遲。

**IMediaObject** 介面包含兩種方法來處理這種情況。 Windows Media Player 會呼叫 **IMediaObject：： AllocateStreamingResources** ，讓您有機會建立您所需的任何緩衝區。 Windows Media Player 稍後會呼叫 **IMediaObject：： FreeStreamingResources** ，以允許您釋放先前配置的任何記憶體。 範例 DSP 外掛程式的執行也會從 *CProjectName*：：**FinalRelease** 呼叫 **FreeStreamingResources** ，以確保在終結外掛程式物件之前釋放所有資源。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**執行音訊 DSP 外掛程式**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




