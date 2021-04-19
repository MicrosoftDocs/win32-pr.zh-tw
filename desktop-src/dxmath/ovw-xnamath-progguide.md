---
description: DirectXMath 提供針對 Windows 優化的數學解決方案。
ms.assetid: c2a64435-b2fb-3638-2eea-3ed52f4c7cd5
title: DirectXMath 程式設計指南
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df406787776f9fa5d1786e6ed6c5998e27a1c059
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974174"
---
# <a name="directxmath-programming-guide"></a><span data-ttu-id="e4ce9-103">DirectXMath 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="e4ce9-103">DirectXMath programming guide</span></span>

<span data-ttu-id="e4ce9-104">DirectXMath 提供針對 Windows 優化的數學解決方案。</span><span class="sxs-lookup"><span data-stu-id="e4ce9-104">DirectXMath provides a math solution optimized for Windows.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e4ce9-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="e4ce9-105">In this section</span></span>



| <span data-ttu-id="e4ce9-106">主題</span><span class="sxs-lookup"><span data-stu-id="e4ce9-106">Topic</span></span>                                                             | <span data-ttu-id="e4ce9-107">描述</span><span class="sxs-lookup"><span data-stu-id="e4ce9-107">Description</span></span>                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4ce9-108">快速入門</span><span class="sxs-lookup"><span data-stu-id="e4ce9-108">Getting Started</span></span>](pg-xnamath-getting-started.md)<br/>      | <span data-ttu-id="e4ce9-109">DirectXMath 程式庫會針對單精確度浮點數向量（ (2D、3D 和 4D) 或矩陣 (3 ×3和4× 4) ），來實作為算術和線性代數運算的最佳和可移植介面。</span><span class="sxs-lookup"><span data-stu-id="e4ce9-109">The DirectXMath Library implements an optimal and portable interface for arithmetic and linear algebra operations on single-precision floating-point vectors (2D, 3D, and 4D) or matrices (3×3 and 4×4).</span></span> <br/>                                                    |
| [<span data-ttu-id="e4ce9-110">新功能</span><span class="sxs-lookup"><span data-stu-id="e4ce9-110">What's New</span></span>](pg-xnamath-whatsnew.md)<br/>                  | <span data-ttu-id="e4ce9-111">DirectXMath 程式庫是以「操作 [數學 c + + SIMD 程式庫」2.04 版](https://walbourn.github.io/)為基礎。</span><span class="sxs-lookup"><span data-stu-id="e4ce9-111">The DirectXMath library is based on the [XNA Math C++ SIMD library version 2.04](https://walbourn.github.io/).</span></span> <span data-ttu-id="e4ce9-112">在此，我們將說明 DirectXMath 與未通過的數學有何不同，以及 DirectXMath 版本有何不同。</span><span class="sxs-lookup"><span data-stu-id="e4ce9-112">Here we describe how DirectXMath differs from XNA Math and how DirectXMath versions differ.</span></span> <br/> |
| [<span data-ttu-id="e4ce9-113">程式碼遷移</span><span class="sxs-lookup"><span data-stu-id="e4ce9-113">Code Migration</span></span>](pg-xnamath-migration.md)<br/>             | <span data-ttu-id="e4ce9-114">本總覽說明使用 [DirectXMath] 程式庫將現有程式碼遷移至程式庫所需的變更。</span><span class="sxs-lookup"><span data-stu-id="e4ce9-114">This overview describes the changes required to migrate existing code using the XNA Math library to the DirectXMath library.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="e4ce9-115">使用 D3DXMath</span><span class="sxs-lookup"><span data-stu-id="e4ce9-115">Working with D3DXMath</span></span>](pg-xnamath-migration-d3dx.md)<br/> | <span data-ttu-id="e4ce9-116">D3DXMath 是適用于 Direct3D 應用程式的數學協助程式程式庫。</span><span class="sxs-lookup"><span data-stu-id="e4ce9-116">D3DXMath is a math helper library for Direct3D applications.</span></span> <br/>                                                                                                                                                                                                |
| [<span data-ttu-id="e4ce9-117">程式碼優化</span><span class="sxs-lookup"><span data-stu-id="e4ce9-117">Code Optimization</span></span>](pg-xnamath-optimizing.md)<br/>         | <span data-ttu-id="e4ce9-118">本主題說明 DirectXMath 程式庫的優化考慮和策略。</span><span class="sxs-lookup"><span data-stu-id="e4ce9-118">This topic describes optimization considerations and strategies with the DirectXMath Library.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="e4ce9-119">程式庫內部</span><span class="sxs-lookup"><span data-stu-id="e4ce9-119">Library Internals</span></span>](pg-xnamath-internals.md)<br/>          | <span data-ttu-id="e4ce9-120">本主題說明 DirectXMath 程式庫的內部設計。</span><span class="sxs-lookup"><span data-stu-id="e4ce9-120">This topic describes the internal design of the DirectXMath library.</span></span><br/>                                                                                                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="e4ce9-121">[相關主題]</span><span class="sxs-lookup"><span data-stu-id="e4ce9-121">Related Topics</span></span>

<dl> <dt>

<span data-ttu-id="e4ce9-122"><span id="DirectXMath_Programming_Reference"></span><span id="directxmath_programming_reference"></span><span id="DIRECTXMATH_PROGRAMMING_REFERENCE"></span>[DirectXMath 程式設計參考](ovw-xnamath-reference.md)</span><span class="sxs-lookup"><span data-stu-id="e4ce9-122"><span id="DirectXMath_Programming_Reference"></span><span id="directxmath_programming_reference"></span><span id="DIRECTXMATH_PROGRAMMING_REFERENCE"></span>[DirectXMath Programming Reference](ovw-xnamath-reference.md)</span></span>
<span data-ttu-id="e4ce9-123"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e4ce9-123"></dt> <dd></dd> </dl></span></span>

## <a name="related-topics"></a><span data-ttu-id="e4ce9-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="e4ce9-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4ce9-125">DirectXMath</span><span class="sxs-lookup"><span data-stu-id="e4ce9-125">DirectXMath</span></span>](directxmath-portal.md)
</dt> </dl>

 

 




