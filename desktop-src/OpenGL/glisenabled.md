---
title: 'glIsEnabled 函式 (Gl) '
description: GllsEnabled 函式會測試功能是否已啟用。
ms.assetid: 18df5a6f-dc21-434d-a2e8-2c58597df037
keywords:
- glIsEnabled 函式 OpenGL
topic_type:
- apiref
api_name:
- glIsEnabled
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fdb2ba206e0a026aef118b06d66097ade9ba9ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686314"
---
# <a name="glisenabled-function"></a>glIsEnabled 函式

**GllsEnabled** 函式會測試功能是否已啟用。

## <a name="syntax"></a>語法


```C++
GLboolean WINAPI glIsEnabled(
   GLenum cap
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*帽* 
</dt> <dd>

表示 OpenGL 功能的符號常數。 接受下列功能。



| 值                                                                                                                                                                                                    | 意義                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span><dl> <dt>**GL \_ ALPHA \_ 測試**</dt> </dl>                                           | 請參閱 [ **glAlphaFunc**](glalphafunc.md)<br/>                                                                                                   |
| <span id="GL_AUTO_NORMAL"></span><span id="gl_auto_normal"></span><dl> <dt>**GL \_ 自動 \_ 正常**</dt> </dl>                                        | 請參閱 [ **glEvalCoord**](glevalcoord-functions.md)<br/>                                                                                         |
| <span id="GL_BLEND"></span><span id="gl_blend"></span><dl> <dt>**GL \_ BLEND**</dt> </dl>                                                           | 請參閱 [ **glBlendFunc**](glblendfunc.md)<br/>                                                                                                   |
| <span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span><dl> <dt>* * GL \_ 剪輯 \_ 平面 * i * * *</dt> </dl> | 請參閱 [ **glClipPlane**](glclipplane.md)<br/>                                                                                                   |
| <span id="GL_COLOR_ARRAY"></span><span id="gl_color_array"></span><dl> <dt>**GL \_ 色彩 \_ 陣列**</dt> </dl>                                        | 請參閱 [ **glColorPointer**](glcolorpointer.md)<br/>                                                                                             |
| <span id="GL_COLOR_LOGIC_OP"></span><span id="gl_color_logic_op"></span><dl> <dt>**GL \_ 色彩 \_ 邏輯 \_ OP**</dt> </dl>                              | 請參閱 [ **glLogicOp**](gllogicop.md)<br/>                                                                                                       |
| <span id="GL_COLOR_MATERIAL"></span><span id="gl_color_material"></span><dl> <dt>**GL \_ 色彩 \_ 材質**</dt> </dl>                               | 請參閱 [ **glColorMaterial**](glcolormaterial.md)<br/>                                                                                           |
| <span id="GL_CULL_FACE"></span><span id="gl_cull_face"></span><dl> <dt>**GL \_ 精選 \_ 臉部**</dt> </dl>                                              | 請參閱 [ **glCullFace**](glcullface.md)<br/>                                                                                                     |
| <span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span><dl> <dt>**GL \_ 深度 \_ 測試**</dt> </dl>                                           | 請參閱 [**glDepthFunc**](gldepthfunc.md) 和 [**glDepthRange**](gldepthrange.md)<br/>                                                          |
| <span id="GL_DITHER"></span><span id="gl_dither"></span><dl> <dt>**GL \_ 遞色**</dt> </dl>                                                        | 請參閱 [ **glEnable**](glenable.md)<br/>                                                                                                         |
| <span id="GL_FOG"></span><span id="gl_fog"></span><dl> <dt>**GL \_ 霧化**</dt> </dl>                                                                 | 請參閱 [ **glFog**](glfog.md)<br/>                                                                                                               |
| <span id="GL_INDEX_ARRAY"></span><span id="gl_index_array"></span><dl> <dt>**GL \_ 索引 \_ 陣列**</dt> </dl>                                        | 請參閱 [ **glIndexPointer**](glindexpointer.md)<br/>                                                                                             |
| <span id="GL_INDEX_LOGIC_OP"></span><span id="gl_index_logic_op"></span><dl> <dt>**GL \_ 索引 \_ 邏輯 \_ OP**</dt> </dl>                              | 請參閱 [ **glLogicOp**](gllogicop.md)<br/>                                                                                                       |
| <span id="GL_LIGHT_i"></span><span id="gl_light_i"></span><span id="GL_LIGHT_I"></span><dl> <dt>* * GL \_ 燈 * i * * *</dt> </dl>                      | 請參閱 [**glLightModel**](gllightmodel-functions.md) 和 [**glLight**](gllight-functions.md)<br/>                                              |
| <span id="GL_LIGHTING"></span><span id="gl_lighting"></span><dl> <dt>**GL \_ 照明**</dt> </dl>                                                  | 請參閱 [**glMaterial**](glmaterial-functions.md)、 [**glLightModel**](gllightmodel-functions.md)和 [**glLight**](gllight-functions.md)<br/> |
| <span id="GL_LINE_SMOOTH"></span><span id="gl_line_smooth"></span><dl> <dt>**GL \_ 行 \_ 平滑**</dt> </dl>                                        | 請參閱 [ **glLineWidth**](gllinewidth.md)<br/>                                                                                                   |
| <span id="GL_LINE_STIPPLE"></span><span id="gl_line_stipple"></span><dl> <dt>**GL \_ 線 \_ STIPPLE**</dt> </dl>                                     | 請參閱 [ **glLineStipple**](gllinestipple.md)<br/>                                                                                               |
| <span id="GL_MAP1_COLOR_4"></span><span id="gl_map1_color_4"></span><dl> <dt>**GL \_ MAP1 \_ 色彩 \_ 4**</dt> </dl>                                    | 請參閱 [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_INDEX"></span><span id="gl_map1_index"></span><dl> <dt>**GL \_ MAP1 \_ 索引**</dt> </dl>                                           | 請參閱 [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_NORMAL"></span><span id="gl_map1_normal"></span><dl> <dt>**GL \_ MAP1 \_ 正常**</dt> </dl>                                        | 請參閱 [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_TEXTURE_COORD_1"></span><span id="gl_map1_texture_coord_1"></span><dl> <dt>**GL \_ MAP1 \_ 材質 \_ COORD \_ 1**</dt> </dl>           | 請參閱 [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_TEXTURE_COORD_2"></span><span id="gl_map1_texture_coord_2"></span><dl> <dt>**GL \_ MAP1 \_ 材質 \_ COORD \_ 2**</dt> </dl>           | 請參閱 [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_TEXTURE_COORD_3"></span><span id="gl_map1_texture_coord_3"></span><dl> <dt>**GL \_ MAP1 \_ 材質 \_ COORD \_ 3**</dt> </dl>           | 請參閱 [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_TEXTURE_COORD_4"></span><span id="gl_map1_texture_coord_4"></span><dl> <dt>**GL \_ MAP1 \_ 材質 \_ COORD \_ 4**</dt> </dl>           | 請參閱 [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_VERTEX_3"></span><span id="gl_map1_vertex_3"></span><dl> <dt>**GL \_ MAP1 \_ 頂點 \_ 3**</dt> </dl>                                 | 請參閱 [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_VERTEX_4"></span><span id="gl_map1_vertex_4"></span><dl> <dt>**GL \_ MAP1 \_ 頂點 \_ 4**</dt> </dl>                                 | 請參閱 [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP2_COLOR_4"></span><span id="gl_map2_color_4"></span><dl> <dt>**GL \_ List.map2 \_ 色彩 \_ 4**</dt> </dl>                                    | 請參閱 [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_INDEX"></span><span id="gl_map2_index"></span><dl> <dt>**GL \_ List.map2 \_ 索引**</dt> </dl>                                           | 請參閱 [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_NORMAL"></span><span id="gl_map2_normal"></span><dl> <dt>**GL \_ List.map2 \_ 正常**</dt> </dl>                                        | 請參閱 [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_TEXTURE_COORD_1"></span><span id="gl_map2_texture_coord_1"></span><dl> <dt>**GL \_ List.map2 \_ 材質 \_ COORD \_ 1**</dt> </dl>           | 請參閱 [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_TEXTURE_COORD_2"></span><span id="gl_map2_texture_coord_2"></span><dl> <dt>**GL \_ List.map2 \_ 材質 \_ COORD \_ 2**</dt> </dl>           | 請參閱 [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_TEXTURE_COORD_3"></span><span id="gl_map2_texture_coord_3"></span><dl> <dt>**GL \_ List.map2 \_ 材質 \_ COORD \_ 3**</dt> </dl>           | 請參閱 [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_TEXTURE_COORD_4"></span><span id="gl_map2_texture_coord_4"></span><dl> <dt>**GL \_ List.map2 \_ 材質 \_ COORD \_ 4**</dt> </dl>           | 請參閱 [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_VERTEX_3"></span><span id="gl_map2_vertex_3"></span><dl> <dt>**GL \_ List.map2 \_ 頂點 \_ 3**</dt> </dl>                                 | 請參閱 [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_VERTEX_4"></span><span id="gl_map2_vertex_4"></span><dl> <dt>**GL \_ List.map2 \_ 頂點 \_ 4**</dt> </dl>                                 | 請參閱 [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_NORMAL_ARRAY"></span><span id="gl_normal_array"></span><dl> <dt>**GL \_ 標準 \_ 陣列**</dt> </dl>                                     | 請參閱 [ **glNormalPointer**](glnormalpointer.md)<br/>                                                                                           |
| <span id="GL_NORMALIZE"></span><span id="gl_normalize"></span><dl> <dt>**GL \_ 標準化**</dt> </dl>                                               | 請參閱 [ **glNormal**](glnormal-functions.md)<br/>                                                                                               |
| <span id="GL_POINT_SMOOTH"></span><span id="gl_point_smooth"></span><dl> <dt>**GL \_ 點 \_ 平滑**</dt> </dl>                                     | 請參閱 [ **glPointSize**](glpointsize.md)<br/>                                                                                                   |
| <span id="GL_POLYGON_OFFSET_FILL"></span><span id="gl_polygon_offset_fill"></span><dl> <dt>**GL \_ 多邊形 \_ 位移 \_ 填滿**</dt> </dl>               | 請參閱 [ **glPolygonOffset**](glpolygonoffset.md)<br/>                                                                                           |
| <span id="GL_POLYGON_OFFSET_LINE"></span><span id="gl_polygon_offset_line"></span><dl> <dt>**GL \_ 多邊形 \_ 位移 \_ 線**</dt> </dl>               | 請參閱 [ **glPolygonOffset**](glpolygonoffset.md)<br/>                                                                                           |
| <span id="GL_POLYGON_OFFSET_POINT"></span><span id="gl_polygon_offset_point"></span><dl> <dt>**GL \_ 多邊形 \_ 位移 \_ 點**</dt> </dl>            | 請參閱 [ **glPolygonOffset**](glpolygonoffset.md)<br/>                                                                                           |
| <span id="GL_POLYGON_SMOOTH"></span><span id="gl_polygon_smooth"></span><dl> <dt>**GL \_ 多邊形 \_ 平滑**</dt> </dl>                               | 請參閱 [ **glPolygonMode**](glpolygonmode.md)<br/>                                                                                               |
| <span id="GL_POLYGON_STIPPLE"></span><span id="gl_polygon_stipple"></span><dl> <dt>**GL \_ 多邊形 \_ STIPPLE**</dt> </dl>                            | 請參閱 [ **glPolygonStipple**](glpolygonstipple.md)<br/>                                                                                         |
| <span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span><dl> <dt>**GL \_ 剪式 \_ 測試**</dt> </dl>                                     | 請參閱 [ **glScissor**](glscissor.md)<br/>                                                                                                       |
| <span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span><dl> <dt>**GL \_ 樣板 \_ 測試**</dt> </dl>                                     | 請參閱 [**glStencilFunc**](glstencilfunc.md) 和 [**glStencilOp**](glstencilop.md)<br/>                                                        |
| <span id="GL_TEXTURE_1D"></span><span id="gl_texture_1d"></span><dl> <dt>**GL \_ 材質 \_ 1d**</dt> </dl>                                           | 請參閱 [ **glTexImage1D**](glteximage1d.md)<br/>                                                                                                 |
| <span id="GL_TEXTURE_2D"></span><span id="gl_texture_2d"></span><dl> <dt>**GL \_ 材質 \_ 2d**</dt> </dl>                                           | 請參閱 [ **glTexImage2D**](glteximage2d.md)<br/>                                                                                                 |
| <span id="GL_TEXTURE_COORD_ARRAY"></span><span id="gl_texture_coord_array"></span><dl> <dt>**GL \_ 紋理 \_ COORD \_ 陣列**</dt> </dl>               | 請參閱 [ **glTexCoordPointer**](gltexcoordpointer.md)<br/>                                                                                       |
| <span id="GL_TEXTURE_GEN_Q"></span><span id="gl_texture_gen_q"></span><dl> <dt>**GL \_ 材質 \_ GEN \_ Q**</dt> </dl>                                 | 請參閱 [ **glTexGen**](gltexgen-functions.md)<br/>                                                                                               |
| <span id="GL_TEXTURE_GEN_R"></span><span id="gl_texture_gen_r"></span><dl> <dt>**GL \_ 材質 \_ GEN \_ R**</dt> </dl>                                 | 請參閱 [ **glTexGen**](gltexgen-functions.md)<br/>                                                                                               |
| <span id="GL_TEXTURE_GEN_S"></span><span id="gl_texture_gen_s"></span><dl> <dt>**GL \_ 材質 \_ GEN \_ S**</dt> </dl>                                 | 請參閱 [ **glTexGen**](gltexgen-functions.md)<br/>                                                                                               |
| <span id="GL_TEXTURE_GEN_T"></span><span id="gl_texture_gen_t"></span><dl> <dt>**GL \_ 材質 \_ GEN \_ T**</dt> </dl>                                 | 請參閱 [ **glTexGen**](gltexgen-functions.md)<br/>                                                                                               |
| <span id="GL_VERTEX_ARRAY"></span><span id="gl_vertex_array"></span><dl> <dt>**GL \_ 頂點 \_ 陣列**</dt> </dl>                                     | 請參閱 [ **glVertexPointer**](glvertexpointer.md)<br/>                                                                                           |



 

</dd> </dl>

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *端點* 不是可接受的值。<br/>                                                                                           |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

 \_ 如果 *端點* 是啟用的功能，GLLSENABLED 函式會傳回 gl TRUE，否則會傳回 gl \_ FALSE。

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

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





