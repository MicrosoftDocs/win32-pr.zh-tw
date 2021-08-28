---
title: 格式協調
description: 格式協調
ms.assetid: 7847d4e3-1250-4c35-88e1-52d61bf1553f
keywords:
- Windows Media Player 外掛程式，格式協調
- 外掛程式，格式協調
- 數位信號處理外掛程式，格式協調
- DSP 外掛程式，格式協商
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69669bc3af82400ea62d154335d117fef185d0b34184be4101ffa5ae309e6ccb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054966"
---
# <a name="format-negotiation"></a>格式協調

針對 Windows Media Player 和 DSP 外掛程式以共用資料，這兩個程式都必須同意其正在處理的資料格式。 DSP 外掛程式會執行播放機呼叫的方法，以判斷外掛程式所支援的格式。 此外掛程式也會執行播放機呼叫以設定目前格式的方法。

如果外掛程式作為 DirextX 媒體物件 (DMO) ，Windows Media Player 藉由呼叫 **IMediaObject** 介面的方法來探索和設定媒體格式。 例如，播放程式會重複呼叫外掛程式的 **IMediaObject：： GetInputType** ，以取得外掛程式所支援的所有輸入格式清單。 DMO 外掛程式使用 **DMO \_ 媒體 \_ 類型** 結構來組織指定媒體格式的資訊。 如需 DMO 外掛程式和播放機如何協商格式的詳細資訊，請參閱[關於 IMediaObject](about-imediaobject.md)。

如果外掛程式做為媒體基礎轉換 (MFT) ，Windows Media Player 會藉由呼叫 **IMFTransform** 介面的方法，來探索和設定媒體格式。 例如，播放程式會重複呼叫外掛程式的 **IMFTransform：： GetInputAvailableType** ，以取得外掛程式所支援的所有輸入格式清單。 MFT 外掛程式和播放機會使用 **IMFMediaType** 介面來組織和交換格式資訊。

只有當外掛程式支援與所播放數位音訊的相同位深度時，Windows Media Player 才會使用音訊 DSP 外掛程式。 比方說，如果數位音訊是20位，則必須撰寫外掛程式來處理20位音訊。 針對 CD 音訊，DSP 外掛程式必須支援20位處理。

在設定為使用身歷聲喇叭的電腦上進行多重通道內容的格式協調期間，Windows Media Player 先嘗試透過呼叫 **IMediaObject：： SetInputType** 和 **IMediaObject：： SetOutputType** 來連線到使用現有輸入和輸出格式的音訊 DSP 外掛程式。 一旦發生此初始協商，播放程式就會列舉外掛程式所支援的格式，並嘗試協調播放機和外掛程式的最佳格式組合。 如果外掛程式接受 **WAVEFORMATEX** 結構所定義的身歷聲音訊 () 為初始協商期間的輸入格式，然後只接受 **WAVEFORMATEXTENSIBLE** 結構) 所定義的多頻道音訊 (，則播放程式會提供多頻道音訊做為外掛程式的輸入格式。 在格式化協商期間，可在 Microsoft Windows XP 作業系統中使用此行為。 它在後續版本中可能會變更或無法使用。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**DSP 外掛程式開發人員總覽**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




