---
title: 'D2DGetInput 函式 (D2d1effecthelpers) '
description: 傳回輸入座標的輸入 N 的色彩。 僅適用于簡單的輸入。
ms.assetid: 74B6F814-53C7-4C8C-B45C-3CB23B9D8BED
keywords:
- D2DGetInput 函式 Direct2D
topic_type:
- apiref
api_name:
- D2DGetInput
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd6ec0fe858149ee53da1f8ca8a02c12756d6a90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979538"
---
# <a name="d2dgetinput-function"></a><span data-ttu-id="84f17-105">D2DGetInput 函式</span><span class="sxs-lookup"><span data-stu-id="84f17-105">D2DGetInput function</span></span>

<span data-ttu-id="84f17-106">傳回輸入座標的輸入 N 的色彩。</span><span class="sxs-lookup"><span data-stu-id="84f17-106">Returns the color of input N at the input coordinate.</span></span> <span data-ttu-id="84f17-107">僅適用于簡單的輸入。</span><span class="sxs-lookup"><span data-stu-id="84f17-107">Only available for simple inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="84f17-108">語法</span><span class="sxs-lookup"><span data-stu-id="84f17-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DGetInput(
  in uint N
);
```

## <a name="parameters"></a><span data-ttu-id="84f17-109">參數</span><span class="sxs-lookup"><span data-stu-id="84f17-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84f17-110">*N* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="84f17-110">*N* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84f17-111">輸入編號。</span><span class="sxs-lookup"><span data-stu-id="84f17-111">The input number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84f17-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="84f17-112">Return value</span></span>

<span data-ttu-id="84f17-113">函數會傳回 **float4**，其中包含 INPUTN 格式的 RGBA 色彩。</span><span class="sxs-lookup"><span data-stu-id="84f17-113">The function returns a **float4**, containing the RGBA color in the format INPUTN.</span></span>

## <a name="remarks"></a><span data-ttu-id="84f17-114">備註</span><span class="sxs-lookup"><span data-stu-id="84f17-114">Remarks</span></span>

<span data-ttu-id="84f17-115">下列範例顯示在算術複合效果中使用的函數。</span><span class="sxs-lookup"><span data-stu-id="84f17-115">The following example shows the function being used as part of an arithmetic composite effect.</span></span>

``` syntax
  
D2D_PS_ENTRY(PS_NAME)  
{  
    MIN_TYPE(float4) sourceColor = D2DGetInput(0);  
    MIN_TYPE(float4) destColor   = D2DGetInput(1);  
      
    MIN_TYPE(float4) output = // TODO: add math to composite source and dest

    return output;  
}  
```

<span data-ttu-id="84f17-116">此外，如需使用此函數的另一個範例，請參閱 [D2D \_ PS \_ 專案](d2d-ps-entry.md) 的備註。</span><span class="sxs-lookup"><span data-stu-id="84f17-116">Also, refer to the remarks for [D2D\_PS\_ENTRY](d2d-ps-entry.md) for another example of the use of this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="84f17-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="84f17-117">Requirements</span></span>



| <span data-ttu-id="84f17-118">需求</span><span class="sxs-lookup"><span data-stu-id="84f17-118">Requirement</span></span> | <span data-ttu-id="84f17-119">值</span><span class="sxs-lookup"><span data-stu-id="84f17-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84f17-120">標頭</span><span class="sxs-lookup"><span data-stu-id="84f17-120">Header</span></span><br/> | <dl> <span data-ttu-id="84f17-121"><dt>D2d1effecthelpers.hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="84f17-121"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="84f17-122">DLL</span><span class="sxs-lookup"><span data-stu-id="84f17-122">DLL</span></span><br/>    | <dl> <span data-ttu-id="84f17-123"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84f17-123"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="84f17-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="84f17-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84f17-125">效果著色器連結</span><span class="sxs-lookup"><span data-stu-id="84f17-125">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="84f17-126">HLSL 協助程式</span><span class="sxs-lookup"><span data-stu-id="84f17-126">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





