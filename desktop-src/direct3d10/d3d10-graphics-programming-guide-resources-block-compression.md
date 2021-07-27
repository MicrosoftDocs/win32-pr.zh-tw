---
description: 區塊壓縮是一種用於降低紋理大小的紋理壓縮技術。
ms.assetid: add98d8f-6846-4dd6-b0e2-a4b6e89cbcc5
title: " (Direct3D 10) 封鎖壓縮"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c3a74fba0b4c7c2adade210a9a54952b5d1269
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436544"
---
# <a name="block-compression-direct3d-10"></a> (Direct3D 10) 封鎖壓縮

區塊壓縮是一種用於降低紋理大小的紋理壓縮技術。 與每個色彩 32 位元的材質相比，區塊壓縮的紋理可省下高達 75% 的空間。 當使用區塊壓縮時，應用程式的效能通常會增加，這是因為磁碟使用量較少。

雖然區塊壓縮會造成失真，但在經過管線轉換並篩選的所有紋理上運作良好，而且建議在這些紋理上使用。 直接對應至螢幕的紋理 (例如圖示和文字等 UI 元素) 不是進行壓縮的好選擇，因為成品會更為醒目。

建立經區塊壓縮的紋理時，所有維度都必須是 4 的倍數，且無法用作管線的輸出。

