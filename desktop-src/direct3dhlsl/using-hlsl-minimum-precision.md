---
title: 使用 HLSL 最小有效位數
description: 從 Windows 8 開始，圖形驅動程式可以使用任何有效位數大於或等於指定的位精確度，來執行最小有效位數 HLSL 純量資料類型。
ms.assetid: 422B0C45-5CEB-4235-AD05-62D36C36CFC6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7f66f35aef3e870edb4e8564a280be89ce34be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682574"
---
# <a name="using-hlsl-minimum-precision"></a><span data-ttu-id="34f43-103">使用 HLSL 最小有效位數</span><span class="sxs-lookup"><span data-stu-id="34f43-103">Using HLSL minimum precision</span></span>

<span data-ttu-id="34f43-104">從 Windows 8 開始，圖形驅動程式可以使用任何有效位數大於或等於指定的位精確度，來執行最小有效位數 HLSL 純量 [資料類型](dx-graphics-hlsl-scalar.md) 。</span><span class="sxs-lookup"><span data-stu-id="34f43-104">Starting with Windows 8, graphics drivers can implement minimum precision [HLSL scalar data types](dx-graphics-hlsl-scalar.md) by using any precision greater than or equal to their specified bit precision.</span></span> <span data-ttu-id="34f43-105">當您的 HLSL 最小精確度著色器程式碼在實 HLSL 最小精確度的硬體上使用時，您會使用較少的記憶體頻寬，因此您也會使用較少的系統電源。</span><span class="sxs-lookup"><span data-stu-id="34f43-105">When your HLSL minimum precision shader code is used on hardware that implements HLSL minimum precision, you use less memory bandwidth and as a result you also use less system power.</span></span>

<span data-ttu-id="34f43-106">您可以藉由呼叫 [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) 與 [**D3D11 \_ 功能 \_ 著色器的 \_ 最小 \_ 精確度 \_ 支援**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) 值，來查詢圖形驅動程式所提供的最小精確度支援。</span><span class="sxs-lookup"><span data-stu-id="34f43-106">You can query for the minimum precision support that the graphics driver provides by calling [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) with the [**D3D11\_FEATURE\_SHADER\_MIN\_PRECISION\_SUPPORT**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) value.</span></span> <span data-ttu-id="34f43-107">如需詳細資訊，請參閱 [HLSL 最小精確度支援](/windows/desktop/direct3d11/direct3d-11-1-features)。</span><span class="sxs-lookup"><span data-stu-id="34f43-107">For more info, see [HLSL minimum precision support](/windows/desktop/direct3d11/direct3d-11-1-features).</span></span>

