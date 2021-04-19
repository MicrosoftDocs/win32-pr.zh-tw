---
description: 您的應用程式可利用樣板緩衝區將 2D 或 3D 影像合成為 3D 場景。
ms.assetid: 9233d15d-fa99-41a2-a253-22f5ae5bf788
title: " (Direct3D 9) 的組合"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01bca61559d2773bd1e4f7dc345e9ad4c1fb6fcb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998052"
---
# <a name="compositing-direct3d-9"></a><span data-ttu-id="90181-103"> (Direct3D 9) 的組合</span><span class="sxs-lookup"><span data-stu-id="90181-103">Compositing (Direct3D 9)</span></span>

<span data-ttu-id="90181-104">您的應用程式可利用樣板緩衝區將 2D 或 3D 影像合成為 3D 場景。</span><span class="sxs-lookup"><span data-stu-id="90181-104">Your application can use the stencil buffer to composite 2D or 3D images onto a 3D scene.</span></span> <span data-ttu-id="90181-105">樣板緩衝區中的遮罩可用於遮蔽轉譯目標的部分表面區域。</span><span class="sxs-lookup"><span data-stu-id="90181-105">A mask in the stencil buffer is used to occlude an area of the rendering target surface.</span></span> <span data-ttu-id="90181-106">儲存的 2D 資訊 (例如文字或點陣圖) 接著便可寫入遮蔽區域。</span><span class="sxs-lookup"><span data-stu-id="90181-106">Stored 2D information, such as text or bitmaps, can then be written to the occluded area.</span></span> <span data-ttu-id="90181-107">或者，您的應用程式也可將其他 3D 原始物件轉譯至轉譯目標表面的樣板遮蔽區域。</span><span class="sxs-lookup"><span data-stu-id="90181-107">Alternately, your application can render additional 3D primitives to the stencil-masked region of the rendering target surface.</span></span> <span data-ttu-id="90181-108">甚至可以轉譯整個場景。</span><span class="sxs-lookup"><span data-stu-id="90181-108">It can even render an entire scene.</span></span>

<span data-ttu-id="90181-109">通常，遊戲會將多個 3D 場景合成在一起。</span><span class="sxs-lookup"><span data-stu-id="90181-109">Games often composite multiple 3D scenes together.</span></span> <span data-ttu-id="90181-110">例如：競速遊戲通常都會顯示後照鏡。</span><span class="sxs-lookup"><span data-stu-id="90181-110">For instance, driving games typically display a rear-view mirror.</span></span> <span data-ttu-id="90181-111">後照鏡便包含了駕駛後方的 3D 場景。</span><span class="sxs-lookup"><span data-stu-id="90181-111">The mirror contains the view of the 3D scene behind the driver.</span></span> <span data-ttu-id="90181-112">該檢視基本上就是合成於駕駛前方檢視的第二個 3D 場景。</span><span class="sxs-lookup"><span data-stu-id="90181-112">It is essentially a second 3D scene composited with the driver's forward view.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90181-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="90181-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90181-114">樣板緩衝區技術</span><span class="sxs-lookup"><span data-stu-id="90181-114">Stencil Buffer Techniques</span></span>](stencil-buffer-techniques.md)
</dt> </dl>

 

 



