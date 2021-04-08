---
title: 移植色彩呼叫
description: 下表列出鳶尾花 GL 色彩函數及其對等的 OpenGL 函數。
ms.assetid: 4ca6c311-d6c8-4d10-9e9c-770a8e6de4bb
keywords:
- 鳶尾花 GL 移植，色彩
- 從鳶尾花 GL 進行移植，色彩
- 從鳶尾花 GL 移植至 OpenGL，色彩
- 從鳶尾花 GL 的 OpenGL 移植，色彩
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 856b9f9d0a62b866ac1c9981d9fbb716cf243341
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671843"
---
# <a name="porting-color-calls"></a><span data-ttu-id="82c2b-107">移植色彩呼叫</span><span class="sxs-lookup"><span data-stu-id="82c2b-107">Porting Color Calls</span></span>

<span data-ttu-id="82c2b-108">下表列出鳶尾花 GL 色彩函數及其對等的 OpenGL 函數。</span><span class="sxs-lookup"><span data-stu-id="82c2b-108">The following table lists IRIS GL color functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="82c2b-109">鳶尾花 GL 函數</span><span class="sxs-lookup"><span data-stu-id="82c2b-109">IRIS GL function</span></span>                  | <span data-ttu-id="82c2b-110">OpenGL 函數</span><span class="sxs-lookup"><span data-stu-id="82c2b-110">OpenGL function</span></span>                                                                                                                               | <span data-ttu-id="82c2b-111">意義</span><span class="sxs-lookup"><span data-stu-id="82c2b-111">Meaning</span></span>                                              |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="82c2b-112">**c**</span><span class="sxs-lookup"><span data-stu-id="82c2b-112">**c**</span></span>                             | [<span data-ttu-id="82c2b-113">glColor</span><span class="sxs-lookup"><span data-stu-id="82c2b-113">glColor</span></span>](glcolor-functions.md)                                                                                                              | <span data-ttu-id="82c2b-114">設定 RGB 色彩。</span><span class="sxs-lookup"><span data-stu-id="82c2b-114">Sets RGB color.</span></span>                                      |
| <span data-ttu-id="82c2b-115">**color**</span><span class="sxs-lookup"><span data-stu-id="82c2b-115">**color**</span></span>                         | [<span data-ttu-id="82c2b-116">glIndex</span><span class="sxs-lookup"><span data-stu-id="82c2b-116">glIndex</span></span>](glindex-functions.md)                                                                                                              | <span data-ttu-id="82c2b-117">設定色彩索引。</span><span class="sxs-lookup"><span data-stu-id="82c2b-117">Sets the color index.</span></span>                                |
| <span data-ttu-id="82c2b-118">**getcolor**</span><span class="sxs-lookup"><span data-stu-id="82c2b-118">**getcolor**</span></span>                      | <span data-ttu-id="82c2b-119">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ 目前 \_ 索引 ) </span><span class="sxs-lookup"><span data-stu-id="82c2b-119">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_CURRENT\_INDEX )</span></span>                                               | <span data-ttu-id="82c2b-120">傳回目前的色彩索引。</span><span class="sxs-lookup"><span data-stu-id="82c2b-120">Returns the current color index.</span></span>                     |
| <span data-ttu-id="82c2b-121">**getmcolor**</span><span class="sxs-lookup"><span data-stu-id="82c2b-121">**getmcolor**</span></span>                     |                                                                                                                                               | <span data-ttu-id="82c2b-122">取得色彩對應專案的 RGB 值複本。</span><span class="sxs-lookup"><span data-stu-id="82c2b-122">Gets a copy of the RGB values for a color map entry.</span></span> |
| <span data-ttu-id="82c2b-123">**gRGBcolor**</span><span class="sxs-lookup"><span data-stu-id="82c2b-123">**gRGBcolor**</span></span>                     | <span data-ttu-id="82c2b-124">**glGet** ( GL \_ 目前 \_ 色彩 ) </span><span class="sxs-lookup"><span data-stu-id="82c2b-124">**glGet**( GL\_CURRENT\_COLOR )</span></span>                                                                                                               | <span data-ttu-id="82c2b-125">取得目前的 RGB 色彩值。</span><span class="sxs-lookup"><span data-stu-id="82c2b-125">Gets the current RGB color values.</span></span>                   |
| <span data-ttu-id="82c2b-126">**mapcolor**</span><span class="sxs-lookup"><span data-stu-id="82c2b-126">**mapcolor**</span></span>                      |                                                                                                                                               |                                                      |
| <span data-ttu-id="82c2b-127">**RGBcolor**</span><span class="sxs-lookup"><span data-stu-id="82c2b-127">**RGBcolor**</span></span>                      | <span data-ttu-id="82c2b-128">**glColor**</span><span class="sxs-lookup"><span data-stu-id="82c2b-128">**glColor**</span></span>                                                                                                                                   | <span data-ttu-id="82c2b-129">設定 RGB 色彩。</span><span class="sxs-lookup"><span data-stu-id="82c2b-129">Sets RGB color.</span></span>                                      |
| <span data-ttu-id="82c2b-130">**writemask**</span><span class="sxs-lookup"><span data-stu-id="82c2b-130">**writemask**</span></span>                     | [<span data-ttu-id="82c2b-131">**glIndexMask**</span><span class="sxs-lookup"><span data-stu-id="82c2b-131">**glIndexMask**</span></span>](glindexmask.md)                                                                                                            | <span data-ttu-id="82c2b-132">設定色彩索引模式的色遮罩。</span><span class="sxs-lookup"><span data-stu-id="82c2b-132">Sets the color-index mode color mask.</span></span>                |
| <span data-ttu-id="82c2b-133">**wmpackRGBwritemask**</span><span class="sxs-lookup"><span data-stu-id="82c2b-133">**wmpackRGBwritemask**</span></span><br/> | [<span data-ttu-id="82c2b-134">**glColorMask**</span><span class="sxs-lookup"><span data-stu-id="82c2b-134">**glColorMask**</span></span>](glcolormask.md)                                                                                                            | <span data-ttu-id="82c2b-135">設定 RGB 色彩模式遮罩。</span><span class="sxs-lookup"><span data-stu-id="82c2b-135">Sets the RGB color mode mask.</span></span>                        |
| <span data-ttu-id="82c2b-136">**getwritemask**</span><span class="sxs-lookup"><span data-stu-id="82c2b-136">**getwritemask**</span></span>                  | <span data-ttu-id="82c2b-137">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( gl \_ COLOR \_ WRITEMASK ) **glGet** ( gl \_ INDEX \_ WRITEMASK ) </span><span class="sxs-lookup"><span data-stu-id="82c2b-137">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_COLOR\_WRITEMASK )**glGet**( GL\_INDEX\_WRITEMASK )</span></span><br/> | <span data-ttu-id="82c2b-138">取得色遮罩。</span><span class="sxs-lookup"><span data-stu-id="82c2b-138">Gets the color mask.</span></span>                                 |
| <span data-ttu-id="82c2b-139">**gRGBmask**</span><span class="sxs-lookup"><span data-stu-id="82c2b-139">**gRGBmask**</span></span>                      | <span data-ttu-id="82c2b-140">**glGet** ( GL \_ 色彩 \_ WRITEMASK ) </span><span class="sxs-lookup"><span data-stu-id="82c2b-140">**glGet**( GL\_COLOR\_WRITEMASK )</span></span>                                                                                                             | <span data-ttu-id="82c2b-141">取得色遮罩。</span><span class="sxs-lookup"><span data-stu-id="82c2b-141">Gets the color mask.</span></span>                                 |
| <span data-ttu-id="82c2b-142">**zwritemask**</span><span class="sxs-lookup"><span data-stu-id="82c2b-142">**zwritemask**</span></span>                    | [<span data-ttu-id="82c2b-143">**glDepthMask**</span><span class="sxs-lookup"><span data-stu-id="82c2b-143">**glDepthMask**</span></span>](gldepthmask.md)                                                                                                            |                                                      |



 

> [!Note]
>
> <span data-ttu-id="82c2b-144">以 [**glDepthMask**](gldepthmask.md)取代 **zwritemask** 時請務必小心;**glDepthMask** 接受布林值引數，而 **zwritemask** 則會使用位欄位。</span><span class="sxs-lookup"><span data-stu-id="82c2b-144">Be careful when replacing **zwritemask** with [**glDepthMask**](gldepthmask.md); **glDepthMask** takes a Boolean argument, whereas **zwritemask** takes a bit field.</span></span>

 

<span data-ttu-id="82c2b-145">如果您想要使用多個色彩對應，您需要使用適當的 Windows 色彩對應功能。</span><span class="sxs-lookup"><span data-stu-id="82c2b-145">If you want to use multiple color maps, you need to use the appropriate Windows color map functions.</span></span> <span data-ttu-id="82c2b-146">因此， **multimap**、 **onemap**、 **getcmmode**、 **setmap** 和 **getmap** 沒有 OpenGL 對等專案。</span><span class="sxs-lookup"><span data-stu-id="82c2b-146">Therefore, **multimap**, **onemap**, **getcmmode**, **setmap**, and **getmap** have no OpenGL equivalents.</span></span>

 

 





