---
description: 用來指出如何拒絕圖元的列舉。
MS-HAID: vspixengine.PIXELKILLREASON
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PIXELKILLREASON 列舉
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 43836288-554B-430C-861D-AAC58DE3B282
api_name:
- PIXELKILLREASON
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f87b072eec1ac98ca68171593765567f5e77e70e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317704"
---
# <a name="span-idvspixenginepixelkillreasonspanpixelkillreason-enumeration"></a><span data-ttu-id="fd81b-103"><span id="vspixengine.pixelkillreason"></span>PIXELKILLREASON 列舉</span><span class="sxs-lookup"><span data-stu-id="fd81b-103"><span id="vspixengine.pixelkillreason"></span>PIXELKILLREASON enumeration</span></span>

<span data-ttu-id="fd81b-104">用來指出如何拒絕圖元的列舉。</span><span class="sxs-lookup"><span data-stu-id="fd81b-104">An enum used to indicate why a pixel was rejected.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd81b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd81b-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="fd81b-106">常數</span><span class="sxs-lookup"><span data-stu-id="fd81b-106">Constants</span></span>

<span data-ttu-id="fd81b-107"><span id="PKR_NONE"></span><span id="pkr_none"></span>**PKR \_ 無**</span><span class="sxs-lookup"><span data-stu-id="fd81b-107"><span id="PKR_NONE"></span><span id="pkr_none"></span>**PKR\_NONE**</span></span>  
<span data-ttu-id="fd81b-108">值，指出未拒絕圖元。</span><span class="sxs-lookup"><span data-stu-id="fd81b-108">A value that indicates that the pixel was not rejected.</span></span>

<span data-ttu-id="fd81b-109"><span id="PKR_SHADERKILL"></span><span id="pkr_shaderkill"></span>**PKR \_ SHADERKILL**</span><span class="sxs-lookup"><span data-stu-id="fd81b-109"><span id="PKR_SHADERKILL"></span><span id="pkr_shaderkill"></span>**PKR\_SHADERKILL**</span></span>  
<span data-ttu-id="fd81b-110">值，表示因為未執行著色器而拒絕圖元。</span><span class="sxs-lookup"><span data-stu-id="fd81b-110">A value that indicates that the pixel was rejected because the shader didn't run.</span></span>

<span data-ttu-id="fd81b-111"><span id="PKR_SCISSORTEST"></span><span id="pkr_scissortest"></span>**PKR \_ SCISSORTEST**</span><span class="sxs-lookup"><span data-stu-id="fd81b-111"><span id="PKR_SCISSORTEST"></span><span id="pkr_scissortest"></span>**PKR\_SCISSORTEST**</span></span>  
<span data-ttu-id="fd81b-112">值，表示因為剪式測試失敗而拒絕圖元。</span><span class="sxs-lookup"><span data-stu-id="fd81b-112">A value that indicates that the pixel was rejected because the scissor test failed.</span></span>

<span data-ttu-id="fd81b-113"><span id="PKR_ALPHATEST"></span><span id="pkr_alphatest"></span>**PKR \_ ALPHATEST**</span><span class="sxs-lookup"><span data-stu-id="fd81b-113"><span id="PKR_ALPHATEST"></span><span id="pkr_alphatest"></span>**PKR\_ALPHATEST**</span></span>  
<span data-ttu-id="fd81b-114">值，表示因為 Alpha 測試失敗而拒絕圖元。</span><span class="sxs-lookup"><span data-stu-id="fd81b-114">A value that indicates that the pixel was rejected because the alpha test failed.</span></span>

<span data-ttu-id="fd81b-115"><span id="PKR_STENCILTEST"></span><span id="pkr_stenciltest"></span>**PKR \_ STENCILTEST**</span><span class="sxs-lookup"><span data-stu-id="fd81b-115"><span id="PKR_STENCILTEST"></span><span id="pkr_stenciltest"></span>**PKR\_STENCILTEST**</span></span>  
<span data-ttu-id="fd81b-116">值，表示因為樣板測試失敗而拒絕圖元。</span><span class="sxs-lookup"><span data-stu-id="fd81b-116">A value that indicates that the pixel was rejected because the stencil test failed.</span></span>

