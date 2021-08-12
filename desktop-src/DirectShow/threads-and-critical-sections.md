---
description: 執行緒和重要區段
ms.assetid: e55acb06-03f4-4191-bffe-3196f41ef2c7
title: 執行緒和重要區段
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d13473a917ae49e80ec658b0d6187fdfdff80c6e3a080a229aca7ccbbe536c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651400"
---
# <a name="threads-and-critical-sections"></a>執行緒和重要區段

本節說明 DirectShow 篩選準則中的執行緒，以及在自訂篩選器中避免損毀或鎖死所應採取的步驟。

本節中的範例會使用虛擬程式碼來說明您需要撰寫的程式碼。 它們假設自訂篩選器使用衍生自 DirectShow 基類的類別，如下所示：

-   CMyInputPin：衍生自 [**CBaseInputPin**](cbaseinputpin.md)。
-   CMyOutputPin：衍生自 [**CBaseOutputPin**](cbaseoutputpin.md)。
-   CMyFilter：衍生自 [**CBaseFilter**](cbasefilter.md)。
-   CMyInputAllocator：輸入釘選器，衍生自 [**CMemAllocator**](cmemallocator.md)。 並非每個篩選都需要自訂配置器。 針對許多篩選準則， **CMemAllocator** 類別已足夠。

此章節包含下列主題。

-   [串流和應用程式執行緒](the-streaming-and-application-threads.md)
-   [暫停中](pausing.md)
-   [接收和傳遞範例](receiving-and-delivering-samples.md)
-   [傳遞資料流程結尾](delivering-the-end-of-stream.md)
-   [清除資料](flushing-data.md)
-   [停止中](stopping.md)
-   [取得緩衝區](getting-buffers.md)
-   [串流處理執行緒和篩選 Graph 管理員](streaming-threads-and-the-filter-graph-manager.md)
-   [篩選準則執行緒的摘要](summary-of-filter-threading.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[篩選準則開發人員的資料 Flow](data-flow-for-filter-developers.md)
</dt> <dt>

[撰寫 DirectShow 篩選](writing-directshow-filters.md)
</dt> </dl>

 

 



