---
title: 'D2DGetInputCoordinate 函式 (D2d1effecthelpers) '
description: 傳回輸入 TEXCOORDN 的值。 僅適用于複雜的輸入。
ms.assetid: 60125E23-53B3-45ED-89FE-684E79004F6B
keywords:
- D2DGetInputCoordinate 函式 Direct2D
topic_type:
- apiref
api_name:
- D2DGetInputCoordinate
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5d9ee759de12bb8b017d582026dd5b5ca8c3fb3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978480"
---
# <a name="d2dgetinputcoordinate-function"></a><span data-ttu-id="74c48-105">D2DGetInputCoordinate 函式</span><span class="sxs-lookup"><span data-stu-id="74c48-105">D2DGetInputCoordinate function</span></span>

<span data-ttu-id="74c48-106">傳回輸入 TEXCOORDN 的值。</span><span class="sxs-lookup"><span data-stu-id="74c48-106">Returns the value of the input TEXCOORDN.</span></span> <span data-ttu-id="74c48-107">僅適用于複雜的輸入。</span><span class="sxs-lookup"><span data-stu-id="74c48-107">Available only for complex inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="74c48-108">語法</span><span class="sxs-lookup"><span data-stu-id="74c48-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DGetInputCoordinate(
  in uint N
);
```

## <a name="parameters"></a><span data-ttu-id="74c48-109">參數</span><span class="sxs-lookup"><span data-stu-id="74c48-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74c48-110">*N* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74c48-110">*N* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74c48-111">輸入編號。</span><span class="sxs-lookup"><span data-stu-id="74c48-111">The input number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74c48-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="74c48-112">Return value</span></span>

<span data-ttu-id="74c48-113">函數會傳回 **float4**，格式為 TEXCOORDN。</span><span class="sxs-lookup"><span data-stu-id="74c48-113">The function returns a **float4**, in the format TEXCOORDN.</span></span>

## <a name="remarks"></a><span data-ttu-id="74c48-114">備註</span><span class="sxs-lookup"><span data-stu-id="74c48-114">Remarks</span></span>

<span data-ttu-id="74c48-115">此函式所傳回的座標在材質空間中。</span><span class="sxs-lookup"><span data-stu-id="74c48-115">The coordinate returned by this function is in texel space.</span></span> <span data-ttu-id="74c48-116">著色器不應該依賴此值的計算方式。</span><span class="sxs-lookup"><span data-stu-id="74c48-116">A shader shouldn't take any dependencies on how this value is calculated.</span></span> <span data-ttu-id="74c48-117">它只能用來取樣圖元著色器的輸入。</span><span class="sxs-lookup"><span data-stu-id="74c48-117">It should use it only to sample the pixel shader's input.</span></span> <span data-ttu-id="74c48-118">如需詳細資訊，請參閱 [將圖元著色器加入至自訂轉換](./custom-effects.md#adding-a-pixel-shader-to-a-custom-transform)。</span><span class="sxs-lookup"><span data-stu-id="74c48-118">For more info, see [Adding a pixel shader to a custom transform](./custom-effects.md#adding-a-pixel-shader-to-a-custom-transform).</span></span>

<span data-ttu-id="74c48-119">下列範例顯示用於置換地圖效果的函式。</span><span class="sxs-lookup"><span data-stu-id="74c48-119">The following example shows the function used for a displacement map effect.</span></span>

``` syntax
float2 GetDisplacementOffset(float4 uv0, float4 uv1)  
{  
    // TODO: return the displacement offset 
}  
  
D2D_PS_ENTRY(DisplacementMapBilinear)  
{  
    const float4 coord0 = D2DGetInputCoordinate(0);  
    const float4 coord1 = D2DGetInputCoordinate(1);  
    return D2DSampleInput(0, GetDisplacementOffset(coord0, coord1) * coord0.zw + coord0.xy);  
}  
```

## <a name="requirements"></a><span data-ttu-id="74c48-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="74c48-120">Requirements</span></span>



| <span data-ttu-id="74c48-121">需求</span><span class="sxs-lookup"><span data-stu-id="74c48-121">Requirement</span></span> | <span data-ttu-id="74c48-122">值</span><span class="sxs-lookup"><span data-stu-id="74c48-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74c48-123">標頭</span><span class="sxs-lookup"><span data-stu-id="74c48-123">Header</span></span><br/> | <dl> <span data-ttu-id="74c48-124"><dt>D2d1effecthelpers.hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="74c48-124"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="74c48-125">DLL</span><span class="sxs-lookup"><span data-stu-id="74c48-125">DLL</span></span><br/>    | <dl> <span data-ttu-id="74c48-126"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74c48-126"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="74c48-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74c48-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74c48-128">效果著色器連結</span><span class="sxs-lookup"><span data-stu-id="74c48-128">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="74c48-129">HLSL 協助程式</span><span class="sxs-lookup"><span data-stu-id="74c48-129">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

