---
description: 篩選開發人員的資料流程
ms.assetid: cc7378c8-e268-4caa-98eb-6dc9c3b5bcad
title: 篩選開發人員的資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccb4e4123e8617190a459ff500d1100c0dbbb8ca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025786"
---
# <a name="data-flow-for-filter-developers"></a>篩選開發人員的資料流程

本節將詳細說明如何透過篩選圖形來移動資料。 它著重于使用 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 或 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) 介面的本機記憶體傳輸。 它適用于撰寫自己的自訂篩選器的開發人員。 如需 Microsoft DirectShow 如何處理資料流程的一般簡介，請參閱 [篩選圖形中的](data-flow-in-the-filter-graph.md)資料流程。

許多資料會透過篩選圖形來移動。 它大致分為兩類：媒體資料和控制資料。 一般情況下，媒體資料會傳輸下游，而控制資料會傳輸到上游。 媒體資料包括構成資料流程的影片畫面、音訊範例、MPEG 封包等等，但也包含排清命令、串流結束通知，以及其他與資料流程一起傳送的資料。 控制資料不是媒體資料流程的一部分。 控制資料的範例包括品質控制要求和搜尋命令。

本節包含下列文章。

-   [傳遞範例](delivering-samples.md)
-   [處理資料](processing-data.md)
-   [資料流程結束通知](end-of-stream-notifications.md)
-   [新區段](new-segments.md)
-   [沖洗](flushing.md)
-   [尋求](seeking.md)
-   [動態格式變更](dynamic-format-changes.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[品質控制管理](quality-control-management.md)
</dt> <dt>

[執行緒和重要區段](threads-and-critical-sections.md)
</dt> <dt>

[撰寫 DirectShow 篩選器](writing-directshow-filters.md)
</dt> </dl>

 

 



