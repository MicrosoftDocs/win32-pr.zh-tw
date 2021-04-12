---
title: 前端、背面和其他緩衝區
description: OpenGL 會在畫面格緩衝區中儲存和操作圖元資料。
ms.assetid: 4af6a5e4-cc62-49e5-a4d5-e54b1348e8fe
keywords:
- Windows 上的 OpenGL，緩衝區
- framebuffers OpenGL
- 色彩緩衝區 OpenGL
- 深度緩衝區 OpenGL
- 累積緩衝區 OpenGL
- 樣板緩衝區 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea487b73af356853bee2054db292cdfe740bd16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372323"
---
# <a name="front-back-and-other-buffers"></a><span data-ttu-id="1401d-109">前端、背面和其他緩衝區</span><span class="sxs-lookup"><span data-stu-id="1401d-109">Front, Back, and Other Buffers</span></span>

<span data-ttu-id="1401d-110">OpenGL 會在畫面格緩衝區中儲存和操作圖元資料。</span><span class="sxs-lookup"><span data-stu-id="1401d-110">OpenGL stores and manipulates pixel data in a framebuffer.</span></span> <span data-ttu-id="1401d-111">畫面格緩衝區包含一組邏輯緩衝區：色彩、深度、累積和樣板緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1401d-111">The framebuffer consists of a set of logical buffers: color, depth, accumulation, and stencil buffers.</span></span> <span data-ttu-id="1401d-112">色彩緩衝區本身是由一組邏輯緩衝區所組成;此集合可以包含左上角、右上角、左上角、右上角和某些數目的輔助緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1401d-112">The color buffer itself consists of a set of logical buffers; this set can include a front-left, a front-right, a back-left, a back-right, and some number of auxiliary buffers.</span></span> <span data-ttu-id="1401d-113">特定的像素格式或 OpenGL 執行可能無法提供所有的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1401d-113">A particular pixel format or OpenGL implementation may not supply all of these buffers.</span></span> <span data-ttu-id="1401d-114">例如，Microsoft 在 Windows 中的 OpenGL 的最新版本不支援 stereoscopic 影像，因此像素格式不能具有左右色彩緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1401d-114">For example, the current version of Microsoft's implementation of OpenGL in Windows does not support stereoscopic images, so a pixel format cannot have left and right color buffers.</span></span> <span data-ttu-id="1401d-115">此外，目前的版本不支援輔助緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1401d-115">In addition, the current version does not support auxiliary buffers.</span></span> <span data-ttu-id="1401d-116">如需 OpenGL 緩衝區和在其上操作之 OpenGL 函數的詳細資訊，請參閱 *Opengl 參考手冊* 和 *Opengl 程式設計指南*。</span><span class="sxs-lookup"><span data-stu-id="1401d-116">For more information on OpenGL buffers and the OpenGL functions that operate on them, see the *OpenGL Reference Manual* and the *OpenGL Programming Guide*.</span></span>

<span data-ttu-id="1401d-117">Microsoft 在 Windows 中執行 OpenGL 的功能支援雙重緩衝的影像。</span><span class="sxs-lookup"><span data-stu-id="1401d-117">Microsoft's implementation of OpenGL in Windows supports double buffering of images.</span></span> <span data-ttu-id="1401d-118">這是一項技術，可讓應用程式將圖元繪製到螢幕上的緩衝區，然後在該影像可供顯示時，將螢幕緩衝的內容複寫到螢幕上的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1401d-118">This is a technique in which an application draws pixels to an off-screen buffer, and then, when that image is ready for display, copies the contents of the off-screen buffer to an on-screen buffer.</span></span> <span data-ttu-id="1401d-119">雙重緩衝能讓影像變更變得平滑，這對動畫影像來說特別重要。</span><span class="sxs-lookup"><span data-stu-id="1401d-119">Double buffering enables smooth image changes, which are especially important for animated images.</span></span>

<span data-ttu-id="1401d-120">使用雙重緩衝處理的應用程式可使用兩個色彩緩衝區： front 緩衝區和背景緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1401d-120">Two color buffers are available to applications that use double buffering: a front buffer and a back buffer.</span></span> <span data-ttu-id="1401d-121">根據預設，繪製命令會被導向至背景緩衝區)  (的背景緩衝區，而前端緩衝區則會顯示在螢幕上。</span><span class="sxs-lookup"><span data-stu-id="1401d-121">By default, drawing commands are directed to the back buffer (the off-screen buffer), while the front buffer is displayed on the screen.</span></span> <span data-ttu-id="1401d-122">當螢幕緩衝區可供顯示時，您可以呼叫 [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)，而 Windows 會將螢幕緩衝區的內容複寫到螢幕緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1401d-122">When the off-screen buffer is ready for display, you call [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers), and Windows copies the contents of the off-screen buffer to the on-screen buffer.</span></span>

<span data-ttu-id="1401d-123">泛型執行會使用與裝置無關的點陣圖 (DIB) 做為背景緩衝區，而螢幕會顯示為 front 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1401d-123">The generic implementation uses a device-independent bitmap (DIB) as the back buffer and the screen display as the front buffer.</span></span> <span data-ttu-id="1401d-124">硬體裝置及其驅動程式可能會使用不同的方法。</span><span class="sxs-lookup"><span data-stu-id="1401d-124">Hardware devices and their drivers may use different approaches.</span></span>

<span data-ttu-id="1401d-125">雙重緩衝是像素格式的屬性。</span><span class="sxs-lookup"><span data-stu-id="1401d-125">Double buffering is a pixel-format property.</span></span> <span data-ttu-id="1401d-126">若要要求像素格式的雙重緩衝，請 \_ 在呼叫 [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)的 [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor)資料結構中，設定 PFD DOUBLEBUFFER 旗標。</span><span class="sxs-lookup"><span data-stu-id="1401d-126">To request double buffering for a pixel format, set the PFD\_DOUBLEBUFFER flag in the [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure in a call to [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).</span></span>

<span data-ttu-id="1401d-127">OpenGL core 函數 [**glDrawBuffer**](gldrawbuffer.md)會選取用於寫入和清除的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1401d-127">The OpenGL core function, [**glDrawBuffer**](gldrawbuffer.md), selects buffers for writing and clearing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1401d-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="1401d-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1401d-129">緩衝區函數</span><span class="sxs-lookup"><span data-stu-id="1401d-129">Buffer Functions</span></span>](buffer-functions.md)
</dt> </dl>

 

 




