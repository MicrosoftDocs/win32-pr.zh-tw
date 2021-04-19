---
description: Direct3D 是一個低層級的 API，用來繪製具有轉譯管線的基本專案，或使用計算著色器執行平行作業。
ms.assetid: 55063BF2-34A3-4E56-882C-86F0949DE557
title: 開始使用 Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2b5a579b589a747c4e7640b3c868d488a7e58f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976933"
---
# <a name="getting-started-with-direct3d"></a><span data-ttu-id="163aa-103">開始使用 Direct3D</span><span class="sxs-lookup"><span data-stu-id="163aa-103">Getting started with Direct3D</span></span>

<span data-ttu-id="163aa-104">Direct3D 是一個低層級的 API，用來繪製具有轉譯管線的基本專案，或是用來執行具有計算著色器的平行作業。</span><span class="sxs-lookup"><span data-stu-id="163aa-104">Direct3D is a low-level API for drawing primitives with the rendering pipeline, or for performing parallel operations with the compute shader.</span></span>

## <a name="what-is-direct3d"></a><span data-ttu-id="163aa-105">什麼是 Direct3D？</span><span class="sxs-lookup"><span data-stu-id="163aa-105">What is Direct3D?</span></span>

<span data-ttu-id="163aa-106">Direct3D 是低層級的 API，可讓您用來繪製每個框架的三角形、線條或點，或在 GPU 上啟動高度平行的作業。</span><span class="sxs-lookup"><span data-stu-id="163aa-106">Direct3D is a low-level API that you can use to draw triangles, lines, or points per frame, or to start highly parallel operations on the GPU.</span></span>

<span data-ttu-id="163aa-107">Direct3D</span><span class="sxs-lookup"><span data-stu-id="163aa-107">Direct3D:</span></span>

-   <span data-ttu-id="163aa-108">隱藏一致抽象概念背後的不同 GPU 執行。</span><span class="sxs-lookup"><span data-stu-id="163aa-108">Hides different GPU implementations behind a coherent abstraction.</span></span> <span data-ttu-id="163aa-109">但是您仍然需要知道如何繪製3D 圖形。</span><span class="sxs-lookup"><span data-stu-id="163aa-109">But you still need to know how to draw 3D graphics.</span></span>
-   <span data-ttu-id="163aa-110">是設計來驅動個別的圖形專用處理器。</span><span class="sxs-lookup"><span data-stu-id="163aa-110">Is designed to drive a separate graphics-specific processor.</span></span> <span data-ttu-id="163aa-111">較新的 Gpu 具有數百個或數千個平行處理器。</span><span class="sxs-lookup"><span data-stu-id="163aa-111">Newer GPUs have hundreds or thousands of parallel processors.</span></span>
-   <span data-ttu-id="163aa-112">強調平行處理。</span><span class="sxs-lookup"><span data-stu-id="163aa-112">Emphasizes parallel processing.</span></span> <span data-ttu-id="163aa-113">您可以設定一連串的轉譯或計算狀態，然後開始操作。</span><span class="sxs-lookup"><span data-stu-id="163aa-113">You set up a bunch of rendering or compute state and then start an operation.</span></span> <span data-ttu-id="163aa-114">您不會等待作業立即提出意見反應。</span><span class="sxs-lookup"><span data-stu-id="163aa-114">You don't wait for immediate feedback from the operation.</span></span> <span data-ttu-id="163aa-115">您不會混合 CPU 和 GPU 作業。</span><span class="sxs-lookup"><span data-stu-id="163aa-115">You don't mix CPU and GPU operations.</span></span>

## <a name="which-direct3d-apis-can-you-use"></a><span data-ttu-id="163aa-116">您可以使用哪些 Direct3D Api？</span><span class="sxs-lookup"><span data-stu-id="163aa-116">Which Direct3D APIs can you use?</span></span>

<span data-ttu-id="163aa-117">您所選擇的 Direct3D Api 取決於您要撰寫的應用程式樣式。</span><span class="sxs-lookup"><span data-stu-id="163aa-117">The Direct3D APIs that you choose depend on the style of app you want to write.</span></span>

