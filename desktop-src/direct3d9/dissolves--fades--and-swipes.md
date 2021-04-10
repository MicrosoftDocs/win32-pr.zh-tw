---
description: 越來越多的應用程式使用電影和影片中常見的特殊效果，例如溶解、滑動和並淡化。
ms.assetid: 6203922f-9594-4e5c-9baa-8b27ac30978f
title: " (Direct3D 9 的溶解、淡化和撥動) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2ad837ea846ca43d61102ce426d415270d2f27f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688107"
---
# <a name="dissolves-fades-and-swipes-direct3d-9"></a><span data-ttu-id="a7359-103"> (Direct3D 9 的溶解、淡化和撥動) </span><span class="sxs-lookup"><span data-stu-id="a7359-103">Dissolves, Fades, and Swipes (Direct3D 9)</span></span>

<span data-ttu-id="a7359-104">越來越多的應用程式使用電影和影片中常見的特殊效果，例如溶解、滑動和並淡化。</span><span class="sxs-lookup"><span data-stu-id="a7359-104">Increasingly, applications employ special effects that are commonly used in movies and video, such as dissolves, swipes, and fades.</span></span>

<span data-ttu-id="a7359-105">在溶解，某個影像會在一系列平滑的畫面中逐漸被另一個取代。</span><span class="sxs-lookup"><span data-stu-id="a7359-105">In a dissolve, one image is gradually replaced by another in a smooth sequence of frames.</span></span> <span data-ttu-id="a7359-106">雖然 Direct3D 提供方法來使用多重紋理混合達到相同效果，但是使用樣板緩衝區執行溶解的應用程式在溶解時，可以將紋理混合功能用於其他效果。</span><span class="sxs-lookup"><span data-stu-id="a7359-106">Although Direct3D provides methods of using multiple texture blending to achieve the same effect, applications that use the stencil buffer for dissolves can use texture-blending capabilities for other effects while they do a dissolve.</span></span>

<span data-ttu-id="a7359-107">當您的應用程式執行溶解時，必須呈現兩個不同的影像。</span><span class="sxs-lookup"><span data-stu-id="a7359-107">When your application performs a dissolve, it must render two different images.</span></span> <span data-ttu-id="a7359-108">它會使用樣板緩衝區控制每個影像的哪些像素要繪製到轉譯目標表面。</span><span class="sxs-lookup"><span data-stu-id="a7359-108">It uses the stencil buffer to control which pixels from each image are drawn to the rendering target surface.</span></span> <span data-ttu-id="a7359-109">您可以定義一系列的樣板遮罩，並將它們複製到連續畫面上的樣板緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a7359-109">You can define a series of stencil masks and copy them into the stencil buffer on successive frames.</span></span> <span data-ttu-id="a7359-110">或者，您可以定義第一個畫面的基底樣板遮罩，並累加變更它。</span><span class="sxs-lookup"><span data-stu-id="a7359-110">Alternately, you can define a base stencil mask for the first frame and alter it incrementally.</span></span>

<span data-ttu-id="a7359-111">在溶解開頭，應用程式設定樣板函式和樣板遮罩，使開始影像的大部分像素都通過樣板測試。</span><span class="sxs-lookup"><span data-stu-id="a7359-111">At the beginning of the dissolve, your application sets the stencil function and stencil mask so that most of the pixels from the starting image pass the stencil test.</span></span> <span data-ttu-id="a7359-112">結束影像的大部分像素應該未通過樣板測試。</span><span class="sxs-lookup"><span data-stu-id="a7359-112">Most of the pixels from the ending image should fail the stencil test.</span></span> <span data-ttu-id="a7359-113">在後續畫面，樣板遮罩會更新，以便開始影像的更少像素通過測試。</span><span class="sxs-lookup"><span data-stu-id="a7359-113">On successive frames, the stencil mask is updated so that fewer and fewer of the pixels in the starting image pass the test.</span></span> <span data-ttu-id="a7359-114">隨著畫面進展，結束影像的更少像素未通過測試。</span><span class="sxs-lookup"><span data-stu-id="a7359-114">As the frames progress, fewer and fewer of the pixels in the ending image fail the test.</span></span> <span data-ttu-id="a7359-115">如此一來，您的應用程式可以使用任何任意溶解模式執行溶解。</span><span class="sxs-lookup"><span data-stu-id="a7359-115">In this manner, your application can perform a dissolve using any arbitrary dissolve pattern.</span></span>

<span data-ttu-id="a7359-116">淡入或淡出是溶解的特殊案例。</span><span class="sxs-lookup"><span data-stu-id="a7359-116">Fading in or fading out is a special case of dissolving.</span></span> <span data-ttu-id="a7359-117">當淡入時，樣板緩衝區用來從黑或白的影像溶解到 3D 場景轉譯。</span><span class="sxs-lookup"><span data-stu-id="a7359-117">When fading in, the stencil buffer is used to dissolve from a black or white image to a rendering of a 3D scene.</span></span> <span data-ttu-id="a7359-118">淡出則相反，應用程式從 3D 場景轉譯開始，然後溶解為黑或白。</span><span class="sxs-lookup"><span data-stu-id="a7359-118">Fading out is the opposite, your application starts with a rendering of a 3D scene and dissolves to black or white.</span></span> <span data-ttu-id="a7359-119">您可以使用任何任意模式執行淡化。</span><span class="sxs-lookup"><span data-stu-id="a7359-119">The fade can be done using any arbitrary pattern you want to employ.</span></span>

<span data-ttu-id="a7359-120">Direct3D 應用程式對滑動使用類似技術。</span><span class="sxs-lookup"><span data-stu-id="a7359-120">Direct3D applications use a similar technique for swipes.</span></span> <span data-ttu-id="a7359-121">例如，當應用程式執行由左向右滑動時，結束影像看起來在開始影像上逐漸從左向右滑動。</span><span class="sxs-lookup"><span data-stu-id="a7359-121">For example, when an application performs a left-to-right swipe, the ending image appears to slide gradually on top of the starting image from left to right.</span></span> <span data-ttu-id="a7359-122">如同溶解，您必須定義一系列的樣板遮罩，並將它們載入到連續畫面上的樣板緩衝區，或者連續修改開始樣板遮罩。</span><span class="sxs-lookup"><span data-stu-id="a7359-122">As in a dissolve, you must define a series of stencil masks that are loaded into the stencil buffer on successive frames, or successively modify the starting stencil mask.</span></span> <span data-ttu-id="a7359-123">樣板遮罩可用來停用開始影像的像素寫入，以及啟用結束影像的像素寫入。</span><span class="sxs-lookup"><span data-stu-id="a7359-123">The stencil masks are used to disable the writing of pixels from the starting image and to enable the writing of pixels from the ending image.</span></span>

<span data-ttu-id="a7359-124">滑動比溶解有點更複雜，因為應用程式必須以滑動反向順序從結束影像讀取像素。</span><span class="sxs-lookup"><span data-stu-id="a7359-124">A swipe is somewhat more complex than a dissolve in that your application must read pixels from the ending image in the reverse order of the swipe.</span></span> <span data-ttu-id="a7359-125">也就是，如果滑動是從左向右移動，您的應用程式必須由右至左從結束影像讀取像素。</span><span class="sxs-lookup"><span data-stu-id="a7359-125">That is, if the swipe is moving from left to right, your application must read pixels from the ending image from right to left.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7359-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="a7359-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7359-127">樣板緩衝區技術</span><span class="sxs-lookup"><span data-stu-id="a7359-127">Stencil Buffer Techniques</span></span>](stencil-buffer-techniques.md)
</dt> </dl>

 

 



