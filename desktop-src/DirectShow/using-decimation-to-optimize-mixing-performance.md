---
description: 使用減去優化混合效能
ms.assetid: 94d4ce86-9d60-4fd4-ab01-851dc073680b
title: 使用減去優化混合效能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2218566ab31d159f6d0ab74320aa45eb5780bdc3de151de8a7c642016441bacf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049615"
---
# <a name="using-decimation-to-optimize-mixing-performance"></a>使用減去優化混合效能

> [!IMPORTANT]
> 本節所述的優化高度取決於基礎硬體。 除非您可以保證應用程式會使用何種類型的圖形硬體，否則可能會嚴重降低影片影像的外觀。

 

HDTV 需要大量的處理能力，但在較新的系統上，大部分都是由圖形配接器來提供。 但是，即使圖形配接器和解碼器可支援1920x1080 的解析度，使用者也不一定會將其監視設定為此解決方案。 在此情況下，需要圖形晶片才能建立 1920 x 1080 映射，然後在將其傳送至框架緩衝區之前，先減少解析度。

因為這會浪費處理能力，所以 VMR 會提供一種方法來刪減 (在轉譯至 DirectDraw 表面時，減少影像) 。 如果映射必須在轉譯後調整大小，就不需要額外的記憶體複製。

**VMR-7：** 若要啟用減去，請使用 MixerPref DecimateOutput 旗標來呼叫 [**IVMRMixerControl：： SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) \_ 。

**VMR-9：** 若要啟用減去，請使用 MixerPref9 DecimateOutput 旗標來呼叫 [**IVMRMixerControl9：： SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) \_ 。

您必須在 VMR 連接之前呼叫 **SetMixingPrefs** 方法。 當圖形正在執行時，不能變更混合喜好設定旗標。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 VMR 混合模式](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



