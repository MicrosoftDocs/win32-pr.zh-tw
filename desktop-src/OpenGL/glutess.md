---
title: 'gluTessCallback 函式 (X.glu 隊) '
description: GluTessCallback 函式會定義鑲嵌式物件的回呼。
ms.assetid: a9709919-d34c-42c4-82b8-6a503f2b39b0
keywords:
- gluTessCallback 函式 OpenGL
topic_type:
- apiref
api_name:
- gluTessCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17cdba8b9dd9a3e762a93923a3c353fbc9578377
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934984"
---
# <a name="glutesscallback-function"></a>gluTessCallback 函式

**GluTessCallback** 函式會定義鑲嵌式物件的回呼。

## <a name="syntax"></a>語法


```C++
void WINAPI gluTessCallback(
   GLUtesselator *tess,
   GLenum        which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*苔 絲* 
</dt> <dd>

使用 [**gluNewTess**](glunewtess.md)) 建立的鑲嵌式物件 (。

</dd> <dt>

*頻率* 
</dt> <dd>

要定義的回呼。 下列值有效： X.GLU 隊 \_ TESS \_ BEGIN、X.glu 隊 \_ TESS \_ begin \_ DATA、x.glu 隊 \_ TESS \_ edge 旗標 \_ 、X.glu 隊 \_ TESS \_ edge 旗 \_ 標 \_ 資料、x.glu 隊 \_ TESS \_ 頂點、x.glu 隊 TESS 頂點資料、x.glu 隊 TESS END、x.glu 隊 TESS 端點 \_ 資料 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ 、x.glu 隊 TESS、x.glu 隊 TESS、x.glu 隊 TESS、x.glu 隊 TESS、、data、error 和 error DATA。

如需這些回呼的詳細資訊，請參閱下列備註一節。

</dd> <dt>

*Fn* 
</dt> <dd>

要呼叫的函式。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

使用 **gluTessCallback** 來指定鑲嵌式物件所要使用的回呼。 如果已定義指定的回呼，則會予以取代。 如果 *fn* 為 **Null**，則現有的回呼會變成未定義。

鑲嵌式物件會使用這些回呼來描述您指定的多邊形如何細分為三角形。

每個回呼都有兩個版本，一個具有可定義的多邊形資料，另一個則沒有。 如果指定了這兩個版本的特定回呼，將會使用您指定的多邊形資料的回呼。 [**GluTessBeginPolygon**](glutessbeginpolygon.md)的 *多邊形 \_ 資料* 參數是在呼叫 **gluTessBeginPolygon** 時所指定之指標的複本。

以下是有效的回呼：



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>回呼</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>GLU_TESS_BEGIN</td>
<td>GLU_TESS_BEGIN 回呼會以 <a href="glbegin.md"><strong>glBegin</strong></a> 的方式叫用，以指出 (三角形) 基本的開頭。 函數會採用 <strong>GLenum</strong>類型的單一引數。 如果您將 GLU_TESS_BOUNDARY_ONLY 屬性設定為 GL_FALSE，則引數會設定為 GL_TRIANGLE_FAN、GL_TRIANGLE_STRIP 或 GL_TRIANGLES。 如果您將 GLU_TESS_BOUNDARY_ONLY 屬性設定為 GL_TRUE，則引數會設定為 GL_LINE_LOOP。 此回呼的函式原型如下： <strong>void</strong> <strong>begin</strong> (<strong>GLenum</strong> <em>類型</em>) ;<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_BEGIN_DATA</td>
<td>GLU_TESS_BEGIN_DATA 與 GLU_TESS_BEGIN 回呼相同，不同之處在于它會接受額外的指標引數。 這個指標等同于呼叫 <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>時所提供的不透明指標。 此回呼的函式原型是： <strong>void</strong> <strong>beginData</strong> (<strong>GLenum</strong> <em>type</em>、 <strong>void</strong> * <em>polygon_data</em>) ;<br/></td>
</tr>
<tr class="odd">
<td>GLU_TESS_EDGE_FLAG</td>
<td>GLU_TESS_EDGE_FLAG 回呼類似于 <a href="gledgeflag-functions.md"><strong>glEdgeFlag</strong></a>。 此函式會採用單一布林值旗標，指出哪些邊緣位於多邊形界限上。 如果 GL_TRUE 旗標，則接下來的每個頂點會開始位於多邊形界限上的邊緣;也就是將內部區域與外部區域分隔開來的邊緣。 如果 GL_FALSE 旗標，則接下來的每個頂點會開始位於多邊形內部的邊緣。 如果在執行第一個頂點回呼之前叫用了定義的) ，則會叫用 GLU_TESS_EDGE_FLAG 回呼 (。 因為三角形風扇和三角形的條紋不支援邊緣旗標，所以不會使用 GL_TRIANGLE_FAN 來呼叫 begin 回呼，或在提供邊緣旗標回呼時 GL_TRIANGLE_STRIP。 相反地，風扇和條紋會轉換成獨立的三角形。 此回呼的函數原型為：<br/> <strong>void</strong> <strong>edgeFlag</strong> (<strong>GLboolean</strong> <em>旗</em> 標) ;<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_EDGE_FLAG_DATA</td>
<td>GLU_TESS_EDGE_FLAG_DATA 回呼與 GLU_TESS_EDGE_FLAG 回呼相同，不同之處在于它會接受額外的指標引數。 這個指標等同于呼叫 <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>時所提供的不透明指標。 此回呼的函式原型是： <strong>void</strong> <strong>edgeFlagData</strong> (<strong>GLboolean</strong> <em>旗</em>標、 <strong>void</strong> * <em>polygon_data</em>) ;<br/></td>
</tr>
<tr class="odd">
<td>GLU_TESS_VERTEX</td>
<td>GLU_TESS_VERTEX 回呼是在 begin 和 end 回呼之間叫用。 它類似于 glVertex，它會定義鑲嵌式進程所建立之三角形的頂點。 函式會接受指標作為其唯一的引數。 此指標與您定義頂點時所提供的不透明指標相同 (請參閱 <a href="glutessvertex.md"><strong>gluTessVertex</strong></a>) 。 此回呼的函數原型是： <strong>void</strong> <strong>頂點</strong> (<strong>void</strong> * <em>vertex_data</em>) ;<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_VERTEX_DATA</td>
<td>GLU_TESS_VERTEX_DATA 與 GLU_TESS_VERTEX 回呼相同，不同之處在于它會接受額外的指標引數。 這個指標等同于呼叫 <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>時所提供的不透明指標。 此回呼的函式原型是： <strong>void</strong>  <strong>vertexData</strong> (void * <em>vertex_data</em>， <strong>void</strong> * <em>polygon_data</em>) ;<br/></td>
</tr>
<tr class="odd">
<td>GLU_TESS_END</td>
<td>GLU_TESS_END 回呼的作用與 <a href="glend.md"><strong>glEnd</strong></a>相同。 它會指出基本的結尾，且不會使用任何引數。 此回呼的函數原型是： <strong>void</strong> <strong>end</strong> (<strong>void</strong>) ;<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_END_DATA</td>
<td>GLU_TESS_END_DATA 回呼與 GLU_TESS_END 回呼相同，不同之處在于它會接受額外的指標引數。 這個指標等同于呼叫 <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>時所提供的不透明指標。 此回呼的函數原型是： <strong>void</strong> <strong>endData</strong> (<strong>void</strong> * <em>polygon_data</em>) ;<br/></td>
</tr>
<tr class="odd">
<td>GLU_TESS_COMBINE</td>
<td>呼叫 GLU_TESS_COMBINE 回呼，以在鑲嵌偵測到交集或合併功能時，建立新頂點。 此函式會採用四個引數：三個元素的陣列，每個元素都是 Gldouble 類型。<br/> 四個指標的陣列。<br/> 四個元素的陣列，每個專案都是 GLfloat 類型。<br/> 指標的指標。<br/> 此回呼的函數原型為： <br/> <strong>void</strong> <strong>結合</strong> (<strong>GLdouble</strong> <em>coords</em>[3]、 <strong>void</strong> * <em>vertex_data</em>[4]、 <strong>GLfloat</strong> <em>權數</em>[4]、 <strong>void</strong>  ** <em>outData</em>) ;<br/> 頂點定義為最多四個現有頂點的線性組合，儲存在 vertex_data 中。 線性組合的係數是依權數提供;這些權數一律會加總為1.0。 即使部分權數為零，所有頂點指標都是有效的。 Coords 參數會提供新頂點的位置。<br/> 配置另一個頂點、使用 vertex_data 和權數來插入參數，並傳回 outData 中的新頂點指標。 這個控制碼是在轉譯回呼期間提供。 在呼叫 <a href="glutessendpolygon.md"><strong>gluTessEndPolygon</strong></a>之後釋放記憶體。<br/> 例如，如果多邊形位於立體空間的任意平面中，而您將色彩與每個頂點建立關聯，GLU_TESS_COMBINE 回呼看起來可能如下所示：<br/>
<pre data-space="preserve"><code>void myCombine( GLdouble coords[3], VERTEX *d[4], 
                GLfloat w[4], VERTEX **dataOut ) 
{ 
    VERTEX *newVertex = new_vertex(); 
    newVertex->x = coords[0]; 
    newVertex->y = coords[1]; 
    newVertex->z = coords[2]; 
    newVertex->r = w[0]*d[0]->r + w[1]*d[1]->r + w[2]*d[2]->r + 
                   w[3]*d[3]->r; 
    newVertex->g = w[0]*d[0]->g + w[1]*d[1]->g + w[2]*d[2]->g + 
                   w[3]*d[3]->g; 
    newVertex->b = w[0]*d[0]->b + w[1]*d[1]->b + w[2]*d[2]->b + 
                   w[3]*d[3]->b; 
    newVertex->a = w[0]*d[0]->a + w[1]*d[1]->a + w[2]*d[2]->a + 
                   w[3]*d[3]->a; 
    *dataOut = newVertex; 
}</code></pre>
當鑲嵌偵測到交集時，GLU_TESS_COMBINE 或 GLU_TESS_COMBINE_DATA 回呼 (請參閱以下) 必須定義，而且必須將非<strong>Null</strong> 指標寫入 dataOut。 否則會發生 GLU_TESS_NEED_COMBINE_CALLBACK 錯誤，而且不會產生任何輸出。  (這是鑲嵌和轉譯期間唯一可能發生的錯誤。 ) <br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_COMBINE_DATA</td>
<td>GLU_TESS_COMBINE_DATA 回呼與 GLU_TESS_COMBINE 回呼相同，不同之處在于它會接受額外的指標引數。 這個指標等同于呼叫 <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>時所提供的不透明指標。 此回呼的函式原型為： <strong>void</strong> <strong>combineData</strong> (<strong>GLdouble</strong> <em>coords</em>[3]、 <strong>void</strong> *<em>vertex_data</em>[4]、 <strong>GLfloat</strong> <em>權數</em>[4]、 <strong>void</strong>  ** <em>outData</em>、 <strong>void</strong> * <em>polygon_data</em>) ;<br/></td>
</tr>
<tr class="odd">
<td>GLU_TESS_ERROR</td>
<td>遇到錯誤時，會呼叫 GLU_TESS_ERROR 回呼。 其中一個引數的類型為 <strong>GLenum</strong>;它會指出發生的特定錯誤，並設定為下列其中一項： GLU_TESS_MISSING_BEGIN_POLYGON<br/> GLU_TESS_MISSING_END_POLYGON<br/> GLU_TESS_MISSING_BEGIN_CONTOUR<br/> GLU_TESS_MISSING_END_CONTOUR<br/> GLU_TESS_COORD_TOO_LARGE<br/> GLU_TESS_NEED_COMBINE_CALLBACK<br/> 呼叫 gluErrorString 來取出描述這些錯誤的字元字串。 此回呼的函數原型如下所示：<br/> <strong>void</strong> <strong>錯誤</strong> (<strong>GLenum</strong> <em>errno</em>) ;<br/> X.GLU 隊程式庫會藉由插入遺失的呼叫，從前四個錯誤中復原。 GLU_TESS_COORD_TOO_LARGE 表示某些頂點座標超過預先定義的常數 GLU_TESS_MAX_COORD 絕對值，且已壓制該值。  (座標值必須夠小，才能將兩個值相乘，而不會發生溢位。 ) GLU_TESS_NEED_COMBINE_CALLBACK 表示鑲嵌偵測到輸入資料中有兩個邊緣之間的交集，但未提供 GLU_TESS_COMBINE 或 GLU_TESS_COMBINE_DATA 回呼。 不會產生任何輸出。<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_ERROR_DATA</td>
<td>GLU_TESS_ERROR_DATA 回呼與 GLU_TESS_ERROR 回呼相同，不同之處在于它會接受額外的指標引數。 這個指標等同于呼叫 <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>時所提供的不透明指標。 此回呼的函式原型是： <strong>void</strong> <strong>errorData</strong> (<strong>GLenum</strong> <em>errno</em>、 <strong>void</strong> * <em>polygon_data</em>) ;<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>X.glu 隊。h</dt> </dl>     |
| 程式庫<br/>                  | <dl> <dt>Glu32 .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEdgeFlag**](gledgeflag-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> <dt>

[**gluDeleteTess**](gludeletetess.md)
</dt> <dt>

[**gluErrorString**](gluerrorstring.md)
</dt> <dt>

[**gluNewTess**](glunewtess.md)
</dt> <dt>

[**gluTessBeginPolygon**](glutessbeginpolygon.md)
</dt> <dt>

[**gluTessEndPolygon**](glutessendpolygon.md)
</dt> <dt>

[**gluTessVertex**](glutessvertex.md)
</dt> </dl>

 

 





