---
description: 傳輸
ms.assetid: 63c5ff5b-293d-4a80-92e8-3ece41321095
title: 傳輸
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb55542e87939168d1d95350fd71081833e4263f342a3e67c00a7c6814d51e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903718"
---
# <a name="transports"></a>傳輸

若要透過篩選圖形來移動媒體資料，DirectShow 濾波器必須支援數個可能的通訊協定之一。 這些通訊協定稱為「傳輸」。 當兩個篩選準則連接時，它們必須支援相同的傳輸;否則無法交換媒體資料。 一般而言，傳輸需要其中一個 pin 支援特定的介面。 當篩選準則連線時，其中一個 pin 會查詢該介面的另一個。

大部分的 DirectShow 濾波器都會將媒體資料保存在主儲存體中，並將其傳遞至其他在 pin 連線上的篩選。 這種類型的傳輸稱為本機記憶體傳輸。 雖然本機記憶體傳輸是 DirectShow 中最常見的傳輸，但是並非所有篩選都使用它。 例如，某些篩選器會沿著硬體路徑傳送媒體資料，並只使用 pin 來提供控制資訊。 例如，請參閱 [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) 介面。

DirectShow 定義本機記憶體傳輸、推播模型和提取模型的兩種機制。 在推送模型中，來源篩選會產生資料，並將它傳遞給下一個篩選器下游。 該篩選會被動接收資料、處理資料，並進一步將它傳送給下游。 在提取模型中，來源篩選會連接到剖析器篩選器。 剖析器篩選器會從來源篩選要求資料。 來源篩選器會藉由傳遞資料來回應要求。 推送模型使用 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 介面，而提取模型則使用 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) 介面。

推送模型比提取模型更常見。 因此，接下來的文章會採用推送模型。 此區段中的最後一篇文章（ [提取模型](pull-model.md)）描述 **IAsyncReader** 介面與 **IMemInputPin** 有何不同。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[篩選 Graph 中的資料 Flow](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



