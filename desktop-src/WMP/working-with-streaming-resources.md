---
title: 使用串流資源
description: 使用串流資源
ms.assetid: 0258ad24-f1b9-4cb3-921c-068072fd2dbb
keywords:
- Windows Media Player 外掛程式，Echo 範例串流資源
- 外掛程式，Echo 範例串流資源
- 數位信號處理外掛程式，Echo 範例串流資源
- DSP 外掛程式，Echo 範例串流資源
- Echo DSP 外掛程式範例，串流資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 268dc57bfad71f8ee46a3b934e671e478ca6a78a6b05fc30b7123e7b3f7f6ba0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118567167"
---
# <a name="working-with-streaming-resources"></a>使用串流資源

Windows Media Player 外掛程式 Wizard 所產生的範例音訊 DSP 外掛程式專案，不需要由外掛程式配置任何串流資源。 不過，Echo 範例需要個別的緩衝區來保存音訊資料一段時間，以建立延遲效果。 緩衝區是由兩個方法管理： **IMediaObject：： AllocateStreamingResources**，它會建立緩衝區，而 **IMediaObject：： FreeStreamingResources** 則會釋放緩衝區。 **IMediaObject** 方法會在 Echo 中實作為。

下列各節提供有關管理緩衝區的進一步資訊：

-   [管理延遲緩衝區的變數](variables-to-manage-the-delay-buffer.md)
-   [執行 IMediaObject：： AllocateStreamingResources](implementing-imediaobject--allocatestreamingresources.md)
-   [執行 IMediaObject：： FreeStreamingResources](implementing-imediaobject--freestreamingresources.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Echo 範例**](the-echo-sample.md)
</dt> </dl>

 

 




