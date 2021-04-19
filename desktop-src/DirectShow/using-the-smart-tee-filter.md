---
description: 使用智慧的 t a 濾波器
ms.assetid: d2828269-6841-41a8-8d45-f864c7e85857
title: 使用智慧的 t a 濾波器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5260469634c613fe05c25eb9f55e24e108e8c434
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997813"
---
# <a name="using-the-smart-tee-filter"></a><span data-ttu-id="6e66f-103">使用智慧的 t a 濾波器</span><span class="sxs-lookup"><span data-stu-id="6e66f-103">Using the Smart Tee Filter</span></span>

<span data-ttu-id="6e66f-104">如果「捕捉」篩選器有個別的「捕捉」和「預覽」 pin，您可以從另一個瀏覽器進行預覽。</span><span class="sxs-lookup"><span data-stu-id="6e66f-104">If a capture filter has separate capture and preview pins, you can capture from one while previewing from the other.</span></span> <span data-ttu-id="6e66f-105">但是，如果篩選沒有預覽 pin，您可以在圖形中包含 [智慧型](smart-tee-filter.md) 指標篩選來進行相同的動作。</span><span class="sxs-lookup"><span data-stu-id="6e66f-105">But if the filter has no preview pin, you can do the same thing by including the [Smart Tee](smart-tee-filter.md) filter in the graph.</span></span> <span data-ttu-id="6e66f-106">此篩選器會將資料從 capture 釘選分割成兩個相同的資料流程，一個用於 capture，另一個用於預覽。</span><span class="sxs-lookup"><span data-stu-id="6e66f-106">This filter splits data from the capture pin into two identical streams, one for capture and one for preview.</span></span> <span data-ttu-id="6e66f-107">下圖說明此程序。</span><span class="sxs-lookup"><span data-stu-id="6e66f-107">The following diagram illustrates this process.</span></span>

![具有智慧型 t i 濾波器的捕獲圖表](images/vidcap05.png)

<span data-ttu-id="6e66f-109">[**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)方法會自動插入智慧的 t a 篩選準則（如果需要的話）。</span><span class="sxs-lookup"><span data-stu-id="6e66f-109">The [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method automatically inserts the Smart Tee Filter if it is required.</span></span> <span data-ttu-id="6e66f-110">但是，如果您使用 **IGraphBuilder** 方法來建立您的圖形，而不是 **RenderStream**，您可能需要插入智慧的 t a 濾波器。</span><span class="sxs-lookup"><span data-stu-id="6e66f-110">However, if you use **IGraphBuilder** methods to build your graph, and not **RenderStream**, you may need to insert the Smart Tee filter.</span></span>

<span data-ttu-id="6e66f-111">在捕獲篩選器上轉譯釘選之前，請檢查篩選準則是否有預覽 pin 或影片埠 pin。</span><span class="sxs-lookup"><span data-stu-id="6e66f-111">Before you render pins on the capture filter, check whether the filter has a preview pin or a video port pin.</span></span> <span data-ttu-id="6e66f-112">如果不是，而且您想要預覽，請將智慧型指標篩選器新增至圖形，並將它連接到 capture 篩選器上的捕獲 pin。</span><span class="sxs-lookup"><span data-stu-id="6e66f-112">If it does not, and you wish to preview, add the Smart Tee filter to the graph and connect it to the capture pin on the capture filter.</span></span>

> [!Note]  
> <span data-ttu-id="6e66f-113">您可以將影片埠 (VP) 釘選為一種預覽 pin，因此具有 VP 釘選的篩選器不需要 Smart t 濾波器。</span><span class="sxs-lookup"><span data-stu-id="6e66f-113">You can treat a video port (VP) pin as a kind of preview pin, so a filter with a VP pin does not need a Smart Tee filter.</span></span> <span data-ttu-id="6e66f-114">不過，VP 釘有一些其他特殊需求。</span><span class="sxs-lookup"><span data-stu-id="6e66f-114">However, VP pins have some other special requirements.</span></span> <span data-ttu-id="6e66f-115">如需詳細資訊，請參閱 [影片埠 pin](video-port-pins.md)。</span><span class="sxs-lookup"><span data-stu-id="6e66f-115">For more information, see [Video Port Pins](video-port-pins.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6e66f-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="6e66f-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e66f-117">Advanced Capture 主題</span><span class="sxs-lookup"><span data-stu-id="6e66f-117">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="6e66f-118">結合影片捕獲和預覽</span><span class="sxs-lookup"><span data-stu-id="6e66f-118">Combining Video Capture and Preview</span></span>](combining-video-capture-and-preview.md)
</dt> <dt>

[<span data-ttu-id="6e66f-119">使用 Pin 類別</span><span class="sxs-lookup"><span data-stu-id="6e66f-119">Working with Pin Categories</span></span>](working-with-pin-categories.md)
</dt> </dl>

 

 



