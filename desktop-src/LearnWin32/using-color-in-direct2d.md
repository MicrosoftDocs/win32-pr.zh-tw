---
title: 在 Direct2D 中使用色彩
description: 在 Direct2D 中使用色彩
ms.assetid: 74b1f12c-b1de-4df1-85ba-0cf7a0009499
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efe6ded6d181ebcbca402161fe6af0b8fb8dd65f7d082632474136a9bd1ff551
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631516"
---
# <a name="using-color-in-direct2d"></a>在 Direct2D 中使用色彩

Direct2D 使用 RGB 色彩模型，其中的色彩是藉由結合紅色、綠色和藍色的不同值形成。 第四個元件（Alpha）測量圖元的透明度。 在 Direct2D 中，每個元件都是一個範圍為 0.0 1.0 的浮點值 \[ \] 。 針對三個色彩元件，此值會測量色彩的濃度。 針對 Alpha 元件，0.0 表示完全透明，1.0 表示完全不透明。 下表顯示各種100% 濃度的組合所產生的色彩。



| 紅色 | 綠色 | 藍色 | 色彩   |
|-----|-------|------|---------|
| 0   | 0     | 0    | 黑色   |
| 1   | 0     | 0    | 紅色     |
| 0   | 1     | 0    | 綠色   |
| 0   | 0     | 1    | 藍色    |
| 0   | 1     | 1    | 11：青色    |
| 1   | 0     | 1    | 桃紅色 |
| 1   | 1     | 0    | 黃色  |
| 1   | 1     | 1    | 白色   |



 

![顯示 rgb 色彩的影像。](images/graphics13.png)

0和1之間的色彩值會導致這些純量的不同陰影。 Direct2D 使用 [**D2D1 \_ COLOR \_ F**](/windows/desktop/Direct2D/d2d1-color-f) 結構來表示色彩。 例如，下列程式碼會指定洋紅。


```C++
    // Initialize a magenta color.

    D2D1_COLOR_F clr;
    clr.r = 1;
    clr.g = 0;
    clr.b = 1;
    clr.a = 1;  // Opaque.
```



您也可以使用衍生自 [**D2D1 \_ color \_ F**](/windows/desktop/Direct2D/d2d1-color-f)結構的 [**D2D1：： ColorF**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf)類別來指定色彩。


```C++
    // Equivalent to the previous example.

    D2D1::ColorF clr(1, 0, 1, 1);
```



## <a name="alpha-blending"></a>Alpha 混色

Alpha 混色藉由使用下列公式，將前景色彩與背景色彩混合來建立半透明區域。

<dl> color = af * Cf + (1-af) * Cb  
</dl>

其中 *Cb* 是背景色彩、 *Cf* 是前景色彩，而 *af* 是前景色彩的 Alpha 值。 此公式會成對套用至每個色彩元件。 例如，假設前景色彩是 **(r = 1.0、G = 0.4、B = 0.0)**（ **Alpha = 0.6**），背景色彩為 **(R = 0.0、G = 0.5、B = 1.0)**。 產生的 Alpha 混合色彩為：

R = (1.0 * 0.6 + 0 * 0.4) = 6   
G = (0.4 * 0.6 + 0.5 * 0.4) =. 44  
B = (0 * 0.6 + 1.0 * 0.4) =. 40  

下圖顯示此混合作業的結果。

![顯示 Alpha 混色的影像。](images/graphics15.png)

## <a name="pixel-formats"></a>像素格式

[**D2D1 \_ COLOR \_ F**](/windows/desktop/Direct2D/d2d1-color-f)結構不會描述圖元在記憶體中的表示方式。 在大多數情況下，這並不重要。 Direct2D 會處理將色彩資訊翻譯成圖元的所有內部詳細資料。 但是，如果您直接使用記憶體中的點陣圖，或結合 Direct2D 與 Direct3D 或 GDI，您可能必須知道像素格式。

