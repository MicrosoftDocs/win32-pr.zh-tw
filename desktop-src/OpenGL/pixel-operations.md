---
title: 圖元作業
description: 圖元作業
ms.assetid: e60cc45b-867c-441a-b579-8c7dbd46ecd9
keywords:
- 圖元運算 OpenGL
topic_type:
- apiref
api_name:
- Pixel Operations
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45d36fc22ace4ee18303ce0eb16c5a10f901510f
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908876"
---
# <a name="pixel-operations"></a>圖元作業

<dl> <dt><span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span>GL \_ 剪式 \_ 測試</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------|
| 描述：     | Scissoring 已啟用                 |
| 屬性群組： | 剪式/啟用                     |
| 初始值：   | GL \_ FALSE                          |
| 取得命令：     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_SCISSOR_BOX"></span><span id="gl_scissor_box"></span>GL \_ 剪狀方塊 \_</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 剪式方塊                                                                      |
| 屬性群組： | 剪刀                                                                          |
| 初始值：   |                                                                                  |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span>GL \_ 樣板 \_ 測試</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------|
| 描述：     | Stenciling 已啟用                 |
| 屬性群組： | 樣板-緩衝區/啟用              |
| 初始值：   | GL \_ FALSE                          |
| 取得命令：     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_STENCIL_FUNC"></span><span id="gl_stencil_func"></span>GL \_ 樣板 \_ FUNC</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 樣板函式                                                                 |
| 屬性群組： | 樣板-緩衝區                                                                   |
| 初始值：   | GL \_ 一律                                                                       |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_VALUE_MASK"></span><span id="gl_stencil_value_mask"></span>GL \_ 樣板 \_ 值 \_ 遮罩</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 樣板遮罩                                                                     |
| 屬性群組： | 樣板-緩衝區                                                                   |
| 初始值：   | 1                                                                              |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_REF"></span><span id="gl_stencil_ref"></span>GL \_ 樣板 \_ 參考</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 樣板參考值                                                          |
| 屬性群組： | 樣板-緩衝區                                                                   |
| 初始值：   | 0                                                                                |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_FAIL"></span><span id="gl_stencil_fail"></span>GL \_ 樣板 \_ 失敗</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 樣板失敗動作                                                              |
| 屬性群組： | 樣板-緩衝區                                                                   |
| 初始值：   | GL \_ 保留                                                                         |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_PASS_DEPTH_FAIL"></span><span id="gl_stencil_pass_depth_fail"></span>GL \_ 樣板 \_ 通過 \_ 深度 \_ 失敗</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 樣板深度緩衝區失敗動作                                                 |
| 屬性群組： | 樣板-緩衝區                                                                   |
| 初始值：   | GL \_ 保留                                                                         |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_PASS_DEPTH_PASS"></span><span id="gl_stencil_pass_depth_pass"></span>GL \_ 樣板 \_ 通過 \_ 深度 \_ 傳遞</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 樣板深度緩衝區傳遞動作                                                 |
| 屬性群組： | 樣板-緩衝區                                                                   |
| 初始值：   | GL \_ 保留                                                                         |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span>GL \_ ALPHA \_ 測試</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------|
| 描述：     | 已啟用 Alpha 測試                 |
| 屬性群組： | 色彩緩衝區/啟用                |
| 初始值：   | GL \_ FALSE                          |
| 取得命令：     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_ALPHA_TEST_FUNC"></span><span id="gl_alpha_test_func"></span>GL \_ ALPHA \_ 測試 \_ FUNC</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | Alpha 測試函式                                                              |
| 屬性群組： | 色彩緩衝區                                                                     |
| 初始值：   | GL \_ 一律                                                                       |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_ALPHA_TEST_REF"></span><span id="gl_alpha_test_ref"></span>GL \_ ALPHA \_ 測試 \_ 參考</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | Alpha 測試參考值                                                       |
| 屬性群組： | 色彩緩衝區                                                                     |
| 初始值：   | 0                                                                                |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span>GL \_ 深度 \_ 測試</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------|
| 描述：     | 深度緩衝區已啟用               |
| 屬性群組： | 深度-緩衝區/啟用                |
| 初始值：   | GL \_ FALSE                          |
| 取得命令：     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_DEPTH_FUNC"></span><span id="gl_depth_func"></span>GL \_ 深度 \_ FUNC</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 深度緩衝區測試函式                                                       |
| 屬性群組： | 深度-緩衝區                                                                     |
| 初始值：   | GL \_ LESS                                                                         |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_BLEND"></span><span id="gl_blend"></span>GL \_ BLEND</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------|
| 描述：     | 已啟用混合                   |
| 屬性群組： | 色彩緩衝區/啟用                |
| 初始值：   | GL \_ FALSE                          |
| 取得命令：     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_BLENC_SRC"></span><span id="gl_blenc_src"></span>GL \_ BLENC \_ SRC</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 混合來源函數                                                         |
| 屬性群組： | 色彩緩衝區                                                                     |
| 初始值：   | GL \_ 1                                                                          |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_BLEND_DST"></span><span id="gl_blend_dst"></span>GL \_ BLEND \_ DST</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 混色 destination 函數                                                    |
| 屬性群組： | 色彩緩衝區                                                                     |
| 初始值：   | GL \_ 零                                                                         |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DITHER"></span><span id="gl_dither"></span>GL \_ 遞色</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------|
| 描述：     | 已啟用遞色                  |
| 屬性群組： | 色彩緩衝區/啟用                |
| 初始值：   | GL \_ TRUE                           |
| 取得命令：     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LOGIC_OP"></span><span id="gl_logic_op"></span>GL \_ 邏輯 \_ OP</dt> <dd> 

| 屬性 | 值 |
|------------------|------------------------------------|
| 描述：     | 邏輯運算已啟用          |
| 屬性群組： | 色彩緩衝區/啟用                |
| 初始值：   | GL \_ FALSE                          |
| 取得命令：     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LOGIC_OP_MODE"></span><span id="gl_logic_op_mode"></span>GL \_ 邏輯 \_ OP \_ 模式</dt> <dd> 

| 屬性 | 值 |
|------------------|----------------------------------------------------------------------------------|
| 描述：     | 邏輯運算函數                                                       |
| 屬性群組： | 色彩緩衝區                                                                     |
| 初始值：   | GL \_ 複製                                                                         |
| 取得命令：     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




