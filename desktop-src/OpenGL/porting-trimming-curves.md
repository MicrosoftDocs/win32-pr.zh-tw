---
title: 移植修剪曲線
description: OpenGL 修剪曲線與鳶尾花 GL 修剪曲線非常類似。 下表列出用來定義修剪曲線和其相等 OpenGL 函數的鳶尾花 GL 函數。
ms.assetid: 9aeea9ca-5ecd-4be1-853d-45b1566b263b
keywords:
- 鳶尾花 GL 移植，修剪曲線
- 從鳶尾花 GL （修剪曲線）進行移植
- 從鳶尾花 GL 移植至 OpenGL，修剪曲線
- 從鳶尾花 GL （修剪曲線）進行 OpenGL 移植
- 修剪曲線
- 曲線
- 鳶尾花 GL 移植，曲線
- 從鳶尾花 GL、曲線移植
- 從鳶尾花 GL （曲線）移植至 OpenGL
- 從鳶尾花 GL、曲線移植的 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad544431adaa7f0b049341ec7314e3e53ae60752d633a48c760ca09334f79d33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553858"
---
# <a name="porting-trimming-curves"></a>移植修剪曲線

OpenGL 修剪曲線與鳶尾花 GL 修剪曲線非常類似。 下表列出用來定義修剪曲線和其相等 OpenGL 函數的鳶尾花 GL 函數。



| 鳶尾花 GL 函數 | OpenGL 函數                        | 意義                              |
|------------------|----------------------------------------|--------------------------------------|
| **bgntrim**      | [**gluBeginTrim**](glubegintrim.md)   | 開始修剪曲線的定義。    |
| **pwlcurve**     | [**gluPwlCurve**](glupwlcurve.md)     | 定義分段線性曲線。    |
| **nurbscurve**   | [**gluNurbsCurve**](glunurbscurve.md) | 指定修剪曲線屬性。 |
| **endtrim**      | [**gluEndTrim**](gluendtrim.md)       | 結束修剪曲線的定義。      |



 

??

 

 




