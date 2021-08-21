---
description: 材質格式 DXT1 適用于不透明或具有單一透明色彩的材質。
ms.assetid: a890ed0a-1f68-45b8-93cb-b621d1908d9f
title: " (Direct3D 9) 的不透明和1位 Alpha 紋理"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bda620810e48cba519322f3f2426555443fb696f524f4fbe7752a8c7aaedba73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728146"
---
# <a name="opaque-and-1-bit-alpha-textures-direct3d-9"></a> (Direct3D 9) 的不透明和1位 Alpha 紋理

材質格式 DXT1 適用于不透明或具有單一透明色彩的材質。

針對每個不透明或 1 位元 alpha 區塊，儲存兩個 16 位元值 (RGB 5:6:5 格式)，以及每像素 2 位元的 4x4 點陣圖。 這總計 16 紋素 64 位元，或每紋素四個位元。 在區塊點陣圖中，每紋素有 2 位元可在四個色彩之間選取，其中兩個會儲存在編碼資料中。 線性插補會將另外兩種色彩從這些儲存的色彩中衍生。 此配置顯示在下圖。

![點陣圖配置的圖表](images/colors1.png)

透過比較儲存在區塊中的兩個 16 位元色彩值可區別 1 位元的 alpha 格式和不透明格式。 它們會被視為不帶正負號的整數。 如果第一個色彩大於第二個，就表示只定義不透明的紋素。 這表示使用四個色彩代表紋素。 在四色編碼中，有兩種衍生的色彩，所有四個色彩平均散佈在 RGB 色彩空間。 這個格式類似 RGB 5:6:5 格式。 否則，對於 1 位元透明度，使用三個色彩，保留第四個來代表透明紋素。

在三色編碼中，有一個衍生的色彩，並保留第四個 2 位元程式碼指出透明紋素 (alpha 資訊)。 這個格式類似 RGBA 5:5:5:1，其中最後一位元用於編碼 alpha 遮罩。

下列程式碼示範的演算法用於決定是否選取三或四個色彩編碼︰


```
if (color_0 > color_1) 
{
    // Four-color block: derive the other two colors.    
    // 00 = color_0, 01 = color_1, 10 = color_2, 11 = color_3
    // These 2-bit codes correspond to the 2-bit fields 
    // stored in the 64-bit block.
    color_2 = (2 * color_0 + color_1 + 1) / 3;
    color_3 = (color_0 + 2 * color_1 + 1) / 3;
}    
else
{ 
    // Three-color block: derive the other color.
    // 00 = color_0,  01 = color_1,  10 = color_2,  
    // 11 = transparent.
    // These 2-bit codes correspond to the 2-bit fields 
    // stored in the 64-bit block. 
    color_2 = (color_0 + color_1) / 2;    
    color_3 = transparent;    

}
```



建議您在混合之前將透明度像素的 RGBA 元件設為零。

下表顯示 8 位元組區塊的記憶體配置。 它假設第一個索引對應 y 座標，第二個對應 x 座標。 例如，材質 \[ 1 \] \[ 2 \] 指的是 (x，y) = (2，1) 的材質地圖圖元。

此資料表包含8位元組 (64 位) 區塊的記憶體配置。



| 單字位址 | 16 位元單字    |
|--------------|----------------|
| 0            | 色彩 \_ 0       |
| 1            | 色彩 \_ 1       |
| 2            | 點陣圖字 \_ 0 |
| 3            | 點陣圖文字 \_ 1 |



 

色彩 \_ 0 和色彩 \_ 1 （兩個極端的色彩）如下所示：



| Bits        | Color                 |
|-------------|-----------------------|
| 4:0 (LSB \*)  | 藍色元件  |
| 10:5        | 綠色元件 |
| 15:11       | 紅色元件   |



 

\*最不重要的位

點陣圖字 \_ 0 的配置如下：



| Bits          | 紋素           |
|---------------|-----------------|
| 1:0 (LSB)     | 材質 \[ 0 \] \[ 0\] |
| 3:2           | 材質 \[ 0 \] \[ 1\] |
| 5:4           | 材質 \[ 0 \] \[ 2\] |
| 7:6           | 材質 \[ 0 \] \[ 3\] |
| 9:8           | 材質 \[ 1 \] \[ 0\] |
| 11:10         | 材質 \[ 1 \] \[ 1\] |
| 13:12         | 材質 \[ 1 \] \[ 2\] |
| 15:14 (MSB \*)  | 材質 \[ 1 \] \[ 3\] |



 

\*最重要的一點 (MSB) 

點陣圖 Word \_ 1 的配置如下：



| Bits        | 紋素           |
|-------------|-----------------|
| 1:0 (LSB)   | 材質 \[ 2 \] \[ 0\] |
| 3:2         | 材質 \[ 2 \] \[ 1\] |
| 5:4         | 材質 \[ 2 \] \[ 2\] |
| 7:6         | 材質 \[ 2 \] \[ 3\] |
| 9:8         | 材質 \[ 3 \] \[ 0\] |
| 11:10       | 材質 \[ 3 \] \[ 1\] |
| 13:12       | 材質 \[ 3 \] \[ 2\] |
| 15:14 (MSB) | 材質 \[ 3 \] \[ 3\] |



 

## <a name="example-of-opaque-color-encoding"></a>不透明色彩編碼的範例

以不透明編碼為例，假設色彩紅色和黑色位於極端。 紅色為色彩 \_ 0，黑色為色彩 \_ 1。 有四個以內插值取代的色彩之之間平均漸層分散。 若要判斷 4x4 點陣圖值，請使用下列的計算︰


```
00 ? color_0
01 ? color_1
10 ? 2/3 color_0 + 1/3 color_1
11 ? 1/3 color_0 + 2/3 color_1
```



然後點陣圖看起來如下列圖表。

![顯示展開點陣圖版面配置的圖表。](images/colors2.png)

這看起來像下列圖解系列色彩。

> [!Note]  
> 在影像中，圖元 (0，0) 出現在左上方。

 

![不透明編碼漸層圖例](images/redsquares.png)

## <a name="example-of-1-bit-alpha-encoding"></a>1位 Alpha 編碼範例

當不帶正負號的16位整數（色彩0） \_ 小於不帶正負號的16位整數（色彩1）時，就會選取此格式 \_ 。 可以使用此格式的範例是樹上樹葉，與藍天對映。 有些紋素可標示成透明，同時有三種綠色系列仍可供樹葉運用。 兩個色彩修正極端，而且第三個插補色彩。

以下是這類圖片的範例圖。

![1 位元 alpha 編碼的圖例](images/greenthing.png)

請注意，影像會顯示為白色，而材質會編碼為透明。 另請注意，在混合之前，透明材質的 RGBA 元件應該設定為零。

適用於色彩和透明度的點陣圖編碼，會使用下列的計算來判定。


```
00 ? color_0
01 ? color_1
10 ? 1/2 color_0 + 1/2 color_1
11   ?   Transparent
```



然後點陣圖看起來如下列圖表。

![展開的點陣圖配置的圖表](images/colors3.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[壓縮的材質資源](compressed-texture-resources.md)
</dt> </dl>

 

 



