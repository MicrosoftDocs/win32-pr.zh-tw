---
description: Direct3D 是一個低層級的 API，用來繪製具有轉譯管線的基本專案，或是用來執行具有計算著色器的平行作業。
ms.assetid: 193640FE-7E88-4BC4-B4CD-867169375F2B
title: Direct3D
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: f4fa0c25ab169b0faae9c467c437b96d0453cd34
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110549"
---
# <a name="direct3d"></a><span data-ttu-id="11b3e-103">Direct3D</span><span class="sxs-lookup"><span data-stu-id="11b3e-103">Direct3D</span></span>

<span data-ttu-id="11b3e-104">Direct3D 是一個低層級的 API，用來繪製具有轉譯管線的基本專案，或是用來執行具有計算著色器的平行作業。</span><span class="sxs-lookup"><span data-stu-id="11b3e-104">Direct3D is a low-level API for drawing primitives with the rendering pipeline, or for performing parallel operations with the compute shader.</span></span> <span data-ttu-id="11b3e-105">如需詳細資訊，請參閱下列內容。</span><span class="sxs-lookup"><span data-stu-id="11b3e-105">See the content below for more information.</span></span>

<span data-ttu-id="11b3e-106">如需取得和安裝 Direct3D 的詳細資訊，請參閱 [direct3d 12 程式設計環境設定](./direct3d12/directx-12-programming-environment-set-up.md)。</span><span class="sxs-lookup"><span data-stu-id="11b3e-106">For info about obtaining and installing Direct3D, see [Direct3D 12 programming environment setup](./direct3d12/directx-12-programming-environment-set-up.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="11b3e-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="11b3e-107">In this section</span></span>

| <span data-ttu-id="11b3e-108">主題</span><span class="sxs-lookup"><span data-stu-id="11b3e-108">Topic</span></span> | <span data-ttu-id="11b3e-109">描述</span><span class="sxs-lookup"><span data-stu-id="11b3e-109">Description</span></span> |
|-|-|
| [<span data-ttu-id="11b3e-110">開始使用 Direct3D</span><span class="sxs-lookup"><span data-stu-id="11b3e-110">Getting started with Direct3D</span></span>](./getting-started-with-direct3d.md) | <span data-ttu-id="11b3e-111">討論 Direct3D 更深入、不同的應用程式模型、不同的版本、轉譯和計算。</span><span class="sxs-lookup"><span data-stu-id="11b3e-111">Discusses Direct3D in more depth, different application models, different versions, rendering, and compute.</span></span> |
| [<span data-ttu-id="11b3e-112">Direct3D 12 圖形</span><span class="sxs-lookup"><span data-stu-id="11b3e-112">Direct3D 12 graphics</span></span>](./direct3d12/direct3d-12-graphics.md) | <span data-ttu-id="11b3e-113">Direct3D 12 提供 API 和平臺，可讓您的應用程式利用配備一或多個 Direct3D 12 相容 Gpu 之電腦的圖形和運算功能。</span><span class="sxs-lookup"><span data-stu-id="11b3e-113">Direct3D 12 provides an API and platform that allows your application to take advantage of the graphics and computing capabilities of PCs equipped with one or more Direct3D 12-compatible GPUs.</span></span> |
| [<span data-ttu-id="11b3e-114">Direct3D 11 圖形</span><span class="sxs-lookup"><span data-stu-id="11b3e-114">Direct3D 11 Graphics</span></span>](./direct3d11/atoc-dx-graphics-direct3d-11.md) | <span data-ttu-id="11b3e-115">您可以使用 Microsoft Direct3D 11 圖形來建立適用于遊戲和科學和桌面應用程式的立體圖形。</span><span class="sxs-lookup"><span data-stu-id="11b3e-115">You can use Microsoft Direct3D 11 graphics to create 3-D graphics for games and scientific and desktop applications.</span></span> |
| [<span data-ttu-id="11b3e-116">DXGI</span><span class="sxs-lookup"><span data-stu-id="11b3e-116">DXGI</span></span>](./direct3ddxgi/dx-graphics-dxgi.md) | <span data-ttu-id="11b3e-117">DXGI 會處理列舉圖形介面卡、列舉顯示模式、選取緩衝區格式、在進程之間共用資源，以及將轉譯的畫面格呈現至視窗或監視器以供顯示。</span><span class="sxs-lookup"><span data-stu-id="11b3e-117">DXGI handles enumerating graphics adapters, enumerating display modes, selecting buffer formats, sharing resources between processes, and presenting rendered frames to a window or monitor for display.</span></span> |
| [<span data-ttu-id="11b3e-118">HLSL</span><span class="sxs-lookup"><span data-stu-id="11b3e-118">HLSL</span></span>](./direct3dhlsl/dx-graphics-hlsl.md) | <span data-ttu-id="11b3e-119">HLSL 是適用于 DirectX 的高階著色器語言。</span><span class="sxs-lookup"><span data-stu-id="11b3e-119">HLSL is the high-level shader language for DirectX.</span></span> <span data-ttu-id="11b3e-120">您可以使用 HLSL，為 Direct3D 管線建立類似 C 的可程式化著色器。</span><span class="sxs-lookup"><span data-stu-id="11b3e-120">Using HLSL, you can create C-like programmable shaders for the Direct3D pipeline.</span></span> |
| [<span data-ttu-id="11b3e-121">Dds</span><span class="sxs-lookup"><span data-stu-id="11b3e-121">DDS</span></span>](./direct3ddds/dx-graphics-dds.md) | <span data-ttu-id="11b3e-122"> (DDS) 的 DirectDraw 表面檔案格式支援未壓縮和壓縮的 (DXTn) 紋理、mipmap、cube 地圖和磁片區對應。</span><span class="sxs-lookup"><span data-stu-id="11b3e-122">The DirectDraw surface file format (DDS) supports uncompressed and compressed (DXTn) textures, mipmaps, cube maps, and volume maps.</span></span> <span data-ttu-id="11b3e-123">它受到 DirectXTex、DirectXTK、舊版 D3DX 和其他 DirectX 工具的支援。</span><span class="sxs-lookup"><span data-stu-id="11b3e-123">It's supported by DirectXTex, DirectXTK, legacy D3DX, and other DirectX tools.</span></span> |
