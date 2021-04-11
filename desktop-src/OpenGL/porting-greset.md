---
title: 移植 greset
description: OpenGL 將鳶尾花 GL 函數 greset 取代為函數 glPushAttrib 和 glPopAttrib。
ms.assetid: 348e8b18-4f12-45d1-a4d2-6533a983236b
keywords:
- 鳶尾花 GL 移植，狀態變數
- 從鳶尾花 GL、狀態變數移植
- 從鳶尾花 GL、狀態變數移植至 OpenGL
- 從鳶尾花 GL、狀態變數移植的 OpenGL
- 狀態變數
- 鳶尾花 GL 移植，greset 函式
- 從鳶尾花 GL、greset 函式移植
- 從鳶尾花 GL、greset 函式移植至 OpenGL
- 從鳶尾花 GL、greset 函式移植的 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078482f47dcaf7fd5f84605e2e0fa32d0cf14729
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372371"
---
# <a name="porting-greset"></a>移植 greset

OpenGL 將鳶尾花 GL 函數 **greset** 取代為函數 [**glPushAttrib**](glpushattrib.md) 和 [**glPopAttrib**](glpopattrib.md)。 使用這些函式來儲存及還原狀態變數的群組。 例如，

``` syntax
void glPushAttrib( GLbitfield mask );
```

這個範例會採用位 OR 的符號常數，指出要推送至屬性堆疊的狀態變數群組。 每個常數都會參考一組狀態變數。 下表顯示具有對等符號常數名稱的屬性群組。 如需與每個常數相關聯之 OpenGL 狀態變數的完整清單，請參閱 [**glPushAttrib**](glpushattrib.md)。



| 屬性                       | 常數                  |
|---------------------------------|---------------------------|
| 累積緩衝區清除值 | GL \_ ACCUM \_ 緩衝區 \_ 位    |
| 色彩緩衝區                    | GL \_ 色彩 \_ 緩衝區 \_ 位    |
| 目前的                         | GL \_ 目前 \_ 位          |
| 深度緩衝區                    | GL \_ 深度 \_ 緩衝區 \_ 位    |
| enable                          | GL \_ 啟用 \_ 位           |
| 評估工具                      | EGL \_ VAL \_ 位             |
| 霧                             | GL \_ 霧化 \_ 位              |
| GL \_ 清單 \_ 基礎設定          | GL \_ 清單 \_ 位             |
| 提示變數                  | GL \_ 提示 \_ 位             |
| 光源變數              | GL \_ 照明 \_ 位         |
| 線條繪圖模式               | GL \_ 行 \_ 位             |
| 圖元模式變數            | GL \_ 圖元 \_ 模式 \_ 位      |
| 點變數                 | GL \_ 點 \_ 位            |
| 多邊形                         | GL \_ 多邊形 \_ 位          |
| 多邊形 stipple                 | GL \_ 多邊形 \_ STIPPLE \_ 位 |
| 剪刀                         | GL \_ 剪式 \_ 位          |
| 樣板緩衝區                  | GL \_ 樣板 \_ 緩衝區 \_ 位  |
| 紋理                         | GL \_ 材質 \_ 位          |
| Transform - 轉換                       | GL \_ 轉換 \_ 位        |
| Viewport - 檢視區                        | GL \_ 區 \_ 位         |
|                                 | GL \_ 所有 \_ ATTRIB \_ 位     |



 

若要將狀態變數的值還原為與最後一個 [**glPushAttrib**](glpushattrib.md)儲存的值，只需呼叫 [**glPopAttrib**](glpopattrib.md)。 您未儲存的變數將保持不變。 屬性堆疊的有限深度至少為16。

 

 




