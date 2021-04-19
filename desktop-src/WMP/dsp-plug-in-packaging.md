---
title: DSP 外掛程式封裝
description: DSP 外掛程式封裝
ms.assetid: 5d40a39b-0fe8-4f77-9465-8e31d1f2708e
keywords:
- Windows Media Player 外掛程式，媒體基礎管線
- 外掛程式，媒體基礎管線
- 數位信號處理外掛程式，媒體基礎管線
- DSP 外掛程式，媒體基礎管線
- 媒體基礎管線
- Windows Media Player 外掛程式、DirectShow 管線
- 外掛程式，DirectShow 管線
- 數位信號處理外掛程式，DirectShow 管線
- DSP 外掛程式，DirectShow 管線
- DirectShow 管線
- 數位信號處理外掛程式，基本
- DSP 外掛程式，基本
- Windows Media Player 外掛程式，基本 DSP
- 外掛程式，基本 DSP
- 基本的 DSP 外掛程式
- Windows Media Player 外掛程式、雙重模式的 DSP
- 外掛程式、雙重模式的 DSP
- 數位信號處理外掛程式、雙重模式
- DSP 外掛程式、雙重模式
- 雙重模式的 DSP 外掛程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62535abe0d82975bf07fef178ac43cf066c6afbd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106995566"
---
# <a name="dsp-plug-in-packaging"></a>DSP 外掛程式封裝

Windows Media Player 使用下列其中一個管線呈現音訊和影片。

-   DirectShow
-   媒體基礎

在 Microsoft Windows XP 及更早版本中，Player 會使用 DirectShow。 在 Windows Vista 中，播放的有時會使用 DirectShow，有時會使用媒體基礎。

專為在 DirectShow 管線中執行而設計的 DSP 外掛程式，稱為 *基本的 dsp 外掛程式*。 基本的 DSP 外掛程式可作為 DirectX 媒體物件 (的) 。 基本的 DSP 外掛程式可在 DirectShow 管線中以原生方式執行，也可以在媒體基礎所提供包裝函式內的媒體基礎管線中執行。

DSP 外掛程式的設計目的是要以原生方式執行 (在 DirectShow 和媒體基礎管線中都不需要包裝函式) ，稱為 *雙重模式的 DSP 外掛程式*。 雙重模式的 DSP 外掛程式可作為一或媒體基礎轉換 (MFT) 。

DSP 外掛程式是封裝為自我註冊 .dll 檔案的 COM 物件。 外掛程式所執行的介面，取決於外掛程式是否設計為基本的 DSP 外掛程式或雙重模式的 DSP 外掛程式而定。 如需有關 DSP 外掛程式必須執行之介面的詳細資訊，請參閱 [必要的介面](required-interfaces.md)。

在媒體基礎管線中執行的 DSP 外掛程式 (原生或包裝) 必須將其執行緒模型註冊為 "Both"。 如需有關登錄子機碼和與 DSP 外掛程式相關聯之專案的詳細資訊，請參閱 [註冊 Dsp 外掛程式](registering-dsp-plug-ins.md)。

在媒體基礎管線中執行自訂介面和執行的 DSP 外掛程式 (原生或包裝) 必須與可封送處理跨進程界限的自訂介面的 proxy stub .dll 檔配對。 如需 proxy 存根元件的詳細資訊，請參閱 Windows Media Player 11 的將 [現有的 Dsp 外掛程式](updating-existing-dsp-plug-ins.md) 和 [更新加入至 Dsp 外掛程式的更新](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md)。

DSP 外掛程式物件不得建立為 singleton。 Windows Media Player 必須能夠建立特定 DSP 外掛程式的多個個別實例。

在 Windows Vista 受保護媒體路徑中執行的 DSP 外掛程式 (PMP) 必須經過簽署。 如需詳細資訊，請參閱 [Windows Vista 中受保護媒體元件的程式碼簽署](/windows-hardware/test/hlk/)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**DSP 外掛程式開發人員總覽**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 