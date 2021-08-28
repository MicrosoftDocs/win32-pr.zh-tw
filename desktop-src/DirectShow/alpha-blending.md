---
description: Alpha 混色
ms.assetid: 56618e74-32cc-48f8-83b6-4fc31ab6fc36
title: 'Alpha 混合 (DirectShow) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ffe2a81affdfb4fec8cd8363330cd0505851eedb96bbf635fe754c50610df82
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537468"
---
# <a name="alpha-blending-directshow"></a>Alpha 混合 (DirectShow) 

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

本文說明[DirectShow 編輯服務](directshow-editing-services.md) (DES) 的 Alpha 混色。

Alpha 會測量圖元或影像的透明度。 在32位未壓縮的 RGB 影片中，四個元件會定義每個圖元： () 的 Alpha 通道，以及 (RGB) 的三個色彩元件。 Alpha 值為零的圖元是完全透明的。 Alpha 值為255的圖元不是透明的。 在這些值之間，圖元具有不同程度的透明度。

DirectShow 定義32位 RGB 影片的兩種媒體類型：

-   **MEDIASUBTYPE \_ARGB32**：影片是32位 RGB，具有有效的 Alpha 色板。
-   **MEDIASUBTYPE \_RGB32**：圖元是32位，但 Alpha 通道不一定是有效的。

若要在 DES 中執行 Alpha 混色，請將影片群組的未壓縮媒體類型設定為 MEDIASUBTYPE \_ ARGB32。 在 c + + 中，呼叫 [**IAMTimelineGroup：： SetMediaType**](iamtimelinegroup-setmediatype.md) 方法。 在 XTL 格式中，將 [**群組**](group-element.md)元素的 [**bitdepth**](bitdepth-attribute.md)屬性設定為32也會完成這項工作。

接下來，您需要包含 Alpha 通道的影片資料。 有幾個選項：

-   您可以使用已具有 Alpha 資料的32位 RGB 影片的 AVI 檔案。 目前， (WMF) 原始程式檔的 MPEG 或 Microsoft Windows 媒體格式不支援 Alpha。
-   DES 支援32位點陣圖 (.bmp) 和 Targa (. tga) 具有 Alpha 資料的檔案。
-   您可以撰寫自訂來源篩選器，以使用 Alpha 建立32位 RGB 資料。 輸出媒體類型必須是 **MEDIASUBTYPE \_ ARGB32**。 在時間軸來源物件中使用篩選做為子物件。

如果您的影片來源沒有 Alpha，您可以使用會建立 Alpha 資料的效果。 [Alpha Setter 效果](alpha-setter-effect.md)會將整個影像的 Alpha 通道設定為常數值。 若要在一段時間內改變 Alpha，請使用具有 Alpha Setter 效果的 [**IPropertySetter**](ipropertysetter.md) 介面。 只要群組的未壓縮媒體類型是 **MEDIASUBTYPE \_ ARGB32**，原始來源就不需要是32位。

最後，將影片傳遞給執行 Alpha 混色的效果或轉換。 [組合器轉換](compositor-transition.md)會執行 Alpha 混合，而[按鍵轉換](key-transition.md)可以使用 Alpha 值來做為索引鍵。

下列範例 XTL 專案會執行 Alpha 混色：


```C++
<timeline>
<group type="video" bitdepth="32" width="320" height="240">
<track>
  <clip start="0" stop="6" src="c:\Example.avi" />
</track>
<track>
  <clip start="0" stop="6" src="c:\Example2.avi">
    <!-- Alpha Setter effect. -->
    <effect clsid="{506D89AE-909A-44f7-9444-ABD575896E35}" start="0" stop="6">
      <param name="alpha" value="255">
        <linear time="6" value="0" />
      </param>
    </effect>
  </clip>
  <!-- Key transition, with alpha keying. -->
  <transition clsid="{C5B19592-145E-11d3-9F04-006008039E37}" start="0" stop="6">
    <param name="KeyType" value="3" />  
  </transition>
</track>
</group>
</timeline>
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 DirectShow 編輯服務](using-directshow-editing-services.md)
</dt> </dl>

 

 



