---
title: 混合
description: 混色結合了片段的 R、G、B 和值，並將其儲存在畫面格緩衝區中的對應位置。
ms.assetid: 02a78ce3-bb0a-4e9c-a2b1-6da8e95bcee5
keywords:
- OpenGL 處理管線，混合
- 混合 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5b38786d2320a646bd6cac096e535e4e1441df98522ac86a146836b929c0986
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118361432"
---
# <a name="blending"></a>混合

混色結合了片段的 R、G、B 和值，並將其儲存在畫面格緩衝區中的對應位置。 只在 RGBA 模式中執行的混色，取決於片段的 Alpha 值，以及對應目前儲存圖元的 Alpha 值;它也可能取決於 RGB 值。 您可以使用 [**glBlendFunc**](glblendfunc.md)來控制混合，以指定來源和目的地混合因數。

 

 




