---
description: 媒體參數
ms.assetid: 48b2bc2e-897d-4aa9-8a50-c2855a17dca5
title: 媒體參數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37cf7229cac3deb5b31a6c6879fd3b5896e5f4098a4cce64ac42d19970f5c569
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584338"
---
# <a name="media-parameters"></a>媒體參數

媒體參數可讓應用程式設定物件的屬性，讓它們以數學決定性的方式變更一段時間。

例如，假設音效工程師正在混用數位主磁帶，而且想要對關切這個領域區段套用稍微延遲，以填滿音效。 如果延遲突然剪下，則會 jarring 效果。 相反地，效果應該會開始100% 的 (不會有延遲) ，而且濕/試混合應該會逐漸增加，直到達到所需的層級為止。 此外，這種轉換應該遵循平滑曲線或線性進展。 為了支援此案例，DMO 可以公開下列介面：

-   [**IMediaParamInfo**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparaminfo) 包含探索所支援屬性之相關資訊的方法。 一般而言，用戶端會在開始串流資料之前呼叫這些方法。
-   [**IMediaParams**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparams) 包含的方法可設定在串流期間參數將遵循的曲線。

這些介面的設計主要是為了 DMOs，但是任何物件都可以支援它們。 在本節中，term *參數* 會參考任何支援這兩個介面的屬性。

本節包含下列主題：

-   [參數曲線](parameter-curves.md)
-   [參數資訊](parameter-information.md)
-   [信封區段](envelope-segments.md)
-   [計算參數值](calculating-parameter-values.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectX 媒體物件](directx-media-objects.md)
</dt> </dl>

 

 



