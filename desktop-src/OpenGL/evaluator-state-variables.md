---
title: 評估工具狀態變數
description: 評估工具狀態變數
ms.assetid: e7d710be-de17-46a0-8ad8-0f65b943ece8
keywords:
- 評估工具狀態變數 OpenGL
topic_type:
- apiref
api_name:
- Evaluator State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 615e7cde4a8f82c3f4a9a95791912c5dc3f77ff3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103932704"
---
# <a name="evaluator-state-variables"></a>評估工具狀態變數

<dl> <dt><span id="GL_ORDER"></span><span id="gl_order"></span>GL \_ 訂單</dt> <dd> 

|                  |                                |
|------------------|--------------------------------|
| 描述：     | 1-d 地圖順序                  |
| 屬性群組： |                                |
| 初始值：   | 1                              |
| 取得命令：     | [**glGetMapiv**](glgetmap.md) |



 

</dd> <dt><span id="GL_ORDER"></span><span id="gl_order"></span>GL \_ 訂單</dt> <dd> 

|                  |                                |
|------------------|--------------------------------|
| 描述：     | 2-d 地圖訂單                 |
| 屬性群組： |                                |
| 初始值：   | 1，1                            |
| 取得命令：     | [**glGetMapiv**](glgetmap.md) |



 

</dd> <dt><span id="GL_COEFF"></span><span id="gl_coeff"></span>GL \_ COEFF</dt> <dd> 

|                  |                                |
|------------------|--------------------------------|
| 描述：     | 1-d 控制點             |
| 屬性群組： |                                |
| 初始值：   |                                |
| 取得命令：     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_COEFF"></span><span id="gl_coeff"></span>GL \_ COEFF</dt> <dd> 

|                  |                                |
|------------------|--------------------------------|
| 描述：     | 2d 控制點             |
| 屬性群組： |                                |
| 初始值：   |                                |
| 取得命令：     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_DOMAIN"></span><span id="gl_domain"></span>GL \_ 網域</dt> <dd> 

|                  |                                |
|------------------|--------------------------------|
| 描述：     | 立體網域端點           |
| 屬性群組： |                                |
| 初始值：   |                                |
| 取得命令：     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_DOMAIN"></span><span id="gl_domain"></span>GL \_ 網域</dt> <dd> 

|                  |                                |
|------------------|--------------------------------|
| 描述：     | 2-d 網域端點           |
| 屬性群組： |                                |
| 初始值：   |                                |
| 取得命令：     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_MAP1_x"></span><span id="gl_map1_x"></span><span id="GL_MAP1_X"></span>GL \_ MAP1 \_ x</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| 描述：     | 立體地圖啟用： *x* 是地圖類型   |
| 屬性群組： | eval/enable                        |
| 初始值：   | GL \_ FALSE                          |
| 取得命令：     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_MAP2_x"></span><span id="gl_map2_x"></span><span id="GL_MAP2_X"></span>GL \_ list.map2 \_ x</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| 描述：     | 2d 地圖啟用： *x* 是地圖類型   |
| 屬性群組： | eval/enable                        |
| 初始值：   | GL \_ FALSE                          |
| 取得命令：     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_MAP1_GRID_DOMAIN"></span><span id="gl_map1_grid_domain"></span>GL \_ MAP1 \_ 方格 \_ 網域</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| 描述：     | 立體方格端點                                                             |
| 屬性群組： | eval                                                                           |
| 初始值：   | 0、1                                                                            |
| 取得命令：     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAP2_GRID_DOMAIN"></span><span id="gl_map2_grid_domain"></span>GL \_ List.map2 \_ 方格 \_ 網域</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| 描述：     | 2d 格線端點                                                             |
| 屬性群組： | eval                                                                           |
| 初始值：   | 0、1、0、1                                                                     |
| 取得命令：     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAP1_GRID_SEGMENTS"></span><span id="gl_map1_grid_segments"></span>GL \_ MAP1 \_ 方格 \_ 區段</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| 描述：     | 立體格線片段                 |
| 屬性群組： | eval                               |
| 初始值：   | 1                                  |
| 取得命令：     | [**glGetFloatv**](glgetfloatv.md) |



 

</dd> <dt><span id="GL_MAP1_GRID_SEGMENTS"></span><span id="gl_map1_grid_segments"></span>GL \_ MAP1 \_ 方格 \_ 區段</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| 描述：     | 2d 方格區段                                                              |
| 屬性群組： | eval                                                                           |
| 初始值：   | 1，1                                                                           |
| 取得命令：     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AUTO_NORMAL"></span><span id="gl_auto_normal"></span>GL \_ 自動 \_ 正常</dt> <dd> 

|                  |                                             |
|------------------|---------------------------------------------|
| 描述：     | 如果已啟用自動一般產生，則為 True |
| 屬性群組： | eval                                        |
| 初始值：   | GL \_ FALSE                                   |
| 取得命令：     | [**glIsEnabled**](glisenabled.md)          |



 

</dd> </dl>

 

 




