---
title: 使用著色器連結
description: 我們會示範如何建立先行編譯的 HLSL 函式、將它們封裝至程式庫，並在執行時間將它們連結到完整的著色器。
ms.assetid: 3A1597FF-F848-415E-BDF8-199C69C05C3B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7528415f1bedb0364a9c4b09126a983222fc42b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103683011"
---
# <a name="using-shader-linking"></a><span data-ttu-id="10878-103">使用著色器連結</span><span class="sxs-lookup"><span data-stu-id="10878-103">Using shader linking</span></span>

<span data-ttu-id="10878-104">我們會示範如何建立先行編譯的 HLSL 函式、將它們封裝至程式庫，並在執行時間將它們連結到完整的著色器。</span><span class="sxs-lookup"><span data-stu-id="10878-104">We show how to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run-time.</span></span> <span data-ttu-id="10878-105">從 Windows 8.1 開始支援著色器連結。</span><span class="sxs-lookup"><span data-stu-id="10878-105">Shader linking is supported starting with Windows 8.1.</span></span>

<span data-ttu-id="10878-106">**目標：** 瞭解如何使用著色器連結。</span><span class="sxs-lookup"><span data-stu-id="10878-106">**Objective:** Learn how to use shader linking.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="10878-107">必要條件</span><span class="sxs-lookup"><span data-stu-id="10878-107">Prerequisites</span></span>

<span data-ttu-id="10878-108">我們假設您熟悉 C++。</span><span class="sxs-lookup"><span data-stu-id="10878-108">We assume that you are familiar with C++.</span></span> <span data-ttu-id="10878-109">您還需要圖形程式設計概念的基本經驗。</span><span class="sxs-lookup"><span data-stu-id="10878-109">You also need basic experience with graphics programming concepts.</span></span>

<span data-ttu-id="10878-110">**完成的總時間：** 60 分鐘。</span><span class="sxs-lookup"><span data-stu-id="10878-110">**Total time to complete:** 60 minutes.</span></span>

## <a name="where-to-go-from-here"></a><span data-ttu-id="10878-111">現在該如何開始</span><span class="sxs-lookup"><span data-stu-id="10878-111">Where to go from here</span></span>

<span data-ttu-id="10878-112">另請參閱 [HLSL 編譯器 api](dx-graphics-d3dcompiler-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="10878-112">Also see [HLSL compiler APIs](dx-graphics-d3dcompiler-reference.md).</span></span>

<span data-ttu-id="10878-113">我們將示範如何：</span><span class="sxs-lookup"><span data-stu-id="10878-113">We show you how to:</span></span>

-   <span data-ttu-id="10878-114">編譯著色器程式碼</span><span class="sxs-lookup"><span data-stu-id="10878-114">Compile your shader code</span></span>
-   <span data-ttu-id="10878-115">將已編譯的程式碼載入著色器程式庫</span><span class="sxs-lookup"><span data-stu-id="10878-115">Load the compiled code into a shader library</span></span>
-   <span data-ttu-id="10878-116">將來源位置的資源系結至目的地位置</span><span class="sxs-lookup"><span data-stu-id="10878-116">Bind the resources from source slots to destination slots</span></span>
-   <span data-ttu-id="10878-117">建立著色器的函式連結圖形 (FLGs) </span><span class="sxs-lookup"><span data-stu-id="10878-117">Construct function-linking-graphs (FLGs) for shaders</span></span>
-   <span data-ttu-id="10878-118">連結著色器圖形與著色器程式庫，以產生 Direct3D 執行時間可使用的著色器 blob</span><span class="sxs-lookup"><span data-stu-id="10878-118">Link shader graphs with a shader library to produce a shader blob that the Direct3D runtime can use</span></span>

<span data-ttu-id="10878-119">接下來我們要建立著色器程式庫，並將來源位置的資源系結至目的地位置。</span><span class="sxs-lookup"><span data-stu-id="10878-119">Next we make a shader library and bind resources from source slots to destination slots.</span></span>

[<span data-ttu-id="10878-120">封裝著色器程式庫</span><span class="sxs-lookup"><span data-stu-id="10878-120">Packaging a shader library</span></span>](pachaging-a-shader-library.md)

## <a name="related-topics"></a><span data-ttu-id="10878-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="10878-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10878-122">HLSL 的程式設計指南</span><span class="sxs-lookup"><span data-stu-id="10878-122">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> <dt>

[<span data-ttu-id="10878-123">Direct3D 11 圖形</span><span class="sxs-lookup"><span data-stu-id="10878-123">Direct3D 11 Graphics</span></span>](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
</dt> <dt>

[<span data-ttu-id="10878-124">DXGI</span><span class="sxs-lookup"><span data-stu-id="10878-124">DXGI</span></span>](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)
</dt> </dl>

 

 