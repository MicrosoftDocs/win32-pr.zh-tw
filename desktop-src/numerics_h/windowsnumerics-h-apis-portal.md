---
title: windowsnumerics .h Api
description: Windowsnumerics 標頭檔會在 Windows. .h 命名空間中定義 c + + 向量和矩陣類型。 它會將來自 Windows 的結構擴充為一系列數學運算子和函式。
ms.assetid: 7aa15f80-c440-4dcb-a9a6-f1000a3a95da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 268caf0a0215c3d25a86a22fb51204472af481fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682931"
---
# <a name="windowsnumericsh-apis"></a><span data-ttu-id="3c6c1-104">windowsnumerics .h Api</span><span class="sxs-lookup"><span data-stu-id="3c6c1-104">windowsnumerics.h APIs</span></span>

<span data-ttu-id="3c6c1-105">Windowsnumerics 標頭檔會在 [**Windows.**](/uwp/api/Windows.Foundation.Numerics) .h 命名空間中定義 c + + 向量和矩陣類型。</span><span class="sxs-lookup"><span data-stu-id="3c6c1-105">The windowsnumerics.h header file defines C++ vector and matrix types in the [**Windows.Foundation.Numerics**](/uwp/api/Windows.Foundation.Numerics) namespace.</span></span> <span data-ttu-id="3c6c1-106">它會將來自 **Windows** 的結構擴充為一系列數學運算子和函式。</span><span class="sxs-lookup"><span data-stu-id="3c6c1-106">It extends the structs from **Windows.Foundation.Numerics** with a range of mathematical operators and functions.</span></span>

<span data-ttu-id="3c6c1-107">這個命名空間僅適用于 c + +。</span><span class="sxs-lookup"><span data-stu-id="3c6c1-107">This namespace is available only in C++.</span></span> <span data-ttu-id="3c6c1-108">它的 .NET 對等專案是 [system.object](/dotnet/api/system.numerics?view=netframework-4.8)。</span><span class="sxs-lookup"><span data-stu-id="3c6c1-108">Its .NET equivalent is [System.Numerics](/dotnet/api/system.numerics?view=netframework-4.8).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3c6c1-109">本節內容</span><span class="sxs-lookup"><span data-stu-id="3c6c1-109">In this section</span></span>

| <span data-ttu-id="3c6c1-110">主題</span><span class="sxs-lookup"><span data-stu-id="3c6c1-110">Topic</span></span> | <span data-ttu-id="3c6c1-111">描述</span><span class="sxs-lookup"><span data-stu-id="3c6c1-111">Description</span></span> |
|-|-|
| [<span data-ttu-id="3c6c1-112">**float2 結構**</span><span class="sxs-lookup"><span data-stu-id="3c6c1-112">**float2 structure**</span></span>](float2-structure.md) | <span data-ttu-id="3c6c1-113">具有兩個元件的向量。</span><span class="sxs-lookup"><span data-stu-id="3c6c1-113">A vector with two components.</span></span> |
| [<span data-ttu-id="3c6c1-114">**float3 結構**</span><span class="sxs-lookup"><span data-stu-id="3c6c1-114">**float3 structure**</span></span>](float3-structure.md) | <span data-ttu-id="3c6c1-115">具有三個元件的向量。</span><span class="sxs-lookup"><span data-stu-id="3c6c1-115">A vector with three components.</span></span> |
| [<span data-ttu-id="3c6c1-116">**float3x2 結構**</span><span class="sxs-lookup"><span data-stu-id="3c6c1-116">**float3x2 structure**</span></span>](float3x2-structure.md) | <span data-ttu-id="3c6c1-117">用於2D 轉換的3x2 矩陣。</span><span class="sxs-lookup"><span data-stu-id="3c6c1-117">A 3x2 matrix, used for 2D transforms.</span></span> |
| [<span data-ttu-id="3c6c1-118">**float4 結構**</span><span class="sxs-lookup"><span data-stu-id="3c6c1-118">**float4 structure**</span></span>](float4-structure.md) | <span data-ttu-id="3c6c1-119">具有四個元件的向量。</span><span class="sxs-lookup"><span data-stu-id="3c6c1-119">A vector with four components.</span></span> |
| [<span data-ttu-id="3c6c1-120">**float4x4 結構**</span><span class="sxs-lookup"><span data-stu-id="3c6c1-120">**float4x4 structure**</span></span>](float4x4-structure.md) | <span data-ttu-id="3c6c1-121">4x4 矩陣，用於3D 轉換。</span><span class="sxs-lookup"><span data-stu-id="3c6c1-121">A 4x4 matrix, used for 3D transforms.</span></span> |
| [<span data-ttu-id="3c6c1-122">**平面結構**</span><span class="sxs-lookup"><span data-stu-id="3c6c1-122">**plane structure**</span></span>](plane-structure.md) | <span data-ttu-id="3c6c1-123">此結構代表使用3D 向量法線和距離值的平面。</span><span class="sxs-lookup"><span data-stu-id="3c6c1-123">This structure represents a plane using a 3D vector normal and a distance value.</span></span> |
| [<span data-ttu-id="3c6c1-124">**四元數結構**</span><span class="sxs-lookup"><span data-stu-id="3c6c1-124">**quaternion structure**</span></span>](quaternion-structure.md) | <span data-ttu-id="3c6c1-125">用來表示旋轉的四個維度向量。</span><span class="sxs-lookup"><span data-stu-id="3c6c1-125">A four dimensional vector, used to represent a rotation.</span></span> |
| [<span data-ttu-id="3c6c1-126">**Windows 數值和 DirectXMath interop Api**</span><span class="sxs-lookup"><span data-stu-id="3c6c1-126">**Windows numerics and DirectXMath interop APIs**</span></span>](windows-numerics-and-directxmath-interop-apis.md) | <span data-ttu-id="3c6c1-127">這些函式會將 DirectXMath SIMD 型別 [XMVECTOR](../dxmath/xmvector-data-type.md)和 [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)中的 SIMD [**類型轉換成和。**](/uwp/api/Windows.Foundation.Numerics)</span><span class="sxs-lookup"><span data-stu-id="3c6c1-127">These functions convert [**Windows.Foundation.Numerics**](/uwp/api/Windows.Foundation.Numerics) types to and from the DirectXMath SIMD types [XMVECTOR](../dxmath/xmvector-data-type.md) and [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span> |