---
title: 轉換狀態變數
description: 轉換狀態變數
ms.assetid: 3a6be5ac-ac7a-4c3e-8b65-0404849ae67c
keywords:
- 轉換狀態變數 OpenGL
topic_type:
- apiref
api_name:
- Transformation State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c79b4363419d97a64184dd2408a9f6221ada52adc49adbb28eb3d049a4b2a36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011916"
---
# <a name="transformation-state-variables"></a>轉換狀態變數

<dl> <dt><span id="GL_MODELVIEW_MATRIX"></span><span id="gl_modelview_matrix"></span>GL \_ 模型 \_ 矩陣</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------|
| 描述：     | 模型矩陣堆疊             |
| 屬性群組： |                                    |
| 初始值：   | 身分識別                           |
| 取得命令：     | [**glGetFloatv**](glgetfloatv.md) |



 

</dd> <dt><span id="GL_PROJECTION_MATRIX"></span><span id="gl_projection_matrix"></span>GL \_ 投射 \_ 矩陣</dt> <dd> 

| 屬性 | 值 |
|------------------|--------------------------------------------------------------------------------|
| 描述：     | 投射矩陣堆疊                                                        |
| 屬性群組： |                                                                                |
| 初始值：   | 身分識別                                                                       |
| 取得命令：     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_TEXTURE_MATRIX"></span><span id="gl_texture_matrix"></span>GL \_ 材質 \_ 矩陣</dt> <dd> 

| 屬性 | 值 |
|------------------|--------------------------------------------------------------------------------|
| 描述：     | 材質矩陣堆疊                                                           |
| 屬性群組： |                                                                                |
| 初始值：   | 身分識別                                                                       |
| 取得命令：     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_VIEWPORT"></span><span id="gl_viewport"></span>GL \_ 區</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 視口原點和範圍                                                       |
| 屬性群組： | Viewport - 檢視區                                                                         |
| 初始值：   |                                                                                  |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_RANGE"></span><span id="gl_depth_range"></span>GL \_ 深度 \_ 範圍</dt> <dd> 

| 屬性 | 值 |
|------------------|--------------------------------------------------------------------------------|
| 描述：     | 深度範圍接近或遠                                                       |
| 屬性群組： | Viewport - 檢視區                                                                       |
| 初始值：   | 0、1                                                                           |
| 取得命令：     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MODELVIEW_STACK_DEPTH"></span><span id="gl_modelview_stack_depth"></span>GL \_ 模型 \_ 堆疊 \_ 深度</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 模型矩陣堆疊指標                                                   |
| 屬性群組： |                                                                                  |
| 初始值：   | 1                                                                                |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_PROJECTION_STACK_DEPTH"></span><span id="gl_projection_stack_depth"></span>GL \_ 投射 \_ 堆疊 \_ 深度</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 投射矩陣堆疊指標                                                  |
| 屬性群組： |                                                                                  |
| 初始值：   | 1                                                                                |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_TEXTURE_STACK_DEPTH"></span><span id="gl_texture_stack_depth"></span>GL \_ 紋理 \_ 堆疊 \_ 深度</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 材質矩陣堆疊指標                                                     |
| 屬性群組： |                                                                                  |
| 初始值：   | 1                                                                                |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MATRIX_MODE"></span><span id="gl_matrix_mode"></span>GL \_ 矩陣 \_ 模式</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 目前的矩陣模式                                                              |
| 屬性群組： | Transform - 轉換                                                                        |
| 初始值：   | GL \_ 模型                                                                    |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_NORMALIZE"></span><span id="gl_normalize"></span>GL \_ 標準化</dt> <dd> 

| 屬性 | 值 |
|------------------|-------------------------------------|
| 描述：     | 目前的一般正規化開啟/關閉 |
| 屬性群組： | 轉換/啟用                    |
| 初始值：   | GL \_ FALSE                           |
| 取得命令：     | [**glIsEnabled**](glisenabled.md)  |



 

</dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL \_ 剪輯 \_ 平面 *i*</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------------|
| 描述：     | 使用者裁剪平面係數         |
| 屬性群組： | Transform - 轉換                                |
| 初始值：   | 0, 0, 0, 0                               |
| 取得命令：     | [**glGetClipPlane**](glgetclipplane.md) |



 

</dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL \_ 剪輯 \_ 平面 *i*</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------|
| 描述：     | *我* 已啟用使用者裁剪平面 |
| 屬性群組： | 轉換/啟用                   |
| 初始值：   | GL \_ FALSE                          |
| 取得命令：     | [**glIsEnabled**](glisenabled.md) |



 

</dd> </dl>

 

 




