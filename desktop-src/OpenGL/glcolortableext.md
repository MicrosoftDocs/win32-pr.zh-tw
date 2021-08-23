---
title: 'glColorTableEXT 函式 (Gl) '
description: GlColorTableEXT 函式會指定適用于目標調色板材質之調色板的格式和大小。
ms.assetid: f3d7b1a1-97a5-47ef-a0ca-5e58acb86bb4
keywords:
- glColorTableEXT 函式 OpenGL
topic_type:
- apiref
api_name:
- glColorTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08e29c6ca255a4e99383da669ae8effe149053ca83bb0a1be4ad1ef238f044d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061818"
---
# <a name="glcolortableext-function"></a>glColorTableEXT 函式

**GlColorTableEXT** 函式會指定適用于目標調色板材質之調色板的格式和大小。

## <a name="syntax"></a>語法


```C++
void WINAPI glColorTableEXT(
         GLenum  target,
         GLenum  internalFormat,
         GLsizei width,
         GLenum  format,
         GLenum  type,
   const GLvoid  *data
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*目標* 
</dt> <dd>

要變更其調色板的目標材質。 必須是材質 \_ 1d、材質 \_ 2D、proxy \_ 材質 \_ 1d 或 proxy \_ 材質 \_ 2d。

</dd> <dt>

*internalFormat* 
</dt> <dd>

調色板的內部格式和解析度。 這個參數可以採用下列其中一個符號值。



| 常數       | 基底格式 | R 位 | G 位 | B 位 | 位 |
|----------------|-------------|--------|--------|--------|--------|
| GL \_ R3 \_ G3 \_ B2 | GL \_ RGB     | 3      | 3      | 2      |        |
| GL \_ RGB4       | GL \_ RGB     | 4      | 4      | 4      |        |
| GL \_ RGB5       | GL \_ RGB     | 5      | 5      | 5      |        |
| GL \_ RGB8       | GL \_ RGB     | 8      | 8      | 8      |        |
| GL \_ RGB10      | GL \_ RGB     | 10     | 10     | 10     |        |
| GL \_ RGB12      | GL \_ RGB     | 12     | 12     | 12     |        |
| GL \_ RGB16      | GL \_ RGB     | 16     | 16     | 16     |        |
| GL \_ RGBA2      | GL \_ RGBA    | 2      | 2      | 2      | 2      |
| GL \_ RGBA4      | GL \_ RGBA    | 4      | 4      | 4      | 4      |
| GL \_ RGB5 \_ A1   | GL \_ RGBA    | 5      | 5      | 5      | 1      |
| GL \_ RGBA8      | GL \_ RGBA    | 8      | 8      | 8      | 8      |
| GL \_ RG10 \_ A2   | GL \_ RGBA    | 10     | 10     | 10     | 2      |
| GL \_ RGB12      | GL \_ RGBA    | 12     | 12     | 12     | 12     |
| GL \_ RGBA16     | GL \_ RGBA    | 16     | 16     | 16     | 16     |



 

</dd> <dt>

*width* (寬度) 
</dt> <dd>

調色板的大小。 某些整數 *n* 必須是 2n = 1。

</dd> <dt>

*format* 
</dt> <dd>

圖元資料的格式。 接受下列符號常數。



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
<td><span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <dt><strong>GL_RGBA</strong></dt> </dl></td>
<td>每個圖元都是四個元件的群組，順序如下：紅色、綠色、藍色、Alpha。 RGBA 格式的決定方式如下： <br/>
<ol>
<li><strong>GlColorTableEXT</strong>函式會將浮點值直接轉換成具有未指定精確度的內部格式。 帶正負號的整數值會以線性方式對應至內部格式，如此一來，最正面的可表示整數值會對應至1.0，而最大的可表示整數值會對應至-1.0。 不帶正負號的整數資料的對應方式如下：最大整數值對應至1.0，而零對應至0.0。</li>
<li><strong>GlColorTableEXT</strong>函式會 GL_c_SCALE 將產生的色彩值相乘，並將其新增至 GL_c_BIAS，其中<em>c</em>是紅色、綠色、藍色和 ALPHA，適用于個別的色彩元件。 結果會壓制到 [0，1] 範圍內。</li>
<li>如果 GL_MAP_COLOR 為 <strong>TRUE</strong>， <strong>glColorTableEXT</strong> 會依 GL_PIXEL_MAP_c_TO_c 查閱資料表的大小來調整每個色彩元件，然後以資料表在該資料表中參考的值取代該元件; <em>c</em> 分別為 R、G、B 或 A。</li>
<li><strong>GlColorTableEXT</strong>函式會將目前的點陣位置<em>z</em>座標和材質座標附加至每個圖元，然後將<em>x</em>和<em>y</em>視窗座標指派給第<em>n</em>個片段（例如<em>x</em>），以將產生的 RGBA 色彩轉換成片段： = <em>x</em><sub>r</sub> + <em>n</em> mod <em>寬度</em><br/> <em></em>Y？ = <em>y</em><sub>r</sub> +<em>n/寬度</em><br/> 其中 (<em>x</em><sub>r</sub> ， <em>y</em><sub>r</sub> ) 是目前的點陣位置。<br/></li>
<li>然後，這些圖元片段的處理方式就像是將點、線條或多邊形所產生的片段一樣。 <strong>GlColorTableEXT</strong>函式會先套用材質對應、霧化和所有片段作業，然後再將片段寫入畫面格緩衝區。</li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <dt><strong>GL_RED</strong></dt> </dl></td>
<td>每個圖元都是單一的紅色元件。<br/> <strong>GlColorTableEXT</strong>函式會以 RGBA 圖元的紅色元件相同的方式，將這個元件轉換成內部格式，然後將其轉換為具有綠色和藍色的 rgba 圖元（設為0.0），並將 Alpha 設定為1.0。 進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt><strong>GL_GREEN</strong></dt> </dl></td>
<td>每個圖元都是一個綠色的元件。<br/> <strong>GlColorTableEXT</strong>函式會以 RGBA 圖元的綠色元件相同的方式，將這個元件轉換成內部格式，然後將其轉換為具有紅色和藍色的 rgba 圖元（設為0.0），並將 Alpha 設定為1.0。 進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。<br/></td>
</tr>
<tr class="even">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt><strong>GL_BLUE</strong></dt> </dl></td>
<td>每個圖元都是單一藍色元件。<br/> <strong>GlColorTableEXT</strong>函式會以 RGBA 圖元 blue 元件的相同方式，將這個元件轉換成內部格式，然後將其轉換為具有紅色和綠色設定為0.0 的 RGBA 圖元，然後將 Alpha 設定為1.0。 進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt><strong>GL_ALPHA</strong></dt> </dl></td>
<td>每個圖元都是單一 Alpha 元件。<br/> <strong>GlColorTableEXT</strong>函式會以 RGBA 圖元 Alpha 元件的相同方式，將這個元件轉換成內部格式，然後將它轉換為紅色、綠色和藍色設定為0.0 的 RGBA 圖元。 進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。<br/></td>
</tr>
<tr class="even">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt><strong>GL_RGB</strong></dt> </dl></td>
<td>每個圖元都是三個元件的群組，順序如下：紅色、綠色、藍色。<br/> <strong>GlColorTableEXT</strong>函式會以 RGBA 圖元的 red、綠和 blue 元件的相同方式，將每個元件轉換成內部格式。 色彩三重轉換成將 Alpha 設定為1.0 的 RGBA 圖元。 進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。<br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <dt><strong>GL_BGR_EXT</strong></dt> </dl></td>
<td>每個圖元都是三個元件的群組，順序如下：藍色、綠色、紅色。<br/> GL_BGR_EXT 提供的格式符合 Windows 裝置獨立點陣圖 (dib) 的記憶體配置。 因此，您的應用程式可以使用 Windows 函式呼叫和 OpenGL 圖元函式呼叫的相同資料。<br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <dt><strong>GL_BGRA_EXT</strong></dt> </dl></td>
<td>每個圖元都是四個元件的群組，順序如下： blue、綠、red、Alpha。<br/> GL_BGRA_EXT 提供的格式符合 Windows 裝置獨立點陣圖 (dib) 的記憶體配置。 因此，您的應用程式可以使用 Windows 函式呼叫和 OpenGL 圖元函式呼叫的相同資料。<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*type* 
</dt> <dd>

*資料* 的資料類型。 接受下列符號常數： GL 不 \_ 帶正負號的 \_ 位元組、gl \_ 位元組、GL 不 \_ 帶正負號 \_ 的 SHORT、gl \_ short、gl 不 \_ 帶正負號 \_ int、gl \_ int 和 gl \_ FLOAT。

下表摘要說明 *型* 別參數之有效常數的意義。



| 值                                                                                                                                                                      | 意義                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <dt>**GL 不 \_ 帶正負號的 \_ 位元組**</dt> </dl>    | 不帶正負號的 8 位元整數<br/>                |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <dt>**GL \_ 位元組**</dt> </dl>                                | 帶正負號的 8 位元整數<br/>                  |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <dt>**GL 不 \_ 帶正負號 \_ 簡短**</dt> </dl> | 不帶正負號的 16 位元整數<br/>               |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <dt>**GL \_ 短期**</dt> </dl>                             | 帶正負號的 16 位元整數<br/>                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <dt>**GL 不 \_ 帶正負號 \_ INT**</dt> </dl>       | 不帶正負號的 32 位元整數<br/>               |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <dt>**GL \_ INT**</dt> </dl>                                   | 32 位元整數<br/>                        |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <dt>**GL \_ FLOAT**</dt> </dl>                             | 單精確度浮點值<br/> |



 

</dd> <dt>

*data* 
</dt> <dd>

指向調色板材質資料的指標。 資料會被視為一個調色板專案的立體材質調色板專案的單一圖元。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *寬度* 是不正確整數。<br/>                                                                                            |
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *target*、 *internalFormat*、 *format* 或 *type* 不是可接受的值。<br/>                                                 |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

調色板紋理是以色彩的調色板和一組影像資料所定義，而這組影像資料是由色彩表 (色彩表) 的色彩專案的索引組成。

**GlColorTableEXT** 函式會指定目標材質的材質調色板。 它會取得記憶體中的 *資料* ，並將資料轉換成每個調色板專案都是立體材質的單一圖元。 **GlColorTableEXT** 函式會解壓縮和轉換資料，並將其轉譯成符合指定格式的內部格式（最接近指定 *格式*）。

如果調色板的 *寬度* 大於材質資料中的色彩索引範圍，部分調色板專案就不會使用。 如果調色板的 *寬度* 小於紋理資料中的色彩索引範圍，則會忽略紋理資料的最高有效位，而且在存取調色板時只會使用索引中適當的位數。 當您使用 PROXY  \_ 材質 \_ 1d 或 proxy 材質2d 指定 proxy 目標時 \_ \_ ，會重設 proxy 材質的選擇區，並設定其參數，但不會傳送或存取任何資料。

當 *目標* 參數為 GL \_ proxy \_ 材質 \_ 1d 或 GL \_ proxy \_ 材質 \_ 2d，且執行不支援針對 *格式* 或 *寬度* 指定的值時， **glColorTableEXT** 可能無法建立要求的色彩表。 在此情況下，color 資料表是空的，而且所有取出的參數都是零。 您可以藉由使用 proxy 目標呼叫 **glColorTableEXT** ，然後呼叫 [**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md) 或 [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) 來判斷 width 參數是否符合 **GlColorTableEXT** 所設定的，來判斷 OpenGL 是否支援特定的色彩表格式和大小。 如果取出的寬度為零，則 **glColorTable** 的色彩表格要求會失敗。 如果取出的寬度不是零，您可以使用紋理1d 或材質2d 的真實目標來呼叫 **glColorTable** ， \_ \_ 以設定色彩表。

> [!Note]  
> **GlColorTableEXT** 函式是延伸模組函式，不是標準 OpenGL 程式庫的一部分，而是 GL \_ EXT \_ \_ 材質擴充功能的一部分。 若要檢查您的 OpenGL 執行是否支援 **glColorTableEXT**，請) 呼叫 [**glGetString**](glgetstring.md) (GL \_ 延伸模組。 如果它傳回 GL \_ EXT \_ \_ （調色板）材質，則會支援 **glColorTableEXT** 。 若要取得擴充函數的函式位址，請呼叫 [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)。

 

若要取出 **glColorTableEXT** 函數所指定的實際色彩資料表資料，請呼叫 [**glGetColorTableEXT**](glgetcolortableext.md)。 若要抓取 **glColorTableEXT** 函式所指定之色彩表的參數（例如 *寬度* 和 *格式*），請呼叫 **glGetColorTableParameterivEXT** 或 **glGetColorTableParameterfvEXT** 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                      |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>Gl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColorSubTableEXT**](glcolorsubtableext.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetColorTableEXT**](glgetcolortableext.md)
</dt> <dt>

[**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md)
</dt> <dt>

[**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md)
</dt> <dt>

[**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





