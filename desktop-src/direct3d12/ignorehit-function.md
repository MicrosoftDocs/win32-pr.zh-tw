---
description: 從任何命中的著色器呼叫，以拒絕點擊並結束著色器。
ms.assetid: ''
title: IgnoreHit 函式
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IgnoreHit
api_type:
- NA
ms.openlocfilehash: 66d450ce5a03e07e779ca5131443cdf67398cf19
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000051"
---
# <a name="ignorehit-function"></a><span data-ttu-id="ec0f4-103">IgnoreHit 函式</span><span class="sxs-lookup"><span data-stu-id="ec0f4-103">IgnoreHit function</span></span>

<span data-ttu-id="ec0f4-104">從 [任何命中的著色器](any-hit-shader.md) 呼叫，以拒絕點擊並結束著色器。</span><span class="sxs-lookup"><span data-stu-id="ec0f4-104">Called from an [any hit shader](any-hit-shader.md) to reject the hit and end the shader.</span></span> <span data-ttu-id="ec0f4-105">點擊搜尋會繼續進行，而不會認可目前點擊的距離和屬性。</span><span class="sxs-lookup"><span data-stu-id="ec0f4-105">The hit search continues on without committing the distance and attributes for the current hit.</span></span>  <span data-ttu-id="ec0f4-106">[交集著色器](intersection-shader.md)中的 [**ReportHit**](reporthit-function.md)呼叫（如果有的話）會傳回 false。</span><span class="sxs-lookup"><span data-stu-id="ec0f4-106">The [**ReportHit**](reporthit-function.md) call in the [intersection shader](intersection-shader.md), if there is one, will return false.</span></span>  <span data-ttu-id="ec0f4-107">任何對光線承載所做的任何修改都會保留在任何點擊著色器中的這個位置。</span><span class="sxs-lookup"><span data-stu-id="ec0f4-107">Any modifications made to the ray payload up to this point in the any hit shader are preserved.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec0f4-108">語法</span><span class="sxs-lookup"><span data-stu-id="ec0f4-108">Syntax</span></span>

```
void IgnoreHit();

```


## <a name="return-value"></a><span data-ttu-id="ec0f4-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="ec0f4-109">Return Value</span></span>

<span data-ttu-id="ec0f4-110">**void**</span><span class="sxs-lookup"><span data-stu-id="ec0f4-110">**void**</span></span>

## <a name="remarks"></a><span data-ttu-id="ec0f4-111">備註</span><span class="sxs-lookup"><span data-stu-id="ec0f4-111">Remarks</span></span>

<span data-ttu-id="ec0f4-112">您可以從下列 raytracing 著色器類型呼叫這個函數：</span><span class="sxs-lookup"><span data-stu-id="ec0f4-112">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="ec0f4-113">**任何命中著色器**</span><span class="sxs-lookup"><span data-stu-id="ec0f4-113">**Any Hit Shader**</span></span>](any-hit-shader.md)




## <a name="see-also"></a><span data-ttu-id="ec0f4-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec0f4-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec0f4-115">Direct3D 12 Raytracing HLSL 參考</span><span class="sxs-lookup"><span data-stu-id="ec0f4-115">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




