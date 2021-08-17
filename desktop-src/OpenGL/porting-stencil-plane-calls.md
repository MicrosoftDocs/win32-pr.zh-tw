---
title: 移植樣板平面呼叫
description: 在 OpenGL 中，您可以使用 OpenGL auxInitDisplayMode 或 ChoosePixelFormat 要求適當的像素格式來配置樣板平面。
ms.assetid: faea8a10-860a-4495-80fb-e83303e397df
keywords:
- 鳶尾花 GL 移植，樣板平面
- 從鳶尾花 GL、樣板平面移植
- 從鳶尾花 GL、樣板平面移植至 OpenGL
- 從鳶尾花 GL、樣板平面移植的 OpenGL
- 樣板平面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4d2c9ea8a9c025c06f179b51cab1301f8ff871740576a6c9e28cdfc1f15ad3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485388"
---
# <a name="porting-stencil-plane-calls"></a>移植樣板平面呼叫

在 OpenGL 中，您可以使用 OpenGL **auxInitDisplayMode** 或 [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)要求適當的像素格式來配置樣板平面。 功能。 下表列出會影響樣板平面及其對等 OpenGL 函式的鳶尾花 GL 函數。



| 鳶尾花 GL 函數             | OpenGL 函數                                         | 意義                                                |
|------------------------------|---------------------------------------------------------|--------------------------------------------------------|
| **stensize**                 | **ChoosePixelFormat**                                   |                                                        |
| 樣板 ( **TRUE**，... )  | [**glEnable**](glenable.md) ( GL \_ 樣板 \_ 測試 )       | 啟用樣板測試。                                 |
| **模具**                  | [**glStencilOp**](glstencilop.md)                      | 設定樣板測試動作。                             |
| 樣板 **( ...** func、... )   | [**glStencilFunc**](glstencilfunc.md)                  | 設定樣板測試的函數和參考值。 |
| **swritemask**               | [**glStencilMask**](glstencilmask.md)                  | 指定可寫入的範本位。           |
|                              | [**glClearStencil**](glclearstencil.md)                | 指定樣板緩衝區的清除值。      |
| **sclear**                   | [**glClear**](glclear.md) ( GL \_ 樣板 \_ 緩衝區 \_ 位 )  |                                                        |



 

樣板-比較函式和樣板通過/失敗作業在 OpenGL 和鳶尾花 GL 中幾乎相等。 鳶尾花 GL 樣板函式旗標前面會加上 SF;具有 GL 的 OpenGL 旗標。 鳶尾花 GL 通過/失敗作業旗標的開頭為 ST;具有 GL 的 OpenGL 旗標。

 

 




