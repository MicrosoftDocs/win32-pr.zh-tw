---
description: D3DX 是提供 helper 服務的公用程式庫。 它是 Direct3D 元件之上的一層。
ms.assetid: a44d25de-f79d-4132-a75a-0c22ccd84341
title: D3DX (Direct3D 9) 中的數學函數支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac69e0385919b015d1f8d3e7d47e221c06a04fbb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109152"
---
# <a name="math-function-support-in-d3dx-direct3d-9"></a><span data-ttu-id="a3bb0-104">D3DX (Direct3D 9) 中的數學函數支援</span><span class="sxs-lookup"><span data-stu-id="a3bb0-104">Math Function Support in D3DX (Direct3D 9)</span></span>

<span data-ttu-id="a3bb0-105">D3DX 是提供 helper 服務的公用程式庫。</span><span class="sxs-lookup"><span data-stu-id="a3bb0-105">D3DX is a utility library that provides helper services.</span></span> <span data-ttu-id="a3bb0-106">它是 Direct3D 元件之上的一層。</span><span class="sxs-lookup"><span data-stu-id="a3bb0-106">It is a layer above the Direct3D component.</span></span>

## <a name="math"></a><span data-ttu-id="a3bb0-107">數學</span><span class="sxs-lookup"><span data-stu-id="a3bb0-107">Math</span></span>

<span data-ttu-id="a3bb0-108">針對下列各項，提供包含在一組函數中的數學支援：</span><span class="sxs-lookup"><span data-stu-id="a3bb0-108">Math support, contained in a set of functions, is provided for:</span></span>

-   <span data-ttu-id="a3bb0-109">色彩計算</span><span class="sxs-lookup"><span data-stu-id="a3bb0-109">Color calculations</span></span>
-   <span data-ttu-id="a3bb0-110">飛機</span><span class="sxs-lookup"><span data-stu-id="a3bb0-110">Planes</span></span>
-   <span data-ttu-id="a3bb0-111">矩陣操作</span><span class="sxs-lookup"><span data-stu-id="a3bb0-111">Matrix manipulation</span></span>
-   <span data-ttu-id="a3bb0-112">四元</span><span class="sxs-lookup"><span data-stu-id="a3bb0-112">Quaternions</span></span>
-   <span data-ttu-id="a3bb0-113">2D 向量</span><span class="sxs-lookup"><span data-stu-id="a3bb0-113">2D vectors</span></span>
-   <span data-ttu-id="a3bb0-114">3D 向量</span><span class="sxs-lookup"><span data-stu-id="a3bb0-114">3D vectors</span></span>
-   <span data-ttu-id="a3bb0-115">4D 向量</span><span class="sxs-lookup"><span data-stu-id="a3bb0-115">4D vectors</span></span>

<span data-ttu-id="a3bb0-116">請注意，與 c + + 多載結合時，基本3D 數學類型的支援很廣泛。</span><span class="sxs-lookup"><span data-stu-id="a3bb0-116">Please note that when coupled with the C++ overloads, the support for basic 3D math types is extensive.</span></span>

<span data-ttu-id="a3bb0-117">如需這些函數的詳細資訊，請參閱 [D3DX 函數](dx9-graphics-reference-d3dx-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="a3bb0-117">For more information about these functions, see [D3DX Functions](dx9-graphics-reference-d3dx-functions.md).</span></span> <span data-ttu-id="a3bb0-118">為了協助找出您所需的功能，它們會分成數個資料夾。</span><span class="sxs-lookup"><span data-stu-id="a3bb0-118">To help find the function you need, they are broken up in several folders.</span></span>

## <a name="float16"></a><span data-ttu-id="a3bb0-119">FLOAT16</span><span class="sxs-lookup"><span data-stu-id="a3bb0-119">FLOAT16</span></span>

<span data-ttu-id="a3bb0-120">使用 FLOAT16 資料類型時，請務必將值限制為最多 D3DX \_ 16F \_ MAX。</span><span class="sxs-lookup"><span data-stu-id="a3bb0-120">When using the FLOAT16 data type, be sure to limit values to a maximum of D3DX\_16F\_MAX.</span></span> <span data-ttu-id="a3bb0-121">任何超過此值的 FLOAT16 值都會導致管線中有未定義的行為。</span><span class="sxs-lookup"><span data-stu-id="a3bb0-121">Any FLOAT16 value that exceeds this will result in undefined behavior in the pipeline.</span></span> <span data-ttu-id="a3bb0-122">請參閱 [其他 D3DX 常數](other-d3dx-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="a3bb0-122">See [Other D3DX Constants](other-d3dx-constants.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3bb0-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="a3bb0-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3bb0-124">D3DX</span><span class="sxs-lookup"><span data-stu-id="a3bb0-124">D3DX</span></span>](d3dx.md)
</dt> </dl>

 

 



