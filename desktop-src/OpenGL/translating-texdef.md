---
title: 翻譯 texdef
description: 下列程式碼範例是鳶尾花 GL 材質定義
ms.assetid: bb2d257d-ee74-4a65-b364-c7a97bccaa78
keywords:
- 鳶尾花 GL 移植，材質
- 從鳶尾花 GL、材質移植
- 從鳶尾花 GL 移植至 OpenGL，材質
- 從鳶尾花 GL （紋理）移植的 OpenGL
- 紋理
- 鳶尾花 GL 移植，texdef
- 從鳶尾花 GL、texdef 移植
- 從鳶尾花 GL （texdef）移植至 OpenGL
- 從鳶尾花 GL texdef 的 OpenGL 移植
- texdef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 479af06bcfd3a50daf56fb0629e4c32f24750081
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840695"
---
# <a name="translating-texdef"></a><span data-ttu-id="df0da-113">翻譯 texdef</span><span class="sxs-lookup"><span data-stu-id="df0da-113">Translating texdef</span></span>

<span data-ttu-id="df0da-114">下列程式碼範例是鳶尾花 GL 材質定義：</span><span class="sxs-lookup"><span data-stu-id="df0da-114">The following code example is an IRIS GL texture definition:</span></span>


```C++
float texprops[] = { TX_MINFILTER, TX_POINT, 
                         TX_MAGFILTER, TX_POINT, 
                         TX_WRAP_S, TX_REPEAT, 
                         TX_WRAP_T, TX_REPEAT, 
                         TX_NULL }; 
 
textdef2d(1, 1, 6, 6, granite_texture, 7, texprops);
```



<span data-ttu-id="df0da-115">在上述範例中， **texdef** 會將 tx \_ 點篩選指定為縮放比例和最小化篩選，並將 tx \_ 重複作為包裝機制。</span><span class="sxs-lookup"><span data-stu-id="df0da-115">In the preceding example, **texdef** specifies the TX\_POINT filter as both the magnification and the minimizing filter, and TX\_REPEAT as the wrapping mechanism.</span></span> <span data-ttu-id="df0da-116">它也會指定材質影像： **花崗岩 \_ 材質**。</span><span class="sxs-lookup"><span data-stu-id="df0da-116">It also specifies the texture image: **granite\_texture**.</span></span>

<span data-ttu-id="df0da-117">在 OpenGL 中， [**glTexImage**](glteximage1d.md) 會指定影像，而 [glTexParameter](gltexparameter-functions.md) 會設定屬性。</span><span class="sxs-lookup"><span data-stu-id="df0da-117">In OpenGL, [**glTexImage**](glteximage1d.md) specifies the image and [glTexParameter](gltexparameter-functions.md) sets the property.</span></span> <span data-ttu-id="df0da-118">若要轉譯鳶尾花 GL 材質定義，請以 **glTexImage** 和一或多個 **glTexParameter** 呼叫來取代 **textdef** 函數。</span><span class="sxs-lookup"><span data-stu-id="df0da-118">To translate IRIS GL texture definitions, replace the **textdef** function with **glTexImage** and one or more calls to **glTexParameter**.</span></span>

<span data-ttu-id="df0da-119">上述鳶尾花 GL 程式碼在轉譯為 OpenGL 時看起來像這樣：</span><span class="sxs-lookup"><span data-stu-id="df0da-119">The preceding IRIS GL code looks like this when translated to OpenGL:</span></span>


```C++
GLfloat nearest[] = {GL_NEAREST}; 
GLfloat repeat = {GL_REPEAT}; 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_MIN_FILTER, nearest); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_MAGILTER, nearest); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_WRAP_S, repeat); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_WRAP_T, nearest); 
glTexImage1D( GL_TEXTURE_1D, 0, 1, 6, 0, GL_RGB, GL_UNSIGNED_SHORT, granite_texture);
```



<span data-ttu-id="df0da-120">下表列出鳶尾花 GL 材質參數及其對等的 OpenGL 參數。</span><span class="sxs-lookup"><span data-stu-id="df0da-120">The following table lists the IRIS GL texture parameters and their equivalent OpenGL parameters.</span></span>



