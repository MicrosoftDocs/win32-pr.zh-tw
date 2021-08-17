---
title: 優先順序
description: 優先順序
ms.assetid: 3865ea8a-2489-4714-9a05-d1082589841f
keywords:
- Windows媒體中繼檔，優先順序順序
- Windows媒體中繼檔，優先順序
- 中繼檔，優先權順序
- 中繼檔，優先順序
- Windows媒體，中繼檔
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 12b55f34dd18fa6122d3f1588111aaffe374f2d87c06ef9100cbac057efd4bd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119467989"
---
# <a name="order-of-precedence"></a>優先順序

並非所有的中繼檔元素屬性都有相等的建立。 某些中繼檔元素屬性會覆寫其他元素屬性。 專案屬性可以根據位置和順序，依據類似的元素屬性來覆寫。 中繼檔播放清單的任何屬性都會覆寫參考 Windows 媒體檔案中包含的屬性。 覆寫另一個屬性的屬性會有較高的優先順序。

下表顯示階層（最高優先順序到最低）。 永遠不會覆寫最高優先順序的專案。



| 範圍                    | 階層                                   |
|--------------------------|---------------------------------------------|
| 「簽署的 DRM 內容」     | 永遠不會覆寫。                           |
| **REF** 元素範圍    | 僅由已簽署的 DRM 內容覆寫。      |
| **ENTRY** 元素範圍  | 覆寫下列類別目錄的元素。 |
| **ASX** 範圍            | 覆寫媒體檔案元素。              |
| Windows媒體檔案範圍 | 由上述所有的覆寫。             |



 

-   「簽署的 DRM 內容」-數位簽章物件。

    已簽署 DRM 內容的屬性將會覆寫所有其他屬性。 例如，將不會覆寫「簽署的 DRM 內容」的著作權資訊。 它一律會進行資料流程處理和呈現。

-   **REF** 元素範圍

    **REF** 元素的屬性將會覆寫其他元素屬性，但不會覆寫已簽署的 DRM 內容。

-   **專案** 範圍

    **專案專案** 的屬性將會由 **REF** 元素屬性覆寫，但會覆寫其他元素屬性。 **輸入專案專案** 的 **標題** 中繼資料會顯示，而不是來自媒體檔案的標題資訊。

-   **ASX** 範圍

    中繼檔中輸入的任何屬性都會覆寫 Windows 媒體檔中所包含的屬性。 **專案專案** 的屬性會覆寫 **ASX** 元素屬性。 在播放 **專案專案** 的參考 media 剪輯時，會顯示來自 **輸入** 元素的 **標題** 中繼資料，而不是來自 **ASX** 元素的標題資訊。

-   Windows媒體檔案範圍

    任何元檔案屬性都會覆寫 Windows 媒體檔案的屬性。 只有在中繼檔中沒有針對該元素定義的中繼資料時，才會顯示媒體檔案中繼資料。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立中繼檔播放清單**](creating-metafile-playlists.md)
</dt> <dt>

[**中繼檔播放清單**](metafile-playlists.md)
</dt> <dt>

[**Windows媒體中繼檔元素參考**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows媒體中繼檔指南**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




