---
title: 紋理狀態變數
description: 紋理狀態變數
ms.assetid: 2d9d3d8b-ecaa-412c-8105-ae2ca801784e
keywords:
- 紋理狀態變數 OpenGL
topic_type:
- apiref
api_name:
- Texturing State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7393fc6e700b028ba3783e5c78d8175e0c3fba4937bf3830d5cae8897aa0d4db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776578"
---
# <a name="texturing-state-variables"></a>紋理狀態變數

<dl> <dt><span id="GL_TEXTURE_x"></span><span id="gl_texture_x"></span><span id="GL_TEXTURE_X"></span>GL \_ 材質 \_ *x*</dt> <dd> 

| 屬性 | 值 |
|------------------|-------------------------------------------------------|
| 描述：     | 如果已啟用 *x* -d 紋理 (*x* 為 1-d 或 2-d) ，則為 True |
| 屬性群組： | 材質/啟用                                        |
| 初始值：   | GL \_ FALSE                                             |
| 取得命令：     | [**glIsEnabled**](glisenabled.md)                    |



 

</dd> <dt><span id="GL_TEXTURE"></span><span id="gl_texture"></span>GL \_ 材質</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------|
| 描述：     |  *詳細資料* 層級的立體材質影像 |
| 屬性群組： |                                              |
| 初始值：   |                                              |
| 取得命令：     | [**glGetTexImage**](glgetteximage.md)       |



 

</dd> <dt><span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span>GL \_ 材質 \_ 寬度</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------|
| 描述：     | 立體材質影像 *我* 的寬度                       |
| 屬性群組： |                                                          |
| 初始值：   | 0                                                        |
| 取得命令：     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span>GL \_ 材質 \_ 高度</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------|
| 描述：     | *x* -D 紋理影像 *我* 的高度                      |
| 屬性群組： |                                                          |
| 初始值：   | 0                                                        |
| 取得命令：     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span>GL \_ 材質 \_ 框線</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------|
| 描述：     | 立體材質影像 *i* 框線                      |
| 屬性群組： |                                                          |
| 初始值：   | 0                                                        |
| 取得命令：     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span>GL \_ 材質 \_ 元件</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------|
| 描述：     | 材質影像元件                                 |
| 屬性群組： |                                                          |
| 初始值：   | 1                                                        |
| 取得命令：     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span>GL \_ 紋理 \_ 框線 \_ 色彩</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------------------|
| 描述：     | 材質框線色彩                           |
| 屬性群組： | 紋理                                        |
| 初始值：   | 0, 0, 0, 0                                     |
| 取得命令：     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span>GL \_ 材質 \_ 最小 \_ 篩選</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------------------|
| 描述：     | 紋理縮制函式                  |
| 屬性群組： | 紋理                                        |
| 初始值：   | GL \_ 最接近 \_ MIPMAP \_ 線性                    |
| 取得命令：     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span>GL \_ 紋理 \_ MAG \_ 篩選</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------------------|
| 描述：     | 材質放大功能                 |
| 屬性群組： | 紋理                                        |
| 初始值：   | GL \_ 線性                                     |
| 取得命令：     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_WRAP__x"></span><span id="gl_texture_wrap__x"></span><span id="GL_TEXTURE_WRAP__X"></span>GL \_ 材質 \_ 換行 \_ *x*</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------------------|
| 描述：     | 材質 wrap 模式 (*x* 是 S 或 T)               |
| 屬性群組： | 紋理                                        |
| 初始值：   | GL \_ 重複                                     |
| 取得命令：     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span>GL \_ 紋理 \_ 環境 \_ 模式</dt> <dd> 

| 屬性 | 值 |
|------------------|--------------------------------------|
| 描述：     | 材質應用程式函式         |
| 屬性群組： | 紋理                              |
| 初始值：   | GL \_ LAMBERT                         |
| 取得命令：     | [**glGetTexEnviv**](glgettexenv.md) |



 

</dd> <dt><span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span>GL \_ 紋理 \_ 環境 \_ 色彩</dt> <dd> 

| 屬性 | 值 |
|------------------|--------------------------------------|
| 描述：     | 材質環境色彩            |
| 屬性群組： | 紋理                              |
| 初始值：   | 0, 0, 0, 0                           |
| 取得命令：     | [**glGetTexEnvfv**](glgettexenv.md) |



 

</dd> <dt><span id="GL_TEXTURE_GEN__x"></span><span id="gl_texture_gen__x"></span><span id="GL_TEXTURE_GEN__X"></span>GL \_ 材質 \_ GEN \_ *x*</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------------|
| 描述：     | Texgen 已啟用 (*x* 是 S、T、R 或 Q)  |
| 屬性群組： | 材質/啟用                           |
| 初始值：   | GL \_ FALSE                                |
| 取得命令：     | [**glIsEnabled**](glisenabled.md)       |



 

</dd> <dt><span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span>GL \_ 眼 \_ 平面</dt> <dd> 

| 屬性 | 值 |
|------------------|--------------------------------------|
| 描述：     | Texgen 平面方程式係數   |
| 屬性群組： | 紋理                              |
| 初始值：   |                                      |
| 取得命令：     | [**glGetTexGenfv**](glgettexgen.md) |



 

</dd> <dt><span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span>GL \_ 物件 \_ 平面</dt> <dd> 

| 屬性 | 值 |
|------------------|--------------------------------------|
| 描述：     | Texgen 物件線性係數    |
| 屬性群組： | 紋理                              |
| 初始值：   |                                      |
| 取得命令：     | [**glGetTexGenfv**](glgettexgen.md) |



 

</dd> <dt><span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span>GL \_ 材質 \_ 產生 \_ 模式</dt> <dd> 

| 屬性 | 值 |
|------------------|--------------------------------------|
| 描述：     | 用於 texgen 的函式             |
| 屬性群組： | 紋理                              |
| 初始值：   | GL \_ 眼 \_ 線性                      |
| 取得命令：     | [**glGetTexGeniv**](glgettexgen.md) |



 

</dd> </dl>

 

 




