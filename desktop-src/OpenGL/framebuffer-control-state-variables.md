---
title: 畫面格緩衝區控制項狀態變數
description: 畫面格緩衝區控制項狀態變數
ms.assetid: ab57e07d-a694-45e7-a3b3-2e856111b87d
keywords:
- 畫面格緩衝區控制項狀態變數 OpenGL
topic_type:
- apiref
api_name:
- Framebuffer Control State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 276019f790e5f4750e446cf4ae2d035e0178d0e79130100a5a5e1954cbdcb73a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061908"
---
# <a name="framebuffer-control-state-variables"></a>畫面格緩衝區控制項狀態變數

<dl> <dt><span id="GL_DRAW_BUFFER"></span><span id="gl_draw_buffer"></span>GL \_ 繪圖 \_ 緩衝區</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------|
| 描述：     | 為繪圖選取的緩衝區           |
| 屬性群組： | 色彩緩衝區                           |
| 初始值：   |                                        |
| 取得命令：     | [**glGetIntegerv**](glgetintegerv.md) |



 

</dd> <dt><span id="GL_INDEX_WRITEMASK"></span><span id="gl_index_writemask"></span>GL \_ 索引 \_ WRITEMASK</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 色彩索引 writemask                                                            |
| 屬性群組： | 色彩緩衝區                                                                     |
| 初始值：   | 1                                                                              |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_COLOR_WRITEMASK"></span><span id="gl_color_writemask"></span>GL \_ 色彩 \_ WRITEMASK</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 色彩寫入可啟用;R、G、B 或                                               |
| 屬性群組： | 色彩緩衝區                                                                     |
| 初始值：   | GL \_ TRUE                                                                         |
| 取得命令：     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_WRITEMASK"></span><span id="gl_depth_writemask"></span>GL \_ 深度 \_ WRITEMASK</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 已啟用深度緩衝區以進行寫入                                                 |
| 屬性群組： | 深度-緩衝區                                                                     |
| 初始值：   | GL \_ TRUE                                                                         |
| 取得命令：     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_WRITEMASK"></span><span id="gl_stencil_writemask"></span>GL \_ 樣板 \_ WRITEMASK</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 樣板-緩衝區 writemask                                                         |
| 屬性群組： | 樣板-緩衝區                                                                   |
| 初始值：   | 1                                                                              |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_COLOR_CLEAR_VALUE"></span><span id="gl_color_clear_value"></span>GL \_ 色彩 \_ 清除 \_ 值</dt> <dd> 

| 屬性 | 值 |
|------------------|--------------------------------------------------------------------------------|
| 描述：     | 色彩緩衝區清除值 (RGBA 模式)                                            |
| 屬性群組： | 色彩緩衝區                                                                   |
| 初始值：   | 0, 0, 0, 0                                                                     |
| 取得命令：     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_INDEX_CLEAR_VALUE"></span><span id="gl_index_clear_value"></span>GL \_ 索引 \_ 清除 \_ 值</dt> <dd> 

| 屬性 | 值 |
|------------------|--------------------------------------------------------------------------------|
| 描述：     | 色彩緩衝區清除值 (色彩索引模式)                                     |
| 屬性群組： | 色彩緩衝區                                                                   |
| 初始值：   | 0                                                                              |
| 取得命令：     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_CLEAR_VALUE"></span><span id="gl_depth_clear_value"></span>GL \_ 深度 \_ 清除 \_ 值</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 深度緩衝區清除值                                                         |
| 屬性群組： | 深度-緩衝區                                                                     |
| 初始值：   | 1                                                                                |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_CLEAR_VALUE"></span><span id="gl_stencil_clear_value"></span>GL \_ 樣板 \_ 清除 \_ 值</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 樣板-緩衝區清除值                                                       |
| 屬性群組： | 樣板-緩衝區                                                                   |
| 初始值：   | 0                                                                                |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_ACCUM_CLEAR_VALUE"></span><span id="gl_accum_clear_value"></span>GL \_ ACCUM \_ 清除 \_ 值</dt> <dd> 

| 屬性 | 值 |
|------------------|--------------------------------------------------------------------------------|
| 描述：     | 累積緩衝區清除值                                                |
| 屬性群組： | accum-緩衝區                                                                   |
| 初始值：   | 0                                                                              |
| 取得命令：     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




