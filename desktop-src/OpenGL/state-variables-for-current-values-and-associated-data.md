---
title: 目前值和相關資料的狀態變數
description: 目前值和相關資料的狀態變數
ms.assetid: 8e47b119-a065-43c5-b7f5-76deaf975ad8
keywords:
- 目前值和相關聯資料 OpenGL 的狀態變數
topic_type:
- apiref
api_name:
- State Variables for Current Values and Associated Data
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 149139bc11698469ce0667c2ecf77bc7ab239adb
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908466"
---
# <a name="state-variables-for-current-values-and-associated-data"></a>目前值和相關資料的狀態變數

<dl> <dt><span id="GL_CURRENT_COLOR"></span><span id="gl_current_color"></span>GL \_ 目前 \_ 色彩</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------------------------------------------|
| 描述：     | 目前的色彩                                                                                                        |
| 屬性群組： | 目前的                                                                                                              |
| 初始值：   | 1，1，1，1                                                                                                           |
| 取得命令：     | [**glGetIntegerv**](glgetintegerv.md)[**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_INDEX"></span><span id="gl_current_index"></span>GL \_ 目前 \_ 索引</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述：     | 目前的色彩索引                                                                                                                                            |
| 屬性群組： | 目前的                                                                                                                                                        |
| 初始值：   | 1                                                                                                                                                              |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)[**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_TEXTURE_COORDS"></span><span id="gl_current_texture_coords"></span>GL \_ 目前 \_ 紋理 \_ COORDS</dt> <dd> 

| 屬性 | 值 |
|------------------|--------------------------------------------------------------------------------|
| 描述：     | 目前的材質座標                                                    |
| 屬性群組： | 目前的                                                                        |
| 初始值：   | 0、0、0、1                                                                     |
| 取得命令：     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_NORMAL"></span><span id="gl_current_normal"></span>GL \_ 目前 \_ 正常</dt> <dd> 

| 屬性 | 值 |
|------------------|--------------------------------------------------------------------------------|
| 描述：     | 目前的一般                                                                 |
| 屬性群組： | 目前的                                                                        |
| 初始值：   | 0、0、1                                                                        |
| 取得命令：     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_POSITION"></span><span id="gl_current_raster_position"></span>GL \_ 目前的 \_ 點陣位置</dt> <dd> 

| 屬性 | 值 |
|------------------|--------------------------------------------------------------------------------|
| 描述：     | 目前的點陣位置                                                        |
| 屬性群組： | 目前的                                                                        |
| 初始值：   | 0、0、0、1                                                                     |
| 取得命令：     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_DISTANCE"></span><span id="gl_current_raster_distance"></span>GL \_ 目前的 \_ 點陣 \_ 距離</dt> <dd> 

| 屬性 | 值 |
|------------------|--------------------------------------------------------------------------------|
| 描述：     | 目前的點陣距離                                                        |
| 屬性群組： | 目前的                                                                        |
| 初始值：   | 0                                                                              |
| 取得命令：     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_COLOR"></span><span id="gl_current_raster_color"></span>GL \_ 目前的 \_ 點陣 \_ 色彩</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述：     | 與點陣定位相關聯的色彩                                                                                                                          |
| 屬性群組： | 目前的                                                                                                                                                        |
| 初始值：   | 1，1，1，1                                                                                                                                                     |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)[**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_INDEX"></span><span id="gl_current_raster_index"></span>GL \_ 目前的 \_ 點陣 \_ 索引</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 描述：     | 與點陣位置相關聯的色彩索引                                                                                                                    |
| 屬性群組： | 目前的                                                                                                                                                        |
| 初始值：   | 1                                                                                                                                                              |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)[**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_TEXTURE_COORDS"></span><span id="gl_current_raster_texture_coords"></span>GL \_ 目前的 \_ 點陣 \_ 紋理 \_ COORDS</dt> <dd> 

| 屬性 | 值 |
|------------------|--------------------------------------------------------------------------------|
| 描述：     | 與點陣位置相關聯的材質座標                            |
| 屬性群組： | 目前的                                                                        |
| 初始值：   | 0、0、0、1                                                                     |
| 取得命令：     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_POSITION_VALID"></span><span id="gl_current_raster_position_valid"></span>GL \_ 目前的目前 \_ 點陣 \_ 位置 \_ 有效</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 點陣位置有效位                                                        |
| 屬性群組： | 目前的                                                                          |
| 初始值：   | GL \_ TRUE                                                                         |
| 取得命令：     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_EDGE_FLAG"></span><span id="gl_edge_flag"></span>GL \_ EDGE \_ 旗標</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 邊緣旗標                                                                        |
| 屬性群組： | 目前的                                                                          |
| 初始值：   | GL \_ TRUE                                                                         |
| 取得命令：     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




