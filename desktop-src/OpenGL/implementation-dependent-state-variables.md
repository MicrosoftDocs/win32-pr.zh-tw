---
title: Implementation-Dependent 狀態變數
description: Implementation-Dependent 狀態變數
ms.assetid: 6778b50c-a6ac-4106-9dd6-3a123c257687
keywords:
- Implementation-Dependent 狀態變數 OpenGL
topic_type:
- apiref
api_name:
- Implementation-Dependent State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afb42c13765678218efcaf58f2b02a01d2f0e160
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022490"
---
# <a name="implementation-dependent-state-variables"></a>Implementation-Dependent 狀態變數

<dl> <dt><span id="GL_MAX_LIGHTS"></span><span id="gl_max_lights"></span>GL \_ 最大 \_ 燈光</dt> <dd> 

|                  |                                        |
|------------------|----------------------------------------|
| 描述：     | 最大光線數目               |
| 屬性群組： |                                        |
| 初始值：   | 8                                      |
| 取得命令：     | [**glGetIntegerv**](glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_CLIP_PLANES"></span><span id="gl_max_clip_planes"></span>GL \_ 最大 \_ 剪輯 \_ 平面</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 使用者裁剪平面的最大數目                                           |
| 屬性群組： |                                                                                  |
| 初始值：   | 6                                                                                |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_MODELVIEW_STACK_DEPTH"></span><span id="gl_max_modelview_stack_depth"></span>GL \_ 最大 \_ 模型 \_ 堆疊 \_ 深度</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 最大模型-矩陣堆疊深度                                             |
| 屬性群組： |                                                                                  |
| 初始值：   | 32                                                                               |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_PROJECTION_STACK_DEPTH"></span><span id="gl_max_projection_stack_depth"></span>GL \_ 最大 \_ 投射 \_ 堆疊 \_ 深度</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 最大投射矩陣堆疊深度                                            |
| 屬性群組： |                                                                                  |
| 初始值：   | 2                                                                                |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_TEXTURE_STACK_DEPTH"></span><span id="gl_max_texture_stack_depth"></span>GL \_ 最大 \_ 紋理 \_ 堆疊 \_ 深度</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 材質矩陣堆疊的深度上限                                            |
| 屬性群組： |                                                                                  |
| 初始值：   | 2                                                                                |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_SUBPIXEL_BITS"></span><span id="gl_subpixel_bits"></span>GL \_ 子圖元 \_ 位</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 以 *x*   和 *y* 表示的子圖元精確度位數                              |
| 屬性群組： |                                                                                  |
| 初始值：   | 4                                                                                |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_TEXTURE_SIZE"></span><span id="gl_max_texture_size"></span>GL \_ 最大 \_ 紋理 \_ 大小</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 材質影像的最大高度或寬度 (沒有框線)                      |
| 屬性群組： |                                                                                  |
| 初始值：   | 64                                                                               |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_PIXEL_MAP_TABLE"></span><span id="gl_max_pixel_map_table"></span>GL \_ 最大 \_ 圖元 \_ 映射 \_ 表</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | **GlPixelMap** 轉譯資料表的大小上限                               |
| 屬性群組： |                                                                                  |
| 初始值：   | 32                                                                               |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_NAME_STACK_DEPTH"></span><span id="gl_max_name_stack_depth"></span>GL \_ 最大 \_ 名稱 \_ 堆疊 \_ 深度</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 最大選取範圍-名稱堆疊深度                                               |
| 屬性群組： |                                                                                  |
| 初始值：   | 64                                                                               |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_LIST_NESTING"></span><span id="gl_max_list_nesting"></span>GL \_ 最大 \_ 清單的 \_ 嵌套</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 最大顯示清單呼叫嵌套                                                |
| 屬性群組： |                                                                                  |
| 初始值：   | 64                                                                               |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_EVAL_ORDER"></span><span id="gl_max_eval_order"></span>GL \_ 最大 \_ EVAL \_ 順序</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 最大評估工具多項式順序                                               |
| 屬性群組： |                                                                                  |
| 初始值：   | 8                                                                                |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_VIEWPORT_DIMS"></span><span id="gl_max_viewport_dims"></span>GL \_ 最大 \_ 視窗區變 \_ 暗</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 最大的視口維度                                                      |
| 屬性群組： |                                                                                  |
| 初始值：   |                                                                                  |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_ATTRIB_STACK_DEPTH"></span><span id="gl_max_attrib_stack_depth"></span>GL \_ 最大的 \_ ATTRIB \_ 堆疊 \_ 深度</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 屬性堆疊的最大深度                                             |
| 屬性群組： |                                                                                  |
| 初始值：   | 16                                                                               |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AUX_BUFFERS"></span><span id="gl_aux_buffers"></span>GL \_ AUX \_ 緩衝區</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 輔助緩衝區數目                                                      |
| 屬性群組： |                                                                                  |
| 初始值：   | 0                                                                                |
| 取得命令：     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_RGBA_MODE"></span><span id="gl_rgba_mode"></span>GL \_ RGBA \_ 模式</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 如果色彩緩衝區儲存 RGBA，則為 True                                                 |
| 屬性群組： |                                                                                  |
| 初始值：   |                                                                                  |
| 取得命令：     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_INDEX_MODE"></span><span id="gl_index_mode"></span>GL \_ 索引 \_ 模式</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 如果色彩緩衝區儲存索引，則為 True                                              |
| 屬性群組： |                                                                                  |
| 初始值：   |                                                                                  |
| 取得命令：     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DOUBLEBUFFER"></span><span id="gl_doublebuffer"></span>GL \_ DOUBLEBUFFER</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 如果有前端和背景緩衝區存在，則為 True                                             |
| 屬性群組： |                                                                                  |
| 初始值：   |                                                                                  |
| 取得命令：     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STEREO"></span><span id="gl_stereo"></span>GL \_ 身歷聲</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| 描述：     | 如果有左方和右緩衝區存在，則為 True                                           |
| 屬性群組： |                                                                                |
| 初始值：   |                                                                                |
| 取得命令：     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POINT_SIZE_RANGE"></span><span id="gl_point_size_range"></span>GL \_ 點數 \_ 大小 \_ 範圍</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| 描述：     | 範圍 (低至高) 的反鋸齒點大小                                 |
| 屬性群組： |                                                                                |
| 初始值：   | 1，1                                                                           |
| 取得命令：     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POINT_SIZE_GRANULARITY"></span><span id="gl_point_size_granularity"></span>GL \_ 點 \_ 大小 \_ 細微性</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| 描述：     | 反鋸齒點大小的資料細微性                                             |
| 屬性群組： |                                                                                |
| 初始值：   |                                                                                |
| 取得命令：     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_WIDTH_RANGE"></span><span id="gl_line_width_range"></span>GL \_ 線條 \_ 寬度 \_ 範圍</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| 描述：     | 反鋸齒線條寬度的範圍 (低至高)                                  |
| 屬性群組： |                                                                                |
| 初始值：   | 1，1                                                                           |
| 取得命令：     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_WIDTH_GRANULARITY"></span><span id="gl_line_width_granularity"></span>GL \_ 行 \_ 寬度 \_ 細微性</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| 描述：     | 反鋸齒線條寬度的資料細微性                                             |
| 屬性群組： |                                                                                |
| 初始值：   |                                                                                |
| 取得命令：     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




