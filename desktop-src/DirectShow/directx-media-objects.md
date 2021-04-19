---
description: DirectX 媒體物件
ms.assetid: e4424740-31b9-4317-8791-6a9aebb0c7e6
title: DirectX 媒體物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2119fc8cce602bc1cc085886edd6852320aca180
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "107001775"
---
# <a name="directx-media-objects"></a>DirectX 媒體物件

> [!Note]  
> DMOs 已被 [媒體基礎轉換](/windows/desktop/medfound/media-foundation-transforms) (MFTs) 取代。 仍支援 SQL-DMO 介面。 但是，如果您要撰寫自訂編解碼器或音訊/視頻處理外掛程式，您應該考慮將它實作為 MFT。

 

 (DMOs) 的 DirectX 媒體物件是以 COM 為基礎的資料串流元件。 在某些方面，DMOs 類似于 Microsoft DirectShow 篩選。 就像 DirectShow 篩選器一樣，DMOs 會取得輸入資料並使用它來產生輸出資料。 不過， (Api) 的應用程式開發介面，比適用于 DirectShow 的相對應 Api 簡單得多。 因此，DMOs 比較容易建立、測試和使用。 DMOs 可用於許多案例：

-   以 DirectShow 為基礎的應用程式可以使用 DMOs，透過稱為「的 DirectShow [包裝](dmo-wrapper-filter.md) 函式」篩選器。 篩選和 DMOs 之間的差異對應用程式而言是透明的。 應用程式不會直接呼叫 SQL-DMO Api。
-   以 Microsoft DirectSound 為基礎的應用程式可以使用 [音訊效果 DMOs]。 同樣地，較高層級的 DirectSound Api 會將應用程式防護為低層級的 SQL-DMO Api。
-   應用程式可以直接使用 DMOs。

因此，藉由撰寫一組，您可以建立可在各種應用程式中使用的元件。 本檔包含下列各節：

-   [關於 DMOs](about-dmos.md)
-   [使用 DMOs](using-dmos.md)
-   [撰寫 SQL-DMO](writing-a-dmo.md)
-   [媒體參數](media-parameters.md)
-   [SQL-DMO 參考](dmo-reference.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow](directshow.md)
</dt> </dl>

 

 
