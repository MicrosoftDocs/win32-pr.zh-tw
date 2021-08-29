---
title: 柵格化狀態變數
description: 柵格化狀態變數
ms.assetid: 57ce3dc0-3983-449a-bbe1-153232727ff8
keywords:
- 點陣化狀態變數 OpenGL
topic_type:
- apiref
api_name:
- Rasterization State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1586861eee26f93bca85b8c0f03e9f746e983046bbda755b67a792d65d660b53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776888"
---
# <a name="rasterization-state-variables"></a>柵格化狀態變數

<dl> <dt><span id="GL_POINT_SIZE"></span><span id="gl_point_size"></span>GL \_ 點 \_ 大小</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------|
| 描述：     | 點大小                         |
| 屬性群組： | 點                              |
| 初始值：   | 1.0                                |
| 取得命令：     | [**glGetFloatv**](glgetfloatv.md) |



 

</dd> <dt><span id="GL_POINT_SMOOTH"></span><span id="gl_point_smooth"></span>GL \_ 點 \_ 平滑</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------|
| 描述：     | 點別名                  |
| 屬性群組： | 點/啟用                       |
| 初始值：   | GL \_ FALSE                          |
| 取得命令：     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LINE_WIDTH"></span><span id="gl_line_width"></span>GL \_ 線條 \_ 寬度</dt> <dd> 

| 屬性 | 值 |
|------------------|--------------------------------------------------------------------------------|
| 描述：     | 線條寬度                                                                     |
| 屬性群組： | line                                                                           |
| 初始值：   | 1.0                                                                            |
| 取得命令：     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_SMOOTH"></span><span id="gl_line_smooth"></span>GL \_ 行 \_ 平滑</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------|
| 描述：     | 線條消除鋸齒               |
| 屬性群組： | line/enable                        |
| 初始值：   | GL \_ FALSE                          |
| 取得命令：     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LINE_STIPPLE_PATTERN"></span><span id="gl_line_stipple_pattern"></span>GL \_ 線 \_ STIPPLE \_ 模式</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 行 stipple                                                                     |
| 屬性群組： | line                                                                             |
| 初始值：   | 1                                                                              |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_STIPPLE_REPEAT"></span><span id="gl_line_stipple_repeat"></span>GL \_ 行 \_ STIPPLE \_ 重複</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 行 stipple 重複                                                              |
| 屬性群組： | line                                                                             |
| 初始值：   | 1                                                                                |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_STIPPLE"></span><span id="gl_line_stipple"></span>GL \_ 線 \_ STIPPLE</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------|
| 描述：     | 行 stipple 啟用                |
| 屬性群組： | line/enable                        |
| 初始值：   | GL \_ FALSE                          |
| 取得命令：     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_CULL_FACE"></span><span id="gl_cull_face"></span>GL \_ 精選 \_ 臉部</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------|
| 描述：     | 已啟用多邊形剔除            |
| 屬性群組： | 多邊形/啟用                     |
| 初始值：   | GL \_ FALSE                          |
| 取得命令：     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_CULL_FACE_MODE"></span><span id="gl_cull_face_mode"></span>GL \_ 精選 \_ 臉部 \_ 模式</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 挑選正面或背面的多邊形                                           |
| 屬性群組： | 多邊形                                                                          |
| 初始值：   | GL \_ 回                                                                         |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_FRONT_FACE"></span><span id="gl_front_face"></span>GL \_ 正面 \_ 臉部</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 多邊形正面臉部的 CW/CCW 指標                                              |
| 屬性群組： | 多邊形                                                                          |
| 初始值：   | GL \_ CCW                                                                          |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POLYGON_SMOOTH"></span><span id="gl_polygon_smooth"></span>GL \_ 多邊形 \_ 平滑</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------|
| 描述：     | 多邊形消除鋸齒            |
| 屬性群組： | 多邊形/啟用                     |
| 初始值：   | GL \_ FALSE                          |
| 取得命令：     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_POLYGON_MODE"></span><span id="gl_polygon_mode"></span>GL \_ 多邊形 \_ 模式</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 多邊形的光柵模式 (front 和 back)                                       |
| 屬性群組： | 多邊形                                                                          |
| 初始值：   | GL \_ 填滿                                                                         |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POLYGON_STIPPLE"></span><span id="gl_polygon_stipple"></span>GL \_ 多邊形 \_ STIPPLE</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------|
| 描述：     | 多邊形 stipple 啟用             |
| 屬性群組： | 多邊形/啟用                     |
| 初始值：   | GL \_ FALSE                          |
| 取得命令：     | [**glIsEnabled**](glisenabled.md) |



 



| 屬性 | 值 |
|------------------|----------------------------------------------------|
| 描述：     | 多邊形 stipple 模式                            |
| 屬性群組： | 多邊形-stipple                                    |
| 初始值：   | 1                                                |
| 取得命令：     | [**glGetPolygonStipple**](glgetpolygonstipple.md) |



 

</dd> </dl>

 

 




