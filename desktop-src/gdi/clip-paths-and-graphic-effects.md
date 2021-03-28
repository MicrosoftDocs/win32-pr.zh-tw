---
description: 應用程式可以使用裁剪和路徑來建立特殊的圖形效果。 下圖顯示以大量 Arial 字型繪製的文字字串。
ms.assetid: fda0d627-406c-44f9-9061-7aea3e2d7f66
title: 剪輯路徑和圖形效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8156a8670747175502b2385e6c24a340345a54f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512921"
---
# <a name="clip-paths-and-graphic-effects"></a><span data-ttu-id="723e9-104">剪輯路徑和圖形效果</span><span class="sxs-lookup"><span data-stu-id="723e9-104">Clip Paths and Graphic Effects</span></span>

<span data-ttu-id="723e9-105">應用程式可以使用裁剪和路徑來建立特殊的圖形效果。</span><span class="sxs-lookup"><span data-stu-id="723e9-105">An application can use clipping and paths to create special graphic effects.</span></span> <span data-ttu-id="723e9-106">下圖顯示以大量 Arial 字型繪製的文字字串。</span><span class="sxs-lookup"><span data-stu-id="723e9-106">The following illustration shows a string of text drawn with a large Arial font.</span></span>

![顯示白色背景上黑色文字的圖例](images/cspth-02.png)

<span data-ttu-id="723e9-108">下圖顯示將文字選取為剪輯路徑的結果，並針對中央位於字串上方和左邊的圓形繪製星形線。</span><span class="sxs-lookup"><span data-stu-id="723e9-108">The next illustration shows the result of selecting the text as a clip path and drawing radial lines for a circle whose center is located above and left of the string.</span></span>

![圖例顯示相同的文字，但填滿了線條，而不是實心黑色](images/cspth-03.png)

> [!Note]  
> <span data-ttu-id="723e9-110">在圖形裝置介面 (GDI) 會將以點陣圖字型建立的文字加入至路徑，然後將字型轉換成大綱或向量字型。</span><span class="sxs-lookup"><span data-stu-id="723e9-110">Before graphics device interface (GDI) adds text created with a bitmapped font to a path, it converts the font to an outline or vector font.</span></span>

 

<span data-ttu-id="723e9-111">應用程式會藉由產生路徑括弧，然後呼叫 [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) 函式來建立剪輯路徑。</span><span class="sxs-lookup"><span data-stu-id="723e9-111">An application creates a clip path by generating a path bracket and then calling the [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) function.</span></span> <span data-ttu-id="723e9-112">在將剪輯路徑選取至 DC 之後，輸出只會顯示在路徑的框線中。</span><span class="sxs-lookup"><span data-stu-id="723e9-112">After a clip path is selected into a DC, output only appears within the borders of the path.</span></span>

<span data-ttu-id="723e9-113">除了建立特殊圖形效果之外，在將影像儲存為增強型中繼檔的應用程式中，剪輯路徑也非常有用。</span><span class="sxs-lookup"><span data-stu-id="723e9-113">In addition to creating special graphics effects, clip paths are also useful in applications that save images as enhanced metafiles.</span></span> <span data-ttu-id="723e9-114">藉由使用剪輯路徑，應用程式可以確保裝置獨立性，因為用來指定路徑的單位是邏輯單元。</span><span class="sxs-lookup"><span data-stu-id="723e9-114">By using a clip path, an application is able to ensure device independence because the units used to specify a path are logical units.</span></span>

 

 



