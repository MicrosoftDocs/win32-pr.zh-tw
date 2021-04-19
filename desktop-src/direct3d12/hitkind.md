---
description: 傳回作為 HitKind 參數傳遞至 ReportHit 的值。
ms.assetid: ''
title: HitKind
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HitKind
api_type:
- NA
ms.openlocfilehash: 81638996dbf69097154a2f1c235f6ab26c28dc8e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972341"
---
# <a name="hitkind"></a><span data-ttu-id="82e85-103">HitKind</span><span class="sxs-lookup"><span data-stu-id="82e85-103">HitKind</span></span>

<span data-ttu-id="82e85-104">傳回作為 **HitKind** 參數傳遞至 [**ReportHit**](reporthit-function.md)的值。</span><span class="sxs-lookup"><span data-stu-id="82e85-104">Returns the value passed as the **HitKind** parameter to [**ReportHit**](reporthit-function.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="82e85-105">語法</span><span class="sxs-lookup"><span data-stu-id="82e85-105">Syntax</span></span>

```
uint HitKind();

```



## <a name="remarks"></a><span data-ttu-id="82e85-106">備註</span><span class="sxs-lookup"><span data-stu-id="82e85-106">Remarks</span></span>

<span data-ttu-id="82e85-107">如果交集是由固定函式三角形交集所報告，則 **HitKind** 會是 (254) 的 **點擊類型 \_ \_ 三角形 \_ 正面 \_ 臉部** ，或 (255) 的 **點擊 \_ 類型 \_ 三角形 \_ \_** 。</span><span class="sxs-lookup"><span data-stu-id="82e85-107">If the intersection was reported by fixed-function triangle intersection, **HitKind** will be one of **HIT\_KIND\_TRIANGLE\_FRONT\_FACE** (254) or **HIT\_KIND\_TRIANGLE\_BACK\_FACE** (255).</span></span>

<span data-ttu-id="82e85-108">您可以從下列 raytracing 著色器類型呼叫這個函數：</span><span class="sxs-lookup"><span data-stu-id="82e85-108">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="82e85-109">**任何命中著色器**</span><span class="sxs-lookup"><span data-stu-id="82e85-109">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="82e85-110">**最接近的點擊著色器**</span><span class="sxs-lookup"><span data-stu-id="82e85-110">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="82e85-111">**交集著色器**</span><span class="sxs-lookup"><span data-stu-id="82e85-111">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="82e85-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="82e85-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82e85-113">Direct3D 12 Raytracing HLSL 參考</span><span class="sxs-lookup"><span data-stu-id="82e85-113">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




