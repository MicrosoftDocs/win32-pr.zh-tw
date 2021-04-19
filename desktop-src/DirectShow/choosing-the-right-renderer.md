---
description: 選擇正確的影片轉譯器
ms.assetid: c57c4c68-ea1c-4198-94b4-e9b6e53bb625
title: 選擇正確的影片轉譯器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38a334fec59f6e3631217d48df7f0e8c83d87462
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972753"
---
# <a name="choosing-the-right-video-renderer"></a>選擇正確的影片轉譯器

DirectShow 提供數個影片轉譯器篩選，在下表中摘要說明。



| 篩選                                                                  | 備註                                           |
|-------------------------------------------------------------------------|---------------------------------------------------|
| [**增強的影片**](enhanced-video-renderer-filter.md) 轉譯器 (EVR)  | 使用 Direct3D 9。 需要 Windows Vista 或更新版本。 |
| [影片混合](video-mixing-renderer-filter-9.md) 轉譯器 9 (VMR-9)    | 使用 Direct3D 9。 需要 Windows XP 或更新版本。    |
| [影片混合篩選器 7](video-mixing-renderer-filter-7.md) (VMR-7)      | 使用 DirectDraw。 需要 Windows XP 或更新版本。    |
| [覆蓋混音器](using-the-overlay-mixer-in-video-capture.md)           | 透過 DirectDraw 支援硬體覆蓋。    |
| 舊版 [影片](video-renderer-filter.md) 轉譯器篩選。              | 使用 DirectDraw 或 (很少) GDI                   |



 

要使用哪一個轉譯器主要取決於您需要支援的 Windows 版本。

-   在 Windows Vista 和更新版本中，如果硬體支援，應用程式應該使用 EVR。 否則，會切換回 VMR 9 或 VMR-7。 EVR 提供比先前轉譯器更佳的效能和更佳的影片品質。 此外，它是設計來搭配桌面視窗管理員 (DWM) 。
-   在 Windows Vista 之前，如果硬體支援，則使用 VMR-9，且不需要影片埠功能。 否則，請使用 VMR-7。
-   在較舊的系統上，您可能需要使用重迭混音器 (的影片埠或硬體重迭支援) 或舊版的影片轉譯器篩選器。

[**IGraphBuilder：： Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render)和 [**RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)方法預設會使用 VMR-7。 如果硬體不支援 VMR-7，則這些方法會切換回舊版的影片轉譯器篩選器。 EVR 和 VMR 不是預設轉譯器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[影片轉譯](video-rendering.md)
</dt> </dl>

 

 



