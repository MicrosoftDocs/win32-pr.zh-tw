---
title: 混合效果
description: 使用 blend 效果來合併2個影像。 此效果有26種 blend 模式。
ms.assetid: 39D8BAA3-8FF3-4F10-99A0-B26FCA3018AE
keywords:
- blend 效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e248d1f7f41721d173510b8d10feac9be2e08f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844243"
---
# <a name="blend-effect"></a>混合效果

使用 blend 效果來合併2個影像。 此效果有26種 blend 模式。

這項效果的 CLSID 是 CLSID \_ D2D1Blend。

-   [混合範例](#blending-examples)
-   [效果屬性](#effect-properties)
-   [Blend 模式](#blend-modes)
-   [HSL 色彩空間轉換](#hsl-color-space-conversions)
    -   [從 RGB 轉換成 HSL](#converting-from-rgb-to-hsl)
    -   [從 HSL 轉換成 RGB](#converting-from-hsl-to-rgb)
-   [輸出點陣圖](#output-bitmap)
-   [範例程式碼](#sample-code)
-   [需求](#requirements)
-   [相關主題](#related-topics)

## <a name="blending-examples"></a>混合範例

以下是 blend 效果的每個 blend 模式的範例影像。 下一節將列出 blend 模式和對應模式屬性的完整清單

![所有可用 blend 模式的效果範例螢幕擷取畫面。](images/blend-modes.png)

以下是使用排除模式的另一個範例。



| 影像1之前                                                             |
|----------------------------------------------------------------------------|
| ![效果前的第一個來源影像。](images/default-before.jpg)    |
| 影像2之前                                                             |
| ![效果之前的第二個影像。](images/4-arthimetic-composite2.jpg) |
| After                                                                      |
| ![轉換後的影像。](images/5-blend.png)                      |



 


```C++
ComPtr<ID2D1Effect> blendEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Blend, &blendEffect);

blendEffect->SetInput(0, bitmap);
blendEffect->SetInput(1, bitmapTwo);
blendEffect->SetValue(D2D1_BLEND_PROP_MODE, D2D1_BLEND_MODE_EXCLUSION);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(blendEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>效果屬性



| 顯示名稱和索引列舉                 | 描述                                                                                                                                                                               |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [模式]<br/> D2D1 \_ BLEND \_ \_ 模式<br/> | 用於效果的 blend 模式。 如需詳細資訊，請參閱 [Blend 模式](#blend-modes) 。 此類型為 D2D1 \_ BLEND \_ 模式。<br/> 預設值為 D2D1 \_ BLEND \_ 模式 \_ 乘。<br/> |



 

## <a name="blend-modes"></a>Blend 模式

此處的表格顯示此效果的所有 blend 模式。 計算效果輸出所需的 helper 函式是在下一節中。

Color： O <sub>PRGB</sub>  =  *f* (f <sub>rgb</sub>，B <sub>rgb</sub>) \* f <sub>a</sub> \* B <sub>a</sub> + f <sub>RGB</sub> \* f <sub>a</sub> \* (1-B <sub>a</sub>) + B <sub>RGB</sub> \* B <sub>a</sub> \* (1-f <sub>a</sub>) 

Alpha： O<sub>a</sub> = F<sub>a</sub> \* (1-B<sub>a</sub>) + B<sub>a</sub>

其中：

-   O<sub>PRGB</sub> 是前置乘輸出色彩
-   O<sub>A</sub> 是輸出 Alpha
-   B<sub>RGB</sub> 是取消前置的目的地色彩
-   B<sub>A</sub> 是目的地 Alpha
-   F<sub>RGB</sub> 是取消前置的來源色彩
-   F<sub>A</sub> 是來源 Alpha
-   *f* (S <sub>Rgb</sub>，D <sub>rgb</sub>) 是一種會因 blend 模式而異的 blend 函數

某些 blend 模式需要從色調、飽和度、亮度 (HSL) 色彩空間轉換成 RGB。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>列舉型別</th>
<th>方程</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D2D1_BLEND_MODE_DARKEN</td>
<td>僅適用于 Alpha 的基本 blend 公式。 <img src="images/blend-mode-darken-1.png" alt="mathematical formula for a darken effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_MULTIPLY</td>
<td>僅適用于 Alpha 的基本 blend 公式。 <img src="images/blend-mode-multiply-1.png" alt="Mathematical formula for a mutiply effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_COLOR_BURN</td>
<td>使用 <em>f</em> (f<sub>Rgb</sub>、B<sub>rgb</sub>) = 的基本 blend 公式 <img src="images/blend-mode-colorburn-1.png" alt="Mathematical formula for a coor burn effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_LINEAR_BURN</td>
<td>使用 <em>f</em> (f<sub>Rgb</sub>、B<sub>rgb</sub>) = 的基本 blend 公式 <img src="images/blend-mode-linearburn-1.png" alt="Mathematical formula for a linear burn effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_DARKER_COLOR</td>
<td>僅適用于 Alpha 的基本 blend 公式。 <img src="images/blend-mode-darkencolor-1.png" alt="Mathematical formla for a darken color effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_LIGHTEN</td>
<td>僅適用于 Alpha 的基本 blend 公式。 <img src="images/blend-mode-lighten-1.png" alt="Mathematical formula for a lighten effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_SCREEN</td>
<td>僅適用于 Alpha 的基本 blend 公式。 <img src="images/blend-mode-screen-1.png" alt="Mathematical formula for a screen effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_COLOR_DODGE</td>
<td>使用 <em>f</em> (f<sub>Rgb</sub>、B<sub>rgb</sub>) = 的基本 blend 公式 <img src="images/blend-mode-colordodge-1.png" alt="Mathematical formula for a color dodge effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_LINEAR_DODGE</td>
<td>使用 <em>f</em> (f<sub>Rgb</sub>、B<sub>rgb</sub>) = 的基本 blend 公式 <img src="images/blend-mode-lineardodge-1.png" alt="Mathematical formula for a linear dodge effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_LIGHTER_COLOR</td>
<td>僅適用于 Alpha 的基本 blend 公式。 <img src="images/blend-mode-lightercolor-1.png" alt="Mathematical formula for a lighter color effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_OVERLAY</td>
<td>使用 <em>f</em> (f<sub>Rgb</sub>、B<sub>rgb</sub>) = 的基本 blend 公式 <img src="images/blend-mode-overlay-1.png" alt="Mathematical formula for an overlay effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_SOFT_LIGHT</td>
<td>使用 <em>f</em> (f<sub>Rgb</sub>、B<sub>rgb</sub>) = 的基本 blend 公式 <img src="images/blend-mode-softlight-1.png" alt="Mathematical formula for a soft light effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_HARD_LIGHT</td>
<td>使用 <em>f</em> (f<sub>Rgb</sub>、B<sub>rgb</sub>) = 的基本 blend 公式 <img src="images/blend-mode-hardlight-1.png" alt="Mathematical formula for a hard light effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_VIVID_LIGHT</td>
<td>使用 <em>f</em> (f<sub>Rgb</sub>、B<sub>rgb</sub>) = 的基本 blend 公式 <img src="images/blend-mode-vividlight-1.png" alt="Mathematical formula for a vivid light effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_LINEAR_LIGHT</td>
<td>使用 <em>f</em> (f<sub>Rgb</sub>、B<sub>rgb</sub>) = 的基本 blend 公式 <img src="images/blend-mode-linearlight-1.png" alt="Mathematical formula for a linear light effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_PIN_LIGHT</td>
<td>使用 <em>f</em> (f<sub>Rgb</sub>、B<sub>rgb</sub>) = 的基本 blend 公式 <img src="images/blend-mode-pinlight-1.png" alt="Mathematical formula for a pin light effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_HARD_MIX</td>
<td>使用 <em>f</em> (f<sub>Rgb</sub>、B<sub>rgb</sub>) = 的基本 blend 公式 <img src="images/blend-mode-hardmix-1.png" alt="Mathematical formula for a hard mix effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_DIFFERENCE</td>
<td>使用 <em>f</em> 的基本 blend 公式 (f<sub>Rgb</sub>、B<sub>RGB</sub>) = abs (f<sub>rgb</sub> - B<sub>rgb</sub>) </td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_EXCLUSION</td>
<td>使用<em>f</em> (f<sub>Rgb</sub>、B<sub>rgb</sub>) = F<sub>rgb</sub> + b<sub>rgb</sub> 2 * f<sub>rgb</sub> * b<sub>rgb</sub>的基本 blend 公式</td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_HUE</td>
<td>僅適用于 Alpha 的基本 blend 公式。 <img src="images/blend-mode-hue-1.png" alt="Mathematical formula for a hue blend effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_SATURATION</td>
<td>僅適用于 Alpha 的基本 blend 公式。 <img src="images/blend-mode-saturation-1.png" alt="Mathematical formula for a sturation blend effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_COLOR</td>
<td>僅適用于 Alpha 的基本 blend 公式。 <img src="images/blend-mode-color-1.png" alt="Mathematical formula for a color blend effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_LUMINOSITY</td>
<td>僅適用于 Alpha 的基本 blend 公式。 <img src="images/blend-mode-luminosity-1.png" alt="Mathematical formula for a luminosity blend effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_DISSOLVE</td>
<td>假設︰
<ul>
<li>目前圖元的場景座標 XY</li>
<li>具決定性的虛擬亂數產生器 rand (XY) 以種子座標 XY 為基礎，具有 [0，1] 值的非偏誤分佈</li>
</ul>
<br/> <img src="images/blend-mode-dissolve-1.png" alt="Mathematical formula for a dissolve blend effect." /><br/></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_SUBTRACT</td>
<td>僅適用于 Alpha 的基本 blend 公式。 <img src="images/blend-mode-subtract-1.png" alt="Mathematical formula for a subtract blend effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_DIVISION</td>
<td>僅適用于 Alpha 的基本 blend 公式。 <img src="images/blend-mode-division-1.png" alt="Mathematical formula for a division blend effect." /></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> 針對所有 Blend 模式，輸出值會預乘並壓制至範圍 \[ 0，1 \] 。

 

## <a name="hsl-color-space-conversions"></a>HSL 色彩空間轉換

亮度元件是使用 RGB 加權來計算：

-   *k*<sub>R</sub> = 0.30
-   *k*<sub>G</sub> = 0.59
-   *k*<sub>B</sub> = 0.11

### <a name="converting-from-rgb-to-hsl"></a>從 RGB 轉換成 HSL

![描述從 rgb 色彩轉換成 hsl 色彩的數學公式。](images/blend-rgb-to-hsl-1.png)

這會將 *S* 和 *L* 置於範圍 \[ \] -1.0，5.0 的0.0、1.0 和 *H* 範圍中 \[ \] 。

### <a name="converting-from-hsl-to-rgb"></a>從 HSL 轉換成 RGB

若要轉換成另一種方式，我們使用先前計算的反向。

If *S* = 0 then *R*  =  *G*  =  *B*  =  *L*

否則會有六個與色調相關的案例：

如果 *H* 大於0，則值位於紅色/洋紅磁區中， *R*  >  *B*  >  *G*。

![數學 equaiton 將 hsl 色彩轉換成 rgb 的六個步驟之一。](images/blend-hsl-to-rgb-1rm.png)

如果 *H* 大於或等於0且小於1，則這些值會在 *R*  >  *G*  >  *B* 的紅色/黃色磁區中。

![數學 equaiton 將 hsl 色彩轉換成 rgb 的六個步驟。](images/blend-hsl-to-rgb-1ry.png)

如果 *H* 大於或等於1且小於2，這些值會在黃色/綠色磁區中， *G*  >  *R*  >  *B*。

![數學 equaiton 將 hsl 色彩轉換成 rgb 的六個步驟三。](images/blend-hsl-to-rgb-1yg.png)

如果 *H* 大於或等於2且小於3，則值會在 *G*  >  *B*  >  *R* 的綠色/青色磁區中。

![數學 equaiton 將 hsl 色彩轉換成 rgb 的六個步驟四。](images/blend-hsl-to-rgb-1gc.png)

如果 *H* 大於或等於3且小於4，則值會在青色/藍色磁區中，其中 *B*  >  *G*  >  *R*。

![數學 equaiton 將 hsl 色彩轉換為 rgb 的五個步驟五。](images/blend-hsl-to-rgb-1cb.png)

如果 *H* 大於或等於4，則值會在藍色/洋紅磁區中（ *B*  >  *R*  >  *G*）。

![數學 equaiton 將 hsl 色彩轉換為 rgb 的步驟六。](images/blend-hsl-to-rgb-1bm.png)

由於混合模式會從兩個不同的色彩建立任意的 HSL 元件組合，因此轉換的 RGB 值通常不會超出範圍，也就是一或多個通道元件可能超出 \[ 0.0、1.0 的法律範圍 \] 。 這些色彩會透過降低飽和度的最小程度來帶回範圍，同時保留色調和亮度：

![數學公式，描述超出範圍實例所需的更正。](images/blend-gamut-correction.png)

## <a name="output-bitmap"></a>輸出點陣圖

這個效果的輸出點陣圖一律是兩個輸入影像的聯集大小。

## <a name="sample-code"></a>範例程式碼

如需此效果的範例，請下載 [Direct2D 複合效果模式範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端 | 適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\] |
| 最低支援的伺服器 | 適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\] |
| 標頭                   | d2d1effects。h                                                                      |
| 程式庫                  | d2d1 .lib，dxguid .lib                                                               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

