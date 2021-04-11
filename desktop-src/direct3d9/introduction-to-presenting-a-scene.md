---
description: 展示 Api 是一組方法，可控制影響使用者在監視器上看到的裝置狀態。 這些方法包括設定顯示模式，以及用來向使用者呈現影像的每一畫面一次的方法。
ms.assetid: fb2ddc0d-50ac-48aa-8a5c-f232b0f8e7aa
title: " (Direct3D 9) 呈現場景的簡介"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d909f2d7fcc04cd58c27c7598ca8f826b27f48a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317712"
---
# <a name="introduction-to-presenting-a-scene-direct3d-9"></a><span data-ttu-id="c8333-104"> (Direct3D 9) 呈現場景的簡介</span><span class="sxs-lookup"><span data-stu-id="c8333-104">Introduction to Presenting a Scene (Direct3D 9)</span></span>

<span data-ttu-id="c8333-105">展示 Api 是一組方法，可控制影響使用者在監視器上看到的裝置狀態。</span><span class="sxs-lookup"><span data-stu-id="c8333-105">The presentation APIs are a set of methods that control the state of the device that affects what the user sees on the monitor.</span></span> <span data-ttu-id="c8333-106">這些方法包括設定顯示模式，以及用來向使用者呈現影像的每一畫面一次的方法。</span><span class="sxs-lookup"><span data-stu-id="c8333-106">These methods include setting display modes and once-per-frame methods that are used to present images to the user.</span></span>

