---
title: 翻譯 tevdef
description: 下列程式碼範例是鳶尾花 GL 紋理環境定義，可指定電視 \_ DECAL 材質-環境參數
ms.assetid: bb4c8231-8102-4ecb-a5d2-c41243c2682d
keywords:
- 鳶尾花 GL 移植，材質
- 從鳶尾花 GL、材質移植
- 從鳶尾花 GL 移植至 OpenGL，材質
- 從鳶尾花 GL （紋理）移植的 OpenGL
- 紋理
- 鳶尾花 GL 移植，tevdef
- 從鳶尾花 GL、tevdef 移植
- 從鳶尾花 GL （tevdef）移植至 OpenGL
- 從鳶尾花 GL tevdef 的 OpenGL 移植
- tevdef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac2610d1467adb6faa1ea105fc8e8734bfb9c4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932530"
---
# <a name="translating-tevdef"></a><span data-ttu-id="f6e88-113">翻譯 tevdef</span><span class="sxs-lookup"><span data-stu-id="f6e88-113">Translating tevdef</span></span>

<span data-ttu-id="f6e88-114">下列程式碼範例是鳶尾花 GL 紋理環境定義，可指定電視 \_ DECAL 材質環境參數：</span><span class="sxs-lookup"><span data-stu-id="f6e88-114">The following code example is an IRIS GL texture-environment definition that specifies the TV\_DECAL texture-environment parameter:</span></span>


```C++
float tevprops[] = {TV_DECAL, TV_NULL}; 
 
tevdef(1, 0, tevprops);
```



<span data-ttu-id="f6e88-115">和轉譯為 OpenGL 的相同程式碼：</span><span class="sxs-lookup"><span data-stu-id="f6e88-115">and the same code translated to OpenGL:</span></span>


```C++
glTexEnvfv(GL_TEXTURE_ENV, GL_TEXTURE_ENV_MODE, GL_DECAL);
```



<span data-ttu-id="f6e88-116">下表列出鳶尾花 GL 紋理環境參數及其對等的 OpenGL 參數。</span><span class="sxs-lookup"><span data-stu-id="f6e88-116">The following table lists the IRIS GL texture-environment parameters and their equivalent OpenGL parameters.</span></span>



| <span data-ttu-id="f6e88-117">鳶尾花 GL 參數</span><span class="sxs-lookup"><span data-stu-id="f6e88-117">IRIS GL parameter</span></span>     | <span data-ttu-id="f6e88-118">OpenGL 參數</span><span class="sxs-lookup"><span data-stu-id="f6e88-118">OpenGL parameter</span></span>             |
|-----------------------|------------------------------|
| <span data-ttu-id="f6e88-119">電視 \_ LAMBERT</span><span class="sxs-lookup"><span data-stu-id="f6e88-119">TV\_MODULATE</span></span>          | <span data-ttu-id="f6e88-120">GL \_ LAMBERT</span><span class="sxs-lookup"><span data-stu-id="f6e88-120">GL\_MODULATE</span></span>                 |
| <span data-ttu-id="f6e88-121">電視 \_ DECAL</span><span class="sxs-lookup"><span data-stu-id="f6e88-121">TV\_DECAL</span></span>             | <span data-ttu-id="f6e88-122">GL \_ DECAL</span><span class="sxs-lookup"><span data-stu-id="f6e88-122">GL\_DECAL</span></span>                    |
| <span data-ttu-id="f6e88-123">電視 \_ BLEND</span><span class="sxs-lookup"><span data-stu-id="f6e88-123">TV\_BLEND</span></span>             | <span data-ttu-id="f6e88-124">GL \_ BLEND</span><span class="sxs-lookup"><span data-stu-id="f6e88-124">GL\_BLEND</span></span>                    |
| <span data-ttu-id="f6e88-125">電視 \_ 色彩</span><span class="sxs-lookup"><span data-stu-id="f6e88-125">TV\_COLOR</span></span>             | <span data-ttu-id="f6e88-126">GL \_ 紋理 \_ 環境 \_ 色彩</span><span class="sxs-lookup"><span data-stu-id="f6e88-126">GL\_TEXTURE\_ENV\_COLOR</span></span>      |
| <span data-ttu-id="f6e88-127">電視 \_ ALPHA</span><span class="sxs-lookup"><span data-stu-id="f6e88-127">TV\_ALPHA</span></span>             | <span data-ttu-id="f6e88-128">沒有直接 OpenGL 對等專案。</span><span class="sxs-lookup"><span data-stu-id="f6e88-128">No direct OpenGL equivalent.</span></span> |
| <span data-ttu-id="f6e88-129">TV \_ 元件 \_ 選取</span><span class="sxs-lookup"><span data-stu-id="f6e88-129">TV\_COMPONENT\_SELECT</span></span> | <span data-ttu-id="f6e88-130">沒有直接 OpenGL 對等專案。</span><span class="sxs-lookup"><span data-stu-id="f6e88-130">No direct OpenGL equivalent.</span></span> |



 

<span data-ttu-id="f6e88-131">如需有關紋理環境參數的詳細資訊，請參閱 [**glTexEnv**](gltexenv-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="f6e88-131">For more information about texture-environment parameters, see [**glTexEnv**](gltexenv-functions.md).</span></span>

 

 




