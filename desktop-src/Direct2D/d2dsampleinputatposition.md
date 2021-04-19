---
title: 'D2DSampleInputAtPosition 函式 (D2d1effecthelpers) '
description: 在絕對場景位置（而非輸入相關位置）輸入 N 的範例。 僅適用于複雜的輸入。
ms.assetid: E839287F-91D1-4591-8DE7-1DFC3001A23D
keywords:
- D2DSampleInputAtPosition 函式 Direct2D
topic_type:
- apiref
api_name:
- D2DSampleInputAtPosition
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e12bba2b83f3956cf4b654c00b0650a6a0ce9a54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993646"
---
# <a name="d2dsampleinputatposition-function"></a><span data-ttu-id="16661-105">D2DSampleInputAtPosition 函式</span><span class="sxs-lookup"><span data-stu-id="16661-105">D2DSampleInputAtPosition function</span></span>

<span data-ttu-id="16661-106">在絕對場景位置（而非輸入相關位置）輸入 N 的範例。</span><span class="sxs-lookup"><span data-stu-id="16661-106">Samples input N at an absolute scene position, rather than an input-relative position.</span></span> <span data-ttu-id="16661-107">僅適用于複雜的輸入。</span><span class="sxs-lookup"><span data-stu-id="16661-107">Only available for complex inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="16661-108">語法</span><span class="sxs-lookup"><span data-stu-id="16661-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DSampleInputAtPosition(
  in uint N,
  in float2 uv
);
```

## <a name="parameters"></a><span data-ttu-id="16661-109">參數</span><span class="sxs-lookup"><span data-stu-id="16661-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16661-110">*N* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="16661-110">*N* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16661-111">輸入編號。</span><span class="sxs-lookup"><span data-stu-id="16661-111">The input number.</span></span>

</dd> <dt>

<span data-ttu-id="16661-112">*uv* \[在\]</span><span class="sxs-lookup"><span data-stu-id="16661-112">*uv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16661-113">Uv 位置。</span><span class="sxs-lookup"><span data-stu-id="16661-113">The uv position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16661-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="16661-114">Return value</span></span>

<span data-ttu-id="16661-115">函數會傳回 **float4**，格式為 TEXCOORDN。</span><span class="sxs-lookup"><span data-stu-id="16661-115">The function returns a **float4**, in the format TEXCOORDN.</span></span>

## <a name="remarks"></a><span data-ttu-id="16661-116">備註</span><span class="sxs-lookup"><span data-stu-id="16661-116">Remarks</span></span>

<span data-ttu-id="16661-117">下列範例會顯示迴圈包裝中使用的函式。</span><span class="sxs-lookup"><span data-stu-id="16661-117">The following example shows the function used in a circular wrap.</span></span>

``` syntax
  
D2D_PS_ENTRY(CircularWrapPS)  
{  
    // TODO: perform math to calculate a circular wrap
  
    // Find the input scene position.  
    float2 inputScenePosition = float2( TODO: add math parameters );  
  
    return D2DSampleInputAtPosition(0, inputScenePosition);  
}
```

## <a name="requirements"></a><span data-ttu-id="16661-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="16661-118">Requirements</span></span>



| <span data-ttu-id="16661-119">需求</span><span class="sxs-lookup"><span data-stu-id="16661-119">Requirement</span></span> | <span data-ttu-id="16661-120">值</span><span class="sxs-lookup"><span data-stu-id="16661-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16661-121">標頭</span><span class="sxs-lookup"><span data-stu-id="16661-121">Header</span></span><br/> | <dl> <span data-ttu-id="16661-122"><dt>D2d1effecthelpers.hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="16661-122"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="16661-123">DLL</span><span class="sxs-lookup"><span data-stu-id="16661-123">DLL</span></span><br/>    | <dl> <span data-ttu-id="16661-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16661-124"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="16661-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="16661-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16661-126">效果著色器連結</span><span class="sxs-lookup"><span data-stu-id="16661-126">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="16661-127">HLSL 協助程式</span><span class="sxs-lookup"><span data-stu-id="16661-127">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





