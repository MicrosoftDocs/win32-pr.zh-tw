---
title: 連接到 Windows Media Player
description: 連接到 Windows Media Player
ms.assetid: c6afbd95-bcf8-438a-b854-776c543a5d51
keywords:
- Windows Media Player 外掛程式、登錄專案
- 外掛程式，登錄專案
- Windows Media Player 外掛程式，連接
- 外掛程式，連接
- 數位信號處理外掛程式，連接
- DSP 外掛程式，連接
- 數位信號處理外掛程式，登錄專案
- DSP 外掛程式，登錄專案
- 登錄、DSP 外掛程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8fa0851e271631e2c37bf716c427b5af34ade14
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374379"
---
# <a name="connecting-to-windows-media-player"></a>連接到 Windows Media Player

Windows Media Player 會自動連接到已安裝並正確註冊的 DSP 外掛程式。 DSP 外掛程式必須呼叫 [IWMPMediaPluginRegistrar：： WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) 來建立必要的登錄專案，以允許 Windows Media Player 辨識外掛程式，並將其列在 [選項] 對話方塊的 [ **外掛程式** ] 索引標籤上。 若要移除 **IWMPMediaPluginRegistrar：： WMPRegisterPlayerPlugin** 建立的登錄專案，外掛程式會呼叫 [IWMPMediaPluginRegistrar：： WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**DSP 外掛程式開發人員總覽**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




