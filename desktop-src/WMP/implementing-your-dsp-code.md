---
title: 執行您的 DSP 程式碼
description: 執行您的 DSP 程式碼
ms.assetid: e1feaaee-1127-4a3a-9a4c-a30584a7e8ff
keywords:
- 'Windows Media Player 外掛程式、數位信號處理 (DSP) '
- '外掛程式，數位信號處理 (DSP) '
- 數位信號處理外掛程式，執行程式碼
- DSP 外掛程式，執行程式碼
- 數位信號處理外掛程式，修改範例程式碼
- DSP 外掛程式，修改範例程式碼
- 音訊 DSP 外掛程式，執行程式碼
- 影片 DSP 外掛程式，執行程式碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c9e17dad39a4ba0ebe79e31d9f3eead843d7f81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969465"
---
# <a name="implementing-your-dsp-code"></a>執行您的 DSP 程式碼

建立好範例 DSP 外掛程式之後，您可以修改程式碼，以建立您自己的 Windows Media Player DSP 外掛程式。 您所變更的方法以及您可以保留的方法，取決於下列因素：

-   您要允許使用者變更的屬性數目。 您肯定會想要變更預設屬性頁的執行，以符合您的需求，而且您可能需要新增其他屬性。
-   您的 DSP 外掛程式是否需要配置任何串流資源。 您的外掛程式可能需要額外的緩衝區。
-   在 Windows Media Player 停止提供輸入緩衝區中的資料之後，您的音訊 DSP 外掛程式是否需要繼續輸出資料。

下列各節使用 Windows Media Player 外掛程式 Wizard 產生的 DSP 外掛程式範例程式碼來說明重要的概念。 您可能會發現，開啟 Microsoft Visual Studio 並先產生範例程式碼很有説明，您可以在閱讀本節時參考它。 如需如何使用 Windows Media Player 外掛程式 Wizard 的詳細資訊，請參閱 [建立 DSP 外掛程式](building-a-dsp-plug-in.md)。



| 區段                                                                    | 描述                                                                                                       |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [執行音訊 DSP 外掛程式](implementing-an-audio-dsp-plug-in.md) | 討論根據 wizard 所產生的範例，建立您自己的音訊 DSP 外掛程式需要知道的事項。 |
| [執行 Video DSP 外掛程式](implementing-a-video-dsp-plug-in.md)   | 討論根據 wizard 所產生的範例，建立自己的影片 DSP 外掛程式需要知道的事項。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於 DSP 外掛程式**](about-dsp-plug-ins.md)
</dt> </dl>

 

 