-   [<span data-ttu-id="34f43-108">宣告具有最小精確度資料類型的變數</span><span class="sxs-lookup"><span data-stu-id="34f43-108">Declare variables with minimum precision data types</span></span>](#declare-variables-with-minimum-precision-data-types)
-   [<span data-ttu-id="34f43-109">測試最小精確度著色器程式碼</span><span class="sxs-lookup"><span data-stu-id="34f43-109">Testing your minimum precision shader code</span></span>](#testing-your-minimum-precision-shader-code)
-   [<span data-ttu-id="34f43-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="34f43-110">Related topics</span></span>](#related-topics)

## <a name="declare-variables-with-minimum-precision-data-types"></a><span data-ttu-id="34f43-111">宣告具有最小精確度資料類型的變數</span><span class="sxs-lookup"><span data-stu-id="34f43-111">Declare variables with minimum precision data types</span></span>

<span data-ttu-id="34f43-112">若要在 HLSL 著色器程式碼中使用最小有效位數，請針對向量) 、 **min16int**、 **min10float** 等類型宣告個別變數，例如 **min16float** (**min16float4** 。</span><span class="sxs-lookup"><span data-stu-id="34f43-112">To use minimum precision in HLSL shader code, declare individual variables with types like **min16float** (**min16float4** for a vector), **min16int**, **min10float**, and so on.</span></span> <span data-ttu-id="34f43-113">使用這些變數時，您的著色器程式碼表示它不需要比變數所指出更多的精確度。</span><span class="sxs-lookup"><span data-stu-id="34f43-113">With these variables, your shader code indicates that it doesn’t require more precision than what the variables indicate.</span></span> <span data-ttu-id="34f43-114">但硬體可以忽略最小精確度指標，並以完整的32位精確度執行。</span><span class="sxs-lookup"><span data-stu-id="34f43-114">But hardware can ignore the minimum precision indicators and run at full 32-bit precision.</span></span> <span data-ttu-id="34f43-115">當您在採用最小精確度的硬體上使用您的著色器程式碼時，您會使用較少的記憶體頻寬，因此，只要您的著色器程式碼不會預期比指定的精確，您也會使用較少的系統電源。</span><span class="sxs-lookup"><span data-stu-id="34f43-115">When your shader code is used on hardware that takes advantage of minimum precision, you use less memory bandwidth and as a result you also use less system power as long as your shader code doesn’t expect more precision than it specified.</span></span>

<span data-ttu-id="34f43-116">您不需要撰寫多個執行和不使用最小精確度的著色器。</span><span class="sxs-lookup"><span data-stu-id="34f43-116">You don't need to author multiple shaders that do and don't use minimum precision.</span></span> <span data-ttu-id="34f43-117">相反地，如果圖形驅動程式回報不支援任何最小有效位數，則建立具有最小精確度的著色器，且最小精確度變數的行為會是完整的32位有效位數。</span><span class="sxs-lookup"><span data-stu-id="34f43-117">Instead, create shaders with minimum precision, and the minimum precision variables behave at full 32-bit precision if the graphics driver reports that it doesn't support any minimum precision.</span></span> <span data-ttu-id="34f43-118">HLSL 最小精確度著色器無法在早于 Windows 8 的作業系統上運作，因此，如果您打算以較早的作業系統為目標，則必須撰寫多個著色器，有些會執行，有些則不會使用最小有效位數。</span><span class="sxs-lookup"><span data-stu-id="34f43-118">HLSL minimum precision shaders don't work on operating systems earlier than Windows 8 so if you plan to target earlier operating systems, you'll need to author multiple shaders, some that do and others that don't use minimum precision.</span></span>

> [!Note]  
> <span data-ttu-id="34f43-119">請勿在著色器內的不同精確度層級之間進行資料切換，因為這些類型的轉換會浪費和降低效能。</span><span class="sxs-lookup"><span data-stu-id="34f43-119">Don't make data switches between different precision levels within a shader because these types of conversions are wasteful and reduce performance.</span></span> <span data-ttu-id="34f43-120">唯一的例外是，著色器常數仍一律為32位，但廠商可以設計圖形硬體，以自由地關閉轉換成 HLSL 指令讀取可能使用的精確度。</span><span class="sxs-lookup"><span data-stu-id="34f43-120">The exception is that shader constants are still always 32 bit, but vendors can design graphics hardware that can freely down-convert to whatever lower precision the HLSL instruction reading might use.</span></span>

 

<span data-ttu-id="34f43-121">藉由使用最小有效位數，您可以在著色器程式碼的各個部分中控制計算的精確度。</span><span class="sxs-lookup"><span data-stu-id="34f43-121">By using minimum precision, you can control the precision of computations in various parts of your shader code.</span></span>

<span data-ttu-id="34f43-122">HLSL 最小精確度的規則類似于 C/c + +，其中運算式中的類型會決定作業的有效位數，而不是最後寫入的型別。</span><span class="sxs-lookup"><span data-stu-id="34f43-122">The rules for HLSL minimum precision are similar to C/C++, where the types in an expression determine the precision of the operation, not the type being eventually written to.</span></span>

## <a name="testing-your-minimum-precision-shader-code"></a><span data-ttu-id="34f43-123">測試最小精確度著色器程式碼</span><span class="sxs-lookup"><span data-stu-id="34f43-123">Testing your minimum precision shader code</span></span>

<span data-ttu-id="34f43-124">參考轉譯器 ([**D3D \_ 驅動程式 \_ 類型 \_ 參考**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type)) 可讓您大致瞭解 HLSL 著色器程式碼中的最小有效位數如何藉由量化每個 HLSL 指令至指定的精確度來運作。</span><span class="sxs-lookup"><span data-stu-id="34f43-124">The reference rasterizer ([**D3D\_DRIVER\_TYPE\_REFERENCE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type)) gives you a rough idea of how minimum precision in your HLSL shader code behaves by quantizing each HLSL instruction to the specified precision.</span></span> <span data-ttu-id="34f43-125">這可協助您探索可能不慎依賴超過最小精確度的程式碼。</span><span class="sxs-lookup"><span data-stu-id="34f43-125">This helps you discover code that might accidentally rely on more than the minimum precision.</span></span> <span data-ttu-id="34f43-126">當您的 HLSL 著色器程式碼使用最小有效位數，但您可以使用它來驗證程式代碼的正確性時，參考轉譯器的執行速度會更快。</span><span class="sxs-lookup"><span data-stu-id="34f43-126">The reference rasterizer doesn’t run any faster when your HLSL shader code uses minimum precision, but you can use it to verify the correctness of your code.</span></span> <span data-ttu-id="34f43-127"> ([**D3D \_ 驅動程式 \_ 類型 \_ 變形**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type)的 [變形](/windows/desktop/direct3d11/overviews-direct3d-11-devices-create-warp)) 不支援在 HLSL 著色器程式碼中使用最小有效位數;變形只會以完整的32位有效位數執行。</span><span class="sxs-lookup"><span data-stu-id="34f43-127">[WARP](/windows/desktop/direct3d11/overviews-direct3d-11-devices-create-warp) ([**D3D\_DRIVER\_TYPE\_WARP**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type)) doesn’t support using minimum precision in HLSL shader code; WARP just runs at full 32-bit precision.</span></span>

## <a name="related-topics"></a><span data-ttu-id="34f43-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="34f43-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34f43-129">HLSL 的程式設計指南</span><span class="sxs-lookup"><span data-stu-id="34f43-129">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 