-   [Block 壓縮的運作方式為何？](#how-does-block-compression-work)
    -   [儲存未壓縮的資料](#storing-uncompressed-data)
    -   [儲存壓縮的資料](#storing-compressed-data)
-   [使用區塊壓縮](#using-block-compression)
    -   [虛擬大小與實體大小](#virtual-size-versus-physical-size)
-   [壓縮演算法](#compression-algorithms)
    -   [BC1](#bc1)
    -   [BC2](#bc2)
    -   [BC3](#bc3)
    -   [BC4](#bc4)
    -   [BC5](#bc5)
-   [使用 Direct3D 10.1 的格式轉換](#format-conversion-using-direct3d-101)
-   [相關主題](#related-topics)

## <a name="how-does-block-compression-work"></a>Block 壓縮的運作方式為何？

區塊壓縮是一種用以減少儲存色彩資料所需記憶體的技術。 藉由將某些色彩儲存為其原始大小，並在其他色彩上使用編碼配置，您可以大幅減少儲存圖片所需的記憶體。 因為硬體會自動解碼壓縮過的資料，所以就不會有使用壓縮紋理而造成效能降低的情形。

若要查看壓縮的運作方式，請查看下列兩個範例。 第一個範例描述儲存未壓縮的資料時使用的記憶體量；第二個範例描述儲存壓縮資料時使用的記憶體量。

### <a name="storing-uncompressed-data"></a>儲存未壓縮的資料

下圖為一個未壓縮的 4 × 4 紋理。 假設每個色彩都包含單一色彩元件 (例如紅色)，並儲存在記憶體的一個位元組內。

![未壓縮的4x4 材質圖例](images/d3d10-block-compress-1.png)

未壓縮的資料會在記憶體中循序配置，且需要 16 位元組的記憶體，如下所示。

![連續記憶體中未壓縮資料的圖例](images/d3d10-block-compress-2.png)

### <a name="storing-compressed-data"></a>儲存壓縮的資料

既然您已經看過未壓縮圖片會使用多少記憶體，現在就來看看壓縮圖片會節省多少記憶體。 [BC4](#bc4)壓縮格式會儲存2個色彩 (1 個位元組的每個) 和 16 3 位索引 (48 位，或6個位元組) 用來在材質中插入原始色彩，如下圖所示。

![bc4 壓縮格式的圖例](images/d3d10-block-compress-3.png)

儲存壓縮資料所需的總空間為 8 位元組，和未壓縮的範例相比省下 50% 的記憶體空間。 使用多個色彩元件時，會省下更大的空間。

區塊壓縮省下的大量記憶體，可促使效能增加。 此效能增長是降低圖片品質而得 (基於色彩內插補點)。不過，品質的下降通常不明顯。

下一節會說明 Direct3D 10 如何讓您輕鬆地在應用程式中使用區塊壓縮。

## <a name="using-block-compression"></a>使用區塊壓縮

建立區塊壓縮紋理，就像未壓縮的材質一樣 (請參閱 [從檔案建立材質](d3d10-graphics-programming-guide-resources-creating-textures.md)) 但您指定了區塊壓縮格式。


```
loadInfo.Format = DXGI_FORMAT_BC1_UNORM;
D3DX10CreateTextureFromFile(...);
```



接著，建立將材質系結至管線的 view。 由於區塊壓縮的材質只能用來做為著色器階段的輸入，因此您想要藉由呼叫 [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview)來建立著色器資源檢視。

依您使用未壓縮紋理的相同方式來使用區塊壓縮紋理。 如果您的應用程式會取得記憶體指標來顯示區塊壓縮資料，你需要處理造成宣告大小和實際大小不同的 Mipmap 內記憶體填補。

### <a name="virtual-size-versus-physical-size"></a>虛擬大小與實體大小

如果您應用程式中的程式碼，使用記憶體指標來引導區塊壓縮紋理記憶體的話，有一個重要考量要注意，這可能會需要修改您應用程式中的程式碼。 區塊壓縮紋理必須在所有維度中都是 4 的倍數，因為區塊壓縮演算法是在 4x4 的材質區塊上執行。 這對原始維度能被 4 整除，但分出的子層級卻不能的 Mipmap 會出現問題。 下列圖表顯示每個 Mipmap 層級的虛擬 (宣告) 大小和實體 (實際) 大小差異。

![未壓縮和壓縮的 mipmap 層級圖表](images/d3d10-block-compress-pad.png)

圖表左側顯示專為未壓縮 60 × 40 紋理而產生的 Mipmap 層級大小。 最上層大小是從產生該紋理的 API 呼叫而來；每個後續層級的大小為先前層級的一半。 對未壓縮紋理而言，虛擬 (宣告) 大小和實體 (實際) 大小之間並無不同。

圖表右側顯示專為使用壓縮之相同 60 × 40 紋理而產生的 Mipmap 層級大小。 請注意第二個和第三個層級都有記憶體填補，讓每個層級的大小都為 4 的因數。 這是必要的，好讓演算法可以在 4×4 材質區塊上執行。 如果您考慮讓 Mipmap 層級小於 4×4，這會特別明顯。在配置紋理記憶體時，這些非常小的 Mipmap 層級大小將會進位成最接近之 4 的因數。

取樣硬體使用虛擬大小。在取樣紋理時，會忽略記憶體填補。 對小於 4x4 的 Mipmap 層級，僅前四個材質會用於 2×2 貼圖，且只有第一個材質會由一個 1×1 區塊使用。 不過，沒有 API 結構會公開實體大小 (包括記憶體填補)。

總結來說，複製包含區塊壓縮資料的區域時，請注意使用對齊的記憶體區塊。 若要在可取得記憶體指標的應用程式中執行此動作，請確定指標使用表面字幅來處理實體記憶體大小。

## <a name="compression-algorithms"></a>壓縮演算法

在 Direct3D 內的區塊壓縮技術，會將未壓縮紋理資料切割為 4×4 的區塊、壓縮每個區塊，並儲存該資料。 基於這個原因，需要壓縮之材質的紋理維度必須要為 4 的倍數。

![區塊壓縮的圖表](images/d3d10-compression-1.png)

上述圖表顯示出一個分割成材質區塊的紋理。 第一個區塊會顯示標記為 a 至 p 的 16 種材質配置，但每個區塊都具有相同的資料組織。

Direct3D 實作多種壓縮配置，其個別實作以下三種不同折衷之處的其中一項：元件的儲存數、每個元件的位元，以及使用的記憶體數量。 使用此表格，以協助您選擇最適合所用資料類型的格式，以及最符合您應用程式的資料解析度。



| 來源資料                     | 資料壓縮解析度 (依位元計算) | 選擇此壓縮格式 |
|---------------------------------|---------------------------------------|--------------------------------|
| 三元件色彩和 Alpha | 色彩 (5:6:5)、Alpha (1) 或沒有 Alpha  | BC1                            |
| 三元件色彩和 Alpha | 色彩 (5:6:5)、Alpha (4)              | [BC2](#bc2)                    |
| 三元件色彩和 Alpha | 色彩 (5:6:5)、Alpha (8)              | [BC3](#bc3)                    |
| 單元件色彩             | 單元件 (8)                     | [BC4](#bc4)                    |
| 雙元件色彩             | 雙元件 (8:8)                  | [BC5](#bc5)                    |



 

### <a name="bc1"></a>BC1

您可以使用第一個區塊壓縮格式 (BC1)  (DXGI 格式 BC1 無型別 \_ \_ \_ 、dxgi \_ FORMAT \_ BC1 \_ UNORM 或 dxgi \_ BC1 \_ UNORM \_ SRGB) 使用5:6:5 色 (5 位紅色、6位綠色、5位藍色) 來儲存三個元件的色彩資料。 即使您的資料也包含 1 位元 Alpha 也是如此。 假設 4×4 紋理使用所能使用的最大資料格式，BC1 格式會將所需的記憶體從 48 位元組 (16 色 × 3 元件/色彩 × 1 位元組/元件) 降低至 8 位元組的記憶體。

此演算法適用於 4×4 材質區塊上。 演算法不會儲存16個色彩，而是會將2個參考色彩儲存 (色 \_ 0 和色彩 \_ 1) 和 16 2 位色彩索引 (區塊 a – p) ，如下圖所示。

![bc1 壓縮的版面配置圖表](images/d3d10-compression-bc1.png)

色彩索引 (a 至 p) 是用來從色彩表查看原始的色彩。 色彩表包含 4 個色彩。 前兩個色彩（色彩 \_ 0 和色彩 \_ 1）是最小和最大的色彩。 其他兩種色彩（色彩 \_ 2 和色彩 \_ 3）是以線性插補計算的中間色彩。


```
color_2 = 2/3*color_0 + 1/3*color_1
color_3 = 1/3*color_0 + 2/3*color_1
```



四個色彩都被指派了 2 位元索引值，這些值將會儲存在 a 至 p 區塊。


```
color_0 = 00
color_1 = 01
color_2 = 10
color_3 = 11
```



最後，每個 a 至 p 區塊中的色彩會與四種在色彩表內的色彩對比，而最接近色彩的索引會儲存在 2 位元區塊中。

此演算法也適用於包含 1 位元 Alpha 的資料。 唯一的差別在於色彩 \_ 3 會設定為 0 (代表透明色彩) 而色彩 \_ 2 則是色彩 \_ 0 和色彩1的線性 blend \_ 。


```
color_2 = 1/2*color_0 + 1/2*color_1;
color_3 = 0;
```





<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Direct3D 9 與 Direct3D 10 之間的差異：<br/> 這種格式同時存在於 Direct3D 9 和10。<br/>
<ul>
<li>在 Direct3D 9 中，BC1 格式稱為 D3DFMT_DXT1。</li>
<li>在 Direct3D 10 中，BC1 格式是以 DXGI_FORMAT_BC1_UNORM 或 DXGI_FORMAT_BC1_UNORM_SRGB 表示。</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc2"></a>BC2

使用 BC2 格式 (DXGI 格式 BC2 無型別 \_ \_ \_ 、dxgi \_ FORMAT \_ BC2 \_ UNORM 或 dxgi \_ BC2 \_ UNORM \_ SRGB) 儲存包含色彩和 Alpha 資料（具有低一致性）的資料 (使用 [BC3](#bc3) 來進行高度一致的 Alpha 資料) 。 BC2 格式將 RGB 資料儲存為 5:6:5 色彩 (5 位元紅色、6 位元綠色、5 位元藍色)，並將 Alpha 儲存為不同的 4 位元值。 假設 4×4 紋理使用所能使用的最大資料格式，此壓縮技術會將所需的記憶體從 64 位元組 (16 色 × 4 元件/色彩 × 1 位元組/元件) 降低至 16 位元組的記憶體。

BC2 格式儲存的色彩與 [BC1](#bc1) 格式的位元數量和資料配置相同。不過，BC2 需要額外 64 位元的記憶體來儲存 Alpha 資料，如下圖所示。

![bc2 壓縮的版面配置圖表](images/d3d10-compression-bc2.png)

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Direct3D 9 與 Direct3D 10 之間的差異：<br/> 這種格式同時存在於 Direct3D 9 和10。<br/>
<ul>
<li>在 Direct3D 9 中，BC2 格式稱為 D3DFMT_DXT2 和 D3DFMT_DXT3。</li>
<li>在 Direct3D 10 中，BC2 格式是以 DXGI_FORMAT_BC2_UNORM 或 DXGI_FORMAT_BC2_UNORM_SRGB 表示。</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc3"></a>BC3

您可以使用 BC3 格式 (DXGI \_ 格式 BC3 無別別 \_ \_ 、dxgi \_ FORMAT \_ BC3 \_ UNORM 或 dxgi \_ BC3 \_ UNORM \_ SRGB) 來儲存高度一致的色彩資料 (使用的 [BC2](#bc2) 與較不一致的 Alpha 資料) 。 BC3 格式使用 5:6:5 色彩 (5 位元紅色、6 位元綠色、5 位元藍色) 儲存色彩資料，並使用 1 個位元組儲存 Alpha 資料。 假設 4×4 紋理使用所能使用的最大資料格式，此壓縮技術會將所需的記憶體從 64 位元組 (16 色 × 4 元件/色彩 × 1 位元組/元件) 降低至 16 位元組的記憶體。

BC3 格式儲存的色彩與 [BC1](#bc1) 格式的位元數量和資料配置相同。不過，BC3 需要額外 64 位元的記憶體來儲存 Alpha 資料。 BC3 格式藉由儲存兩個參考值並在它們之間內插補點來處理 Alpha (和 BC1 儲存 RGB 色彩的方式相同)。

此演算法適用於 4×4 材質區塊上。 演算法不會儲存16個 Alpha 值，而是會儲存2個參考 Alpha (Alpha \_ 0 和 Alpha \_ 1) 和 16 3 位色彩索引 (Alpha a 到 p) ，如下圖所示。

![bc3 壓縮的版面配置圖表](images/d3d10-compression-bc3.png)

BC3 格式使用 Alpha 索引 (a 至 p)，從包含 8 個值的查閱資料表查詢原始的色彩。 前兩個值（Alpha \_ 0 和 Alpha \_ 1）是最小值和最大值，其他六個中間值則是使用線性插補來計算。

此演算法藉由檢查兩個 Alpha 參考值來判斷插入的 Alpha 值數目。 如果 Alpha \_ 0 大於 Alpha \_ 1，則 BC3 會將6個 Alpha 值插補，否則會插入4。 當 BC3 僅插入 4 個 Alpha 值時，它就會設定兩個額外 Alpha 值 (0 為完全透明，而 255 為完全不透明)。 BC3 藉由儲存對應插補 Alpha 值的位元程式碼，以壓縮 4×4 材質區域中的 Alpha 值，插補進的 Alpha 值最符合特定材質的原始 Alpha。


```
if( alpha_0 > alpha_1 )
{
  // 6 interpolated alpha values.
  alpha_2 = 6/7*alpha_0 + 1/7*alpha_1; // bit code 010
  alpha_3 = 5/7*alpha_0 + 2/7*alpha_1; // bit code 011
  alpha_4 = 4/7*alpha_0 + 3/7*alpha_1; // bit code 100
  alpha_5 = 3/7*alpha_0 + 4/7*alpha_1; // bit code 101
  alpha_6 = 2/7*alpha_0 + 5/7*alpha_1; // bit code 110
  alpha_7 = 1/7*alpha_0 + 6/7*alpha_1; // bit code 111
}
else
{
  // 4 interpolated alpha values.
  alpha_2 = 4/5*alpha_0 + 1/5*alpha_1; // bit code 010
  alpha_3 = 3/5*alpha_0 + 2/5*alpha_1; // bit code 011
  alpha_4 = 2/5*alpha_0 + 3/5*alpha_1; // bit code 100
  alpha_5 = 1/5*alpha_0 + 4/5*alpha_1; // bit code 101
  alpha_6 = 0;                         // bit code 110
  alpha_7 = 255;                       // bit code 111
}
```





<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Direct3D 9 與 Direct3D 10 之間的差異：<br/>
<ul>
<li>在 Direct3D 9 中，BC3 格式稱為 D3DFMT_DXT4 和 D3DFMT_DXT5。</li>
<li>在 Direct3D 10 中，BC3 格式是以 DXGI_FORMAT_BC3_UNORM 或 DXGI_FORMAT_BC3_UNORM_SRGB 表示。</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc4"></a>BC4

使用 BC4 格式儲存每個色彩都使用 8 位元的單一元件色彩資料。 相較于 [BC1](#bc1)) ，精確度 (的結果，BC4 適合用 dxgi 格式 BC4 UNORM 格式，將浮點數資料儲存在 \[ 0 到1的範圍內， \] \_ \_ \_ 而 \[ \] 使用 dxgi \_ 格式 \_ BC4 \_ SNORM 格式的-1 到 + 1。 假設 4×4 紋理使用所能使用的最大資料格式，此壓縮技術會將所需的記憶體從 16 位元組 (16 色 × 1 元件/色彩 × 1 位元組/元件) 降低至 8 位元組。

此演算法適用於 4×4 材質區塊上。 演算法不會儲存16種色彩，而是會儲存2個參考色彩 (紅色 \_ 0 和紅色 \_ 1) 和 16 3 位色彩索引 (紅色 a 到紅色 p) ，如下圖所示。

![bc4 壓縮的版面配置圖表](images/d3d10-compression-bc4.png)

此演算法使用 3 位元索引，從一個包含 8 種顏色的顏色表內查詢顏色。 前兩個色彩（紅色 \_ 0 和紅色 \_ 1）是最小和最大的色彩。 此演算法使用線性插補來計算出剩餘的色彩。

此演算法藉由檢查兩個參考值來判斷插入的色彩值數目。 如果紅色 \_ 0 大於紅色 \_ 1，則 BC4 會將6個色彩值插補，否則會插入4。 當 BC4 僅插入 4 個色彩值時，它會設定兩個額外的色彩值 (0.0f 為完全透明，而 1.0f 為完全不透明)。 BC4 藉由儲存對應插補 Alpha 值的位元程式碼，以壓縮 4×4 材質區域中的 Alpha 值，插補進的 Alpha 值最符合特定材質的原始 Alpha。

-   [BC4 \_ UNORM](/windows)
-   [BC4 \_ SNORM](/windows)

### <a name="bc4_unorm"></a>BC4 \_ UNORM

單一元件資料的內插補點方式如下列程式碼範例所示。


```
unsigned word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = 0.0f;                     // bit code 110
  red_7 = 1.0f;                     // bit code 111
}
```



參考色彩會被指派 3 位元索引 (因為有 8 個值，所以是 000-111)，此索引會於壓縮期間儲存在紅色 a 到紅色 p 區塊內。

### <a name="bc4_snorm"></a>BC4 \_ SNORM

DXGI \_ 格式 \_ BC4 \_ SNORM 完全相同，不同之處在于資料是以 SNORM 範圍編碼，以及在插入4個色彩值時。 單一元件資料的內插補點方式如下列程式碼範例所示。


```
signed word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = -1.0f;                     // bit code 110
  red_7 =  1.0f;                     // bit code 111
}
```



參考色彩會被指派 3 位元索引 (因為有 8 個值，所以是 000-111)，此索引會於壓縮期間儲存在紅色 a 到紅色 p 區塊內。

### <a name="bc5"></a>BC5

以 BC5 格式儲存每個色彩都使用 8 位元的雙元件色彩資料。 相較于 [BC1](#bc1)) ，精確度 (的結果，BC5 適合用 dxgi 格式 BC5 UNORM 格式，將浮點數資料儲存在 \[ 0 到1的範圍內， \] \_ \_ \_ 而 \[ \] 使用 dxgi \_ 格式 \_ BC5 \_ SNORM 格式的-1 到 + 1。 假設 4×4 紋理使用所能使用的最大資料格式，此壓縮技術會將所需的記憶體從 32 位元組 (16 色 × 2 元件/色彩 × 1 位元組/元件) 降低至 16 位元組。

此演算法適用於 4×4 材質區塊上。 演算法不會針對這兩個元件儲存16個色彩，而是會為每個元件儲存2個參考色彩 (紅色 \_ 0、紅色 \_ 1、綠色 \_ 0 和綠色 \_ 1) 和每個元件的 16 3 位色彩索引， (紅色 a 到紅色 p，綠色 a 到綠色 p) ，如下圖所示。

![bc5 壓縮的版面配置圖表](images/d3d10-compression-bc5.png)

此演算法使用 3 位元索引，從一個包含 8 種顏色的顏色表內查詢顏色。 前兩個色彩（紅色 \_ 0 和紅色 \_ 1 (或綠色 \_ 0 和綠色 \_ 1) ）是最小和最大的色彩。 此演算法使用線性插補來計算出剩餘的色彩。

此演算法藉由檢查兩個參考值來判斷插入的色彩值數目。 如果紅色 \_ 0 大於紅色 \_ 1，則 BC5 會將6個色彩值插補，否則會插入4。 當 BC5 僅插入 4 個色彩值時，它會將剩下的兩個色彩值設定為 0.0f 和 1.0f。

-   [BC5 \_ UNORM](/windows)
-   [BC5 \_ SNORM](/windows)

### <a name="bc5_unorm"></a>BC5 \_ UNORM

單一元件資料的內插補點方式如下列程式碼範例所示。 綠色元件的計算方法都很相似。


```
unsigned word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = 0.0f;                     // bit code 110
  red_7 = 1.0f;                     // bit code 111
}
```



參考色彩會被指派 3 位元索引 (因為有 8 個值，所以是 000-111)，此索引會於壓縮期間儲存在紅色 a 到紅色 p 區塊內。

### <a name="bc5_snorm"></a>BC5 \_ SNORM

DXGI \_ 格式 \_ BC5 \_ SNORM 完全相同，不同之處在于資料是以 SNORM 範圍編碼，而且當插入4個數據值時，另外兩個值為-1.0 f 和 1.0 f。 單一元件資料的內插補點方式如下列程式碼範例所示。 綠色元件的計算方法都很相似。


```
signed word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = -1.0f;                    // bit code 110
  red_7 =  1.0f;                    // bit code 111
}
```



參考色彩會被指派 3 位元索引 (因為有 8 個值，所以是 000-111)，此索引會於壓縮期間儲存在紅色 a 到紅色 p 區塊內。

## <a name="format-conversion-using-direct3d-101"></a>使用 Direct3D 10.1 的格式轉換

Direct3D 10.1 可讓 prestructured 型別紋理與相同位寬度的區塊壓縮紋理之間進行複製。 可以完成此工作的函式為 [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) 和 [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)。

從 Direct3D 10.1 開始，您可以使用 [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) 和 [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) ，在幾種格式類型之間複製。 此類型的複製作業會執行一種格式轉換，將資源資料重新解譯為不同的格式類型。 請將此範例納入考慮，它用更典型的轉換行為方式來顯示重新解譯資料之間的不同︰


```
    FLOAT32 f = 1.0f;
    UINT32 u;
```



若要將 ' f ' 重新解譯為 ' u ' 的類型，請使用 [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy)：


```
    memcpy( &u, &f, sizeof( f ) ); // ‘u’ becomes equal to 0x3F800000.
```



在上述重新解譯中，資料的基礎值不會變更。[memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy) 會將浮點數重新解譯為不帶正負號的整數。

若要執行更常見的轉換類型，請使用下列設定︰


```
    u = f; // ‘u’ becomes 1.
```



在上述轉換中，資料的基礎值有所變更。

下表列出允許的來源和目的地格式，您可以在此格式轉換的重新解譯類型內使用。 您必須正確地為值進行編碼，才能讓重新解譯正常運作。



| 位元寬度 | 未壓縮資源                                                                                                                                               | 區塊壓縮資源                                                                                                                                           |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 32        | DXGI \_ 格式 \_ R32 \_ UINT<br/> DXGI \_ 格式 \_ R32 \_ 聖<br/>                                                                                               | DXGI \_ 格式 \_ R9G9B9E5 \_ SHAREDEXP                                                                                                                                   |
| 64        | DXGI \_ 格式 \_ R16G16B16A16 \_ UINT<br/> DXGI \_ 格式 \_ R16G16B16A16 \_ 聖<br/> DXGI \_ 格式 \_ R32G32 \_ UINT<br/> DXGI \_ 格式 \_ R32G32 \_ 聖<br/> | DXGI \_ 格式 \_ BC1 \_ UNORM \[ \_ SRGB\]<br/> DXGI \_ 格式 \_ BC4 \_ UNORM<br/> DXGI \_ 格式 \_ BC4 \_ SNORM<br/>                                               |
| 128       | DXGI \_ 格式 \_ R32G32B32A32 \_ UINT<br/> DXGI \_ 格式 \_ R32G32B32A32 \_ 聖<br/>                                                                             | DXGI \_ 格式 \_ BC2 \_ UNORM \[ \_ SRGB\]<br/> DXGI \_ 格式 \_ BC3 \_ UNORM \[ \_ SRGB\]<br/> DXGI \_ 格式 \_ BC5 \_ UNORM<br/> DXGI \_ 格式 \_ BC5 \_ SNORM<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (Direct3D 10) 的資源 ](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