-   [<span data-ttu-id="c8333-107">**IDirect3DDevice9::Present**</span><span class="sxs-lookup"><span data-stu-id="c8333-107">**IDirect3DDevice9::Present**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)
-   [<span data-ttu-id="c8333-108">**IDirect3DDevice9::Reset**</span><span class="sxs-lookup"><span data-stu-id="c8333-108">**IDirect3DDevice9::Reset**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
-   [<span data-ttu-id="c8333-109">**IDirect3DDevice9::GetGammaRamp**</span><span class="sxs-lookup"><span data-stu-id="c8333-109">**IDirect3DDevice9::GetGammaRamp**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp)
-   [<span data-ttu-id="c8333-110">**IDirect3DDevice9::SetGammaRamp**</span><span class="sxs-lookup"><span data-stu-id="c8333-110">**IDirect3DDevice9::SetGammaRamp**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)
-   [<span data-ttu-id="c8333-111">**IDirect3DDevice9::GetRasterStatus**</span><span class="sxs-lookup"><span data-stu-id="c8333-111">**IDirect3DDevice9::GetRasterStatus**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrasterstatus)

<span data-ttu-id="c8333-112">若要瞭解簡報 Api，您必須熟悉下列詞彙。</span><span class="sxs-lookup"><span data-stu-id="c8333-112">Familiarity with the following terms is necessary to understand the presentation APIs.</span></span>

-   <span data-ttu-id="c8333-113">前端緩衝區。</span><span class="sxs-lookup"><span data-stu-id="c8333-113">front buffer.</span></span> <span data-ttu-id="c8333-114">由圖形介面卡轉譯並顯示在監視器或其他輸出裝置上的記憶體矩形。</span><span class="sxs-lookup"><span data-stu-id="c8333-114">A rectangle of memory that is translated by the graphics adapter and displayed on the monitor or other output device.</span></span>
-   <span data-ttu-id="c8333-115">背景緩衝區。</span><span class="sxs-lookup"><span data-stu-id="c8333-115">back buffer.</span></span> <span data-ttu-id="c8333-116">其內容可升級至前端緩衝區的介面。</span><span class="sxs-lookup"><span data-stu-id="c8333-116">A surface whose contents can be promoted to the front buffer.</span></span>
-   <span data-ttu-id="c8333-117">交換鏈。</span><span class="sxs-lookup"><span data-stu-id="c8333-117">swap chain.</span></span> <span data-ttu-id="c8333-118">可連續呈現給前端緩衝區的後置緩衝區集合。</span><span class="sxs-lookup"><span data-stu-id="c8333-118">A collection of back buffers that can be serially presented to the front buffer.</span></span> <span data-ttu-id="c8333-119">一般而言，全螢幕交換鏈會以 (DDI) 的方式來呈現後續影像，並將設備磁碟機介面替換為視窗中的交換鏈，以提供具有 blitting DDI 的影像。</span><span class="sxs-lookup"><span data-stu-id="c8333-119">Typically, a full-screen swap chain presents subsequent images with the flipping device driver interface (DDI), and a windowed swap chain presents images with the blitting DDI.</span></span>

<span data-ttu-id="c8333-120">由於 Direct3D 9 有一個交換鏈作為裝置的屬性，因此每個裝置一律至少有一個交換鏈。</span><span class="sxs-lookup"><span data-stu-id="c8333-120">Because Direct3D 9 has one swap chain as a property of the device, there is always at least one swap chain per device.</span></span> <span data-ttu-id="c8333-121">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面具有一組方法，可操作隱含交換鏈，而且是交換鏈本身介面的複本。</span><span class="sxs-lookup"><span data-stu-id="c8333-121">The [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface has a set of methods that manipulate the implicit swap chain and are a copy of the swap chain's own interface.</span></span> <span data-ttu-id="c8333-122">應用程式可以建立額外的交換鏈;不過，這對一般的單一視窗或全螢幕應用程式而言並不是必要的。</span><span class="sxs-lookup"><span data-stu-id="c8333-122">Applications can create additional swap chains; however, this is not necessary for the typical single window or full-screen application.</span></span>

<span data-ttu-id="c8333-123">在 Direct3D 9 中不會直接公開 front 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="c8333-123">The front buffer is not directly exposed in Direct3D 9.</span></span> <span data-ttu-id="c8333-124">因此，應用程式無法鎖定或轉譯至前端緩衝區。</span><span class="sxs-lookup"><span data-stu-id="c8333-124">As a result, applications cannot lock or render to the front buffer.</span></span> <span data-ttu-id="c8333-125">如需詳細資訊，請參閱 [ (Direct3D 9) 存取色彩前端緩衝區 ](accessing-the-color-front-buffer.md)。</span><span class="sxs-lookup"><span data-stu-id="c8333-125">For details, see [Accessing the Color Front Buffer (Direct3D 9)](accessing-the-color-front-buffer.md).</span></span>

> [!Note]  
> <span data-ttu-id="c8333-126">DirectX 7 提供許多同時呼叫的簡報 Api。</span><span class="sxs-lookup"><span data-stu-id="c8333-126">DirectX 7 provided a number of presentation APIs that were called together.</span></span> <span data-ttu-id="c8333-127">IDirectDraw7：： SetCooperativeLevel、IDirectDraw7：： SetDisplayMode 和 IDirectDraw7：： CreateSurface 序列是很好的範例。</span><span class="sxs-lookup"><span data-stu-id="c8333-127">A good example of this is the IDirectDraw7::SetCooperativeLevel, IDirectDraw7::SetDisplayMode, and IDirectDraw7::CreateSurface sequence.</span></span> <span data-ttu-id="c8333-128">此外，IDirectDrawSurface7：： Flip 和 IDirectDrawSurface7：： Blt 方法會將轉譯的框架傳輸傳送給監視器。</span><span class="sxs-lookup"><span data-stu-id="c8333-128">Additionally, the IDirectDrawSurface7::Flip and IDirectDrawSurface7::Blt methods signaled the transport of rendered frames to the monitor.</span></span> <span data-ttu-id="c8333-129">Direct3D 9 將這些 Api 群組折迭成兩種主要方法：重設和呈現。</span><span class="sxs-lookup"><span data-stu-id="c8333-129">Direct3D 9 collapses these groups of APIs into two main methods, Reset and Present.</span></span> <span data-ttu-id="c8333-130">重設 subsumes SetCooperativeLevel、SetDisplayMode、CreateSurface 和某些要翻轉的參數。</span><span class="sxs-lookup"><span data-stu-id="c8333-130">Reset subsumes SetCooperativeLevel, SetDisplayMode, CreateSurface, and some of the parameters to flip.</span></span> <span data-ttu-id="c8333-131">提供 array.blit 的 subsumes flip 和簡報用途。</span><span class="sxs-lookup"><span data-stu-id="c8333-131">Present subsumes flip and the presentation uses of blit.</span></span>

 

<span data-ttu-id="c8333-132">[**IDirect3D9：： CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)的呼叫代表裝置的隱含重設。</span><span class="sxs-lookup"><span data-stu-id="c8333-132">A call to [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) represents an implicit reset of the device.</span></span> <span data-ttu-id="c8333-133">Direct3D 9 API 沒有主要表面的概念;您無法建立代表主要表面的物件。</span><span class="sxs-lookup"><span data-stu-id="c8333-133">The Direct3D 9 API has no notion of a primary surface; you cannot create an object that represents the primary surface.</span></span> <span data-ttu-id="c8333-134">它會被視為裝置的內部屬性。</span><span class="sxs-lookup"><span data-stu-id="c8333-134">It is considered to be an internal property of the device.</span></span>

<span data-ttu-id="c8333-135">Gamma 斜坡與交換鏈相關聯，並使用 [**IDirect3DDevice9：： GetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp) 和 [**IDirect3DDevice9：： SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) 方法來操作。</span><span class="sxs-lookup"><span data-stu-id="c8333-135">Gamma ramps are associated with a swap chain and are manipulated with the [**IDirect3DDevice9::GetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp) and [**IDirect3DDevice9::SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8333-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="c8333-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8333-137">呈現場景</span><span class="sxs-lookup"><span data-stu-id="c8333-137">Presenting a Scene</span></span>](presenting-a-scene.md)
</dt> </dl>

 

 
