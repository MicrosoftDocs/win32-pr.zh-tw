---
description: DirectXMath 程式庫是以「運算元學 c + + SIMD 程式庫2.x 版」為基礎。 在此，我們將說明 DirectXMath 與未通過的數學有何不同，以及 DirectXMath 版本有何不同。
ms.assetid: 105800d3-a191-c78f-316a-bf2daf7b27a6
title: '新功能 (DirectXMath) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1df1e7f25789ca6f58205ce9f45482e0a49540d1
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827624"
---
# <a name="whats-new-directxmath"></a><span data-ttu-id="f6956-104">新功能 (DirectXMath) </span><span class="sxs-lookup"><span data-stu-id="f6956-104">What's New (DirectXMath)</span></span>

<span data-ttu-id="f6956-105">DirectXMath 程式庫是以「操作 [數學 c + + SIMD 程式庫」2.04 版](https://walbourn.github.io/xna-math-version-2-04/)為基礎。</span><span class="sxs-lookup"><span data-stu-id="f6956-105">The DirectXMath library is based on the [XNA Math C++ SIMD library version 2.04](https://walbourn.github.io/xna-math-version-2-04/).</span></span> <span data-ttu-id="f6956-106">在此，我們將說明 DirectXMath 與未通過的數學有何不同，以及 DirectXMath 版本有何不同。</span><span class="sxs-lookup"><span data-stu-id="f6956-106">Here we describe how DirectXMath differs from XNA Math and how DirectXMath versions differ.</span></span>

-   [<span data-ttu-id="f6956-107">Rlease 歷程記錄</span><span class="sxs-lookup"><span data-stu-id="f6956-107">Rlease history</span></span>](#release-history)
-   [<span data-ttu-id="f6956-108">DirectXMath 與未通過數學的差異</span><span class="sxs-lookup"><span data-stu-id="f6956-108">DirectXMath differences from XNA Math</span></span>](#directxmath-differences-from-xna-math)
-   [<span data-ttu-id="f6956-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="f6956-109">Related topics</span></span>](#related-topics)

## <a name="release-history"></a><span data-ttu-id="f6956-110">版本歷程記錄</span><span class="sxs-lookup"><span data-stu-id="f6956-110">Release history</span></span>

<table>
 <tr>
  <td><span data-ttu-id="f6956-111">Windows 10 SDK (20348) 2104 版</span><span class="sxs-lookup"><span data-stu-id="f6956-111">Windows 10 SDK (20348), version 2104</span></span></td><td><span data-ttu-id="f6956-112">DirectXMath 3.16</span><span class="sxs-lookup"><span data-stu-id="f6956-112">DirectXMath 3.16</span></span></td>
 </td>
 <tr>
  <td><span data-ttu-id="f6956-113">Windows 10 5 月2020更新 SDK</span><span class="sxs-lookup"><span data-stu-id="f6956-113">Windows 10 May 2020 Update SDK</span></span></td><td><span data-ttu-id="f6956-114">DirectXMath 3.14</span><span class="sxs-lookup"><span data-stu-id="f6956-114">DirectXMath 3.14</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="f6956-115">Windows 10 2018 年10月更新 SDK</span><span class="sxs-lookup"><span data-stu-id="f6956-115">Windows 10 October 2018 Update SDK</span></span></td><td><span data-ttu-id="f6956-116">DirectXMath 3.13</span><span class="sxs-lookup"><span data-stu-id="f6956-116">DirectXMath 3.13</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="f6956-117">Windows 10 2018 年4月更新 SDK</span><span class="sxs-lookup"><span data-stu-id="f6956-117">Windows 10 April 2018 Update SDK</span></span><br /><span data-ttu-id="f6956-118">Windows 10 Fall Creators Update SDK</span><span class="sxs-lookup"><span data-stu-id="f6956-118">Windows 10 Fall Creators Update SDK</span></span></td><td><span data-ttu-id="f6956-119">DirectXMath 3.11</span><span class="sxs-lookup"><span data-stu-id="f6956-119">DirectXMath 3.11</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="f6956-120">Windows 10 Creators Update SDK</span><span class="sxs-lookup"><span data-stu-id="f6956-120">Windows 10 Creators Update SDK</span></span></td><td><span data-ttu-id="f6956-121">DirectXMath 3.10</span><span class="sxs-lookup"><span data-stu-id="f6956-121">DirectXMath 3.10</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="f6956-122">Windows 10 周年 SDK</span><span class="sxs-lookup"><span data-stu-id="f6956-122">Windows 10 Anniversary SDK</span></span></td><td><span data-ttu-id="f6956-123">DirectXMath 3.09</span><span class="sxs-lookup"><span data-stu-id="f6956-123">DirectXMath 3.09</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="f6956-124">Windows 10 SDK (2015 年11月) </span><span class="sxs-lookup"><span data-stu-id="f6956-124">Windows 10 SDK (November 2015)</span></span></td><td><span data-ttu-id="f6956-125">DirectXMath 3.08</span><span class="sxs-lookup"><span data-stu-id="f6956-125">DirectXMath 3.08</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="f6956-126">適用于 Windows 8.1 (2015 春季的 Windows SDK) </span><span class="sxs-lookup"><span data-stu-id="f6956-126">Windows SDK for Windows 8.1 (Spring 2015)</span></span></td><td><span data-ttu-id="f6956-127">DirectXMath 3.07</span><span class="sxs-lookup"><span data-stu-id="f6956-127">DirectXMath 3.07</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="f6956-128">Windows 8.1 的 Windows SDK</span><span class="sxs-lookup"><span data-stu-id="f6956-128">Windows SDK for Windows 8.1</span></span></td><td><span data-ttu-id="f6956-129">DirectXMath 3.06</span><span class="sxs-lookup"><span data-stu-id="f6956-129">DirectXMath 3.06</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="f6956-130">Windows 8 的 Windows SDK</span><span class="sxs-lookup"><span data-stu-id="f6956-130">Windows SDK for Windows 8</span></span></td><td><span data-ttu-id="f6956-131">DirectXMath 3.03</span><span class="sxs-lookup"><span data-stu-id="f6956-131">DirectXMath 3.03</span></span></td>
 </tr>
</table>

<span data-ttu-id="f6956-132">如需詳細資訊，請參閱 [DirectXMath 版本](https://github.com/Microsoft/DirectXMath/releases) 。</span><span class="sxs-lookup"><span data-stu-id="f6956-132">See [DirectXMath releases](https://github.com/Microsoft/DirectXMath/releases) for more information.</span></span>

## <a name="directxmath-differences-from-xna-math"></a><span data-ttu-id="f6956-133">DirectXMath 與未通過數學的差異</span><span class="sxs-lookup"><span data-stu-id="f6956-133">DirectXMath differences from XNA Math</span></span>

<span data-ttu-id="f6956-134">以下是 DirectXMath 程式庫主要與「運算元學」程式庫有何不同：</span><span class="sxs-lookup"><span data-stu-id="f6956-134">Here is how the DirectXMath library primarily differs from the XNA Math library:</span></span>

-   <span data-ttu-id="f6956-135">DirectXMath 僅限 c + + (命名空間、多載、新範本等) 。</span><span class="sxs-lookup"><span data-stu-id="f6956-135">DirectXMath is C++ only (namespaces, overloads, new templates, and so on).</span></span>
-   <span data-ttu-id="f6956-136">需要 c + + 11 標準程式庫支援 (也就是在) 上的 stdint.h。</span><span class="sxs-lookup"><span data-stu-id="f6956-136">Requires C++11 standard library support (that is, stdint.h, and so on).</span></span>
-   <span data-ttu-id="f6956-137">Windows RT 平臺的 ARM 霓虹燈內建支援。</span><span class="sxs-lookup"><span data-stu-id="f6956-137">ARM-NEON intrinsics support for the Windows RT platform.</span></span>
-   <span data-ttu-id="f6956-138">新的色彩功能 (色彩空間轉換、.NET 色彩常數) 。</span><span class="sxs-lookup"><span data-stu-id="f6956-138">New color functionality (color space conversions, .NET color constants).</span></span>
-   <span data-ttu-id="f6956-139">界限磁片區類型 (先前在 DirectX SDK 衝突範例) 的 XNACollision 標頭中的版本。</span><span class="sxs-lookup"><span data-stu-id="f6956-139">Bounding volume types (a version of which was previously in the XNACollision header in the DirectX SDK Collision sample).</span></span>
-   <span data-ttu-id="f6956-140">沒有 Xbox 360 版本可供使用。</span><span class="sxs-lookup"><span data-stu-id="f6956-140">No Xbox 360 version is available.</span></span> <span data-ttu-id="f6956-141">Xbox 360 XDK 會繼續寄送 XNAMath v2. x;移除 Xbox 360 特定的資料類型和函數變異。</span><span class="sxs-lookup"><span data-stu-id="f6956-141">The Xbox 360 XDK continues to ship XNAMath v2.x; removal of Xbox 360 specific data types and function variants.</span></span>
-   <span data-ttu-id="f6956-142">修改 [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) ，以改善 SSE 和 ARM 霓虹燈內建函式的優化。</span><span class="sxs-lookup"><span data-stu-id="f6956-142">Reworked [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) for improved optimization for SSE and ARM-NEON intrinsics.</span></span>
-   <span data-ttu-id="f6956-143">[**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)類型完全不透明。</span><span class="sxs-lookup"><span data-stu-id="f6956-143">The [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) type is fully opaque.</span></span> <span data-ttu-id="f6956-144">若要存取 **XMMATRIX** 的個別元素，請使用其他類型，例如 [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4)。</span><span class="sxs-lookup"><span data-stu-id="f6956-144">To access individual elements of **XMMATRIX**, use other types such as [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6956-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="f6956-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6956-146">DirectXMath 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="f6956-146">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)
</dt> <dt>

[<span data-ttu-id="f6956-147">DirectXMath 版本</span><span class="sxs-lookup"><span data-stu-id="f6956-147">DirectXMath releases</span></span>](https://github.com/Microsoft/DirectXMath/releases)
</dt> </dl>

 

 
