---
title: 執行音訊 DSP 外掛程式
description: 執行音訊 DSP 外掛程式
ms.assetid: 93ff0c45-f418-443d-8fba-c0a62f6e4e80
keywords:
- Windows Media Player 外掛程式、音訊 DSP
- 外掛程式、音訊 DSP
- 數位信號處理外掛程式，執行程式碼
- DSP 外掛程式，執行程式碼
- 數位信號處理外掛程式，修改範例程式碼
- DSP 外掛程式，修改範例程式碼
- 數位信號處理外掛程式，音訊執行
- DSP 外掛程式，音訊執行
- 音訊 DSP 外掛程式，執行程式碼
- 音訊 DSP 外掛程式，修改範例程式碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f18ca0aada7072ca7cd1c0796c3cd6770a9b45340a4d9f67a342944f4c22887
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338639"
---
# <a name="implementing-an-audio-dsp-plug-in"></a>執行音訊 DSP 外掛程式

若要建立處理音訊的 Windows Media Player DSP 外掛程式，您必須修改名為 **DoProcessOutput** 的函式中的範例程式碼。 每次 Windows Media Player 成功呼叫 **IMediaObject：:P rocessoutput**，就會呼叫 **DoProcessOutput** 。 它是執行數位信號處理工作的函式，這些工作會產生 DSP 外掛程式預定產生的聲音結果。

處理音訊串流就像處理計時事件一樣。 **DoProcessOutput** 將會以特定間隔重複呼叫。 每次程式碼執行時，都必須處理特定數目的位元組資料。 **DoProcessOutput** 包含下列參數：



| 參數          | 描述                                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| *pbOutputData*     | 這是緩衝區的 **位元組** 指標，可讓您的 **DoProcessOutput** 執行必須複製其處理過的資料。 |
| *pbInputData*      | 這是緩衝區的常數 **位元組** 指標，其中包含要處理的資料。                               |
| *cbBytesToProcess* | 這是 **DWORD** 值，包含要處理之輸入緩衝區中的位元組數目。             |



 

下列各節提供有關如何修改 Windows Media Player 外掛程式 Wizard 產生的程式碼，以建立您自己的音訊 DSP 外掛程式的詳細資料：

-   [執行 DoProcessOutput](implementing-doprocessoutput.md)
-   [將屬性新增至範例音訊 DSP 外掛程式](adding-properties-to-the-sample-audio-dsp-plug-in.md)
-   [執行 DSP 外掛程式的屬性頁](implementing-the-property-page-for-a-dsp-plug-in.md)
-   [變更範例音訊 DSP 外掛程式屬性](changing-the-sample-audio-dsp-plug-in-property.md)
-   [關於中斷](about-discontinuity.md)
-   [關於配置串流資源](about-allocating-streaming-resources.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於 DSP 外掛程式**](about-dsp-plug-ins.md)
</dt> </dl>

 

 




