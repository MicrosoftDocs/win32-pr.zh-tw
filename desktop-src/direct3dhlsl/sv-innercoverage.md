---
title: SV_InnerCoverage
description: SV \_ InputCoverage 代表低估的保守式點陣化資訊， (也就是是否保證可以完全涵蓋) 的圖元。
ms.assetid: 5BB3C3FB-E5ED-4395-B389-300DE67C984B
keywords:
- SV_InnerCoverage HLSL
topic_type:
- apiref
api_name:
- SV_InnerCoverage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1ac278f0524446b5171ef278e169fbe7c3a082f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996965"
---
# <a name="sv_innercoverage"></a><span data-ttu-id="50e1b-104">SV \_ InnerCoverage</span><span class="sxs-lookup"><span data-stu-id="50e1b-104">SV\_InnerCoverage</span></span>

<span data-ttu-id="50e1b-105">SV \_ InputCoverage 代表低估的保守式點陣化資訊， (也就是是否保證可以完全涵蓋) 的圖元。</span><span class="sxs-lookup"><span data-stu-id="50e1b-105">SV\_InputCoverage represents underestimated conservative rasterization information (i.e. whether a pixel is guaranteed-to-be-fully covered).</span></span>

## <a name="type"></a><span data-ttu-id="50e1b-106">類型</span><span class="sxs-lookup"><span data-stu-id="50e1b-106">Type</span></span>



|      |
|------|
| <span data-ttu-id="50e1b-107">類型</span><span class="sxs-lookup"><span data-stu-id="50e1b-107">Type</span></span> |
| <span data-ttu-id="50e1b-108">uint</span><span class="sxs-lookup"><span data-stu-id="50e1b-108">uint</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="50e1b-109">備註</span><span class="sxs-lookup"><span data-stu-id="50e1b-109">Remarks</span></span>

<span data-ttu-id="50e1b-110">第3層支援需要此系統產生的值，且僅適用于該層。</span><span class="sxs-lookup"><span data-stu-id="50e1b-110">This system generated value is required for tier 3 support, and is only available in that tier.</span></span> <span data-ttu-id="50e1b-111">此輸入與 SV \_ 涵蓋範圍互斥-兩者皆無法使用。</span><span class="sxs-lookup"><span data-stu-id="50e1b-111">This input is mutually exclusive with SV\_Coverage - both cannot be used.</span></span>

<span data-ttu-id="50e1b-112">若要存取 SV \_ InnerCoverage，必須將它宣告為一個圖元著色器輸入暫存器中的單一元件。</span><span class="sxs-lookup"><span data-stu-id="50e1b-112">To access SV\_InnerCoverage, it must be declared as a single component out of one of the pixel shader input registers.</span></span> <span data-ttu-id="50e1b-113">宣告上的插補模式必須是常數 (插補不會套用) 。</span><span class="sxs-lookup"><span data-stu-id="50e1b-113">The interpolation mode on the declaration must be constant (interpolation does not apply).</span></span>

<span data-ttu-id="50e1b-114">您可以在 D3D 11.3 和 D3D12 中使用保守的點陣化功能。</span><span class="sxs-lookup"><span data-stu-id="50e1b-114">Conservative rasterization is available in both D3D11.3 and D3D12.</span></span> <span data-ttu-id="50e1b-115">請參閱：</span><span class="sxs-lookup"><span data-stu-id="50e1b-115">Refer to:</span></span>

-   [<span data-ttu-id="50e1b-116">D3D 11.3 保守柵格化</span><span class="sxs-lookup"><span data-stu-id="50e1b-116">D3D11.3 Conservative Rasterization</span></span>](/windows/desktop/direct3d11/conservative-rasterization)
-   [<span data-ttu-id="50e1b-117">D3D12 保守的點陣化</span><span class="sxs-lookup"><span data-stu-id="50e1b-117">D3D12 Conservative Rasterization</span></span>](/windows/desktop/direct3d12/conservative-rasterization)

## <a name="see-also"></a><span data-ttu-id="50e1b-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50e1b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50e1b-119">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="50e1b-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> <dt>

[<span data-ttu-id="50e1b-120">著色器模型5.1 系統值</span><span class="sxs-lookup"><span data-stu-id="50e1b-120">Shader Model 5.1 System Values</span></span>](shader-model-5-1-system-values.md)
</dt> </dl>

 

 
