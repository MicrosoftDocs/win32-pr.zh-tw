---
description: Direct3D 應用程式使用印花來控制從特定原始影像繪製到轉譯目標表面上的像素。 應用程式將印花套用至原始物件的影像，以正確地轉譯共面多邊形。
ms.assetid: 0d57983c-c8f3-4095-9495-a3ec5d280bda
title: 'Decaling (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5606bdbc798d8b1e834aff53b04984f659af650
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108752"
---
# <a name="decaling-direct3d-9"></a><span data-ttu-id="31ae0-104">Decaling (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="31ae0-104">Decaling (Direct3D 9)</span></span>

<span data-ttu-id="31ae0-105">Direct3D 應用程式使用印花來控制從特定原始影像繪製到轉譯目標表面上的像素。</span><span class="sxs-lookup"><span data-stu-id="31ae0-105">Direct3D applications use decaling to control which pixels from a particular primitive image are drawn to the rendering target surface.</span></span> <span data-ttu-id="31ae0-106">應用程式將印花套用至原始物件的影像，以正確地轉譯共面多邊形。</span><span class="sxs-lookup"><span data-stu-id="31ae0-106">Applications apply decals to the images of primitives to enable coplanar polygons to render correctly.</span></span>

<span data-ttu-id="31ae0-107">例如：將輪胎標記及黃線畫上道路之後，標記應該要直接出現在道路上方。</span><span class="sxs-lookup"><span data-stu-id="31ae0-107">For instance, when applying tire marks and yellow lines to a roadway, the markings should appear directly on top of the road.</span></span> <span data-ttu-id="31ae0-108">但是，標記和道路的 z 值是相同的。</span><span class="sxs-lookup"><span data-stu-id="31ae0-108">However, the z values of the markings and the road are the same.</span></span> <span data-ttu-id="31ae0-109">因此，深度緩衝區不一定會在這兩者之間正常分離。</span><span class="sxs-lookup"><span data-stu-id="31ae0-109">Therefore, the depth buffer might not produce a clean separation between the two.</span></span> <span data-ttu-id="31ae0-110">某些後方原始物件的像素可能會轉譯至前方原始物件的上方，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="31ae0-110">Some pixels in the back primitive may be rendered on top of the front primitive and vice versa.</span></span> <span data-ttu-id="31ae0-111">產生的影像似乎在影格間不斷閃爍。</span><span class="sxs-lookup"><span data-stu-id="31ae0-111">The resulting image appears to shimmer from frame to frame.</span></span> <span data-ttu-id="31ae0-112">此效果稱為「*z 衝突*」或「*影格閃爍*」。</span><span class="sxs-lookup"><span data-stu-id="31ae0-112">This effect is called *z-fighting* or *flimmering*.</span></span>

<span data-ttu-id="31ae0-113">若要解決這個問題，可使用樣板將後方原始物件上印花出現的區域遮蔽。</span><span class="sxs-lookup"><span data-stu-id="31ae0-113">To solve this problem, use a stencil to mask the section of the back primitive where the decal will appear.</span></span> <span data-ttu-id="31ae0-114">關閉 z 緩衝，並將前方原始物件的影像轉譯至轉譯目標表面上已被遮蔽的區域。</span><span class="sxs-lookup"><span data-stu-id="31ae0-114">Turn off z-buffering and render the image of the front primitive into the masked-off area of the render-target surface.</span></span>

<span data-ttu-id="31ae0-115">雖然您可使用多重紋理混合解決這個問題，如此一來會限制應用程式可產生的其他特殊效果數目。</span><span class="sxs-lookup"><span data-stu-id="31ae0-115">Although multiple texture blending can be used to solve this problem, doing so limits the number of other special effects that your application can produce.</span></span> <span data-ttu-id="31ae0-116">使用樣板緩衝區套用印花會釋出紋理混合階段供其他效果使用。</span><span class="sxs-lookup"><span data-stu-id="31ae0-116">Using the stencil buffer to apply decals frees up texture blending stages for other effects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="31ae0-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="31ae0-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31ae0-118">樣板緩衝區技術</span><span class="sxs-lookup"><span data-stu-id="31ae0-118">Stencil Buffer Techniques</span></span>](stencil-buffer-techniques.md)
</dt> </dl>

 

 



