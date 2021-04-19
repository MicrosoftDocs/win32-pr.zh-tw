---
title: Direct3D 12 參考
description: 本節涵蓋適用于 Direct3D 12 圖形程式設計的 Api。
ms.assetid: C4958E15-28BA-4275-882B-244D4CC22E1A
ms.localizationpriority: low
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: 1b430449392bafc8caf89f908d2d6102df35259d
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "106979662"
---
# <a name="direct3d-12-reference"></a><span data-ttu-id="af77f-103">Direct3D 12 參考</span><span class="sxs-lookup"><span data-stu-id="af77f-103">Direct3D 12 reference</span></span>

<span data-ttu-id="af77f-104">本節涵蓋適用于 Direct3D 12 圖形程式設計的 Api。</span><span class="sxs-lookup"><span data-stu-id="af77f-104">This section covers APIs for Direct3D 12-based graphics programming.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="af77f-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="af77f-105">In this section</span></span>

| <span data-ttu-id="af77f-106">主題</span><span class="sxs-lookup"><span data-stu-id="af77f-106">Topic</span></span> | <span data-ttu-id="af77f-107">描述</span><span class="sxs-lookup"><span data-stu-id="af77f-107">Description</span></span> |
|-|-|
| [<span data-ttu-id="af77f-108">介面階層</span><span class="sxs-lookup"><span data-stu-id="af77f-108">Interface hierarchy</span></span>](interface-hierarchy.md) | <span data-ttu-id="af77f-109">此圖顯示介面繼承階層。</span><span class="sxs-lookup"><span data-stu-id="af77f-109">The diagram shows the interface inheritance hierarchy.</span></span> |
| [<span data-ttu-id="af77f-110">D3D12 參考中的範例程式碼</span><span class="sxs-lookup"><span data-stu-id="af77f-110">Example code in the D3D12 reference</span></span>](notes-on-example-code.md) | <span data-ttu-id="af77f-111">說明如何使用 Direct3D 12 檔中的範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="af77f-111">Explains the use of example code in the Direct3D 12 documentation.</span></span> |
| [<span data-ttu-id="af77f-112">核心參考</span><span class="sxs-lookup"><span data-stu-id="af77f-112">Core reference</span></span>](direct3d-12-core-reference.md) | <span data-ttu-id="af77f-113">本節涵蓋 d3d12 中宣告的 Direct3D 12 Api，包括適用于緩衝區、材質和 views 的 Api。</span><span class="sxs-lookup"><span data-stu-id="af77f-113">This section covers Direct3D 12 APIs declared in d3d12.h, including APIs for buffers, textures, and views.</span></span> |
| [<span data-ttu-id="af77f-114">Debug 圖層參考</span><span class="sxs-lookup"><span data-stu-id="af77f-114">Debug layer reference</span></span>](direct3d-12-sdklayers-reference.md) | <span data-ttu-id="af77f-115">本節涵蓋 d3d12sdklayers 中宣告的 Direct3D 12 Api，此 Api 適用于 debug 層。</span><span class="sxs-lookup"><span data-stu-id="af77f-115">This section covers Direct3D 12 APIs declared in d3d12sdklayers.h, which is for the debug layer.</span></span> |
| [<span data-ttu-id="af77f-116">著色器參考</span><span class="sxs-lookup"><span data-stu-id="af77f-116">Shader reference</span></span>](d3d12-graphics-reference-shader-reference.md) | <span data-ttu-id="af77f-117">本節涵蓋 d3d12shader 中宣告的 Direct3D 12 Api，有助於建立及管理可程式化著色器。</span><span class="sxs-lookup"><span data-stu-id="af77f-117">This section covers Direct3D 12 APIs declared in d3d12shader.h, which helps create and manage programmable shaders.</span></span> <span data-ttu-id="af77f-118">著色器是可執行檔程式，以獨佔方式使用 HLSL 進行程式設計。</span><span class="sxs-lookup"><span data-stu-id="af77f-118">Shaders are executable programs that are programmed exclusively using HLSL.</span></span> |
| [<span data-ttu-id="af77f-119">11on12 參考</span><span class="sxs-lookup"><span data-stu-id="af77f-119">11on12 reference</span></span>](direct3d-11on12-reference.md) | <span data-ttu-id="af77f-120">本節涵蓋 d3d11on12 中宣告的 Direct3D 12 Api。</span><span class="sxs-lookup"><span data-stu-id="af77f-120">This section covers Direct3D 12 APIs declared in d3d11on12.h.</span></span> <span data-ttu-id="af77f-121">Direct3D 11on12 Api 可協助您以累加方式將程式碼從 D3D11 移植到 D3D12。</span><span class="sxs-lookup"><span data-stu-id="af77f-121">The Direct3D 11on12 APIs help you port code incrementally from D3D11 to D3D12.</span></span> |
| [<span data-ttu-id="af77f-122">直接 Machine Learning (DirectML) 參考</span><span class="sxs-lookup"><span data-stu-id="af77f-122">Direct Machine Learning (DirectML) reference</span></span>](direct3d-directml-reference.md) | <span data-ttu-id="af77f-123">本節涵蓋在 DirectML 中宣告的直接 Machine Learning (DirectML) Api。</span><span class="sxs-lookup"><span data-stu-id="af77f-123">This section covers Direct Machine Learning (DirectML) APIs declared in directml.h.</span></span> |
| [<span data-ttu-id="af77f-124">D3D12 的 Helper 結構和函式</span><span class="sxs-lookup"><span data-stu-id="af77f-124">Helper structures and functions for D3D12</span></span>](helper-structures-and-functions-for-d3d12.md) | <span data-ttu-id="af77f-125">這些 helper 結構和 helper 函式是在 **d3dx12** 中宣告。</span><span class="sxs-lookup"><span data-stu-id="af77f-125">These helper structures and helper functions are declared in **d3dx12.h**.</span></span> |
| [<span data-ttu-id="af77f-126">Direct3D 12 傳回碼</span><span class="sxs-lookup"><span data-stu-id="af77f-126">Direct3D 12 return codes</span></span>](d3d12-graphics-reference-returnvalues.md) | <span data-ttu-id="af77f-127">以下是來自 API 函數的傳回碼。</span><span class="sxs-lookup"><span data-stu-id="af77f-127">The following are return codes from API functions.</span></span> |
| [<span data-ttu-id="af77f-128">Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="af77f-128">Direct3D 12 Raytracing</span></span>](direct3d-12-raytracing.md) | <span data-ttu-id="af77f-129">本節提供與 Direct3D 12 Raytracing 相關之 Api 的連結。</span><span class="sxs-lookup"><span data-stu-id="af77f-129">This section provides links to APIs that are relevant to Direct3D 12 Raytracing.</span></span> |
| [<span data-ttu-id="af77f-130">Windows 7 上的 Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="af77f-130">Direct3D 12 On Windows 7</span></span>](direct3d-12on7-reference.md) | <span data-ttu-id="af77f-131">本節涵蓋中宣告的 Direct3D 12 Api `d3d12downlevel.h` ，僅供 Windows 7 使用。</span><span class="sxs-lookup"><span data-stu-id="af77f-131">This section covers Direct3D 12 APIs declared in `d3d12downlevel.h`, for use solely on Windows 7.</span></span> <span data-ttu-id="af77f-132">如需詳細資訊，請參閱 [將 DirectX 12 遊戲移植到 Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/) 。</span><span class="sxs-lookup"><span data-stu-id="af77f-132">See [Porting DirectX 12 games to Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/) for more details.</span></span> |

## <a name="related-topics"></a><span data-ttu-id="af77f-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="af77f-133">Related topics</span></span>

* [<span data-ttu-id="af77f-134">Direct3D 12 圖形</span><span class="sxs-lookup"><span data-stu-id="af77f-134">Direct3D 12 graphics</span></span>](direct3d-12-graphics.md)
* [<span data-ttu-id="af77f-135">Direct3D 12 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="af77f-135">Direct3D 12 programming guide</span></span>](directx-12-programming-guide.md)
* [<span data-ttu-id="af77f-136">DirectX advanced learning 影片教學課程</span><span class="sxs-lookup"><span data-stu-id="af77f-136">DirectX advanced learning video tutorials</span></span>](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA)
