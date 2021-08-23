---
title: 著色狀態變數
description: 著色狀態變數
ms.assetid: 783a798a-f45c-4262-99b8-badd15f52cd5
keywords:
- 著色狀態變數 OpenGL
topic_type:
- apiref
api_name:
- Coloring State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fafcd3400df351ac9dd8f50a1b4c4fb31f5a1ef14924f55588d3b9b1866c65a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063288"
---
# <a name="coloring-state-variables"></a>著色狀態變數

<dl> <dt><span id="GL_FOG_COLOR"></span><span id="gl_fog_color"></span>GL \_ 霧化 \_ 色彩</dt> <dd> 

| 屬性 | 值 |
|------------------|--------------------------------------------------------------------------------|
| 描述：     | 霧化色彩                                                                      |
| 屬性群組： | 霧                                                                            |
| 初始值：   | 0、0、0、0                                                                        |
| 取得命令：     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_FOG_INDEX"></span><span id="gl_fog_index"></span>GL \_ 霧化 \_ 索引</dt> <dd> 

| 屬性 | 值 |
|------------------|--------------------------------------------------------------------------------|
| 描述：     | 霧化索引                                                                      |
| 屬性群組： | 霧                                                                            |
| 初始值：   | 0                                                                              |
| 取得命令：     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_FOG_DENSITY"></span><span id="gl_fog_density"></span>GL \_ 霧化 \_ 密度</dt> <dd> 

| 屬性 | 值 |
|------------------|--------------------------------------------------------------------------------|
| 描述：     | 指數霧化密度                                                        |
| 屬性群組： | 霧                                                                            |
| 初始值：   | 1.0                                                                            |
| 取得命令：     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_FOG_START"></span><span id="gl_fog_start"></span>GL \_ 霧化 \_ 開始</dt> <dd> 

| 屬性 | 值 |
|------------------|--------------------------------------------------------------------------------|
| 描述：     | 線性霧化開始                                                               |
| 屬性群組： | 霧                                                                            |
| 初始值：   | 0.0                                                                            |
| 取得命令：     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_FOG_END"></span><span id="gl_fog_end"></span>GL \_ 霧化 \_ 結束</dt> <dd> 

| 屬性 | 值 |
|------------------|--------------------------------------------------------------------------------|
| 描述：     | 線性霧化結束                                                                 |
| 屬性群組： | 霧                                                                            |
| 初始值：   | 1.0                                                                            |
| 取得命令：     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_FOG_MODE"></span><span id="gl_fog_mode"></span>GL \_ 霧化 \_ 模式</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 霧化模式                                                                         |
| 屬性群組： | 霧                                                                              |
| 初始值：   | GL \_ EXP                                                                          |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_FOG"></span><span id="gl_fog"></span>GL \_ 霧化</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------|
| 描述：     | 如果已啟用霧化則為 True                |
| 屬性群組： | 霧化/啟用                         |
| 初始值：   | GL \_ FALSE                          |
| 取得命令：     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_SHADE_MODEL"></span><span id="gl_shade_model"></span>GL \_ 陰影 \_ 模型</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | **glShadeModel** 設定                                                         |
| 屬性群組： | 光源                                                                         |
| 初始值：   | GL \_ 平滑                                                                       |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




