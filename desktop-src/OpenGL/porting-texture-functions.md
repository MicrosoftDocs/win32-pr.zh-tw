---
title: 移植材質函數
description: 移植材質函數
ms.assetid: 03e0b0fc-3812-4744-a0f1-3dcb466d679d
keywords:
- 鳶尾花 GL 移植，材質
- 從鳶尾花 GL、材質移植
- 從鳶尾花 GL 移植至 OpenGL，材質
- 從鳶尾花 GL （紋理）移植的 OpenGL
- 紋理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2cba8b105089553084a93f997517d19cf371e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021674"
---
# <a name="porting-texture-functions"></a><span data-ttu-id="7e48c-108">移植材質函數</span><span class="sxs-lookup"><span data-stu-id="7e48c-108">Porting Texture Functions</span></span>

<span data-ttu-id="7e48c-109">將鳶尾花 GL 材質函數移植至 OpenGL 時，請記住下列幾點：</span><span class="sxs-lookup"><span data-stu-id="7e48c-109">When porting IRIS GL texture functions to OpenGL, keep the following points in mind:</span></span>

-   <span data-ttu-id="7e48c-110">OpenGL 不會維護材質的表格;它只會使用立體材質和2D 材質。</span><span class="sxs-lookup"><span data-stu-id="7e48c-110">OpenGL doesn't maintain tables of textures; it uses either 1-D texture and 2-D texture only.</span></span> <span data-ttu-id="7e48c-111">若要從鳶尾花 GL 程式碼重複使用紋理，請將它們放在顯示清單中。</span><span class="sxs-lookup"><span data-stu-id="7e48c-111">To reuse the textures from your IRIS GL code, put them in a display list.</span></span>
-   <span data-ttu-id="7e48c-112">OpenGL 不會自動產生 mipmap。</span><span class="sxs-lookup"><span data-stu-id="7e48c-112">OpenGL doesn't automatically generate mipmaps.</span></span> <span data-ttu-id="7e48c-113">如果您使用的是 mipmap，則必須先呼叫 [**gluBuild2DMipmaps**](glubuild2dmipmaps.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="7e48c-113">If you're using mipmaps, you must first call the [**gluBuild2DMipmaps**](glubuild2dmipmaps.md) function.</span></span>
-   <span data-ttu-id="7e48c-114">在 OpenGL 中，您可以使用 [**glEnable**](glenable.md) 和 [**glDisable**](gldisable.md) 來開啟和關閉紋理功能。</span><span class="sxs-lookup"><span data-stu-id="7e48c-114">In OpenGL, you use [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) to turn texturing capabilities on and off.</span></span>
-   <span data-ttu-id="7e48c-115">在 OpenGL 中，紋理大小比鳶尾花 GL 更嚴格。</span><span class="sxs-lookup"><span data-stu-id="7e48c-115">In OpenGL, texture size is more strictly regulated than in IRIS GL.</span></span> <span data-ttu-id="7e48c-116">OpenGL 材質的大小必須：</span><span class="sxs-lookup"><span data-stu-id="7e48c-116">The size of an OpenGL texture must be:</span></span>

    <span data-ttu-id="7e48c-117">2 *n* + 2 *b*</span><span class="sxs-lookup"><span data-stu-id="7e48c-117">2 *n* + 2 *b*</span></span>

    <span data-ttu-id="7e48c-118">其中 *n* 是整數， *b* 是：</span><span class="sxs-lookup"><span data-stu-id="7e48c-118">where *n* is an integer and *b* is:</span></span>

    -   <span data-ttu-id="7e48c-119">0，如果材質沒有框線</span><span class="sxs-lookup"><span data-stu-id="7e48c-119">0, if the texture has no border</span></span>
    -   <span data-ttu-id="7e48c-120">1，如果材質有框線圖元 (OpenGL 材質可以有1圖元的框線。 ) </span><span class="sxs-lookup"><span data-stu-id="7e48c-120">1, if the texture has a border pixel (OpenGL textures can have 1-pixel borders.)</span></span>

<span data-ttu-id="7e48c-121">下表列出鳶尾花 GL 紋理函式及其一般 OpenGL 對應專案。</span><span class="sxs-lookup"><span data-stu-id="7e48c-121">The following table lists IRIS GL texture functions and their general OpenGL equivalents.</span></span>



