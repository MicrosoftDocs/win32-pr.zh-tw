---
title: 關於 IWMPPluginEnable
description: 關於 IWMPPluginEnable
ms.assetid: 7611a197-f404-4cfb-88b0-05348a41ac42
keywords:
- Windows Media Player 外掛程式，介面
- 外掛程式，介面
- 數位信號處理外掛程式，介面
- DSP 外掛程式，介面
- 介面、DSP 外掛程式
- Windows Media Player 外掛程式、IWMPPluginEnable 介面
- 外掛程式，IWMPPluginEnable 介面
- 數位信號處理外掛程式，IWMPPluginEnable 介面
- DSP 外掛程式，IWMPPluginEnable 介面
- IWMPPluginEnable 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce7bf0f58be1d2623539cc5ac1329838246c8697
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931939"
---
# <a name="about-iwmppluginenable"></a>關於 IWMPPluginEnable

Windows Media Player 的 DSP 外掛程式需要 **IWMPPluginEnable** 介面。 **IWMPPluginEnable** 包含兩種方法，可儲存 Windows Media Player 是否已啟用 DSP 外掛程式。 Windows Media Player 會在建立 DSP 外掛程式的實例時呼叫 **IWMPPluginEnable：： SetEnable** ，如果已啟用外掛程式則傳遞 **TRUE** 值，否則為 **FALSE** 。

即使使用者選擇停用，也可能仍載入 DSP 外掛程式。 停用時，外掛程式必須將資料從輸入緩衝區複製到輸出緩衝區，並只執行格式轉換處理（如果適用）。

Windows Media Player 也會在釋放 DSP 外掛程式的實例之前呼叫這個方法。 這有助於讓外掛程式的用戶端檢查外掛程式是否目前已啟用。 例如，使用者介面外掛程式可能會變更其控制項的外觀，以警示使用者未連線到 DSP 外掛程式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**必要的介面**](required-interfaces.md)
</dt> </dl>

 

 




