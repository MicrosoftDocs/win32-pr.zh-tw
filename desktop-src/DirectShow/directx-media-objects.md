---
description: DirectX 媒體物件
ms.assetid: e4424740-31b9-4317-8791-6a9aebb0c7e6
title: DirectX 媒體物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00ef7dc17ab595748d9ccbfa16e33e7b4b8057d161c7f1e5d9f589e6768ec35f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821193"
---
# <a name="directx-media-objects"></a>DirectX 媒體物件

> [!Note]  
> DMOs 已被 [媒體基礎轉換](/windows/desktop/medfound/media-foundation-transforms) (MFTs) 取代。 仍支援 DMO 介面。 但是，如果您要撰寫自訂編解碼器或音訊/視頻處理外掛程式，您應該考慮將它實作為 MFT。

 

 (DMOs) 的 DirectX 媒體物件是以 COM 為基礎的資料串流元件。 在某些方面，DMOs 與 Microsoft DirectShow 濾波器類似。 如同 DirectShow 篩選，DMOs 會取得輸入資料，並使用它來產生輸出資料。 不過， (Api) 的應用程式開發介面比 DirectShow 的相對應 Api 簡單得多。 因此，DMOs 比較容易建立、測試和使用。 DMOs 可用於許多案例：

-   以 DirectShow 為基礎的應用程式可以透過稱為[DMO 包裝](dmo-wrapper-filter.md)函式的 DirectShow 篩選器來使用 DMOs。 篩選和 DMOs 之間的差異對應用程式而言是透明的。 應用程式不會直接呼叫 DMO api。
-   以 Microsoft DirectSound 為基礎的應用程式可以使用 [音訊效果 DMOs]。 同樣地，較高層級的 DirectSound api 會將應用程式從低層級的 DMO api 中防護。
-   應用程式可以直接使用 DMOs。

因此，藉由撰寫 DMO，您會建立可用於各種應用程式的元件。 本檔包含下列各節：

-   [關於 DMOs](about-dmos.md)
-   [使用 DMOs](using-dmos.md)
-   [撰寫 DMO](writing-a-dmo.md)
-   [媒體參數](media-parameters.md)
-   [DMO參考](dmo-reference.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow](directshow.md)
</dt> </dl>

 

 
