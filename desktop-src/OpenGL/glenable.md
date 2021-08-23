---
title: 'glEnable 函式 (Gl) '
description: 'GlEnable 和 glDisable 函數會啟用或停用 OpenGL 功能。 |glEnable 函式 (Gl) '
ms.assetid: cd4590dd-ae41-47c9-9861-10d72318840f
keywords:
- glEnable 函式 OpenGL
topic_type:
- apiref
api_name:
- glEnable
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4ef13323f72efd516a0c5321cb410885904ac5245b5198b21ea9e4a4b29f3c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119625628"
---
# <a name="glenable-function"></a>glEnable 函式

**GlEnable** 和 [**glDisable**](gldisable.md)函數會啟用或停用 OpenGL 功能。

## <a name="syntax"></a>語法


```C++
void WINAPI glEnable(
   GLenum cap
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*帽* 
</dt> <dd>

表示 OpenGL 功能的符號常數。

如需值 *上限* 的討論，請參閱下列備註一節。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *上限* 不是先前 [備註] 區段中所列的其中一個值。<br/>                                                   |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlEnable** 和 **glDisable** 函式會啟用和停用各種 OpenGL 圖形功能。 使用 [**glIsEnabled**](glisenabled.md) 或 [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 來判斷任何功能目前的設定。

**GlEnable** 和 **glDisable** 都採用單一引數（ *cap*），其可採用下列其中一個值：



| 值                       | 意義                                                                                                                                                                                                                                                     |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GL \_ ALPHA \_ 測試             | 啟用時，請進行 Alpha 測試。 請參閱 [**glAlphaFunc**](glalphafunc.md)。                                                                                                                                                                                       |
| GL \_ 自動 \_ 正常            | 若已啟用，則當 GL \_ List.map2 \_ 頂點 \_ 3 或 gl \_ list.map2 \_ 頂點 \_ 4 產生頂點時，計算介面標準向量會 analytically。 請參閱 [**glMap2**](glmap2.md)。                                                                                        |
| GL \_ BLEND                   | 若已啟用，請將內送 RGBA 色彩值與色彩緩衝區中的值混合。 請參閱 [**glBlendFunc**](glblendfunc.md)。                                                                                                                              |
| GL \_ 剪輯 \_ 平面 *i*          | 若已啟用，則會根據使用者 *定義的裁剪平面來* 裁剪幾何。 請參閱 [**glClipPlane**](glclipplane.md)。                                                                                                                                                  |
| GL \_ 色彩 \_ 邏輯 \_ OP        | 啟用時，將目前的邏輯作業套用至傳入的 RGBA 色彩和色彩緩衝區值。 請參閱 [**glLogicOp**](gllogicop.md)。                                                                                                                     |
| GL \_ 色彩 \_ 材質         | 啟用時，有一或多個材質參數可追蹤目前的色彩。 請參閱 [**glColorMaterial**](glcolormaterial.md)。                                                                                                                                   |
| GL \_ 精選 \_ 臉部              | 若已啟用，則根據視窗座標中的纏繞來挑選多邊形。 請參閱 [**glCullFace**](glcullface.md)。                                                                                                                                               |
| GL \_ 深度 \_ 測試             | 如果啟用，請進行深度比較，並更新深度緩衝區。 請參閱 [**glDepthFunc**](gldepthfunc.md) 和 [**glDepthRange**](gldepthrange.md)。                                                                                                              |
| GL \_ 遞色                  | 若已啟用，則會先將色彩元件或索引寫入色彩緩衝區，然後再將其寫入。                                                                                                                                                                 |
| GL \_ 霧化                     | 若已啟用，請將 [霧化色彩] 混合成紋理後色彩。 請參閱 [**glFog**](glfog.md)。                                                                                                                                                                    |
| GL \_ 索引 \_ 邏輯 \_ OP        | 若已啟用，請將目前的邏輯運算套用至傳入索引和色彩緩衝區索引。 請參閱 [**glLogicOp**](gllogicop.md)。                                                                                                                         |
| GL \_ 燈                | 若已啟用，請在光源方程式的評估中包含淺 *i* 。 請參閱 [**glLightModel**](gllightmodel-functions.md) 和 [**glLight**](gllight-functions.md)。                                                                                      |
| GL \_ 照明                | 若已啟用，請使用目前的光源參數來計算頂點色彩或索引。 如果停用，請將目前的色彩或索引與每個頂點產生關聯。 請參閱 [**glMaterial**](glmaterial-functions.md)、 **glLightModel** 和 **glLight**。                |
| GL \_ 行 \_ 平滑            | 若已啟用，請使用正確的篩選繪製行。 如果停用，則繪製別名行。 請參閱 [**glLineWidth**](gllinewidth.md)。                                                                                                                                     |
| GL \_ 線 \_ STIPPLE           | 若已啟用，則會在繪製線條時使用目前的行 stipple 模式。 請參閱 [**glLineStipple**](gllinestipple.md)。                                                                                                                                            |
| GL \_ 邏輯 \_ OP               | 啟用時，將目前選取的邏輯作業套用至內送和色彩緩衝區索引。 請參閱 [**glLogicOp**](gllogicop.md)。                                                                                                                    |
| GL \_ MAP1 \_ 色彩 \_ 4          | 如果啟用， [**glEvalCoord1**](glevalcoord-functions.md)、 [**glEvalMesh1**](glevalmesh-functions.md)和 [**GLEVALPOINT1**](glevalpoint.md) 的呼叫會產生 RGBA 值。 另請參閱 [**glMap1**](glmap1.md)。                                           |
| GL \_ MAP1 \_ 索引             | 如果啟用，呼叫 **glEvalCoord1**、 **glEvalMesh1** 和 **glEvalPoint1** 會產生色彩索引。 另請參閱 **glMap1**。                                                                                                                                   |
| GL \_ MAP1 \_ 正常            | 如果啟用， [**glEvalCoord1**](glevalcoord-functions.md)、 [**glEvalMesh1**](glevalmesh-functions.md)和 [**glEvalPoint1**](glevalpoint.md) 的呼叫會產生法線。 另請參閱 [**glMap1**](glmap1.md)。                                               |
| GL \_ MAP1 \_ 材質 \_ COORD \_ 1 | 如果啟用， **glEvalCoord1**、 **glEvalMesh1** 和 **glEvalPoint1** 的呼叫會產生 *s* 材質座標。 另請參閱 **glMap1**。                                                                                                                         |
| GL \_ MAP1 \_ 材質 \_ COORD \_ 2 | 如果啟用，呼叫 [**glEvalCoord1**](glevalcoord-functions.md)、 [**glEvalMesh1**](glevalmesh-functions.md)和 [**glEvalPoint1**](glevalpoint.md) 會產生 *s* 和 *t* 材質座標。 另請參閱 [**glMap1**](glmap1.md)。                       |
| GL \_ MAP1 \_ 材質 \_ COORD \_ 3 | 如果啟用， **glEvalCoord1**、 **glEvalMesh1** 和 **glEvalPoint1** 的呼叫會產生 *s*、 *t* 和 *r* 材質座標。 另請參閱 **glMap1**。                                                                                                           |
| GL \_ MAP1 \_ 材質 \_ COORD \_ 4 | 如果啟用， [glEvalCoord1](glevalcoord-functions.md)、 [glEvalMesh1](glevalmesh-functions.md)和 [**glEvalPoint1**](glevalpoint.md) 的呼叫會產生 *s*、 *t*、 *r* 和 *q* 材質座標。 另請參閱 [**glMap1**](glmap1.md)。                    |
| GL \_ MAP1 \_ 頂點 \_ 3         | 如果啟用， **glEvalCoord1**、 **glEvalMesh1** 和 **glEvalPoint1** 的呼叫會產生 *x*、 *y* 和 *z* 頂點座標。 另請參閱 **glMap1**。                                                                                                            |
| GL \_ MAP1 \_ 頂點 \_ 4         | 如果啟用， [**glEvalCoord1**](glevalcoord-functions.md)、 [**glEvalMesh1**](glevalmesh-functions.md)和 [**glEvalPoint1**](glevalpoint.md) 的呼叫會產生同質 *x*、 *y*、 *z* 和 *w* 頂點座標。 另請參閱 [**glMap1**](glmap1.md)。 |
| GL \_ List.map2 \_ 色彩 \_ 4          | 如果啟用， [**glEvalCoord2**](glevalcoord-functions.md)、 [**glEvalMesh2**](glevalmesh-functions.md)和 [**GLEVALPOINT2**](glevalpoint.md) 的呼叫會產生 RGBA 值。 另請參閱 [**glMap2**](glmap2.md)。                                           |
| GL \_ List.map2 \_ 索引             | 如果啟用，呼叫 **glEvalCoord2**、 **glEvalMesh2** 和 **glEvalPoint2** 會產生色彩索引。 另請參閱 **glMap2**。                                                                                                                                   |
| GL \_ List.map2 \_ 正常            | 如果啟用， [**glEvalCoord2**](glevalcoord-functions.md)、 [**glEvalMesh2**](glevalmesh-functions.md)和 [**glEvalPoint2**](glevalpoint.md) 的呼叫會產生法線。 另請參閱 [**glMap2**](glmap2.md)。                                               |
| GL \_ List.map2 \_ 材質 \_ COORD \_ 1 | 如果啟用， **glEvalCoord2**、 **glEvalMesh2** 和 **glEvalPoint2** 的呼叫會產生 *s* 材質座標。 另請參閱 **glMap2**。                                                                                                                         |
| GL \_ List.map2 \_ 材質 \_ COORD \_ 2 | 如果啟用，呼叫 [**glEvalCoord2**](glevalcoord-functions.md)、 [**glEvalMesh2**](glevalmesh-functions.md)和 [**glEvalPoint2**](glevalpoint.md) 會產生 *s* 和 *t* 材質座標。 另請參閱 [**glMap2**](glmap2.md)。                       |
| GL \_ List.map2 \_ 材質 \_ COORD \_ 3 | 如果啟用， **glEvalCoord2**、 **glEvalMesh2** 和 **glEvalPoint2** 的呼叫會產生 *s*、 *t* 和 *r* 材質座標。 另請參閱 **glMap2**。                                                                                                           |
| GL \_ List.map2 \_ 材質 \_ COORD \_ 4 | 如果啟用， [**glEvalCoord2**](glevalcoord-functions.md)、 [**glEvalMesh2**](glevalmesh-functions.md)和 [**glEvalPoint2**](glevalpoint.md) 的呼叫會產生 *s*、 *t*、 *r* 和 *q* 材質座標。 另請參閱 [**glMap2**](glmap2.md)。            |
| GL \_ List.map2 \_ 頂點 \_ 3         | 如果啟用， **glEvalCoord2**、 **glEvalMesh2** 和 **glEvalPoint2** 的呼叫會產生 *x*、 *y* 和 *z* 頂點座標。 另請參閱 **glMap2**。                                                                                                            |
| GL \_ List.map2 \_ 頂點 \_ 4         | 如果啟用， [**glEvalCoord2**](glevalcoord-functions.md)、 [**glEvalMesh2**](glevalmesh-functions.md)和 [**glEvalPoint2**](glevalpoint.md) 的呼叫會產生同質 *x*、 *y*、 *z* 和 *w* 頂點座標。 另請參閱 [**glMap2**](glmap2.md)。 |
| GL \_ 標準化               | 啟用時，以 **glNormal** 指定的一般向量會在轉換之後調整為單位長度。 請參閱 [**glNormal**](glnormal-functions.md)。                                                                                                          |
| GL \_ 點 \_ 平滑           | 若已啟用，請使用適當的篩選繪製點。 如果已停用，請繪製別名點。 請參閱 [**glPointSize**](glpointsize.md)。                                                                                                                                    |
| GL \_ 多邊形 \_ 位移 \_ 填滿   | 如果啟用，而且多邊形是以 GL \_ 填滿模式轉譯，則在執行深度比較之前，會先將位移新增至多邊形片段的深度值。 請參閱 [**glPolygonOffset**](glpolygonoffset.md)**。**                                      |
| GL \_ 多邊形 \_ 位移 \_ 線   | 如果啟用，而且多邊形是以 GL \_ 線模式轉譯，則在執行深度比較之前，會先將位移新增至多邊形片段的深度值。 請參閱 **glPolygonOffset**。                                                                 |
| GL \_ 多邊形 \_ 位移 \_ 點  | 如果啟用，則在執行深度比較之前，會將位移加入多邊形片段的深度值，如果多邊形是以 GL \_ 點模式轉譯。 請參閱 [**glPolygonOffset**](glpolygonoffset.md)。                                             |
| GL \_ 多邊形 \_ 平滑         | 如果啟用，則繪製具有適當篩選的多邊形。 如果停用，則繪製別名的多邊形。 請參閱 [**glPolygonMode**](glpolygonmode.md)。                                                                                                                            |
| GL \_ 多邊形 \_ STIPPLE        | 若已啟用，則在轉譯多邊形時使用目前的多邊形 stipple 模式。 請參閱 [**glPolygonStipple**](glpolygonstipple.md)。                                                                                                                              |
| GL \_ 剪式 \_ 測試           | 如果已啟用，則捨棄剪式矩形外部的片段。 請參閱 [**glScissor**](glscissor.md)。                                                                                                                                                   |
| GL \_ 樣板 \_ 測試           | 若已啟用，請進行樣板測試並更新樣板緩衝區。 請參閱 [**glStencilFunc**](glstencilfunc.md) 和 [**glStencilOp**](glstencilop.md)。                                                                                                            |
| GL \_ 材質 \_ 1d             | 如果啟用，則會 (執行一維紋理，除非同時啟用了二維紋理) 。 請參閱 [**glTexImage1D**](glteximage1d.md)。                                                                                                            |
| GL \_ 材質 \_ 2d             | 如果啟用，則會執行二維紋理。 請參閱 [**glTexImage2D**](glteximage2d.md)。                                                                                                                                                               |
| GL \_ 材質 \_ GEN \_ Q         | 如果啟用，則會使用以 [**glTexGen**](gltexgen-functions.md)定義的材質產生函數來計算 *q* 紋理座標。 否則，會使用目前的 *q* 紋理座標。                                                        |
| GL \_ 材質 \_ GEN \_ R         | 啟用時，會使用以 [**glTexGen**](gltexgen-functions.md)定義的材質產生函數來計算 *r* 材質座標。 如果停用，則會使用目前的 *r* 材質座標。                                                      |
| GL \_ 材質 \_ GEN \_ S         | 若已啟用，則會使用以 **glTexGen** 定義的材質產生函數來計算 *s* 材質座標。 如果停用，則會 *使用目前的* 材質座標。                                                                                |
| GL \_ 材質 \_ GEN \_ T         | 若已啟用，則會使用以 [**glTexGen**](gltexgen-functions.md)定義的材質產生函數來計算 *t* 材質座標。 如果停用，則會使用目前的 *t* 材質座標。                                                      |



 

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

[**glArrayElement**](glarrayelement.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBlendFunc**](glblendfunc.md)
</dt> <dt>

[**glClipPlane**](glclipplane.md)
</dt> <dt>

[**glColorMaterial**](glcolormaterial.md)
</dt> <dt>

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glCullFace**](glcullface.md)
</dt> <dt>

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glDepthRange**](gldepthrange.md)
</dt> <dt>

[**glDisable**](gldisable.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glEvalCoord1**](glevalcoord-functions.md)
</dt> <dt>

[**glEvalMesh1**](glevalmesh-functions.md)
</dt> <dt>

[**glEvalPoint1**](glevalpoint.md)
</dt> <dt>

[**glFog**](glfog.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> <dt>

[**glLineWidth**](gllinewidth.md)
</dt> <dt>

[**glLineStipple**](gllinestipple.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glPointSize**](glpointsize.md)
</dt> <dt>

[**glPolygonMode**](glpolygonmode.md)
</dt> <dt>

[**glPolygonStipple**](glpolygonstipple.md)
</dt> <dt>

[**glScissor**](glscissor.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> <dt>

[**glStencilOp**](glstencilop.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glTexGen**](gltexgen-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





