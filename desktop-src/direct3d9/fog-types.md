---
description: 有兩種方式可以在場景中加入霧化：使用圖元霧化和/或頂點霧化。
ms.assetid: 96531830-2df1-40d4-af46-09b1ca153834
title: " (Direct3D 9) 的霧化類型"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b5dd845373ac4a42a32ab7a9965501df4894568
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108745"
---
# <a name="fog-types-direct3d-9"></a><span data-ttu-id="1bd2f-103"> (Direct3D 9) 的霧化類型</span><span class="sxs-lookup"><span data-stu-id="1bd2f-103">Fog Types (Direct3D 9)</span></span>

<span data-ttu-id="1bd2f-104">有兩種方式可以在場景中加入霧化：使用圖元霧化和/或頂點霧化。</span><span class="sxs-lookup"><span data-stu-id="1bd2f-104">There are two ways to add fog to a scene: with pixel fog and/or vertex fog.</span></span> <span data-ttu-id="1bd2f-105">下列主題說明用於霧化方的公式，以及如何執行頂點和圖元霧化。</span><span class="sxs-lookup"><span data-stu-id="1bd2f-105">The following topics illustrate the formulas used in fog equations, as well as implementing vertex and pixel fog.</span></span> <span data-ttu-id="1bd2f-106">應用程式可以使用頂點著色器和圖元霧化（如有需要）來執行霧化。</span><span class="sxs-lookup"><span data-stu-id="1bd2f-106">An application can implement fog with a vertex shader, and pixel fog simultaneously if desired.</span></span>

-   [<span data-ttu-id="1bd2f-107">霧化公式</span><span class="sxs-lookup"><span data-stu-id="1bd2f-107">Fog Formulas</span></span>](fog-formulas.md)
-   [<span data-ttu-id="1bd2f-108">霧化參數</span><span class="sxs-lookup"><span data-stu-id="1bd2f-108">Fog Parameters</span></span>](fog-parameters.md)
-   [<span data-ttu-id="1bd2f-109">霧化混色</span><span class="sxs-lookup"><span data-stu-id="1bd2f-109">Fog Blending</span></span>](fog-blending.md)
-   [<span data-ttu-id="1bd2f-110">霧化色彩</span><span class="sxs-lookup"><span data-stu-id="1bd2f-110">Fog Color</span></span>](fog-color.md)
-   [<span data-ttu-id="1bd2f-111">頂點霧化</span><span class="sxs-lookup"><span data-stu-id="1bd2f-111">Vertex Fog</span></span>](vertex-fog.md)
-   [<span data-ttu-id="1bd2f-112">圖元霧化</span><span class="sxs-lookup"><span data-stu-id="1bd2f-112">Pixel Fog</span></span>](pixel-fog.md)

<span data-ttu-id="1bd2f-113">霧化混色由轉譯狀態控制;它不是可程式化的圖元管線的一部分。</span><span class="sxs-lookup"><span data-stu-id="1bd2f-113">Fog blending is controlled by render states; it is not part of the programmable pixel pipeline.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1bd2f-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="1bd2f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bd2f-115">框架緩衝區</span><span class="sxs-lookup"><span data-stu-id="1bd2f-115">Frame Buffer</span></span>](frame-buffer.md)
</dt> </dl>

 

 



