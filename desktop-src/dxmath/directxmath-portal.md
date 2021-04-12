---
description: .
ms.assetid: 719954bf-0d7d-f647-2d3f-a77d87df204e
title: DirectXMath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f316939514d9a186fcd5ef36372f31709b69a7a
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2021
ms.locfileid: "104321776"
---
# <a name="directxmath"></a><span data-ttu-id="f3df2-103">DirectXMath</span><span class="sxs-lookup"><span data-stu-id="f3df2-103">DirectXMath</span></span>

## <a name="purpose"></a><span data-ttu-id="f3df2-104">目的</span><span class="sxs-lookup"><span data-stu-id="f3df2-104">Purpose</span></span>

<span data-ttu-id="f3df2-105">DirectXMath API 提供 SIMD 的 c + + 類型和函式，適用于 DirectX 應用程式常見的一般線性代數和圖形數學運算。</span><span class="sxs-lookup"><span data-stu-id="f3df2-105">The DirectXMath API provides SIMD-friendly C++ types and functions for common linear algebra and graphics math operations common to DirectX applications.</span></span> <span data-ttu-id="f3df2-106">此程式庫會透過 Visual C++ 編譯器中的 SSE、AVX 和 ARM-霓虹燈內建支援，提供 Windows 32 位的優化版本 (x86) 、Windows 64 位 (x64) ，以及 ARM/ARM64 上的 Windows。</span><span class="sxs-lookup"><span data-stu-id="f3df2-106">The library provides optimized versions for Windows 32-bit (x86), Windows 64-bit (x64), and Windows on ARM/ARM64 through SSE, AVX, and ARM-NEON intrinsics support in the Visual C++ compiler.</span></span>

<span data-ttu-id="f3df2-107">針對剛 DirectXMath 的開發人員，您可能想要考慮在 directx [11](https://go.microsoft.com/fwlink/?LinkId=248929)DirectX12 的 *directx 工具套件* 中使用 SimpleMath 包裝函式  /  [](https://go.microsoft.com/fwlink/?LinkID=615561)作為起點。</span><span class="sxs-lookup"><span data-stu-id="f3df2-107">For developers new to DirectXMath, you may want to consider using the SimpleMath wrapper in the *DirectX Tool Kit* for [DirectX 11](https://go.microsoft.com/fwlink/?LinkId=248929) / [DirectX12](https://go.microsoft.com/fwlink/?LinkID=615561) as a starting point.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f3df2-108">本節內容</span><span class="sxs-lookup"><span data-stu-id="f3df2-108">In this section</span></span>



| <span data-ttu-id="f3df2-109">主題</span><span class="sxs-lookup"><span data-stu-id="f3df2-109">Topic</span></span>                                                                     | <span data-ttu-id="f3df2-110">描述</span><span class="sxs-lookup"><span data-stu-id="f3df2-110">Description</span></span>                                                                      |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="f3df2-111">DirectXMath 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="f3df2-111">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)<br/>     | <span data-ttu-id="f3df2-112">DirectXMath 提供針對 Windows 優化的數學解決方案。</span><span class="sxs-lookup"><span data-stu-id="f3df2-112">DirectXMath provides a math solution optimized for Windows.</span></span><br/>           |
| [<span data-ttu-id="f3df2-113">DirectXMath 程式設計參考</span><span class="sxs-lookup"><span data-stu-id="f3df2-113">DirectXMath Programming Reference</span></span>](ovw-xnamath-reference.md)<br/> | <span data-ttu-id="f3df2-114">本章節包含 DirectXMath 程式庫的參考資料。</span><span class="sxs-lookup"><span data-stu-id="f3df2-114">This section contains reference material for the DirectXMath Library.</span></span><br/> |



 

## <a name="developer-audience"></a><span data-ttu-id="f3df2-115">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="f3df2-115">Developer audience</span></span>

<span data-ttu-id="f3df2-116">DirectXMath 程式庫是專為 c + + 開發人員所設計，適用于在 Windows Store 應用程式、Xbox 遊戲和 Windows 的傳統桌面應用程式中使用遊戲和 DirectX 圖形的程式。</span><span class="sxs-lookup"><span data-stu-id="f3df2-116">The DirectXMath library is designed for C++ developers working on games and DirectX graphics in Windows Store apps, Xbox games, and traditional desktop apps for Windows.</span></span>

## <a name="obtaining-directxmath"></a><span data-ttu-id="f3df2-117">取得 DirectXMath</span><span class="sxs-lookup"><span data-stu-id="f3df2-117">Obtaining DirectXMath</span></span>
 
<span data-ttu-id="f3df2-118">DirectXMath 標頭隨附于 Visual Studio 2012 （含）以後版本隨附的 Windows SDK，而作為所有內嵌標頭時，不會連結任何 DLL 或靜態程式庫。</span><span class="sxs-lookup"><span data-stu-id="f3df2-118">The DirectXMath headers ship in the Windows SDK that comes with Visual Studio 2012 or later, and as an all inline header there is no DLL or static library to link against.</span></span> <span data-ttu-id="f3df2-119">它也可做為 [NuGet](https://www.nuget.org/packages/directxmath/)上的套件。</span><span class="sxs-lookup"><span data-stu-id="f3df2-119">It is also available as a package on [NuGet](https://www.nuget.org/packages/directxmath/).</span></span>

<span data-ttu-id="f3df2-120">DirectXMath 是在[GitHub](https://github.com/Microsoft/DirectXMath)上裝載之[MIT 授權](https://opensource.org/licenses/MIT)下的開放原始碼。</span><span class="sxs-lookup"><span data-stu-id="f3df2-120">DirectXMath is open source under the [MIT license](https://opensource.org/licenses/MIT) hosted on [GitHub](https://github.com/Microsoft/DirectXMath).</span></span>




