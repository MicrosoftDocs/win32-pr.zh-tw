---
title: 移植可取得矩陣和轉換的函式
description: 下表列出的鳶尾花 GL 函數會取得矩陣和轉換的狀態，以及其 OpenGL 對等專案。
ms.assetid: 53546bc0-ce1d-47e0-ab5e-5d6789c6db2a
keywords:
- 鳶尾花 GL 移植，矩陣
- 從鳶尾花 GL （矩陣）移植
- 從鳶尾花 GL （矩陣）移植至 OpenGL
- 從鳶尾花 GL （矩陣）進行 OpenGL 移植
- 矩陣
- 鳶尾花 GL 移植，轉換
- 從鳶尾花 GL 進行移植，轉換
- 從鳶尾花 GL 移植至 OpenGL，轉換
- 從鳶尾花 GL 的 OpenGL 移植，轉換
- 轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b32ab017e81c9875666785786b29d9c94c7fd1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932320"
---
# <a name="porting-functions-that-get-matrices-and-transformations"></a>移植可取得矩陣和轉換的函式

下表列出的鳶尾花 GL 函數會取得矩陣和轉換的狀態，以及其 OpenGL 對等專案。



| 鳶尾花 GL 矩陣查詢                  | OpenGL glGet 矩陣查詢         | 意義                                                         |
|---------------------------------------|-----------------------------------|-----------------------------------------------------------------|
| **getmmode**                          | GL \_ 矩陣 \_ 模式                  | 傳回目前的矩陣模式。                                |
| 在 **MVIEWING** 模式中 **getmatrix**    | GL \_ 模型 \_ 矩陣             | 傳回目前模型視圖矩陣的複本。                |
| 在 **MPROJECTION** 模式中 **getmatrix** | GL \_ 投射 \_ 矩陣            | 傳回目前投射矩陣的複本。                |
| 在 **MTEXTURE** 模式中 **getmatrix**    | GL \_ 材質 \_ 矩陣               | 傳回目前材質矩陣的複本。                   |
| 不適用。                       | GL \_ 最大 \_ 模型 \_ 堆疊 \_ 深度  | 傳回模型視圖矩陣堆疊支援的最大深度。 |
| 不適用。                       | GL \_ 最大 \_ 投射 \_ 堆疊 \_ 深度 | 傳回投影矩陣堆疊支援的最大深度。 |
| 不適用。                       | GL \_ 最大 \_ 紋理 \_ 堆疊 \_ 深度    | 傳回材質矩陣堆疊支援的最大深度。    |
| 不適用。                       | GL \_ 模型 \_ 堆疊 \_ 深度       | 傳回模型視圖堆疊上的矩陣數目。             |
| 不適用。                       | GL \_ 投射 \_ 堆疊 \_ 深度      | 傳回投射堆疊上的矩陣數目。             |
| 不適用。                       | GL \_ 紋理 \_ 堆疊 \_ 深度         | 傳回紋理堆疊上的矩陣數目。                |



 

??

 

 