-   <span data-ttu-id="163aa-118">如果您想要撰寫 UWP 應用程式，請使用 Direct3D 11、DXGI 和 HLSL Api 的子集。</span><span class="sxs-lookup"><span data-stu-id="163aa-118">If you want to write a UWP app, use a subset of Direct3D 11, DXGI, and HLSL APIs.</span></span> <span data-ttu-id="163aa-119">如需這些 Api 的清單，請參閱 [適用于 UWP 應用程式的 Win32 和 COM api](/uwp/win32-and-com/win32-and-com-for-uwp-apps)。</span><span class="sxs-lookup"><span data-stu-id="163aa-119">For a list of these APIs, see [Win32 and COM APIs for UWP apps](/uwp/win32-and-com/win32-and-com-for-uwp-apps).</span></span> <span data-ttu-id="163aa-120">若要瞭解如何撰寫 Direct3D 11 Windows Store 應用程式，請參閱 [使用 DirectX 建立3d 圖形](/previous-versions/windows/apps/hh465137(v=win.10))。</span><span class="sxs-lookup"><span data-stu-id="163aa-120">To learn how to write a Direct3D 11 Windows Store app, see [Create 3D graphics with DirectX](/previous-versions/windows/apps/hh465137(v=win.10)).</span></span>
-   <span data-ttu-id="163aa-121">如果您撰寫桌面應用程式，您可以使用一組完整的 Direct3D 11、DXGI 和 HLSL Api。</span><span class="sxs-lookup"><span data-stu-id="163aa-121">If you write a desktop app, you can use the full set of Direct3D 11, DXGI, and HLSL APIs.</span></span>
-   <span data-ttu-id="163aa-122">從 Windows 8 開始，我們不會再主動支援適用于傳統型應用程式的「使用」架構。</span><span class="sxs-lookup"><span data-stu-id="163aa-122">Starting with Windows 8, we no longer actively support the XNA framework for desktop apps.</span></span> <span data-ttu-id="163aa-123">但是，Windows Store 應用程式、UWP 應用程式和桌面應用程式可以使用完整的 [XAudio2](/windows/desktop/xaudio2/xaudio2-apis-portal) 和 [DirectXMath](/windows/desktop/dxmath/directxmath-portal) api 集。</span><span class="sxs-lookup"><span data-stu-id="163aa-123">But Windows Store apps, UWP apps, and desktop apps can use the full set of the [XAudio2](/windows/desktop/xaudio2/xaudio2-apis-portal) and [DirectXMath](/windows/desktop/dxmath/directxmath-portal) APIs.</span></span> <span data-ttu-id="163aa-124">傳統型應用程式可以使用一組完整的 [XInput](/windows/desktop/xinput/xinput-game-controller-apis-portal) api，而 Windows Store 應用程式和 UWP 應用程式可以使用大部分的 XInput api;如需詳細資訊，請參閱 [XInput 版本](/windows/desktop/xinput/xinput-versions)。</span><span class="sxs-lookup"><span data-stu-id="163aa-124">Desktop apps can use the full set of the [XInput](/windows/desktop/xinput/xinput-game-controller-apis-portal) APIs, while Windows Store apps and UWP apps can use most of the XInput APIs; for more info, see [XInput Versions](/windows/desktop/xinput/xinput-versions).</span></span>

## <a name="which-direct3d-version"></a><span data-ttu-id="163aa-125">哪個 Direct3D 版本？</span><span class="sxs-lookup"><span data-stu-id="163aa-125">Which Direct3D version?</span></span>

<span data-ttu-id="163aa-126">您所選擇的 Direct3D API 版本取決於您要作為目標的作業系統和硬體層級。</span><span class="sxs-lookup"><span data-stu-id="163aa-126">The Direct3D API version that you choose depends on the operating system and hardware level that you want to target.</span></span>

