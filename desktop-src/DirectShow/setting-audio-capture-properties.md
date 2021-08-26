---
description: 設定音訊捕獲屬性
ms.assetid: 81400072-91d7-4db4-86d3-d072663e691f
title: 設定音訊捕獲屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0230f3a9679871380f6eecf09ad5589bfc02c13e0d1433bab8e3b4075de2cf5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078808"
---
# <a name="setting-audio-capture-properties"></a>設定音訊捕獲屬性

音訊捕獲篩選器上的每個輸入 pin 都會公開 [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) 介面。 您可以使用此介面來啟用或停用特定的輸入，方法是呼叫釘選上的 [**IAMAudioInputMixer：:p ui \_ 啟用**](/windows/desktop/api/Strmif/nf-strmif-iamaudioinputmixer-put_enable) 方法。 此外，也可以使用此介面來設定輸入的屬性，例如低音、高音和音量層級。 如果您要一次捕捉多個輸入，您可以透過篩選器本身的 **IAMAudioInputMixer** 介面，控制整體的低音、高音和音量層級。

適用于 capture 的可用取樣率和音訊格式取決於驅動程式。 在音訊捕獲篩選器的輸出釘選上使用 [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) 介面，以列舉可用的取樣率和格式，並設定所需的格式。 篩選可將下游連接到任何接受輸出釘選媒體類型的篩選。

音訊捕獲篩選器也會公開 [**IAMBufferNegotiation**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation) 介面。 此介面適用于控制音訊預覽中的延遲量。 根據預設，音訊捕獲篩選器會使用半秒的緩衝區大小。 此緩衝區大小最適合用於捕捉，但會導致半秒的預覽延遲。 若要減少延遲，請先呼叫 [**IAMBufferNegotiation：： SuggestAllocatorProperties**](/windows/desktop/api/Strmif/nf-strmif-iambuffernegotiation-suggestallocatorproperties) 方法，再連接音訊捕獲篩選器的輸出 pin。 這個方法會採用配置器 [**\_ 屬性**](/windows/win32/api/strmif/ns-strmif-allocator_properties) 結構的指標。 您可以使用 **cbBuffer** 成員來指定緩衝區大小（以位元組為單位）。 80毫秒的緩衝區通常是安全的，但30或40毫秒的緩衝區可能已足夠。 如果緩衝區太小，則音效品質將會降低。

 

 



