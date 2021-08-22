---
title: 執行 CEcho DoProcessOutput
description: 執行 CEcho DoProcessOutput
ms.assetid: afd91022-4e2d-46a2-a0f4-cd2b558536d6
keywords:
- Windows Media Player 外掛程式，Echo 範例 DoProcessOutput 方法
- 外掛程式，Echo 範例 DoProcessOutput 方法
- 數位信號處理外掛程式，Echo 範例 DoProcessOutput 方法
- DSP 外掛程式，Echo 範例 DoProcessOutput 方法
- Echo DSP 外掛程式範例，DoProcessOutput 方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07054950cabadbc835c9904d48cdb4e6ddf5f05c0822c997558381958a9857d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135641"
---
# <a name="implementing-cechodoprocessoutput"></a>執行 CEcho：:D oProcessOutput

**DoProcessOutput** 方法會執行數位信號處理。 這是對 Windows Media Player 所提供的資料進行變更的方法。 這是此方法的結果，當您的 Echo 範例外掛程式完成時，您會收到回應的回應。

在此範例中，外掛程式只會處理8位或16位的音訊。 您將需要對外掛程式的 wizard 範例程式碼進行一些變更，以移除處理較高位深度音訊的區段。 不過，請務必研究這些區段，因為您可能會決定為這些格式新增您自己的 echo 執行。

下列各節詳細說明您需要對程式碼進行的變更：

-   [移除程式碼以處理大於16個位的程式碼](removing-the-code-to-process-greater-than-16-bits.md)
-   [處理音訊資料](processing-the-audio-data.md)
-   [要執行處理的變數](variables-to-perform-processing.md)
-   [建立 Echo 效果](creating-the-echo-effect.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Echo 範例**](the-echo-sample.md)
</dt> </dl>

 

 




