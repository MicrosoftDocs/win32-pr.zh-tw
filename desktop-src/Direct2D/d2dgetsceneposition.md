---
title: 'D2DGetScenePosition 函式 (D2d1effecthelpers) '
description: 傳回輸入場景位置的值 \_ 。 只有當 D2D \_ 需要 \_ 場景 \_ 位置在原始程式檔中宣告時，才可使用。
ms.assetid: 451E4C31-D93D-44B6-81D1-AC5FD986ACBD
keywords:
- D2DGetScenePosition 函式 Direct2D
topic_type:
- apiref
api_name:
- D2DGetScenePosition
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace0ee4d60f8c140825e41ba47de941bca09e67c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995060"
---
# <a name="d2dgetsceneposition-function"></a><span data-ttu-id="b31f5-105">D2DGetScenePosition 函式</span><span class="sxs-lookup"><span data-stu-id="b31f5-105">D2DGetScenePosition function</span></span>

<span data-ttu-id="b31f5-106">傳回輸入場景位置的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b31f5-106">Returns the value of the input SCENE\_POSITION.</span></span> <span data-ttu-id="b31f5-107">只有當 D2D \_ 需要 \_ 場景 \_ 位置在原始程式檔中宣告時，才可使用。</span><span class="sxs-lookup"><span data-stu-id="b31f5-107">Only available when D2D\_REQUIRES\_SCENE\_POSITION is declared in the source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="b31f5-108">語法</span><span class="sxs-lookup"><span data-stu-id="b31f5-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DGetScenePosition(void);
```

## <a name="parameters"></a><span data-ttu-id="b31f5-109">參數</span><span class="sxs-lookup"><span data-stu-id="b31f5-109">Parameters</span></span>

<span data-ttu-id="b31f5-110">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="b31f5-110">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b31f5-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b31f5-111">Return value</span></span>

<span data-ttu-id="b31f5-112">函數會傳回格式場景位置的 **float4** \_ 。</span><span class="sxs-lookup"><span data-stu-id="b31f5-112">The function returns a **float4** in the format SCENE\_POSITION.</span></span>

## <a name="remarks"></a><span data-ttu-id="b31f5-113">備註</span><span class="sxs-lookup"><span data-stu-id="b31f5-113">Remarks</span></span>

<span data-ttu-id="b31f5-114">下列範例示範如何在產生溶解模式時使用函數。</span><span class="sxs-lookup"><span data-stu-id="b31f5-114">The following example shows the use of the function in generating a dissolve pattern.</span></span>

``` syntax
D2D_PS_ENTRY(BlendDissolve)  
{  
    min16float4 dest   = D2DGetInput(0);  
    min16float4 source = D2DGetInput(1);  
  
    min16float4 color = dest;  
  
    if ((source.a > 0.0) && (source.a >= Rand((min16float2)D2DGetScenePosition().xy)))  
    {  
        // TODO: perform  dissovlve math
    }  
  
    return color;  
}  
```

## <a name="requirements"></a><span data-ttu-id="b31f5-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="b31f5-115">Requirements</span></span>



| <span data-ttu-id="b31f5-116">需求</span><span class="sxs-lookup"><span data-stu-id="b31f5-116">Requirement</span></span> | <span data-ttu-id="b31f5-117">值</span><span class="sxs-lookup"><span data-stu-id="b31f5-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b31f5-118">標頭</span><span class="sxs-lookup"><span data-stu-id="b31f5-118">Header</span></span><br/> | <dl> <span data-ttu-id="b31f5-119"><dt>D2d1effecthelpers.hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="b31f5-119"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="b31f5-120">DLL</span><span class="sxs-lookup"><span data-stu-id="b31f5-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="b31f5-121"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b31f5-121"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="b31f5-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b31f5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b31f5-123">效果著色器連結</span><span class="sxs-lookup"><span data-stu-id="b31f5-123">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="b31f5-124">HLSL 協助程式</span><span class="sxs-lookup"><span data-stu-id="b31f5-124">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





