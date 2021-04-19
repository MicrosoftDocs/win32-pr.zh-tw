---
description: 使用影片混合轉譯器
ms.assetid: 3d0fdfac-ec7e-4e02-886b-2039c607dac7
title: 使用影片混合轉譯器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5baf7d559eed0d3111876924520952b55c6da2e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983718"
---
# <a name="using-the-video-mixing-renderer"></a>使用影片混合轉譯器

就效能和廣泛的功能而言， (VMR) 濾波器的影片混合轉譯器代表 Windows 平臺上的下一代影片轉譯。 VMR 會取代重迭 [混音](overlay-mixer-filter.md) 器和 [影片](video-renderer-filter.md)轉譯器，並新增許多新的混合功能。

VMR 有兩個版本：

-   VMR-7，使用 DirectDraw 7 進行轉譯。
-   使用 Direct3D 9 的 VMR-9。

VMR-7 可在 Windows XP 和更新版本上使用，但無法再轉散發。 VMR-9 可在 DirectX 9 支援的所有平臺上轉散發。 這兩個 VMR 篩選在其執行和其公開的介面中非常類似。

VMR-9 有自己的 CLSID 以及本身的一組介面、結構和列舉型別，這些型別與 VMR-7 的對應資料類型不一定相同，原因是 DirectDraw 7 和 Direct3D 9 之間的根本差異。 VMR-9 介面的結尾都是 "9"，例如 **IVMRStreamConfig9**，而結構和列舉型別在其名稱中都有 "VMR9"，以區別于與 VMR-7 搭配使用的資料類型。

若要確保回溯相容性，VMR-9 不是任何系統上的預設轉譯器。 若要使用 VMR-9，您必須使用 [**IFilterGraph：： AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) 方法，明確地將它新增至篩選圖形，並在連接到任何上游篩選器之前進行設定。

本文包含下列各節。 除非有注明，否則這些章節中的資訊適用于 VMR-7 和 VMR 9 的篩選準則。

-   [關於影片混合轉譯](about-the-video-mixing-render.md)
-   [作業的 VMR 模式](vmr-modes-of-operation.md)
-   [建立 VMR 9 篩選圖形](building-a-vmr-9-filter-graph.md)
-   [使用 VMR 混合模式](using-vmr-mixing-mode.md)
-   [設定交錯喜好設定](setting-deinterlace-preferences.md)
-   [使用 VMR 來進行 DirectShow 篩選器開發人員](using-the-vmr-for-directshow-filter-developers.md)
-   [使用認證輸出保護通訊協定 (COPP) ](using-certified-output-protection-protocol--copp.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[影片混合轉譯器篩選器7](video-mixing-renderer-filter-7.md)
</dt> <dt>

[影片混合轉譯器篩選器9](video-mixing-renderer-filter-9.md)
</dt> </dl>

 

 