-   <span data-ttu-id="163aa-127">如果您想要以 Windows 8 和更新版本為目標，請使用 Direct3D 11 Api。</span><span class="sxs-lookup"><span data-stu-id="163aa-127">If you want to target Windows 8 and later, use Direct3D 11 APIs.</span></span>
-   <span data-ttu-id="163aa-128">使用 Direct3D 9 Api 搭配 Windows XP 及更新版本。</span><span class="sxs-lookup"><span data-stu-id="163aa-128">Use Direct3D 9 APIs with Windows XP and later.</span></span> <span data-ttu-id="163aa-129">所有硬體都支援 Direct3D 9 Api （甚至是較新的 Direct3D 11 層級硬體）。</span><span class="sxs-lookup"><span data-stu-id="163aa-129">All hardware supports Direct3D 9 APIs, even newer Direct3D 11-level hardware.</span></span>
-   <span data-ttu-id="163aa-130">使用 Direct3D 10 Api 搭配 Windows Vista 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="163aa-130">Use Direct3D 10 APIs with Windows Vista and later.</span></span> <span data-ttu-id="163aa-131">只有 Direct3D 10 層級和更新版本的硬體支援 Direct3D 10 Api。</span><span class="sxs-lookup"><span data-stu-id="163aa-131">Only Direct3D 10-level and later hardware support Direct3D 10 APIs.</span></span>
-   <span data-ttu-id="163aa-132">使用 Direct3D 10.1 和 Direct3D 11 Api 搭配 Windows 7 及更新版本。</span><span class="sxs-lookup"><span data-stu-id="163aa-132">Use Direct3D 10.1 and Direct3D 11 APIs with Windows 7 and later.</span></span> <span data-ttu-id="163aa-133">您也可以下載 [KB 971644](https://support.microsoft.com/kb/971644)，搭配 Windows Vista 搭配 Service Pack 2 (SP2) 來使用 direct3d 10.1 和 Direct3d 11 api。</span><span class="sxs-lookup"><span data-stu-id="163aa-133">You can also use Direct3D 10.1 and Direct3D 11 APIs with Windows Vista with Service Pack 2 (SP2) by downloading [KB 971644](https://support.microsoft.com/kb/971644).</span></span>

## <a name="direct3d-rendering-pipeline"></a><span data-ttu-id="163aa-134">Direct3D 轉譯管線</span><span class="sxs-lookup"><span data-stu-id="163aa-134">Direct3D Rendering Pipeline</span></span>

<span data-ttu-id="163aa-135">在 Direct3D 轉譯 [管線](./direct3d11/overviews-direct3d-11-graphics-pipeline.md)中，資料會從數個來源（例如，tributaries）進行流動。</span><span class="sxs-lookup"><span data-stu-id="163aa-135">In the Direct3D [rendering pipeline](./direct3d11/overviews-direct3d-11-graphics-pipeline.md), data flows from several sources, like the tributaries of a river.</span></span>

-   <span data-ttu-id="163aa-136">流程的某些部分是可程式化的。</span><span class="sxs-lookup"><span data-stu-id="163aa-136">Some parts of the flow are programmable.</span></span>
-   <span data-ttu-id="163aa-137">有些部分具有旋鈕和撥號。</span><span class="sxs-lookup"><span data-stu-id="163aa-137">Some parts have knobs and dials.</span></span>
-   <span data-ttu-id="163aa-138">資料來源是封包 (頂點的序列串流) 或可編制索引的陣列 (著色器資源) 。</span><span class="sxs-lookup"><span data-stu-id="163aa-138">Sources of data are either serial streams of packets (vertices) or indexable arrays (shader resources).</span></span>
-   <span data-ttu-id="163aa-139">頂點和著色器資源會流入可增強的基本專案。</span><span class="sxs-lookup"><span data-stu-id="163aa-139">Vertices and shader resources flow into primitives, which you can amplify.</span></span>
-   <span data-ttu-id="163aa-140">基本和著色器資源會流入圖元作業。</span><span class="sxs-lookup"><span data-stu-id="163aa-140">Primitives and shader resources flow into pixel operations.</span></span>

## <a name="direct3d-compute-shader"></a><span data-ttu-id="163aa-141">Direct3D 計算著色器</span><span class="sxs-lookup"><span data-stu-id="163aa-141">Direct3D Compute Shader</span></span>

<span data-ttu-id="163aa-142">使用 Direct3D [計算著色器](./direct3d11/direct3d-11-advanced-stages-compute-shader.md)，所有 GPU 的處理器都會平行執行。</span><span class="sxs-lookup"><span data-stu-id="163aa-142">With the Direct3D [compute shader](./direct3d11/direct3d-11-advanced-stages-compute-shader.md), all the GPU's processors execute in parallel.</span></span> <span data-ttu-id="163aa-143">因此，計算著色器的行為就像是 pond。</span><span class="sxs-lookup"><span data-stu-id="163aa-143">So the compute shader behaves more like a pond than a river.</span></span>
