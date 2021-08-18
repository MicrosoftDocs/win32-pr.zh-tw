---
title: 'Windows Media Player SDK (所需的介面) '
description: 瞭解 DirectShow 或媒體基礎中 Windows Media Player 所需的介面。
ms.assetid: 202d5769-edff-46df-bc05-bbb630a8f3f4
keywords:
- Windows Media Player 外掛程式，介面
- 外掛程式，介面
- 數位信號處理外掛程式，介面
- DSP 外掛程式，介面
- 介面、DSP 外掛程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18a3552cbe741b3b527c899e5bb7d68fe4d7c4e0bdc61203f822c57111e94a46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119646828"
---
# <a name="required-interfaces-windows-media-player-sdk"></a>Windows Media Player SDK (所需的介面) 

Windows Media Player 使用下列其中一個管線呈現音訊和影片。

-   DirectShow
-   媒體基礎

在 Microsoft Windows XP 及更早版本中，Player 會使用 DirectShow。 在 Windows Vista 中，播放機有時會使用 DirectShow，有時會使用媒體基礎。

DSP 外掛程式會執行下列部分或所有介面：

-   **IMediaObject**
-   **IWMPPluginEnable**
-   **IMFTransform**
-   **IMFGetService**
-   **ISpecifyPropertyPages**

可在 DirectShow 管線中執行的外掛程式，可執行 **IMediaObject** 和 **IWMPPluginEnable** 。 它也可以在媒體基礎所提供包裝函式內的媒體基礎管線中執行。 此類型的外掛程式稱為「Microsoft DirectX 媒體物件 (DMO) 。 通常會將 DMO 視為類似 DirectShow 中的篩選物件。 DMO 檔位於 Windows SDK 的 DirectShow 區段中。

 (執行 **IMFTransform** 和 **IMFGetService** 的外掛程式可以原生方式執行，媒體基礎管線中) 不需要任何包裝函式。 此類型的外掛程式稱為媒體基礎轉換 (MFT) 。 MFT 檔位於 Windows SDK 的媒體基礎區段中。

實 **IMediaObject**、 **IWMPPluginEnable**、 **IMFTransform** 和 **IMFGetService** 的外掛程式可以在 DirectShow 管線中執行，也可以在媒體基礎管線中以原生方式執行。 這種類型的外掛程式（稱為 *雙重模式的 DSP 外掛程式*）可以扮演 DMO 或 MFT 的角色。

當 Windows Media Player 在媒體基礎管線中使用雙重模式的 DSP 外掛程式時，它會先查詢 **IMFTransform** 介面。 如果查詢失敗，請 Windows Media Player **IMediaObject** 介面的查詢。 如果 **IMediaObject** 查詢成功，則外掛程式會包裝並新增至媒體基礎管線。

無論管線為何，允許使用者設定屬性的任何 DSP 外掛程式都必須執行 **ISpecifyPropertyPages**。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**DSP 外掛程式開發人員總覽**](dsp-plug-in-developer-overview.md)
</dt> <dt>

[**DSP 外掛程式介面**](dsp-plug-in-interfaces.md)
</dt> <dt>

[**DSP 外掛程式封裝**](dsp-plug-in-packaging.md)
</dt> </dl>

 

 




