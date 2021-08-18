---
title: Echo 範例
description: Echo 範例
ms.assetid: f28af52f-e948-464c-9600-aa516ab984f4
keywords:
- Windows Media Player 外掛程式，Echo 範例總覽
- 外掛程式，Echo 範例總覽
- 數位信號處理外掛程式，Echo 範例總覽
- DSP 外掛程式，Echo 範例總覽
- 程式設計指南，DSP 外掛程式
- 範例，DSP 外掛程式
- Echo DSP 外掛程式範例，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 103054e82157d83085713937759de8aa9ed250a5491146ebe0c71559ab1ca338
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119762788"
---
# <a name="the-echo-sample"></a>Echo 範例

Windows Media Player 外掛程式 Wizard 可以建立 Microsoft Visual C++ 的 DSP 外掛程式專案。 由 wizard 產生的預設程式碼可讓使用者提供介於0和1之間的縮放比例，以供程式用來作為音訊範例的乘數。 這是非常簡單的執行，可讓您研究以瞭解 Windows Media Player 與 DSP 外掛程式的互動方式。《[關於 DSP 外掛程式](about-dsp-plug-ins.md)」一節中的資訊可協助您瞭解預設的執行方式。

本節所述的範例比較複雜一點。 此範例可讓使用者指定延遲時間（以毫秒為單位）和效果層級。 在播放包含脈衝程式碼 (PCM) 音訊的檔案時，此程式碼會使用這些值來產生 echo 效果。 Windows Media Player 轉譯的許多檔案類型都會使用 PCM 音訊。

本指南分為下列幾節：



| 區段                                                                                | 描述                                                                                                         |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Echo 範例總覽](echo-sample-overview.md)                                       | 描述範例的一般需求和規格。 描述外掛程式的運作方式。              |
| [Echo 範例屬性](echo-sample-properties.md)                                   | 描述如何修改 wizard 程式碼屬性，並針對 Echo 範例所需的新屬性加入方法。 |
| [修改 Echo 範例屬性頁](modifying-the-echo-sample-property-page.md) | 示範如何修改現有的屬性頁執行，以搭配 Echo 範例使用。                         |
| [使用串流資源](working-with-streaming-resources.md)               | 示範如何加入程式碼，以配置及釋放 Echo 範例所需的緩衝區。                                |
| [執行 CEcho：:D oProcessOutput](implementing-cecho--doprocessoutput.md)         | 說明如何執行可建立 echo 效果的程式碼。                                                   |
| [使用 Echo 範例 DSP 外掛程式](using-the-echo-sample-dsp-plug-in.md)             | 描述如何使用已完成的範例。                                                                          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**DSP 外掛程式程式設計指南**](dsp-plug-ins-programming-guide.md)
</dt> </dl>

 

 




