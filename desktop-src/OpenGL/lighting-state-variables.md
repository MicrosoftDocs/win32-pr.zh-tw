---
title: 光源狀態變數
description: 光源狀態變數
ms.assetid: a9fb1e22-5e33-4b46-9c3b-2f64de5dd646
keywords:
- 燈光狀態變數 OpenGL
topic_type:
- apiref
api_name:
- Lighting State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c5a2d029727f4ff4a9eee353230e0843a39f082
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909846"
---
# <a name="lighting-state-variables"></a>光源狀態變數

<dl> <dt><span id="GL_LIGHTING"></span><span id="gl_lighting"></span>GL \_ 照明</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------|
| 描述：     | 如果已啟用光源則為 True        |
| 屬性群組： | 光源/啟用                    |
| 初始值：   | GL \_ FALSE                          |
| 取得命令：     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_COLOR_MATERIAL"></span><span id="gl_color_material"></span>GL \_ 色彩 \_ 材質</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------|
| 描述：     | 如果已啟用色彩追蹤，則為 True  |
| 屬性群組： | 光源                           |
| 初始值：   | GL \_ FALSE                          |
| 取得命令：     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_COLOR_MATERIAL_PARAMETER"></span><span id="gl_color_material_parameter"></span>GL \_ 色彩 \_ 材質 \_ 參數</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 材質屬性追蹤目前的色彩                                       |
| 屬性群組： | 光源                                                                         |
| 初始值：   | GL \_ 環境 \_ 和 \_ 擴散                                                        |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_COLOR_MATERIAL_FACE"></span><span id="gl_color_material_face"></span>GL \_ 色 \_ 材質 \_ 臉部</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 受色彩追蹤影響的臉部                                                 |
| 屬性群組： | 光源                                                                         |
| 初始值：   | GL \_ 正面 \_ 和 \_ 背面                                                             |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>GL \_ 環境</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------------|
| 描述：     | 環境材質色彩                   |
| 屬性群組： | 光源                                 |
| 初始值：   |  (0.2、0.2、0.2、1.0)                         |
| 取得命令：     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL \_ 擴散</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------------|
| 描述：     | 擴散材質色彩                   |
| 屬性群組： | 光源                                 |
| 初始值：   |  (0.8、0.8、0.8、1.0)                         |
| 取得命令：     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>GL \_ 反射</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------------|
| 描述：     | 反射材質色彩                  |
| 屬性群組： | 光源                                 |
| 初始值：   |  (0.0、0.0、0.0、1.0)                         |
| 取得命令：     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_EMISSION"></span><span id="gl_emission"></span>GL \_ 排放</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------------|
| 描述：     | 放射材質色彩                  |
| 屬性群組： | 光源                                 |
| 初始值：   |  (0.0、0.0、0.0、1.0)                         |
| 取得命令：     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_SHININESS"></span><span id="gl_shininess"></span>GL \_ 反光</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------------|
| 描述：     | 材質的反射指數            |
| 屬性群組： | 光源                                 |
| 初始值：   | 0.0                                      |
| 取得命令：     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span>GL \_ LIGHT \_ 模型 \_ 環境</dt> <dd> 

| 屬性 | 值 |
|------------------|--------------------------------------------------------------------------------|
| 描述：     | 環境場景色彩                                                            |
| 屬性群組： | 光源                                                                       |
| 初始值：   |  (0.2、0.2、0.2、1.0)                                                               |
| 取得命令：     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span>GL \_ 光 \_ 模型 \_ 本機 \_ 檢視器</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 檢視器為本機                                                                  |
| 屬性群組： | 光源                                                                         |
| 初始值：   | GL \_ FALSE                                                                        |
| 取得命令：     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span>GL \_ 燈 \_ 模型 \_ 二 \_ 邊</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 使用雙面光源                                                           |
| 屬性群組： | 光源                                                                         |
| 初始值：   | GL \_ FALSE                                                                        |
| 取得命令：     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>GL \_ 環境</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------|
| 描述：     | Light *i* 的環境濃度     |
| 屬性群組： | 光源                           |
| 初始值：   |  (0.0、0.0、0.0、1.0)                   |
| 取得命令：     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL \_ 擴散</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------|
| 描述：     | 淺 *i* 的擴散濃度     |
| 屬性群組： | 光源                           |
| 初始值：   |                                    |
| 取得命令：     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>GL \_ 反射</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------|
| 描述：     | *光源的* 反射濃度    |
| 屬性群組： | 光源                           |
| 初始值：   |                                    |
| 取得命令：     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_POSITION"></span><span id="gl_position"></span>GL \_ 位置</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------|
| 描述：     | *燈的* 位置              |
| 屬性群組： | 光源                           |
| 初始值：   |  (0.0、0.0、1.0、0.0)                   |
| 取得命令：     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span>GL \_ 常數 \_ 衰減</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------|
| 描述：     | 定值衰減因數        |
| 屬性群組： | 光源                           |
| 初始值：   | 1.0                                |
| 取得命令：     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span>GL \_ 線性 \_ 衰減</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------|
| 描述：     | 線性衰減因數          |
| 屬性群組： | 光源                           |
| 初始值：   | 0.0                                |
| 取得命令：     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span>GL \_ 二次 \_ 衰減</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------|
| 描述：     | 二次方衰減因數       |
| 屬性群組： | 光源                           |
| 初始值：   | 0.0                                |
| 取得命令：     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span>GL \_ 點 \_ 方向</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------|
| 描述：     | *淺色的* 焦點方向   |
| 屬性群組： | 光源                           |
| 初始值：   |  (0.0、0.0、-1.0)                      |
| 取得命令：     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span>GL \_ 點 \_ 指數</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------|
| 描述：     | Light *i* 的焦點指數    |
| 屬性群組： | 光源                           |
| 初始值：   | 0.0                                |
| 取得命令：     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span>GL \_ 點 \_ 截止</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------|
| 描述：     | *光源的* 焦點角度       |
| 屬性群組： | 光源                           |
| 初始值：   | 180.0                              |
| 取得命令：     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_LIGHT_i"></span><span id="gl_light_i"></span><span id="GL_LIGHT_I"></span>GL \_ 燈</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------|
| 描述：     | 如果 *已啟用* 光線，則為 True          |
| 屬性群組： | 光源/啟用                    |
| 初始值：   | GL \_ FALSE                          |
| 取得命令：     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span>GL \_ 色彩 \_ 索引</dt> <dd> 

| 屬性 | 值 |
|------------------|--------------------------------------------------------------------------------|
| 描述：     | *C (* 色彩索引光源的) 、 *c (d)* 和 *C (s)*                         |
| 屬性群組： | 光源/啟用                                                                |
| 初始值：   | 0、1、1                                                                          |
| 取得命令：     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




