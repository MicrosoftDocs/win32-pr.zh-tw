---
title: 緩衝區函數
description: 若要將螢幕緩衝區的內容複寫到螢幕緩衝區，請呼叫 SwapBuffers。
ms.assetid: 605eba4e-ee38-4e62-adf8-1b7894030cb0
keywords:
- WGL 函式，緩衝區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a93858b8085171a9139bc5ab329e531ddbb699
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106975583"
---
# <a name="buffer-functions"></a><span data-ttu-id="8f893-104">緩衝區函數</span><span class="sxs-lookup"><span data-stu-id="8f893-104">Buffer Functions</span></span>

<span data-ttu-id="8f893-105">若要將螢幕緩衝區的內容複寫到螢幕緩衝區，請呼叫 [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)。</span><span class="sxs-lookup"><span data-stu-id="8f893-105">To copy the contents of an off-screen buffer to an on-screen buffer, call [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span></span> <span data-ttu-id="8f893-106">**SwapBuffers** 函式會接受裝置內容的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8f893-106">The **SwapBuffers** function takes a handle to a device context.</span></span> <span data-ttu-id="8f893-107">指定之裝置內容的目前像素格式必須包含背景緩衝區。</span><span class="sxs-lookup"><span data-stu-id="8f893-107">The current pixel format for the specified device context must include a back buffer.</span></span> <span data-ttu-id="8f893-108">根據預設，背景緩衝區會在螢幕上，而前端緩衝區會在螢幕上。</span><span class="sxs-lookup"><span data-stu-id="8f893-108">By default, the back buffer is off-screen, and the front buffer is on-screen.</span></span>

> [!Note]  
> <span data-ttu-id="8f893-109">**SwapBuffers** 函式不會實際交換這兩個緩衝區的內容，而是會將一個緩衝區的內容複寫到另一個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="8f893-109">The **SwapBuffers** function does not really swap the contents of the two buffers, but rather copies the contents of one buffer to another.</span></span> <span data-ttu-id="8f893-110">在呼叫 **SwapBuffers** 之後，不會定義非螢幕緩衝區的內容。</span><span class="sxs-lookup"><span data-stu-id="8f893-110">The contents of the off-screen buffer are undefined after a call to **SwapBuffers**.</span></span> <span data-ttu-id="8f893-111">因此，兩個連續呼叫 **SwapBuffers** 的結果為未定義。</span><span class="sxs-lookup"><span data-stu-id="8f893-111">Thus, the result of two consecutive calls to **SwapBuffers** is undefined.</span></span>

 

<span data-ttu-id="8f893-112">下圖顯示呼叫 **SwapBuffers** 時，如何複製緩衝區的內容。</span><span class="sxs-lookup"><span data-stu-id="8f893-112">The following illustration shows how the contents of the buffers are copied when calling **SwapBuffers**.</span></span>

![此圖顯示連續呼叫 SwapBuffers 函式的未定義結果。](images/opengl00.png)

<span data-ttu-id="8f893-114">許多 OpenGL 核心函數也會管理緩衝區。</span><span class="sxs-lookup"><span data-stu-id="8f893-114">Several OpenGL core functions also manage buffers.</span></span> <span data-ttu-id="8f893-115">[**GlDrawBuffer**](gldrawbuffer.md)函式是與雙重緩衝最相關的函數;它會指定 OpenGL 繪製的畫面格緩衝區或緩衝區。</span><span class="sxs-lookup"><span data-stu-id="8f893-115">The [**glDrawBuffer**](gldrawbuffer.md) function is the one most relevant to double buffering; it specifies the framebuffer or buffers that OpenGL draws into.</span></span>

<span data-ttu-id="8f893-116">下列函數也會影響緩衝區：</span><span class="sxs-lookup"><span data-stu-id="8f893-116">The following functions also affect buffers:</span></span>

-   [<span data-ttu-id="8f893-117">**glReadBuffer**</span><span class="sxs-lookup"><span data-stu-id="8f893-117">**glReadBuffer**</span></span>](glreadbuffer.md)
-   [<span data-ttu-id="8f893-118">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="8f893-118">**glReadPixels**</span></span>](glreadpixels.md)
-   [<span data-ttu-id="8f893-119">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="8f893-119">**glCopyPixels**</span></span>](glcopypixels.md)
-   [<span data-ttu-id="8f893-120">**glAccum**</span><span class="sxs-lookup"><span data-stu-id="8f893-120">**glAccum**</span></span>](glaccum.md)
-   [<span data-ttu-id="8f893-121">**glColorMask**</span><span class="sxs-lookup"><span data-stu-id="8f893-121">**glColorMask**</span></span>](glcolormask.md)
-   [<span data-ttu-id="8f893-122">**glDepthMask**</span><span class="sxs-lookup"><span data-stu-id="8f893-122">**glDepthMask**</span></span>](gldepthmask.md)
-   [<span data-ttu-id="8f893-123">**glIndexMask**</span><span class="sxs-lookup"><span data-stu-id="8f893-123">**glIndexMask**</span></span>](glindexmask.md)
-   [<span data-ttu-id="8f893-124">**glStencilMask**</span><span class="sxs-lookup"><span data-stu-id="8f893-124">**glStencilMask**</span></span>](glstencilmask.md)
-   [<span data-ttu-id="8f893-125">**glClearAccum**</span><span class="sxs-lookup"><span data-stu-id="8f893-125">**glClearAccum**</span></span>](glclearaccum.md)
-   [<span data-ttu-id="8f893-126">**glClearColor**</span><span class="sxs-lookup"><span data-stu-id="8f893-126">**glClearColor**</span></span>](glclearcolor.md)
-   [<span data-ttu-id="8f893-127">**glClearDepth**</span><span class="sxs-lookup"><span data-stu-id="8f893-127">**glClearDepth**</span></span>](glcleardepth.md)
-   [<span data-ttu-id="8f893-128">**glClearIndex**</span><span class="sxs-lookup"><span data-stu-id="8f893-128">**glClearIndex**</span></span>](glclearindex.md)
-   [<span data-ttu-id="8f893-129">**glClearStencil**</span><span class="sxs-lookup"><span data-stu-id="8f893-129">**glClearStencil**</span></span>](glclearstencil.md)

 

 




