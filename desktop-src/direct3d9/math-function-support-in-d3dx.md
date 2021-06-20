---
description: 深入瞭解 D3DX 中的數學函數支援。 D3DX 是提供 helper 服務的公用程式庫。 它是 Direct3D 元件之上的一層。
ms.assetid: a44d25de-f79d-4132-a75a-0c22ccd84341
title: D3DX (Direct3D 9) 中的數學函數支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a28c32b13d185694e4ffa41c314cf9f77cbb18b7
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407521"
---
# <a name="math-function-support-in-d3dx-direct3d-9"></a><span data-ttu-id="9cf91-105">D3DX (Direct3D 9) 中的數學函數支援</span><span class="sxs-lookup"><span data-stu-id="9cf91-105">Math Function Support in D3DX (Direct3D 9)</span></span>

<span data-ttu-id="9cf91-106">D3DX 是提供 helper 服務的公用程式庫。</span><span class="sxs-lookup"><span data-stu-id="9cf91-106">D3DX is a utility library that provides helper services.</span></span> <span data-ttu-id="9cf91-107">它是 Direct3D 元件之上的一層。</span><span class="sxs-lookup"><span data-stu-id="9cf91-107">It is a layer above the Direct3D component.</span></span>

## <a name="math"></a><span data-ttu-id="9cf91-108">數學</span><span class="sxs-lookup"><span data-stu-id="9cf91-108">Math</span></span>

<span data-ttu-id="9cf91-109">針對下列各項，提供包含在一組函數中的數學支援：</span><span class="sxs-lookup"><span data-stu-id="9cf91-109">Math support, contained in a set of functions, is provided for:</span></span>

-   <span data-ttu-id="9cf91-110">色彩計算</span><span class="sxs-lookup"><span data-stu-id="9cf91-110">Color calculations</span></span>
-   <span data-ttu-id="9cf91-111">飛機</span><span class="sxs-lookup"><span data-stu-id="9cf91-111">Planes</span></span>
-   <span data-ttu-id="9cf91-112">矩陣操作</span><span class="sxs-lookup"><span data-stu-id="9cf91-112">Matrix manipulation</span></span>
-   <span data-ttu-id="9cf91-113">四元</span><span class="sxs-lookup"><span data-stu-id="9cf91-113">Quaternions</span></span>
-   <span data-ttu-id="9cf91-114">2D 向量</span><span class="sxs-lookup"><span data-stu-id="9cf91-114">2D vectors</span></span>
-   <span data-ttu-id="9cf91-115">3D 向量</span><span class="sxs-lookup"><span data-stu-id="9cf91-115">3D vectors</span></span>
-   <span data-ttu-id="9cf91-116">4D 向量</span><span class="sxs-lookup"><span data-stu-id="9cf91-116">4D vectors</span></span>

<span data-ttu-id="9cf91-117">請注意，與 c + + 多載結合時，基本3D 數學類型的支援很廣泛。</span><span class="sxs-lookup"><span data-stu-id="9cf91-117">Please note that when coupled with the C++ overloads, the support for basic 3D math types is extensive.</span></span>

<span data-ttu-id="9cf91-118">如需這些函數的詳細資訊，請參閱 [D3DX 函數](dx9-graphics-reference-d3dx-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="9cf91-118">For more information about these functions, see [D3DX Functions](dx9-graphics-reference-d3dx-functions.md).</span></span> <span data-ttu-id="9cf91-119">為了協助找出您所需的功能，它們會分成數個資料夾。</span><span class="sxs-lookup"><span data-stu-id="9cf91-119">To help find the function you need, they are broken up in several folders.</span></span>

## <a name="float16"></a><span data-ttu-id="9cf91-120">FLOAT16</span><span class="sxs-lookup"><span data-stu-id="9cf91-120">FLOAT16</span></span>

<span data-ttu-id="9cf91-121">使用 FLOAT16 資料類型時，請務必將值限制為最多 D3DX \_ 16F \_ MAX。</span><span class="sxs-lookup"><span data-stu-id="9cf91-121">When using the FLOAT16 data type, be sure to limit values to a maximum of D3DX\_16F\_MAX.</span></span> <span data-ttu-id="9cf91-122">任何超過此值的 FLOAT16 值都會導致管線中有未定義的行為。</span><span class="sxs-lookup"><span data-stu-id="9cf91-122">Any FLOAT16 value that exceeds this will result in undefined behavior in the pipeline.</span></span> <span data-ttu-id="9cf91-123">請參閱 [其他 D3DX 常數](other-d3dx-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="9cf91-123">See [Other D3DX Constants](other-d3dx-constants.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9cf91-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="9cf91-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cf91-125">D3DX</span><span class="sxs-lookup"><span data-stu-id="9cf91-125">D3DX</span></span>](d3dx.md)
</dt> </dl>

 

 



