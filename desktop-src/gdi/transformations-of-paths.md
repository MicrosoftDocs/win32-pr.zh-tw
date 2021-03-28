---
description: 路徑是使用邏輯單元和目前的轉換來定義的。
ms.assetid: a5a426ec-25e8-4fe1-985c-d078227e8aba
title: 路徑的轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eb2c033b5769a4edff29beba6cccbd80cfd26de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973520"
---
# <a name="transformations-of-paths"></a><span data-ttu-id="0ca10-103">路徑的轉換</span><span class="sxs-lookup"><span data-stu-id="0ca10-103">Transformations of Paths</span></span>

<span data-ttu-id="0ca10-104">路徑是使用邏輯單元和目前的轉換來定義的。</span><span class="sxs-lookup"><span data-stu-id="0ca10-104">Paths are defined using logical units and current transformations.</span></span> <span data-ttu-id="0ca10-105"> (如果已呼叫 [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) 函式，則邏輯單元為全球單位;否則，邏輯單元為頁面單位。 ) 應用程式可使用世界轉換來調整、旋轉、切變、轉譯和反映定義路徑的線條和貝茲曲線。</span><span class="sxs-lookup"><span data-stu-id="0ca10-105">(If the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function has been called, the logical units are world units; otherwise, the logical units are page units.) An application can use world transformations to scale, rotate, shear, translate, and reflect the lines and Bézier curves that define a path.</span></span>

> [!Note]  
> <span data-ttu-id="0ca10-106">在路徑括弧內的世界轉換，只會影響設定轉換之後繪製的線條和曲線。</span><span class="sxs-lookup"><span data-stu-id="0ca10-106">A world transformation within a path bracket only affects those lines and curves drawn after the transformation was set.</span></span> <span data-ttu-id="0ca10-107">它不會影響在設定之前繪製的線條和曲線。</span><span class="sxs-lookup"><span data-stu-id="0ca10-107">It will have no affect on those lines and curves that were drawn before it was set.</span></span> <span data-ttu-id="0ca10-108">如需世界轉換的說明，請參閱 [座標空間和轉換](coordinate-spaces-and-transformations.md)。</span><span class="sxs-lookup"><span data-stu-id="0ca10-108">For a description of the world transformation, see [Coordinate Spaces and Transformations](coordinate-spaces-and-transformations.md).</span></span>

 

<span data-ttu-id="0ca10-109">如果畫筆是幾何畫筆，應用程式也可以使用 [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) 來概述用來勾勒出路徑的畫筆形狀。</span><span class="sxs-lookup"><span data-stu-id="0ca10-109">An application can also use [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) to outline the shape of the pen used to outline a path if the pen is a geometric pen.</span></span> <span data-ttu-id="0ca10-110">如需幾何畫筆的描述，請參閱 [畫筆](pens.md)。</span><span class="sxs-lookup"><span data-stu-id="0ca10-110">For a description of geometric pens, see [Pens](pens.md).</span></span>

 

 



