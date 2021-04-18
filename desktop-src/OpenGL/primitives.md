---
title: " (OpenGL) 的基本專案"
description: 基本
ms.assetid: a16e5090-8e33-43f4-91df-241a7dd9a860
keywords:
- OpenGL、基本
- OpenGL 處理管線，基本
- 基本 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7f68662515604e555629f7463b239baaf0ef444
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106976348"
---
# <a name="primitives-opengl"></a><span data-ttu-id="a75f1-106"> (OpenGL) 的基本專案</span><span class="sxs-lookup"><span data-stu-id="a75f1-106">Primitives (OpenGL)</span></span>

<span data-ttu-id="a75f1-107">在下一個處理階段中，會在下列步驟中將基本專案轉換成圖元片段：</span><span class="sxs-lookup"><span data-stu-id="a75f1-107">During the next stage of processing, primitives are converted to pixel fragments in the following steps:</span></span>

-   <span data-ttu-id="a75f1-108">會適當地裁剪基本專案。</span><span class="sxs-lookup"><span data-stu-id="a75f1-108">Primitives are clipped appropriately.</span></span>
-   <span data-ttu-id="a75f1-109">需要對色彩和材質資料進行對應的調整，而相關的座標則會轉換成視窗座標。</span><span class="sxs-lookup"><span data-stu-id="a75f1-109">Necessary corresponding adjustments are made to the color and texture data, and the relevant coordinates are transformed to window coordinates.</span></span>
-   <span data-ttu-id="a75f1-110">柵格化會將裁剪的基本專案轉換成圖元片段。</span><span class="sxs-lookup"><span data-stu-id="a75f1-110">Rasterization converts the clipped primitives to pixel fragments.</span></span>

<span data-ttu-id="a75f1-111">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="a75f1-111">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="a75f1-112">裁剪</span><span class="sxs-lookup"><span data-stu-id="a75f1-112">Clipping</span></span>](clipping.md)
-   [<span data-ttu-id="a75f1-113">轉換成視窗座標</span><span class="sxs-lookup"><span data-stu-id="a75f1-113">Transforming to Window Coordinates</span></span>](transforming-to-window-coordinates.md)
-   [<span data-ttu-id="a75f1-114">點陣化</span><span class="sxs-lookup"><span data-stu-id="a75f1-114">Rasterizing</span></span>](rasterizing.md)
-   [<span data-ttu-id="a75f1-115">基本參考</span><span class="sxs-lookup"><span data-stu-id="a75f1-115">Primitives Reference</span></span>](primitives-reference.md)

 

 




