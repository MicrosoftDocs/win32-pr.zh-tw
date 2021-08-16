---
title: Turbulence 效果
description: 您可以使用 turbulence 效果，根據 Perlin 雜訊函式來產生點陣圖。
ms.assetid: 86C1990E-958C-46D7-840A-E4A17F1D1740
keywords:
- turbulence 效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c4eb8f57f98c8e69591b7772d710d6deb7a78c801f3ca027175c55460c2d529
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824486"
---
# <a name="turbulence-effect"></a>Turbulence 效果

您可以使用 turbulence 效果，根據 Perlin 雜訊函式來產生點陣圖。

Turbulence 效果沒有輸入影像。

這項效果的 CLSID 是 CLSID \_ D2D1Turbulence。

-   [範例影像](#example-image)
-   [效果屬性](#effect-properties)
-   [雜訊模式](#noise-modes)
-   [輸出點陣圖](#output-bitmap)
-   [需求](#requirements)
-   [相關主題](#related-topics)

## <a name="example-image"></a>範例影像

![顯示 turbulence 效果輸出的效果範例螢幕擷取畫面。](images/32-turbulence.png)

Turbulence 效果會計算一或多個 Perlin 雜訊函數 octaves 的總和。 Perlin 雜訊是虛擬隨機函數，其值取決於頻率、位置和種子值。 效果會使用其中一個方程式來產生 RGBA 值。

如果您選取 D2D1 \_ TURBULENCE \_ 雜訊碎形 \_ 加 \_ 總雜訊模式，效果會使用這個方程式。

![顯示用來產生點陣圖之 turbulence 函數的螢幕擷取畫面。](images/turbulence-equation1.png)

如果您選取 D2D1 \_ TURBULENCE \_ 雜訊 \_ TURBULENCE 雜訊模式，效果就會使用此方程式。

![用來產生點陣圖的 turbulence 函數。](images/turbulence-equation2.png)

> [!Note]  
> `PerlinNoise`函數的範圍為 \[ -1、1 \] 。

 

此效果會輸出預乘 Alpha 的圖元值。

## <a name="effect-properties"></a>效果屬性



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>顯示名稱和索引列舉</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Offset<br/> D2D1_TURBULENCE_PROP_OFFSET<br/></td>
<td>產生 turbulence 輸出的座標。<br/> 用來產生 Perlin 雜訊的演算法與位置相依，因此不同的位移會導致不同的輸出。 這個屬性未系結，而且單位是在 Dip 中指定 <br/>
<blockquote>
[!Note]<br />
位移與轉譯沒有相同的效果，因為雜訊函式輸出是無限的，且函式會在磚周圍換行。
</blockquote>
<br/> 此類型為 D2D1_VECTOR_2F。<br/> 預設值為 {0.0 f，0.0 f}。<br/></td>
</tr>
<tr class="even">
<td>大小<br/> D2D1_TURBULENCE_PROP_SIZE<br/></td>
<td>Turbulence 輸出的大小。<br/> 這個屬性未系結，而且單位是在 Dip 中指定 <br/>
<br/> 此類型為 D2D1_VECTOR_2F。<br/> 預設值為 {0.0 f，0.0 f}。<br/></td>
</tr>
<tr class="odd">
<td>BaseFrequency<br/> D2D1_TURBULENCE_PROP_BASE_FREQUENCY<br/></td>
<td>X 和 Y 方向的基底頻率。 這個屬性是浮點數，而且必須大於0。 單位會以 1/下降來指定。 <br/> 針對基底頻率，1 (1/Dip) 的值會導致 Perlin 雜訊完成兩個圖元之間的整個迴圈。 這些圖元的簡化插補會產生完全隨機的圖元，因為圖元之間沒有相互關聯。<br/> 針對基底頻率，值為 0.1 (1/Dip) ，Perlin 雜訊函式每10次都會重複一次。 這會導致圖元之間的相互關聯，而且可以看見一般的 turbulence 效果。<br/> 此類型為 D2D1_VECTOR_2F。<br/> 預設值為 {0.01 f，0.01 f}。<br/></td>
</tr>
<tr class="even">
<td>NumOctaves<br/> D2D1_TURBULENCE_PROP_NUM_OCTAVES<br/></td>
<td>雜訊函數的 octaves 數目。 這個屬性是 UINT32，而且必須大於0。<br/> 此類型為 UINT32。<br/> 預設值為 1。<br/></td>
</tr>
<tr class="odd">
<td>Seed<br/> D2D1_TURBULENCE_PROP_SEED<br/></td>
<td>虛擬隨機產生器的種子。 這個屬性未系結。<br/> 此類型為 UINT32。<br/> 預設值為 0。<br/></td>
</tr>
<tr class="even">
<td>雜訊<br/> D2D1_TURBULENCE_PROP_NOISE<br/></td>
<td>Turbulence 雜訊模式。 這個屬性可以是 <em>碎形 sum</em> 或 <em>turbulence</em>。 指出是否要根據碎形雜訊或 Turbulence 函數來產生點陣圖。 如需詳細資訊，請參閱 <a href="#noise-modes">雜訊模式</a> 。 <br/> 此類型為 D2D1_TURBULENCE_NOISE。<br/> 預設值為 D2D1_TURBULENCE_NOISE_FRACTAL_SUM。<br/></td>
</tr>
<tr class="odd">
<td>Stitchable<br/> D2D1_TURBULENCE_PROP_STITCHABLE<br/></td>
<td>開啟或關閉裝訂。 基礎頻率會經過調整，以便拼接輸出點陣圖。 如果您想要並排顯示 turbulence 效果輸出的多個複本，這會很有用。
<ul>
<li>您可以使用圖格效果) 來將輸出點陣圖 (並排顯示，而不會顯示接縫的外觀。 基礎頻率會經過調整，以便拼接輸出點陣圖。</li>
<li>False：基底頻率未調整，所以如果點陣圖已並排顯示，則圖格之間可能會出現接縫。</li>
</ul>
<br/> 此類型為 BOOL。<br/> 預設值為 FALSE。<br/></td>
</tr>
</tbody>
</table>



 

## <a name="noise-modes"></a>雜訊模式



| 列舉型別                           | 描述                                                                           |
|---------------------------------------|---------------------------------------------------------------------------------------|
| D2D1 \_ TURBULENCE \_ 雜訊 \_ 碎形 \_ 總和 | 計算 octaves 的總和，將輸出範圍從 \[ -1，1 \] ，移至 \[ 0，1 \] 。 |
| D2D1 \_ TURBULENCE \_ 雜訊 \_ TURBULENCE   | 計算每個 octave 之絕對值的總和。                                  |



 

> [!Note]  
> 這兩種模式都不包含輸出值的明確夾具。

 

## <a name="output-bitmap"></a>輸出點陣圖

此效果會產生邏輯上無限大小的點陣圖。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端 | Windows 7 傳統型應用程式的 Windows 8 和平臺更新 \[ \| Windows 儲存應用程式\] |
| 最低支援的伺服器 | Windows 7 傳統型應用程式的 Windows 8 和平臺更新 \[ \| Windows 儲存應用程式\] |
| 標頭                   | d2d1effects。h                                                                      |
| 程式庫                  | d2d1 .lib，dxguid .lib                                                               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

