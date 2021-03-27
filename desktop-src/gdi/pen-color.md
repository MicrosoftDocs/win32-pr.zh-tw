---
description: Color 屬性指定畫筆的色彩。
ms.assetid: ce775359-65fc-40d0-8725-b392cc0464a6
title: 畫筆色彩
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92d831994ac444207832574dc104a9d5c2582db8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512861"
---
# <a name="pen-color"></a><span data-ttu-id="04a6f-103">畫筆色彩</span><span class="sxs-lookup"><span data-stu-id="04a6f-103">Pen Color</span></span>

<span data-ttu-id="04a6f-104">Color 屬性指定畫筆的色彩。</span><span class="sxs-lookup"><span data-stu-id="04a6f-104">The color attribute specifies the pen's color.</span></span> <span data-ttu-id="04a6f-105">應用程式可以使用 [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) 宏儲存紅色、綠色、藍色的三個，以指定 [COLORREF](colorref.md) 結構中所需的色彩，並將此結構的位址傳遞至 [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen)、 [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)或 [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) 函式，以建立具有唯一色彩的表面畫筆。</span><span class="sxs-lookup"><span data-stu-id="04a6f-105">An application can create a cosmetic pen with a unique color by using the [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) macro to store the red, green, blue triplet that specifies the desired color in a [COLORREF](colorref.md) structure and passing this structure's address to the [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect), or [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) function.</span></span> <span data-ttu-id="04a6f-106"> (股票筆的限制為黑色、白色和不可見 ) 。如需 RGB triplet 和色彩的詳細資訊，請參閱 [色彩](colors.md)。</span><span class="sxs-lookup"><span data-stu-id="04a6f-106">(The stock pens are limited to black, white, and invisible.) For more information about RGB triplets and color, see [Colors](colors.md).</span></span>

 

 



