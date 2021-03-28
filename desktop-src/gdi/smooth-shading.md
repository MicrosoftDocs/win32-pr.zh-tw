---
description: 平滑陰影是使用色彩漸層來將區域著色的方法。
ms.assetid: 94f26d15-fb76-47ec-b805-f04975d41b43
title: 平滑陰影
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5b73738c03147083099a5070e61fe21ca5cac76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193790"
---
# <a name="smooth-shading"></a>平滑陰影

*平滑陰影* 是使用色彩漸層來將區域著色的方法。 包含色彩資訊，以及繪圖基本的界限，會指定色彩漸層。 GDI 會以線性方式，在以色彩端點傳遞的基本型別內插上色彩。 色彩和頂點資訊包含在 [**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) 結構中的位置資訊。

使用 [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) 函數來填滿三角形或矩形結構。 若要以平滑的陰影填滿三角形，請使用三個三角形端點來呼叫 **GradientFill** 。 若要以平滑的陰影填滿矩形，請使用左上角和右下角的矩形座標來呼叫 **GradientFill** 。 **GradientFill** 會參考 [**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex)、漸層 [**\_ 矩形**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect)和漸層 [**\_ 三角形**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle) 結構。

如需範例，請參閱 [繪製陰影三角形](drawing-a-shaded-triangle.md)。

 

 



