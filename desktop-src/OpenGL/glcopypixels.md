---
title: 'glCopyPixels 函式 (Gl) '
description: GlCopyPixels 函式會複製畫面格緩衝區中的圖元。
ms.assetid: c4055928-7b8b-4d0f-94f3-e3b9c0503308
keywords:
- glCopyPixels 函式 OpenGL
topic_type:
- apiref
api_name:
- glCopyPixels
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a7ba0833534d21e48c251da6491fee2996c3ed9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934510"
---
# <a name="glcopypixels-function"></a>glCopyPixels 函式

**GlCopyPixels** 函式會複製畫面格緩衝區中的圖元。

## <a name="syntax"></a>語法


```C++
void WINAPI glCopyPixels(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height,
   GLenum  type
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*x* 
</dt> <dd>

要複製之圖元矩形區域左下角的視窗 x 平面座標。

</dd> <dt>

*y* 
</dt> <dd>

要複製之圖元矩形區域左下角的視窗 y 平面座標。

</dd> <dt>

*width* (寬度) 
</dt> <dd>

要複製之圖元矩形區域的寬度維度。 不可為負值。

</dd> <dt>

*height* (高度) 
</dt> <dd>

要複製之圖元矩形區域的高度維度。 不可為負值。

</dd> <dt>

*type* 
</dt> <dd>

指定 **glCopyPixels** 是否要複製色彩值、深度值或樣板值。 可接受的符號常數為。



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
<td><span id="GL_COLOR"></span><span id="gl_color"></span><dl> <dt><strong>GL_COLOR</strong></dt> </dl></td>
<td><strong>GlCopyPixels</strong>函式會從目前指定為讀取來源緩衝區的緩衝區讀取索引或 RGBA 色彩 (查看<a href="glreadbuffer.md"><strong>glReadBuffer</strong></a>) 。 <br/> 如果 OpenGL 處於色彩索引模式：<br/>
<ol>
<li>從這個緩衝區讀取的每個索引都會轉換成指向二進位點右邊未指定位數的固定點格式。</li>
<li>每個索引都會 GL_INDEX_SHIFT 位左移，並新增至 GL_INDEX_OFFSET。如果 GL_INDEX_SHIFT 為負數，則向右移位。 無論是哪一種情況，在結果中都不會以零位填滿指定的位位置。<br/></li>
<li>如果 GL_MAP_COLOR 為 true，就會將索引取代為它在查閱資料表 GL_PIXEL_MAP_I_TO_I 中所參考的值。</li>
<li>如果索引的查閱取代是否已完成，索引的整數部分就是， <strong>而</strong>ed 的整數部分是 2<em><sup>b</sup></em> 1，其中 <em>b</em> 是色彩索引緩衝區中的位數。</li>
</ol>
如果 OpenGL 處於 RGBA 模式：<br/>
<ol>
<li>每個讀取之圖元的紅色、綠色、藍色和 Alpha 元件都會轉換成具有未指定精確度的內部浮點格式。</li>
<li>轉換會將最大可表示的元件值對應至1.0，並將元件值0對應至0.0。</li>
<li>產生的浮點色彩值接著會乘以 GL_c_SCALE 並新增至 GL_c_BIAS，其中 <em>c</em> 是紅色、綠色、藍色和 ALPHA，適用于個別的色彩元件。</li>
<li>結果會壓制到 [0，1] 範圍內。</li>
<li>如果 GL_MAP_COLOR 為 true，則每個色彩元件都會依查閱資料表的大小進行調整 GL_PIXEL_MAP_c_TO_c，然後以它在該資料表中參考的值取代; <em>c</em> 分別為 R、G、B 或 A。 接著，會將目前的點陣位置<em>z</em>座標和材質座標附加至每個圖元，然後指派視窗座標 (<em>x</em><sub>r</sub> + i、 <em>y</em><sub>r</sub> + <em>j</em>) ，其中 (<em>x</em><sub>r</sub> 、 <em>y</em><sub>r</sub> ) 是目前的點陣位置，而圖元是在<em>j</em>資料列中<em>i</em>位置的圖元，則會將結果的索引或 RGBA 色彩轉換成片段。 然後，這些圖元片段的處理方式就像是將點、線條或多邊形所產生的片段一樣。 材質對應、霧化和所有片段作業都是在片段寫入至畫面格緩衝區之前套用。<br/></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_DEPTH"></span><span id="gl_depth"></span><dl> <dt><strong>GL_DEPTH</strong></dt> </dl></td>
<td>深度的值會從深度緩衝區讀取，並直接轉換成具有未指定精確度的內部浮點格式。 產生的浮點數深度值接著會乘以 GL_DEPTH_SCALE，並新增至 GL_DEPTH_BIAS。 結果會壓制至範圍 [0，1]。 <br/> 然後，會將目前的點陣位置色彩或色彩索引和材質座標附加至每個圖元，然後指派視窗座標 (<em>x</em><sub>r</sub> + i、 <em>y</em><sub>r</sub> + <em>j</em>) ，其中 (<em>x</em><sub>r</sub> 、 <em>y</em><sub>r</sub> ) 是目前的點陣位置，而圖元是在<em>j</em>資料列中<em>i</em>位置的圖元，則會轉換成片段。 然後，這些圖元片段的處理方式就像是將點、線條或多邊形所產生的片段一樣。 材質對應、霧化和所有片段作業都是在片段寫入至畫面格緩衝區之前套用。<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_STENCIL"></span><span id="gl_stencil"></span><dl> <dt><strong>GL_STENCIL</strong></dt> </dl></td>
<td>樣板索引會從樣板緩衝區中讀取，並轉換為內部的固定點格式，並在二進位點右邊有未指定的位數。 然後，每個固定點索引會依 GL_INDEX_SHIFT 位向左移，並新增至 GL_INDEX_OFFSET。 如果 GL_INDEX_SHIFT 為負數，則向右移位。 無論是哪一種情況，在結果中都不會以零位填滿指定的位位置。 如果 GL_MAP_STENCIL 為 true，就會將索引取代為它在查閱資料表 GL_PIXEL_MAP_S_TO_S 中所參考的值。 如果索引的查閱取代是否已完成，索引的整數部分就是， <strong>而</strong>ed 的整數部分則是 2<sup>b</sup> - 1，其中 <em>b</em> 是樣板緩衝區中的位數。 接著會將產生的樣板索引寫入至樣板緩衝區，以便從<em>j</em>資料列的<em>i</em>位置讀取的索引會寫入位置 (<em>x</em><sub>r</sub> + <em>i</em>， <em>y</em><sub>r</sub> + <em>j</em>) ，其中 (<em>x</em><sub>r</sub> ， <em>y</em><sub>r</sub> ) 是目前的點陣位置。 只有圖元擁有權的測試、剪下測試和樣板 writemask 會影響這些寫入。<br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *類型* 不是可接受的值。<br/>                                                                                          |
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *寬度* 或高度都是負數。<br/>                                                                                     |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | *類型* 為 GL \_ 深度且沒有深度緩衝區。<br/>                                                                        |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | *類型* 為 GL 樣板，但沒有 \_ 任何樣板緩衝區。<br/>                                                                    |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlCopyPixels** 函式會從指定的畫面格緩衝區位置將螢幕對齊的圖元矩形複製到相對於目前點陣位置的區域。 只有在整個圖元來源區域都在視窗的公開部分內時，才會妥善定義其作業。 從視窗外部或未公開之視窗的區域產生的複本結果，會與硬體相依或未定義。

*X* 和 *y* 參數指定要複製之矩形區域左下角的視窗座標。 *寬度* 和 *高度* 參數指定要複製之矩形區域的維度。 *寬度* 和 *高度* 都必須是非負值。

有幾個參數會控制正在複製的圖元資料處理。 這些參數會以三個函式設定： [**glPixelTransfer**](glpixeltransfer.md)、 [**glPixelMap**](glpixelmap.md)和 [**glPixelZoom**](glpixelzoom.md)。 本主題說明 **glCopyPixels** 這三個函式所指定的大部分（但非全部）參數的效果。

**GlCopyPixels** 函式會在 (*x* i、y j) 的左下角，將每個圖元的值複製到  +     +   0 = *i* 的  <  *寬度* 和 0 = *j*  <  *高度*。 這個圖元稱為 *j* 資料列中的 *i* 圖元。 在每個資料列中，會以資料列順序從最小到最高的資料列複製圖元。

*Type* 參數會指定是否要複製 color、depth 或樣板資料。

目前為止所描述的點陣化會假設圖元縮放因數為1.0。 如果您使用 [**glPixelZoom**](glpixelzoom.md) 來變更 *x* 和 *y* 圖元縮放因數，圖元會轉換成片段，如下所示。 如果 (*x*<sub>r</sub> ， *y*<sub>r</sub> ) 是目前的點陣位置，而指定的圖元位於來源圖元矩形的 *j* 資料列中的 *i* 個位置，則會為其中心位於矩形中邊角為矩形的圖元產生片段。

 (*x*<sub>r</sub>  +  *zoom*？ i，y <sub>r</sub>  +  *zoom*<sub>y</sub> *j*) 

及

 (*x*<sub>r</sub>  +  *縮放比例*？  (*i* + 1) ， *y*<sub>r</sub>  +  *zoom*<sub>y</sub> (*j* + 1) ) 

哪裡 *縮放*？是 gl zoom \_ \_ X 和 *ZOOM*<sub>y</sub> 的值是 gl zoom y 的值 \_ \_ 。

[**GlPixelStore**](glpixelstore-functions.md)指定的模式不會影響 **glCopyPixels** 的操作。

下列函式會取出與 **glCopyPixels** 相關的資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 目前 \_ 點陣 \_ 位置的 glGet

具有引數 GL \_ 目前 \_ 點陣 \_ 位置 \_ 有效的 glGet

若要將視窗左下角的色彩圖元複製到目前的點陣位置，請使用

**glCopyPixels** ( 0、0、1、1、GL \_ 色彩 ) ;

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
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

[**glReadBuffer**](glreadbuffer.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> </dl>

 

 





