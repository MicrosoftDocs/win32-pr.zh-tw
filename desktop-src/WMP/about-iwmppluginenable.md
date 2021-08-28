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
ms.openlocfilehash: dfa64c811bbc981114f47b6fee15af29a6402594eabec2b857d0098adb8db747
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470478"
---
# <a name="about-iwmppluginenable"></a>關於 IWMPPluginEnable

Windows Media Player 的 DSP 外掛程式需要 **IWMPPluginEnable** 介面。**IWMPPluginEnable** 包含兩種方法，可儲存 Windows Media Player 是否已啟用 DSP 外掛程式。 Windows Media Player 會在建立 DSP 外掛程式的實例時呼叫 **IWMPPluginEnable：： SetEnable** ，如果已啟用外掛程式則傳遞 **TRUE** 值，否則為 **FALSE** 。

即使使用者選擇停用，也可能仍載入 DSP 外掛程式。 停用時，外掛程式必須將資料從輸入緩衝區複製到輸出緩衝區，並只執行格式轉換處理（如果適用）。

Windows Media Player 也會在釋放 DSP 外掛程式的實例之前呼叫這個方法。 這有助於讓外掛程式的用戶端檢查外掛程式是否目前已啟用。 例如，使用者介面外掛程式可能會變更其控制項的外觀，以警示使用者未連線到 DSP 外掛程式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**必要的介面**](required-interfaces.md)
</dt> </dl>

 

 




