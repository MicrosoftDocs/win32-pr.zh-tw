---
title: DSP 外掛程式嚮導
description: DSP 外掛程式嚮導
ms.assetid: 3d1ae5ef-12c4-4db3-815a-2adc73353f20
keywords:
- Windows Media Player 外掛程式，外掛程式嚮導
- 外掛程式、外掛程式嚮導
- 數位信號處理外掛程式，外掛程式嚮導
- DSP 外掛程式，外掛程式嚮導
- 外掛程式嚮導
- Visual Studio，DSP 外掛程式 wizard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a7228056d821d2c2bca258f5c236fe1dce11d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507185"
---
# <a name="dsp-plug-in-wizard"></a>DSP 外掛程式嚮導

Windows Media Player SDK 提供可讓您新增至 Visual Studio 的外掛程式 wizard。 Wizard 可以產生各種外掛程式的範例程式碼，包括下列類型的 DSP 外掛程式：

-   音訊 DSP 外掛程式
-   音訊 DSP 外掛程式 (雙重模式) 
-   影片 DSP 外掛程式
-    (雙重模式的影片 DSP 外掛程式) 

這兩個基本的範例外掛程式（音訊 DSP 和 Video DSP）都會以 DirectX 媒體物件的形式運作， (的) 。 也就是說，每個範例外掛程式都會執行 **IMediaObject** 介面。 這兩個雙重模式範例外掛程式的每一個都可以做為一或媒體基礎轉換 (MFT) 。 也就是說，每個雙重模式的範例外掛程式都會同時執行 **IMediaObject** 介面和 **IMFTransform** 介面。

您可以編譯、連結、註冊和測試範例外掛程式程式碼。 然後您可以修改產生的範例程式碼，以建立您自己的 DSP 外掛程式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立 DSP 外掛程式**](building-a-dsp-plug-in.md)
</dt> <dt>

[**DSP 外掛程式開發人員總覽**](dsp-plug-in-developer-overview.md)
</dt> <dt>

[**Windows Media Player 11 的 DSP 外掛程式嚮導更新**](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md)
</dt> </dl>

 

 




