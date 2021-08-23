---
description: 子
ms.assetid: 03cbd590-b573-4a98-9ab7-fe548800cfcb
title: 子
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaf828d0049816c0cbf932b96344b0270c4c9dbfb835a0750736551ff67b319b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633478"
---
# <a name="subobjects"></a>子

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

來源、效果和轉換都有指向其他 COM *物件的內部指標，稱為子* 物件。 子物件會執行物件的實際工作。 來源的子物件是建立影片或音訊資料的元件。 效果或轉換的子物件是轉換資料的元件;例如，在影片效果中，它會在影片串流中建立視覺效果。

子物件的類型取決於物件的類型：

-   來源：任何 DirectShow 來源篩選器或剖析器篩選器，支援搜尋並產生 DES 支援的格式。 如果有 DirectShow 篩選準則可將其解碼，則它可以是壓縮格式。
-   效果：適用于影片、任何2D 單一輸入 Microsoft® DirectX®轉換物件。 音訊的任何 DirectShow 音效效果篩選。
-   轉換：適用于影片、任何雙 D 雙輸入 DirectX 轉換物件。 音訊不支援轉換。

群組、組合和追蹤沒有子群組。

應用程式不會直接設定子物件指標。 針對效果和轉換，應用程式會呼叫 [**IAMTimelineObj：： SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) 方法來指定子物件的 GUID。 針對來源物件，應用程式通常會呼叫 [**IAMTimelineSrc：： SetMediaName**](iamtimelinesrc-setmedianame.md) 來指定原始程式檔的名稱。 但是， **SetSubObjectGUID** 方法也可以用於來源物件，以指定篩選 (CLSID) 的類別識別碼。

如需詳細資訊，請參閱使用 [來源](working-with-sources.md) 及 [處理效果和轉換](working-with-effects-and-transitions.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[時間軸元件的總覽](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



