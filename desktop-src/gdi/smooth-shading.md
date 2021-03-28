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
# <a name="smooth-shading"></a><span data-ttu-id="d36b3-103">平滑陰影</span><span class="sxs-lookup"><span data-stu-id="d36b3-103">Smooth Shading</span></span>

<span data-ttu-id="d36b3-104">*平滑陰影* 是使用色彩漸層來將區域著色的方法。</span><span class="sxs-lookup"><span data-stu-id="d36b3-104">*Smooth shading* is a method of shading a region with a color gradient.</span></span> <span data-ttu-id="d36b3-105">包含色彩資訊，以及繪圖基本的界限，會指定色彩漸層。</span><span class="sxs-lookup"><span data-stu-id="d36b3-105">Including color information, along with the bounds of drawing primitive, specifies the color gradient.</span></span> <span data-ttu-id="d36b3-106">GDI 會以線性方式，在以色彩端點傳遞的基本型別內插上色彩。</span><span class="sxs-lookup"><span data-stu-id="d36b3-106">GDI linearly interpolates the color of the inside of the primitive passed on the color endpoints.</span></span> <span data-ttu-id="d36b3-107">色彩和頂點資訊包含在 [**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) 結構中的位置資訊。</span><span class="sxs-lookup"><span data-stu-id="d36b3-107">Color and vertex information is included with position information in the [**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) structure.</span></span>

<span data-ttu-id="d36b3-108">使用 [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) 函數來填滿三角形或矩形結構。</span><span class="sxs-lookup"><span data-stu-id="d36b3-108">Use the [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) function to fill a triangle or rectangle structure.</span></span> <span data-ttu-id="d36b3-109">若要以平滑的陰影填滿三角形，請使用三個三角形端點來呼叫 **GradientFill** 。</span><span class="sxs-lookup"><span data-stu-id="d36b3-109">To fill a triangle with smooth shading, call **GradientFill** with the three triangle endpoints.</span></span> <span data-ttu-id="d36b3-110">若要以平滑的陰影填滿矩形，請使用左上角和右下角的矩形座標來呼叫 **GradientFill** 。</span><span class="sxs-lookup"><span data-stu-id="d36b3-110">To fill a rectangle with smooth shading, call **GradientFill** with the upper-left and lower-right rectangle coordinates.</span></span> <span data-ttu-id="d36b3-111">**GradientFill** 會參考 [**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex)、漸層 [**\_ 矩形**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect)和漸層 [**\_ 三角形**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle) 結構。</span><span class="sxs-lookup"><span data-stu-id="d36b3-111">**GradientFill** references the [**TRIVERTEX**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex), [**GRADIENT\_RECT**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect), and [**GRADIENT\_TRIANGLE**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle) structures.</span></span>

<span data-ttu-id="d36b3-112">如需範例，請參閱 [繪製陰影三角形](drawing-a-shaded-triangle.md)。</span><span class="sxs-lookup"><span data-stu-id="d36b3-112">For an example, see [Drawing a Shaded Triangle](drawing-a-shaded-triangle.md).</span></span>

 

 



