---
title: 'D2DSampleInput 函式 (D2d1effecthelpers) '
description: 在位置 uv 的輸入 N 範例。 僅適用于複雜的輸入。
ms.assetid: 8C1E3B23-D05B-4FCC-B32F-A5870A7C3FEF
keywords:
- D2DSampleInput 函式 Direct2D
topic_type:
- apiref
api_name:
- D2DSampleInput
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5929e9c113e5fa9a7c8a72003357b280a810e49e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983207"
---
# <a name="d2dsampleinput-function"></a><span data-ttu-id="b7414-105">D2DSampleInput 函式</span><span class="sxs-lookup"><span data-stu-id="b7414-105">D2DSampleInput function</span></span>

<span data-ttu-id="b7414-106">在位置 uv 的輸入 N 範例。</span><span class="sxs-lookup"><span data-stu-id="b7414-106">Samples input N at position uv.</span></span> <span data-ttu-id="b7414-107">僅適用于複雜的輸入。</span><span class="sxs-lookup"><span data-stu-id="b7414-107">Only available for complex inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7414-108">語法</span><span class="sxs-lookup"><span data-stu-id="b7414-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DSampleInput(
  in uint N,
  in float2 uv
);
```

## <a name="parameters"></a><span data-ttu-id="b7414-109">參數</span><span class="sxs-lookup"><span data-stu-id="b7414-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7414-110">*N* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7414-110">*N* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7414-111">輸入編號。</span><span class="sxs-lookup"><span data-stu-id="b7414-111">The input number.</span></span>

</dd> <dt>

<span data-ttu-id="b7414-112">*uv* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7414-112">*uv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7414-113">Uv 位置。</span><span class="sxs-lookup"><span data-stu-id="b7414-113">The uv position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7414-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="b7414-114">Return value</span></span>

<span data-ttu-id="b7414-115">函數會傳回 **float4**，格式為 TEXCOORDN。</span><span class="sxs-lookup"><span data-stu-id="b7414-115">The function returns a **float4**, in the format TEXCOORDN.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7414-116">備註</span><span class="sxs-lookup"><span data-stu-id="b7414-116">Remarks</span></span>

<span data-ttu-id="b7414-117">下列範例顯示用來計算表面法線的函數。</span><span class="sxs-lookup"><span data-stu-id="b7414-117">The following example shows the function being used to calculate surface normals.</span></span>

``` syntax
   
float3 CalculateSurfaceNormal(TAPARGS)  
{  
    float3 normal = float3(0, 0, 1.0);  
  
    // unrolled loop  
    normal.xy += tap1.zw * D2DSampleInput(0, tap1.xy).a;  
    normal.xy += tap2.zw * D2DSampleInput(0, tap2.xy).a;  
    normal.xy += tap3.zw * D2DSampleInput(0, tap3.xy).a;  
    normal.xy += tap4.zw * D2DSampleInput(0, tap4.xy).a;  
    normal.xy += tap5.zw * D2DSampleInput(0, tap5.xy).a;  
    normal.xy += tap6.zw * D2DSampleInput(0, tap6.xy).a;  
  
    normal = normalize(normal);  
      
    return normal;  
}  
```

## <a name="requirements"></a><span data-ttu-id="b7414-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7414-118">Requirements</span></span>



| <span data-ttu-id="b7414-119">需求</span><span class="sxs-lookup"><span data-stu-id="b7414-119">Requirement</span></span> | <span data-ttu-id="b7414-120">值</span><span class="sxs-lookup"><span data-stu-id="b7414-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7414-121">標頭</span><span class="sxs-lookup"><span data-stu-id="b7414-121">Header</span></span><br/> | <dl> <span data-ttu-id="b7414-122"><dt>D2d1effecthelpers.hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="b7414-122"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="b7414-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b7414-123">DLL</span></span><br/>    | <dl> <span data-ttu-id="b7414-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7414-124"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="b7414-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7414-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7414-126">效果著色器連結</span><span class="sxs-lookup"><span data-stu-id="b7414-126">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="b7414-127">HLSL 協助程式</span><span class="sxs-lookup"><span data-stu-id="b7414-127">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





