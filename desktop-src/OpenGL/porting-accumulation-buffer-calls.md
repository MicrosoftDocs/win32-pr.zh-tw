---
title: 移植累積的緩衝區呼叫
description: 您必須向 OpenGL auxInitDisplayMode 或 ChoosePixelFormat 函數要求適當的像素格式，以配置累積緩衝區。
ms.assetid: 523728ce-4aae-4247-a3dc-23864231cad1
keywords:
- 鳶尾花 GL 移植，累積緩衝區
- 從鳶尾花 GL 進行移植，累積緩衝區
- 從鳶尾花 GL 移植至 OpenGL，累積緩衝區
- 鳶尾花 GL 的 OpenGL 移植，累積緩衝區
- 累積緩衝區 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8a9e1999da2d76f19f6cc0a4c86072f68a1aa239829edcb3f22bf8c873ed181
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936237"
---
# <a name="porting-accumulation-buffer-calls"></a>移植累積的緩衝區呼叫

您必須向 OpenGL **auxInitDisplayMode** 或 [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) 函數要求適當的像素格式，以配置累積緩衝區。 下表列出會影響累積緩衝區的鳶尾花 GL 函數及其對等的 OpenGL 函數。



| 鳶尾花 GL 函數       | OpenGL 函數                                       | 意義                                                                       |
|------------------------|-------------------------------------------------------|-------------------------------------------------------------------------------|
| **acsize**             | **auxInitDisplayMode** 或 **ChoosePixelFormat**       | 指定累積緩衝區中每個色彩元件的 bitplanes 數目。 |
| **acbuf**              | [**glAccum**](glaccum.md)                            | 在累積緩衝區上運作。                                          |
|                        | [**glClearAccum**](glclearaccum.md)                  | 設定累積緩衝區的明確值。                                    |
| **acbuf** ( AC \_ CLEAR )  | [**glClear**](glclear.md) ( GL \_ ACCUM \_ 緩衝區 \_ 位 )  | 清除累積緩衝區。                                               |



 

下表列出鳶尾花 GL **acbuf** 參數，以及相等的 OpenGL [**glAccum**](glaccum.md) 參數。



| 鳶尾花 GL 參數     | OpenGL 參數 |
|-----------------------|------------------|
| AC \_ 累積        | GL \_ ACCUM        |
| AC \_ CLEAR \_ 累積 | GL \_ 負載         |
| AC \_ 退回            | GL \_ 退貨       |
| AC \_ MULT              | GL \_ MULT         |
| AC \_ 新增               | GL \_ 新增          |



 

 

 