<span data-ttu-id="fd81b-117"><span id="PKR_DEPTHTEST"></span><span id="pkr_depthtest"></span>**PKR \_ DEPTHTEST**</span><span class="sxs-lookup"><span data-stu-id="fd81b-117"><span id="PKR_DEPTHTEST"></span><span id="pkr_depthtest"></span>**PKR\_DEPTHTEST**</span></span>  
<span data-ttu-id="fd81b-118">值，表示因為深度測試失敗，所以已拒絕圖元。</span><span class="sxs-lookup"><span data-stu-id="fd81b-118">A value that indicates that the pixel was rejected because the depth test failed.</span></span>

<span data-ttu-id="fd81b-119"><span id="PKR_NOTCOMPUTABLE"></span><span id="pkr_notcomputable"></span>**PKR \_ NOTCOMPUTABLE**</span><span class="sxs-lookup"><span data-stu-id="fd81b-119"><span id="PKR_NOTCOMPUTABLE"></span><span id="pkr_notcomputable"></span>**PKR\_NOTCOMPUTABLE**</span></span>  
<span data-ttu-id="fd81b-120">值，表示無法計算圖元歷史記錄。</span><span class="sxs-lookup"><span data-stu-id="fd81b-120">A value that indicates that the pixel history can't be computed.</span></span>

<span data-ttu-id="fd81b-121"><span id="PKR_ERROR"></span><span id="pkr_error"></span>**PKR \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="fd81b-121"><span id="PKR_ERROR"></span><span id="pkr_error"></span>**PKR\_ERROR**</span></span>  
<span data-ttu-id="fd81b-122">值，表示因為發生一般錯誤，所以已拒絕圖元。</span><span class="sxs-lookup"><span data-stu-id="fd81b-122">A value that indicates that the pixel was rejected because of a general error.</span></span>

<span data-ttu-id="fd81b-123"><span id="PKR_NOINTERSECTION"></span><span id="pkr_nointersection"></span>**PKR \_ NOINTERSECTION**</span><span class="sxs-lookup"><span data-stu-id="fd81b-123"><span id="PKR_NOINTERSECTION"></span><span id="pkr_nointersection"></span>**PKR\_NOINTERSECTION**</span></span>  
<span data-ttu-id="fd81b-124">值，表示因為繪製呼叫不會相交圖元，所以已拒絕圖元。</span><span class="sxs-lookup"><span data-stu-id="fd81b-124">A value that indicates that the pixel was rejected because the draw call does not intersect the pixel.</span></span>

<span data-ttu-id="fd81b-125"><span id="PKR_OCCLUDED"></span><span id="pkr_occluded"></span>**PKR \_ PIXELS OCCLUDED**</span><span class="sxs-lookup"><span data-stu-id="fd81b-125"><span id="PKR_OCCLUDED"></span><span id="pkr_occluded"></span>**PKR\_OCCLUDED**</span></span>  
<span data-ttu-id="fd81b-126">值，表示因為繪圖已 pixels occluded，所以已拒絕圖元。</span><span class="sxs-lookup"><span data-stu-id="fd81b-126">A value that indicates that the pixel was rejected because the draw was occluded.</span></span>

<span data-ttu-id="fd81b-127"><span id="PKR_DEPTHSTENCILTEST"></span><span id="pkr_depthstenciltest"></span>**PKR \_ DEPTHSTENCILTEST**</span><span class="sxs-lookup"><span data-stu-id="fd81b-127"><span id="PKR_DEPTHSTENCILTEST"></span><span id="pkr_depthstenciltest"></span>**PKR\_DEPTHSTENCILTEST**</span></span>  
<span data-ttu-id="fd81b-128">值，表示因為深度和樣板測試失敗，所以已拒絕圖元。</span><span class="sxs-lookup"><span data-stu-id="fd81b-128">A value that indicates that the pixel was rejected because the depth and stencil test failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd81b-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd81b-129">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="fd81b-130">標頭</span><span class="sxs-lookup"><span data-stu-id="fd81b-130">Header</span></span></p></td><td><span data-ttu-id="fd81b-131">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="fd81b-131">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



