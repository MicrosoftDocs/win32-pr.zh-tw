---
description: 幾何畫筆的維度是以邏輯單元來指定。
ms.assetid: e7030490-d10c-4d1c-87ae-5b4cc4858ee1
title: 幾何畫筆
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9725f6440f62458d4c87232400f16e27f9b978ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991222"
---
# <a name="geometric-pens"></a><span data-ttu-id="288ef-103">幾何畫筆</span><span class="sxs-lookup"><span data-stu-id="288ef-103">Geometric Pens</span></span>

<span data-ttu-id="288ef-104">幾何畫筆的維度是以邏輯單元來指定。</span><span class="sxs-lookup"><span data-stu-id="288ef-104">The dimensions of a geometric pen are specified in logical units.</span></span> <span data-ttu-id="288ef-105">因此，以幾何畫筆繪製的線條可以調整，也就是它們可能會變得較寬或較窄，視目前的世界轉換而定。</span><span class="sxs-lookup"><span data-stu-id="288ef-105">Therefore, lines drawn with a geometric pen can be scaled that is, they may appear wider or narrower, depending on the current world transformation.</span></span> <span data-ttu-id="288ef-106">如需有關「世界」轉換的詳細資訊，請參閱 [座標空間和轉換](coordinate-spaces-and-transformations.md)。</span><span class="sxs-lookup"><span data-stu-id="288ef-106">For more information about world transformation, see [Coordinate Spaces and Transformations](coordinate-spaces-and-transformations.md).</span></span>

<span data-ttu-id="288ef-107">除了與裝飾畫筆共用的三個屬性 (寬度、樣式和色彩) 之外，幾何畫筆還具有下列四個屬性：模式、選擇性的影線、結束樣式和聯結樣式。</span><span class="sxs-lookup"><span data-stu-id="288ef-107">In addition to the three attributes shared with cosmetic pens (width, style, and color), geometric pens possess the following four attributes: pattern, optional hatch, end style, and join style.</span></span> <span data-ttu-id="288ef-108">如需這些屬性的詳細資訊，請參閱 [畫筆屬性](pen-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="288ef-108">For more information about these attributes, see [Pen Attributes](pen-attributes.md).</span></span>

<span data-ttu-id="288ef-109">若要建立幾何畫筆，應用程式會使用 [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) 函數。</span><span class="sxs-lookup"><span data-stu-id="288ef-109">To create a geometric pen, an application uses the [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) function.</span></span> <span data-ttu-id="288ef-110">如同裝飾筆， [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) 函式會在應用程式的 DC 中選取幾何畫筆。</span><span class="sxs-lookup"><span data-stu-id="288ef-110">As with cosmetic pens, the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function selects a geometric pen into the application's DC.</span></span>

 

 