| <span data-ttu-id="df0da-121">鳶尾花 GL 材質參數</span><span class="sxs-lookup"><span data-stu-id="df0da-121">IRIS GL texture parameter</span></span> | <span data-ttu-id="df0da-122">OpenGL 材質參數</span><span class="sxs-lookup"><span data-stu-id="df0da-122">OpenGL texture parameter</span></span>                                  |
|---------------------------|-----------------------------------------------------------|
| <span data-ttu-id="df0da-123">TX \_ MINFILTER</span><span class="sxs-lookup"><span data-stu-id="df0da-123">TX\_MINFILTER</span></span>             | <span data-ttu-id="df0da-124">GL \_ 材質 \_ 最小 \_ 篩選</span><span class="sxs-lookup"><span data-stu-id="df0da-124">GL\_TEXTURE\_MIN\_FILTER</span></span>                                  |
| <span data-ttu-id="df0da-125">TX \_ MAGFILTER</span><span class="sxs-lookup"><span data-stu-id="df0da-125">TX\_MAGFILTER</span></span>             | <span data-ttu-id="df0da-126">GL \_ 紋理 \_ MAG \_ 篩選</span><span class="sxs-lookup"><span data-stu-id="df0da-126">GL\_TEXTURE\_MAG\_FILTER</span></span>                                  |
| <span data-ttu-id="df0da-127">德克薩斯 \_ 換行，德克薩斯 \_ 換行 \_</span><span class="sxs-lookup"><span data-stu-id="df0da-127">TX\_WRAP, TX\_WRAP\_S</span></span>     | <span data-ttu-id="df0da-128">GL \_ 材質 \_ 換行 \_</span><span class="sxs-lookup"><span data-stu-id="df0da-128">GL\_TEXTURE\_WRAP\_S</span></span>                                      |
| <span data-ttu-id="df0da-129">德克薩斯 \_ 換行，德克薩斯 \_ 換行 \_ T</span><span class="sxs-lookup"><span data-stu-id="df0da-129">TX\_WRAP, TX\_WRAP\_T</span></span>     | <span data-ttu-id="df0da-130">GL \_ 紋理 \_ WRAP \_ TGL \_ 材質 \_ 框線 \_ 色彩</span><span class="sxs-lookup"><span data-stu-id="df0da-130">GL\_TEXTURE\_WRAP\_TGL\_TEXTURE\_BORDER\_COLOR</span></span><br/> |



 

<span data-ttu-id="df0da-131">下表列出鳶尾花 GL 材質參數的可能值，以及其對等的 OpenGL 參數。</span><span class="sxs-lookup"><span data-stu-id="df0da-131">The following table lists the possible values of the IRIS GL texture parameters and their equivalent OpenGL parameters.</span></span>



| <span data-ttu-id="df0da-132">鳶尾花 GL 材質參數</span><span class="sxs-lookup"><span data-stu-id="df0da-132">IRIS GL texture parameter</span></span> | <span data-ttu-id="df0da-133">OpenGL 材質參數</span><span class="sxs-lookup"><span data-stu-id="df0da-133">OpenGL texture parameter</span></span>     |
|---------------------------|------------------------------|
| <span data-ttu-id="df0da-134">TX \_ 點</span><span class="sxs-lookup"><span data-stu-id="df0da-134">TX\_POINT</span></span>                 | <span data-ttu-id="df0da-135">\_最接近的 GL</span><span class="sxs-lookup"><span data-stu-id="df0da-135">GL\_NEAREST</span></span>                  |
| <span data-ttu-id="df0da-136">TX \_ 雙線性</span><span class="sxs-lookup"><span data-stu-id="df0da-136">TX\_BILINEAR</span></span>              | <span data-ttu-id="df0da-137">GL \_ 線性</span><span class="sxs-lookup"><span data-stu-id="df0da-137">GL\_LINEAR</span></span>                   |
| <span data-ttu-id="df0da-138">TX \_ MIPMAP \_ 點</span><span class="sxs-lookup"><span data-stu-id="df0da-138">TX\_MIPMAP\_POINT</span></span>         | <span data-ttu-id="df0da-139">最接近最接近 MIPMAP 的 GL \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="df0da-139">GL\_NEAREST\_MIPMAP\_NEAREST</span></span> |
| <span data-ttu-id="df0da-140">TX \_ MIPMAP \_ 雙線性</span><span class="sxs-lookup"><span data-stu-id="df0da-140">TX\_MIPMAP\_BILINEAR</span></span>      | <span data-ttu-id="df0da-141">\_最接近的 GL 線性 \_ MIPMAP \_</span><span class="sxs-lookup"><span data-stu-id="df0da-141">GL\_LINEAR\_MIPMAP\_NEAREST</span></span>  |
| <span data-ttu-id="df0da-142">TX \_ MIPMAP \_ 線性</span><span class="sxs-lookup"><span data-stu-id="df0da-142">TX\_MIPMAP\_LINEAR</span></span>        | <span data-ttu-id="df0da-143">GL \_ 最接近 \_ MIPMAP \_ 線性</span><span class="sxs-lookup"><span data-stu-id="df0da-143">GL\_NEAREST\_MIPMAP\_LINEAR</span></span>  |
| <span data-ttu-id="df0da-144">TX \_ 三線性</span><span class="sxs-lookup"><span data-stu-id="df0da-144">TX\_TRILINEAR</span></span>             | <span data-ttu-id="df0da-145">GL \_ 線性 \_ MIPMAP \_ 線性</span><span class="sxs-lookup"><span data-stu-id="df0da-145">GL\_LINEAR\_MIPMAP\_LINEAR</span></span>   |



 

 

 