[**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列舉定義了像素格式的清單。 這份清單相當長，但只有少數幾個與 Direct2D 相關。  (其他專案則是由 Direct3D) 使用。



| 像素格式                                                                                                                           | 描述                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_FORMAT_B8G8R8A8_UNORM"></span><span id="dxgi_format_b8g8r8a8_unorm"></span>**DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM**<br/> | 這是最常見的像素格式。 所有圖元元件 (紅色、綠色、藍色和 Alpha) 為8位不帶正負號的整數。 元件會以 *BGRA* 順序排列在記憶體中。  (請參閱下面的圖例。 ) <br/>                                          |
| <span id="DXGI_FORMAT_R8G8B8A8_UNORM"></span><span id="dxgi_format_r8g8b8a8_unorm"></span>**DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM**<br/> | 圖元元件是以 *RGBA* 順序為8位不帶正負號的整數。 換句話說，會交換紅色和藍色的元件，相對於 **DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM**。 只有硬體裝置才支援此格式。<br/>                             |
| <span id="DXGI_FORMAT_A8_UNORM"></span><span id="dxgi_format_a8_unorm"></span>**DXGI \_ 格式 \_ A8 \_ UNORM**<br/>                   | 此格式包含8位 Alpha 元件，不含 RGB 元件。 它很適合用來建立不透明度遮罩。 若要閱讀有關在 Direct2D 中使用不透明度遮罩的詳細資訊，請參閱 [相容的 A8 轉譯目標總覽](/windows/desktop/Direct2D/compatible-a8-rendertargets)。<br/> |



 

下圖顯示 BGRA 圖元版面配置。

![顯示 bgra 圖元版面配置的圖表。](images/graphics14.png)

若要取得轉譯目標的像素格式，請呼叫 [**ID2D1RenderTarget：： GetPixelFormat**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelformat)。 像素格式可能不符合顯示器解析度。 例如，顯示可能會設定為16位色彩，即使轉譯目標使用32位色彩也一樣。

### <a name="alpha-mode"></a>Alpha 模式

轉譯目標也有 Alpha 模式，它會定義如何處理 Alpha 值。



| Alpha 模式                           | 說明                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **D2D1 \_ ALPHA \_ 模式 \_ 忽略**        | 不會執行任何 Alpha 混色。 系統會忽略 Alpha 值。                                                                                                                                                                                                                                                                          |
| **\_直接 D2D1 ALPHA \_ 模式 \_**      | 直線。 圖元的色彩元件代表 Alpha 混色之前的色彩濃度。                                                                                                                                                                                                                           |
| **預 \_ 乘的 D2D1 ALPHA \_ 模式 \_** | 預乘 Alpha。 圖元的色彩元件表示色彩濃度乘以 Alpha 值。 這種格式比直接 Alpha 更有效率，因為 Alpha 混色公式的 (af Cf) 的詞彙是預先計算的。 不過，這種格式不適合儲存在影像檔案中。 |



 

以下是直接 Alpha 和預乘 Alpha 之間差異的範例。 假設想要的色彩是純紅色 (100% 濃度) 50% Alpha。 作為 Direct2D 類型，此色彩會以 (1，0，0，0.5) 表示。 使用直接 Alpha 和假設為8位的色彩元件，圖元的紅色元件為0xFF。 使用預乘 Alpha，紅色的元件會以50% 為相等的0x80 來調整。

[**D2D1 \_ COLOR \_ F**](/windows/desktop/Direct2D/d2d1-color-f)資料類型一律會使用直接 Alpha 表示色彩。 如有需要，Direct2D 會將圖元轉換成預乘的 Alpha 格式。

如果您知道您的程式不會執行任何 Alpha 混色，請使用 **D2D1 \_ Alpha \_ 模式來 \_ 略** 過 Alpha 模式來建立呈現目標。 此模式可以改善效能，因為 Direct2D 可以略過 Alpha 計算。 如需詳細資訊，請參閱 [改善 Direct2D 應用程式的效能](/windows/desktop/Direct2D/improving-direct2d-performance)。

## <a name="next"></a>下一個

[在 Direct2D 中套用轉換](applying-transforms-in-direct2d.md)

 

