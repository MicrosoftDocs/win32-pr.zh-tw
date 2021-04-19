---
title: 移植混合程式碼
description: 在鳶尾花 GL 中，當您同時繪製至前端和後端緩衝區時，會藉由讀取其中一個緩衝區、與該色彩混合，然後將結果寫入兩個緩衝區來進行混合。 但是在 OpenGL 中，每個緩衝區會依序讀取、混合式，然後寫入。
ms.assetid: 18334c6b-586d-44a3-aa95-d10589ba99f4
keywords:
- 鳶尾花 GL 移植，混合
- 從鳶尾花 GL 進行移植，混合
- 從鳶尾花 GL 移植至 OpenGL，混合
- 從鳶尾花 GL 進行 OpenGL 移植，混合
- 混色
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7956c675848f454b660126a7a17869295a827438
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969477"
---
# <a name="porting-blending-code"></a>移植混合程式碼

在鳶尾花 GL 中，當您同時繪製至前端和後端緩衝區時，會藉由讀取其中一個緩衝區、與該色彩混合，然後將結果寫入兩個緩衝區來進行混合。 但是在 OpenGL 中，每個緩衝區會依序讀取、混合式，然後寫入。

下表列出鳶尾花 GL 混合函式及其對等的 OpenGL 函數。



| 鳶尾花 GL 函數  | OpenGL 函數                            | 意義                     |
|-------------------|--------------------------------------------|-----------------------------|
|                   | [**glEnable**](glenable.md) ( GL \_ BLEND )  | 開啟混色。          |
| **blendfunction** | [**glBlendFunc**](glblendfunc.md)         | 指定 blend 函數。 |



 

OpenGL **glBlendFunc** 函式和鳶尾花 GL **blendfunction** 函數幾乎完全相同。 下表列出鳶尾花 GL blend 因數及其 OpenGL 對等專案。



| 鳶尾花 GL          | Opengl                     | 備註             |
|------------------|----------------------------|-------------------|
| BF \_ 零         | GL \_ 零                   |                   |
| BF \_ 一          | GL \_ 1                    |                   |
| BF \_ SA           | GL \_ SRC \_ ALPHA             |                   |
| BF \_ MSA          | GL \_ 1 \_ 減去 \_ SRC \_ ALPHA |                   |
| BF \_ DA           | GL \_ DST \_ ALPHA             |                   |
| BF \_ MDA          | GL \_ 1 \_ 減去 \_ DST \_ ALPHA |                   |
| BF \_ SC           | GL \_ SRC \_ 色彩             |                   |
| BF \_ SERVICES.MSC          | GL \_ 1 \_ 減去 \_ SRC \_ 色彩 | 僅限目的地。 |
| BF \_ DC           | GL \_ DST \_ 色彩             | 僅限來源。      |
| BF \_ MDC          | GL \_ 1 \_ 減去 \_ DST \_ 色彩 | 僅限來源。      |
| BF \_ MIN \_ SA \_ MDA | GL \_ SRC \_ ALPHA \_ 飽和   |                   |



 

??

 

 




