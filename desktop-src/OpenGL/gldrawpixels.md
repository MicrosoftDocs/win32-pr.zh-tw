---
title: 'glDrawPixels 函式 (Gl) '
description: GlDrawPixels 函式會將圖元區塊寫入至畫面格緩衝區。
ms.assetid: c4eda64f-a75e-4e6d-984d-af49414b94d8
keywords:
- glDrawPixels 函式 OpenGL
topic_type:
- apiref
api_name:
- glDrawPixels
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e25adc8ad28791086020a37d3a30651e169bfd07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094148"
---
# <a name="gldrawpixels-function"></a>glDrawPixels 函式

**GlDrawPixels** 函式會將圖元區塊寫入至畫面格緩衝區。

## <a name="syntax"></a>語法


```C++
void WINAPI glDrawPixels(
         GLsizei width,
         GLsizei height,
         GLenum  format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*width* (寬度) 
</dt> <dd>

將寫入至畫面格緩衝區之圖元矩形的寬度維度。

</dd> <dt>

*height* (高度) 
</dt> <dd>

將寫入至畫面格緩衝區之圖元矩形的高度維度。

</dd> <dt>

*format* 
</dt> <dd>

圖元資料的格式。 可接受的符號常數如下所示。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>值</th>
<th>意義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <dt><strong>GL_COLOR_INDEX</strong></dt> </dl></td>
<td>每個圖元都是單一值，也就是色彩索引。 <br/>
<ol>
<li><strong>GlDrawPixels</strong>函式會將每個圖元轉換成固定點格式，而不會有二進位點右邊未指定的位數數目，而不論記憶體資料類型為何。 浮點值會轉換成真正的固定點值。 <strong>GlDrawPixels</strong>函式會將帶正負號和不帶正負號的整數資料轉換成設定為零的所有小數位。 函數會將點陣圖資料轉換為0.0 或1.0。</li>
<li><strong>GlDrawPixels</strong>函式會將 GL_INDEX_SHIFT 位左方的每個固定點索引移至 GL_INDEX_OFFSET，並將它加入至。 如果 GL_INDEX_SHIFT 為負數，則向右移位。 無論是哪一種情況，在結果中都不會以零位填滿指定的位位置。</li>
<li>在 RGBA 模式中， <strong>glDrawPixels</strong> 會使用 GL_PIXEL_MAP_I_TO_R、GL_PIXEL_MAP_I_TO_G、GL_PIXEL_MAP_I_TO_B 和 GL_PIXEL_MAP_I_TO_A 資料表，將產生的索引轉換成 RGBA 圖元。 當在色彩索引模式中，且 GL_MAP_COLOR 為 true 時，會將索引取代為查閱資料表中 <strong>glDrawPixels</strong> 參考的值 GL_PIXEL_MAP_I_TO_I。</li>
<li>如果索引的查閱取代是否已完成，索引的整數部分就是 <strong>和</strong>2<sup>b</sup> - 1 的 ed，其中 <em>b</em> 是色彩索引緩衝區中的位數。</li>
<li>接著，會將目前的點陣位置 <em>z</em>座標和材質座標附加至每個圖元，然後將 <em>x</em> 和 <em>y</em> 視窗座標指派給 <em>n</em>個片段（例如 <em>x</em>），以將產生的索引或 RGBA 色彩轉換成片段： = <em>x</em><sub>r</sub> + <em>n</em> mod <em>寬度</em><br/> <em>y</em>？ = <em>y</em><sub>r</sub> + <em>n/寬度</em><br/> 其中 (<em>x</em><sub>r</sub> ， <em>y</em><sub>r</sub> ) 是目前的點陣位置。<br/></li>
<li><strong>GlDrawPixels</strong>函式會將這些圖元片段視為與透過將點、線條或多邊形所產生的片段一樣。 它會先套用材質對應、霧化和所有片段作業，然後再將片段寫入至畫面格緩衝區。</li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_STENCIL_INDEX"></span><span id="gl_stencil_index"></span><dl> <dt><strong>GL_STENCIL_INDEX</strong></dt> </dl></td>
<td>每個圖元都是單一值，也就是樣板索引。 <br/>
<ol>
<li><strong>GlDrawPixels</strong>函式會將它轉換成固定點格式，而不指定二進位點右邊的位數（不論記憶體資料類型為何）。 浮點值會轉換成真正的固定點值。 <strong>GlDrawPixels</strong>函式會將帶正負號和不帶正負號的整數資料轉換成設定為零的所有小數位。 點陣圖資料會轉換為0.0 或1.0。</li>
<li><strong>GlDrawPixels</strong>函式會將每個固定點索引 GL_INDEX_SHIFT 位左移，並將其新增至 GL_INDEX_OFFSET。 如果 GL_INDEX_SHIFT 為負數，則向右移位。 無論是哪一種情況，在結果中都不會以零位填滿指定的位位置。</li>
<li>如果 GL_MAP_STENCIL 為 true，就會將索引取代為查閱資料表 GL_PIXEL_MAP_S_TO_S 中所參考的 <strong>glDrawPixels</strong> 值。</li>
<li>如果索引的查閱取代是否已完成，索引的整數部分就是， <strong>而</strong>ed 的整數部分則是 2<sup>b</sup> - 1，其中 <em>b</em> 是樣板緩衝區中的位數。 接著會將產生的樣板索引寫入至樣板緩衝區，以便將第 <em>n</em>個索引寫入至位置 <em>x</em>？ = <em>x</em><sub>r</sub> + <em>n</em> mod <em>寬度</em><br/> <em>y</em>？ = <em>y</em><sub>r</sub> + <em>n/寬度</em><br/> 其中 (<em>x</em><sub>r</sub> ， <em></em> y<sub>r</sub> ) 是目前的點陣位置。 只有圖元擁有權測試、剪下測試和樣板 writemask 會影響這些寫入。<br/></li>
</ol></td>
</tr>
<tr class="odd">
<td><span id="GL_DEPTH_COMPONENT"></span><span id="gl_depth_component"></span><dl> <dt><strong>GL_DEPTH_COMPONENT</strong></dt> </dl></td>
<td>每個圖元都是一個深度的元件。 <br/>
<ol>
<li><strong>GlDrawPixels</strong>函式會將浮點數據直接轉換成具有未指定精確度的內部浮點格式。 帶正負號的整數資料會以線性方式對應至內部浮點格式，讓最正面可表示的整數值對應至1.0，而最大的可表示值會對應至-1.0。 不帶正負號的整數資料的對應方式如下：最大整數值對應至1.0，而零對應至0.0。</li>
<li><strong>GlDrawPixels</strong>函式會 GL_DEPTH_SCALE 將產生的浮點數深度值相乘，並將其新增至 GL_DEPTH_BIAS。 結果會壓制至範圍 [0，1]。</li>
<li><strong>GlDrawPixels</strong>函式會將目前的點陣位置色彩或色彩索引和材質座標附加至每個圖元，然後將<em>x</em>和<em>y</em>視窗座標指派給<em>n</em>個片段（例如<em>x</em>），以將產生的深度元件轉換成片段： = <em></em>x<sub>r</sub> + <em>n</em> mod <em>寬度</em><br/> <em>y</em>？ = <em>y</em><sub>r</sub> + <em>n/寬度</em><br/> 其中 (<em></em> x<sub>r</sub> ，<em>y</em><sub>r</sub> ) 是目前的點陣位置。<br/></li>
<li>然後，這些圖元片段的處理方式就像是將點、線條或多邊形所產生的片段一樣。 <strong>GlDrawPixels</strong>函式會先套用材質對應、霧化和所有片段作業，然後再將片段寫入畫面格緩衝區。</li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <dt><strong>GL_RGBA</strong></dt> </dl></td>
<td>每個圖元都是四個元件的群組，順序如下：紅色、綠色、藍色、Alpha。 <br/>
<ol>
<li><strong>GlDrawPixels</strong>函式會將浮點值直接轉換成具有未指定精確度的內部浮點格式。 帶正負號的整數值會以線性方式對應至內部浮點格式，使最大的可表示整數值對應至1.0，而最大的可表示值會對應至-1.0。 不帶正負號的整數資料的對應方式如下：最大整數值對應至1.0，而零對應至0.0。</li>
<li><strong>GlDrawPixels</strong>函式會 GL_c_SCALE 來乘以產生的浮點色彩值，並將其新增至 GL_c_BIAS，其中<em>c</em>是紅色、綠色、藍色和 ALPHA （適用于個別色彩元件）。 結果會壓制到 [0，1] 範圍內。</li>
<li>如果 GL_MAP_COLOR 為 true， <strong>glDrawPixels</strong> 會依 GL_PIXEL_MAP_c_TO_c 的查閱資料表大小來調整每個色彩元件，然後以該資料表中參考的值取代該元件; <em>c</em> 分別為 R、G、B 或 A。</li>
<li><strong>GlDrawPixels</strong>函式會將目前的點陣位置<em>z</em>座標和材質座標附加至每個圖元，然後將<em>x</em>和<em>y</em>視窗座標指派給第<em>n</em>個片段（例如<em>x</em>），以將產生的 RGBA 色彩轉換成片段： = <em>x</em><sub>r</sub> + <em>n</em> mod <em>寬度</em><br/> <em>y</em>？ = <em>y</em><sub>r</sub> + <em>n/width</em><br/> 其中 (<em>x</em><sub>r</sub> ，<em>y</em><sub>r</sub> ) 是目前的點陣位置。<br/></li>
<li>然後，這些圖元片段的處理方式就像是將點、線條或多邊形所產生的片段一樣。 <strong>GlDrawPixels</strong>函式會先套用材質對應、霧化和所有片段作業，然後再將片段寫入畫面格緩衝區。</li>
</ol></td>
</tr>
<tr class="odd">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <dt><strong>GL_RED</strong></dt> </dl></td>
<td>每個圖元都是單一的紅色元件。<br/> <strong>GlDrawPixels</strong>函式會以 RGBA 圖元的紅色元件相同的方式，將這個元件轉換成內部浮點格式，然後將其轉換為具有綠色和藍色設定為0.0 的 RGBA 圖元，並將 Alpha 設定為1.0。 進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。<br/></td>
</tr>
<tr class="even">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt><strong>GL_GREEN</strong></dt> </dl></td>
<td>每個圖元都是一個綠色的元件。<br/> <strong>GlDrawPixels</strong>函式會以 RGBA 圖元綠色元件的相同方式，將這個元件轉換成內部浮點格式，然後將其轉換為具有紅色和藍色設定為0.0 的 RGBA 圖元，然後將 Alpha 設定為1.0。 進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt><strong>GL_BLUE</strong></dt> </dl></td>
<td>每個圖元都是單一藍色元件。<br/> <strong>GlDrawPixels</strong>函式會以 rgba 圖元 blue 元件的相同方式，將這個元件轉換成內部浮點格式，然後將它轉換成具有紅色和綠色設定為0.0 的 RGBA 圖元，然後將 Alpha 設定為1.0。 進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。<br/></td>
</tr>
<tr class="even">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt><strong>GL_ALPHA</strong></dt> </dl></td>
<td>每個圖元都是單一 Alpha 元件。<br/> <strong>GlDrawPixels</strong>函式會以 RGBA 圖元 Alpha 元件的相同方式，將這個元件轉換成內部浮點格式，然後再將它轉換為紅色、綠色和藍色設定為0.0 的 RGBA 圖元。 進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt><strong>GL_RGB</strong></dt> </dl></td>
<td>每個圖元都是三個元件的群組，順序如下：紅色、綠色、藍色。 <strong>GlDrawPixels</strong>函式會以 RGBA 圖元的 red、綠和 blue 元件相同的方式，將每個元件轉換成內部浮點格式。 色彩三重轉換成將 Alpha 設定為1.0 的 RGBA 圖元。 進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。<br/></td>
</tr>
<tr class="even">
<td><span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <dt><strong>GL_LUMINANCE</strong></dt> </dl></td>
<td>每個圖元都是單一亮度元件。<br/> <strong>GlDrawPixels</strong>函式會以 RGBA 圖元的紅色元件相同的方式，將這個元件轉換成內部浮點格式，然後將它轉換成具有紅色、綠色和藍色的 rgba 圖元（設定為已轉換的亮度值），並將 Alpha 設定為1.0。 進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <dt><strong>GL_LUMINANCE_ALPHA</strong></dt> </dl></td>
<td>每個圖元都是以下列順序組成的兩個元件群組：亮度、Alpha。<br/> <strong>GlDrawPixels</strong>函式會以 RGBA 圖元的紅色元件相同的方式，將兩個元件轉換成內部浮點格式，然後將它們轉換成具有紅色、綠色和藍色的 rgba 圖元（設定為轉換的亮度值），並將 Alpha 設定為轉換的 Alpha 值。 進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。<br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <dt><strong>GL_BGR_EXT</strong></dt> </dl></td>
<td>每個圖元都是三個元件的群組，順序如下：藍色、綠色、紅色。<br/> GL_BGR_EXT 提供的格式符合 Windows 裝置獨立點陣圖 (Dib) 的記憶體配置。 因此，您的應用程式可以使用 Windows 函式呼叫和 OpenGL 圖元函式呼叫的相同資料。<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <dt><strong>GL_BGRA_EXT</strong></dt> </dl></td>
<td>每個圖元都是四個元件的群組，順序如下： blue、綠、red、Alpha。<br/> GL_BGRA_EXT 提供的格式符合 Windows 裝置獨立點陣圖 (Dib) 的記憶體配置。 因此，您的應用程式可以使用 Windows 函式呼叫和 OpenGL 圖元函式呼叫的相同資料。<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*type* 
</dt> <dd>

*圖元* 的資料類型。 以下是接受的符號常數及其意義。



| 值                                                                                                                                                                      | 意義                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <dt>**GL 不 \_ 帶正負號的 \_ 位元組**</dt> </dl>    | 不帶正負號的 8 位元整數<br/>                 |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <dt>**GL \_ 位元組**</dt> </dl>                                | 帶正負號的 8 位元整數<br/>                   |
| <span id="GL_BITMAP"></span><span id="gl_bitmap"></span><dl> <dt>**GL \_ 點陣圖**</dt> </dl>                          | 不帶正負號的8位整數中的單一位<br/> |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <dt>**GL 不 \_ 帶正負號 \_ 簡短**</dt> </dl> | 不帶正負號的 16 位元整數<br/>                |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <dt>**GL \_ 短期**</dt> </dl>                             | 帶正負號的 16 位元整數<br/>                  |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <dt>**GL 不 \_ 帶正負號 \_ INT**</dt> </dl>       | 不帶正負號的 32 位元整數<br/>                |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <dt>**GL \_ INT**</dt> </dl>                                   | 32 位元整數<br/>                         |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <dt>**GL \_ FLOAT**</dt> </dl>                             | 單精確度浮點數<br/>        |



 

</dd> <dt>

*圖元* 
</dt> <dd>

圖元資料的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *寬度* 或 *高度* 都是負數。<br/>                                                                                                                                          |
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *格式* 或 *類型* 都不是可接受的值。 <br/>                                                                                                                             |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | *格式* 為 GL \_ RED、GL \_ 綠、gl \_ BLUE、gl \_ ALPHA、GL \_ RGB、GL \_ RGBA、GL \_ BGR \_ EXT、gl \_ BGRA \_ EXT、gl \_ 亮度或 gl \_ 亮度 \_ ALPHA，且 OpenGL 處於色彩索引模式。<br/> |
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *類型* 為 gl \_ 點陣圖， *格式* 不是 gl \_ 色彩 \_ 索引或 gl 樣板 \_ \_ 索引。<br/>                                                                                         |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | *格式* 為 GL 樣板索引，但沒有樣板 \_ \_ 緩衝區。<br/>                                                                                                                  |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/>                                                        |


## <a name="remarks"></a>備註

**GlDrawPixels** 函式會從記憶體讀取圖元資料，並將其寫入相對於目前點陣位置的畫面格緩衝區。 使用 [**glRasterPos**](glrasterpos-functions.md) 來設定目前的點陣位置，並使用 [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 搭配引數 GL \_ 目前的 \_ 點陣 \_ 位置來查詢點陣位置。

有幾個參數會定義記憶體中圖元資料的編碼，並控制圖元資料在放置於畫面格緩衝區之前的處理。 這些參數設定有四個函數： [**glPixelStore**](glpixelstore-functions.md)、 [**glPixelTransfer**](glpixeltransfer.md)、 [**glPixelMap**](glpixelmap.md)和 [**glPixelZoom**](glpixelzoom.md)。 本主題說明 **glDrawPixels** 這四個函式所指定之許多（但不是全部）參數的影響。

資料是從 *圖元* 讀取為帶正負號或不帶正負號的位元組序列、帶正負號或不帶正負號的短整數、帶正負號或不帶正負號的整數，或是單精確度浮點值（視 *類型* 而定）。 這些位元組、短、整數或浮點數值都會被視為一個色彩或深度元件，或一個索引（視 *格式* 而定）。 索引一律會個別處理。 色彩元件會根據 *格式*，再次視為一、二、三或四個值的群組。 個別的索引和元件群組都稱為圖元。 如果 *type* 是 gl \_ BITMAP，則資料必須為不帶正負號的位元組，且 *格式* 必須是 gl \_ 色彩 \_ 索引或 gl 樣板 \_ \_ 索引。 每個不帶正負號的位元組都會被視為 8 1 位圖元，而依 GL 解壓縮 LSB 的位排序會 \_ \_ \_ 先 (請參閱 [**glPixelStore**](glpixelstore-functions.md)) 。

*寬度*（依 *高度* 圖元）會從記憶體讀取，從位置 *圖元* 開始。 根據預設，這些圖元取自連續的記憶體位置，但在讀取所有 *寬度* 的圖元之後，讀取指標會前進到下一個4位元組的界限。 **GlPixelStore** 函式會指定與引數 GL 解除封裝對齊的4位元組資料列對齊 \_ \_ ，而且您可以將它設定為1、2、4或8個位元組。 其他圖元存放區參數會在讀取第一個圖元之前，以及讀取所有 *寬度* 圖元之後，指定不同的讀取指標的進展。 **GlPixelStore** 函式會根據 [**glPixelTransfer**](glpixeltransfer.md)和 [**glPixelMap**](glpixelmap.md)所指定數個參數的值，以相同的方式在每個 *高度寬度* 的圖元上運作。 這些作業的詳細資料，以及圖元繪製所在的目標緩衝區，是依 *格式* 指定的像素格式所特有。

目前為止所描述的點陣化會假設圖元縮放因數為1.0。 如果您使用 [**glPixelZoom**](glpixelzoom.md) 來變更 *x* 和 *y* 圖元縮放因數，圖元會轉換成片段，如下所示。 如果 (*xr，年*) 是目前的點陣位置，而指定的圖元是在第 *n* 個數據行和第 *m* 個圖元的資料列中，則會為其中心位於矩形中，有邊角的圖元產生片段

 (*x*<sub>r</sub>  +  *縮放比例*？*n*、 *y*<sub>r</sub>  +  *縮放*<sub>y</sub> *m*) 

 (*x*<sub>r</sub>  +  *縮放比例*？  (*n* + 1) ， *y*<sub>r</sub>  +  *縮放*<sub>y</sub> (*m* + 1) ) 

哪裡 *縮放*？是 gl zoom \_ \_ X 和 *ZOOM*<sub>y</sub> 的值是 gl zoom y 的值 \_ \_ 。

下列函式會取出與 **glDrawPixels** 相關的資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 目前 \_ 點陣 \_ 位置的 glGet

具有引數 GL \_ 目前 \_ 點陣 \_ 位置 \_ 有效的 glGet

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Gl</dt> </dl>         |
| 程式庫<br/>                  | <dl> <dt>Opengl32 .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**glAlphaFunc**](glalphafunc.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBlendFunc**](glblendfunc.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glPixelMap**](glpixelmap.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glPixelZoom**](glpixelzoom.md)
</dt> <dt>

[**glRasterPos**](glrasterpos-functions.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glScissor**](glscissor.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> </dl>

 

 





