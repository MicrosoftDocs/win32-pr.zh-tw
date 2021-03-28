---
title: 如何建立交換鏈
description: 本主題說明如何建立交換鏈，以封裝兩個或多個用於呈現和顯示的緩衝區。
ms.assetid: 0e290b37-0807-42c7-9e50-fd2db6affb14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8355eafff6e233b89be82fd9e58ca53224248e84
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375981"
---
# <a name="how-to-create-a-swap-chain"></a><span data-ttu-id="cb679-103">如何：建立交換鏈</span><span class="sxs-lookup"><span data-stu-id="cb679-103">How To: Create a Swap Chain</span></span>

<span data-ttu-id="cb679-104">本主題說明如何建立交換鏈，以封裝兩個或多個用於呈現和顯示的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="cb679-104">This topic show how to create a swap chain that encapsulates two or more buffers that are used for rendering and display.</span></span> <span data-ttu-id="cb679-105">它們通常會包含顯示裝置的前端緩衝區，以及做為呈現目標的背景緩衝區。</span><span class="sxs-lookup"><span data-stu-id="cb679-105">They usually contain a front buffer that is presented to the display device and a back buffer that serves as the render target.</span></span> <span data-ttu-id="cb679-106">當立即內容完成轉譯至背景緩衝區之後，交換鏈會藉由交換這兩個緩衝區來呈現後端緩衝區。</span><span class="sxs-lookup"><span data-stu-id="cb679-106">After the immediate context is done rendering to the back buffer, the swap chain presents the back buffer by swapping the two buffers.</span></span>

<span data-ttu-id="cb679-107">交換鏈定義了數種轉譯特性，包括：</span><span class="sxs-lookup"><span data-stu-id="cb679-107">The swap chain defines several rendering characteristics including:</span></span>

-   <span data-ttu-id="cb679-108">轉譯區域的大小。</span><span class="sxs-lookup"><span data-stu-id="cb679-108">The size of the render area.</span></span>
-   <span data-ttu-id="cb679-109">顯示更新率。</span><span class="sxs-lookup"><span data-stu-id="cb679-109">The display refresh rate.</span></span>
-   <span data-ttu-id="cb679-110">顯示模式。</span><span class="sxs-lookup"><span data-stu-id="cb679-110">The display mode.</span></span>
-   <span data-ttu-id="cb679-111">介面格式。</span><span class="sxs-lookup"><span data-stu-id="cb679-111">The surface format.</span></span>

<span data-ttu-id="cb679-112">藉由填妥 [**DXGI \_ 交換 \_ 鏈 \_ DESC**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) 結構並初始化 [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) 介面，來定義交換鏈的特性。</span><span class="sxs-lookup"><span data-stu-id="cb679-112">Define the characteristics of the swap chain by filling in a [**DXGI\_SWAP\_CHAIN\_DESC**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) structure and initializing an [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) interface.</span></span> <span data-ttu-id="cb679-113">藉由呼叫 [**IDXGIFactory：： CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) 或 [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain)，初始化交換鏈。</span><span class="sxs-lookup"><span data-stu-id="cb679-113">Initialize a swap chain by calling [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) or [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span></span>

## <a name="create-a-device-and-a-swap-chain"></a><span data-ttu-id="cb679-114">建立裝置和交換鏈</span><span class="sxs-lookup"><span data-stu-id="cb679-114">Create a device and a swap chain</span></span>

<span data-ttu-id="cb679-115">若要初始化裝置和交換鏈，請使用下列兩個函式的其中一種：</span><span class="sxs-lookup"><span data-stu-id="cb679-115">To initialize a device and swap chain, use one of the following two functions:</span></span>

-   <span data-ttu-id="cb679-116">當您想要在裝置初始化時同時初始化交換鏈時，請使用 [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) 函數。</span><span class="sxs-lookup"><span data-stu-id="cb679-116">Use the [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) function when you want to initialize the swap chain at the same time as device initialization.</span></span> <span data-ttu-id="cb679-117">這通常是最簡單的選項。</span><span class="sxs-lookup"><span data-stu-id="cb679-117">This usually is the easiest option.</span></span>

-   <span data-ttu-id="cb679-118">當您已經使用 [**IDXGIFactory：： CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain)建立交換鏈時，請使用 [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice)函數。</span><span class="sxs-lookup"><span data-stu-id="cb679-118">Use the [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) function when you have already created a swap chain using [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb679-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="cb679-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb679-120">裝置</span><span class="sxs-lookup"><span data-stu-id="cb679-120">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> <dt>

[<span data-ttu-id="cb679-121">如何使用 Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="cb679-121">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 