| <span data-ttu-id="7e48c-122">鳶尾花 GL 函數</span><span class="sxs-lookup"><span data-stu-id="7e48c-122">IRIS GL function</span></span> | <span data-ttu-id="7e48c-123">OpenGL 函數</span><span class="sxs-lookup"><span data-stu-id="7e48c-123">OpenGL function</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="7e48c-124">意義</span><span class="sxs-lookup"><span data-stu-id="7e48c-124">Meaning</span></span>                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e48c-125">**textdef2d**</span><span class="sxs-lookup"><span data-stu-id="7e48c-125">**textdef2d**</span></span>    | <span data-ttu-id="7e48c-126">[**glTexImage2D**](glteximage2d.md)[**glTexParameter**](gltexparameter-functions.md)</span><span class="sxs-lookup"><span data-stu-id="7e48c-126">[**glTexImage2D**](glteximage2d.md)[**glTexParameter**](gltexparameter-functions.md)</span></span><br/> [<span data-ttu-id="7e48c-127">**gluBuild2DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="7e48c-127">**gluBuild2DMipmaps**</span></span>](glubuild2dmipmaps.md)<br/>                                                                                                           | <span data-ttu-id="7e48c-128">指定2D 材質影像。</span><span class="sxs-lookup"><span data-stu-id="7e48c-128">Specifies a 2-D texture image.</span></span>                                                              |
| <span data-ttu-id="7e48c-129">**textbind**</span><span class="sxs-lookup"><span data-stu-id="7e48c-129">**textbind**</span></span>     | <span data-ttu-id="7e48c-130">**glTexImage2DglTexParameter**</span><span class="sxs-lookup"><span data-stu-id="7e48c-130">**glTexImage2DglTexParameter**</span></span><br/> <span data-ttu-id="7e48c-131">**gluBuild2DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="7e48c-131">**gluBuild2DMipmaps**</span></span><br/>                                                                                                                                                                                            | <span data-ttu-id="7e48c-132">選取材質函數。</span><span class="sxs-lookup"><span data-stu-id="7e48c-132">Selects a texture function.</span></span>                                                                 |
| <span data-ttu-id="7e48c-133">**tevdef**</span><span class="sxs-lookup"><span data-stu-id="7e48c-133">**tevdef**</span></span>       | [<span data-ttu-id="7e48c-134">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="7e48c-134">**glTexEnv**</span></span>](gltexenv-functions.md)                                                                                                                                                                                                                                | <span data-ttu-id="7e48c-135">定義材質對應環境。</span><span class="sxs-lookup"><span data-stu-id="7e48c-135">Defines a texture-mapping environment.</span></span>                                                      |
| <span data-ttu-id="7e48c-136">**tevbind**</span><span class="sxs-lookup"><span data-stu-id="7e48c-136">**tevbind**</span></span>      | <span data-ttu-id="7e48c-137">**glTexEnv**[**glTexImage1D**](glteximage1d.md)</span><span class="sxs-lookup"><span data-stu-id="7e48c-137">**glTexEnv**[**glTexImage1D**](glteximage1d.md)</span></span><br/>                                                                                                                                                                                                           | <span data-ttu-id="7e48c-138">選取材質環境。</span><span class="sxs-lookup"><span data-stu-id="7e48c-138">Selects a texture environment.</span></span>                                                              |
| <bpt id="p1">**</bpt>t2<ept id="p1">**</ept>           | [<span data-ttu-id="7e48c-140">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="7e48c-140">**glTexCoord**</span></span>](gltexcoord-functions.md)                                                                                                                                                                                                                            | <span data-ttu-id="7e48c-141">設定目前的材質座標。</span><span class="sxs-lookup"><span data-stu-id="7e48c-141">Sets the current texture coordinates.</span></span>                                                       |
| <span data-ttu-id="7e48c-142">**texgen**</span><span class="sxs-lookup"><span data-stu-id="7e48c-142">**texgen**</span></span>       | <span data-ttu-id="7e48c-143">[**glTexGen**](gltexgen-functions.md)[**glGetTexParameter**](glgettexparameter.md)</span><span class="sxs-lookup"><span data-stu-id="7e48c-143">[**glTexGen**](gltexgen-functions.md)[**glGetTexParameter**](glgettexparameter.md)</span></span><br/> [<span data-ttu-id="7e48c-144">**gluBuild1DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="7e48c-144">**gluBuild1DMipmaps**</span></span>](glubuild1dmipmaps.md)<br/> [<span data-ttu-id="7e48c-145">**gluBuild2DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="7e48c-145">**gluBuild2DMipmaps**</span></span>](glubuild2dmipmaps.md)<br/> [<span data-ttu-id="7e48c-146">**gluScaleImage**</span><span class="sxs-lookup"><span data-stu-id="7e48c-146">**gluScaleImage**</span></span>](gluscaleimage.md)<br/> | <span data-ttu-id="7e48c-147">控制材質座標的產生。將影像調整為任意大小。</span><span class="sxs-lookup"><span data-stu-id="7e48c-147">Controls generation of texture coordinates.Scales an image to an arbitrary size.</span></span><br/> |



 

<span data-ttu-id="7e48c-148">如需有關紋理的詳細資訊，請參閱 *OpenGL 程式設計指南*。</span><span class="sxs-lookup"><span data-stu-id="7e48c-148">For more information on texturing, see the *OpenGL Programming Guide*.</span></span>

<span data-ttu-id="7e48c-149">本主題包含下列各項的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7e48c-149">This topic includes information on the following.</span></span>

-   [<span data-ttu-id="7e48c-150">翻譯 tevdef</span><span class="sxs-lookup"><span data-stu-id="7e48c-150">Translating tevdef</span></span>](translating-tevdef.md)
-   [<span data-ttu-id="7e48c-151">翻譯 texdef</span><span class="sxs-lookup"><span data-stu-id="7e48c-151">Translating texdef</span></span>](translating-texdef.md)
-   [<span data-ttu-id="7e48c-152">翻譯 texgen</span><span class="sxs-lookup"><span data-stu-id="7e48c-152">Translating texgen</span></span>](translating-texgen.md)

 

 





