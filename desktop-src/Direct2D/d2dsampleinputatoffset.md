---
title: 'D2DSampleInputAtOffset 函式 (D2d1effecthelpers) '
description: 在輸入座標的位移位移上取樣輸入 N。 僅適用于複雜的輸入。
ms.assetid: 4A01264E-04E3-49BD-9EF8-7834D9B8B0B8
keywords:
- D2DSampleInputAtOffset 函式 Direct2D
topic_type:
- apiref
api_name:
- D2DSampleInputAtOffset
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7718f8f48ddfd316d1312dbdff3a5da1f45dfb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993240"
---
# <a name="d2dsampleinputatoffset-function"></a><span data-ttu-id="7898d-105">D2DSampleInputAtOffset 函式</span><span class="sxs-lookup"><span data-stu-id="7898d-105">D2DSampleInputAtOffset function</span></span>

<span data-ttu-id="7898d-106">在輸入座標的位移位移上取樣輸入 N。</span><span class="sxs-lookup"><span data-stu-id="7898d-106">Samples input N at an offset of offset from the input coordinate.</span></span> <span data-ttu-id="7898d-107">僅適用于複雜的輸入。</span><span class="sxs-lookup"><span data-stu-id="7898d-107">Only available for complex inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="7898d-108">語法</span><span class="sxs-lookup"><span data-stu-id="7898d-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DSampleInputAtOffset(
  in uint N,
  in float2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="7898d-109">參數</span><span class="sxs-lookup"><span data-stu-id="7898d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7898d-110">*N* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7898d-110">*N* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7898d-111">輸入編號。</span><span class="sxs-lookup"><span data-stu-id="7898d-111">The input number.</span></span>

</dd> <dt>

<span data-ttu-id="7898d-112">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7898d-112">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7898d-113">Uv 位移。</span><span class="sxs-lookup"><span data-stu-id="7898d-113">The uv offset.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7898d-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="7898d-114">Return value</span></span>

<span data-ttu-id="7898d-115">函數會傳回 **float4**，格式為 TEXCOORDN。</span><span class="sxs-lookup"><span data-stu-id="7898d-115">The function returns a **float4**, in the format TEXCOORDN.</span></span>

## <a name="remarks"></a><span data-ttu-id="7898d-116">備註</span><span class="sxs-lookup"><span data-stu-id="7898d-116">Remarks</span></span>

<span data-ttu-id="7898d-117">下列範例顯示在反白顯示和遮蔽漸層遮罩中使用的函式。</span><span class="sxs-lookup"><span data-stu-id="7898d-117">The following example shows the function being used as part of a highlighting and shadows gradient mask.</span></span>

``` syntax
  
D2D_PS_ENTRY(HighlightsAndShadowsGradientMask)  
{  
    MIN_TYPE(float4) blurred = D2DGetInput(0);  
  
    // Compute X and Y gradients 
    MIN_TYPE(float) dX1 = D2DSampleInputAtOffset(0, float2(1, 0));
    MIN_TYPE(float) dX2 = D2DSampleInputAtOffset(0, float2(-1, 0));
    MIN_TYPE(float) dY1 = D2DSampleInputAtOffset(0, float2(0, 1));
    MIN_TYPE(float) dY2 = D2DSampleInputAtOffset(0, float2(0, -1));
    
    // TODO: math to calculate shadow gradients

    // Return the value in the alpha channel.  
    blurred.a = // TODO: math to calculate blurred value
  
    return blurred;  
}  
```

## <a name="requirements"></a><span data-ttu-id="7898d-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="7898d-118">Requirements</span></span>



| <span data-ttu-id="7898d-119">需求</span><span class="sxs-lookup"><span data-stu-id="7898d-119">Requirement</span></span> | <span data-ttu-id="7898d-120">值</span><span class="sxs-lookup"><span data-stu-id="7898d-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7898d-121">標頭</span><span class="sxs-lookup"><span data-stu-id="7898d-121">Header</span></span><br/> | <dl> <span data-ttu-id="7898d-122"><dt>D2d1effecthelpers.hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="7898d-122"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="7898d-123">DLL</span><span class="sxs-lookup"><span data-stu-id="7898d-123">DLL</span></span><br/>    | <dl> <span data-ttu-id="7898d-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7898d-124"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="7898d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7898d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7898d-126">效果著色器連結</span><span class="sxs-lookup"><span data-stu-id="7898d-126">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="7898d-127">HLSL 協助程式</span><span class="sxs-lookup"><span data-stu-id="7898d-127">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





