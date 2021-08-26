---
description: 時間軸模型
ms.assetid: 53e782a2-0fab-46b4-b029-20017d9905bd
title: 時間軸模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67e5eeb60dce31fa466a518476bb3da341a3d2fda4fdeaa47ca58a89a904dded
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903804"
---
# <a name="the-timeline-model"></a>時間軸模型

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

*時間軸* 是一種物件，可 [DirectShow 編輯](directshow-editing-services.md) (DES) 用來代表影片編輯專案的服務。 編輯專案會以來源剪輯集合的形式啟動，其取自影片檔案、音效檔或仍為影像檔案。 剪輯的線性序列會形成 *軌跡*。在 DirectShow 編輯服務 (DES) 中，音訊和影片都會放在不同的曲目中。

曲目也可以分層。 多個音訊曲目會混合在一起，而且可能包含音訊效果，例如淡化或回音。 使用多個影片曲目來建立轉換。 例如，您可以建立從一個剪輯到另一個剪輯的抹除。 另一個範例是色度鍵，其中一個剪輯的背景會以不同的播放軌來進行索引。 (satelite 影像前面的氣象預測器是一種色度加密範例。 ) 

DES 使用樹狀結構來代表編輯：

-   音訊和影片剪輯會形成分葉節點或 *來源* 物件。
-   具有統一媒體類型 (音訊或影片) 的來源集合是一份播放 *軌*。
-   追蹤的集合是 *組合*。 組合會轉譯成它所包含之所有追蹤的複合。 組合可以包含其他組合，以允許追蹤的複雜排列。
-   組合的最上層集合和追蹤 (全都代表相同的媒體類型) 為 *群組*。
-   一或多個群組形成 *時間軸*。 時間軸是樹狀結構中的根節點。

時間軸必須包含至少一個群組。 每個群組都代表最終生產環境中的單一資料流程。 一般專案包含一個影片群組和一個音訊群組。 組合是選擇性的;如果有需要，則會提供更多結構。

下圖顯示組成時間軸的子父代關聯性：

![節點結構](images/timeline1.png)

以下顯示時間軸作為時態順序：

![時間軸圖例](images/timeline2.png)

頂端的箭號代表時間軸的方向，從零開始。 在「影片」群組中，「追蹤1」的優先順序高於「追蹤0」。 追蹤1中的來源物件會遮蔽追蹤0中的來源物件。 其中的 track 1 是空的，track 0 「顯示于」。 如先前所述，曲目只會一起混合在一起。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 DirectShow 編輯服務開始使用](getting-started-with-directshow-editing-services.md)
</dt> <dt>

[建立時間軸](constructing-a-timeline.md)
</dt> </dl>

 

 



