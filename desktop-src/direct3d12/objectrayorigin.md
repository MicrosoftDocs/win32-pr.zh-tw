---
description: 目前光線的物件空間原點。
ms.assetid: ''
title: ObjectRayOrigin
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObjectRayOrigin
api_type:
- NA
ms.openlocfilehash: b64d3f2e6648d47659f180bf2aa3c1e912882677
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970540"
---
# <a name="objectrayorigin"></a><span data-ttu-id="4d5cd-103">ObjectRayOrigin</span><span class="sxs-lookup"><span data-stu-id="4d5cd-103">ObjectRayOrigin</span></span>

<span data-ttu-id="4d5cd-104">目前光線的物件空間原點。</span><span class="sxs-lookup"><span data-stu-id="4d5cd-104">The object-space origin for the current ray.</span></span> <span data-ttu-id="4d5cd-105">物件空間是指目前最下層加速結構的空間。</span><span class="sxs-lookup"><span data-stu-id="4d5cd-105">Object-space refers to the space of the current bottom-level acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d5cd-106">語法</span><span class="sxs-lookup"><span data-stu-id="4d5cd-106">Syntax</span></span>

```
float3 ObjectRayOrigin();

```

## <a name="remarks"></a><span data-ttu-id="4d5cd-107">備註</span><span class="sxs-lookup"><span data-stu-id="4d5cd-107">Remarks</span></span>

<span data-ttu-id="4d5cd-108">您可以從下列 raytracing 著色器類型呼叫這個函數：</span><span class="sxs-lookup"><span data-stu-id="4d5cd-108">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="4d5cd-109">**任何命中著色器**</span><span class="sxs-lookup"><span data-stu-id="4d5cd-109">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="4d5cd-110">**最接近的點擊著色器**</span><span class="sxs-lookup"><span data-stu-id="4d5cd-110">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="4d5cd-111">**交集著色器**</span><span class="sxs-lookup"><span data-stu-id="4d5cd-111">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="4d5cd-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d5cd-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d5cd-113">Direct3D 12 Raytracing HLSL 參考</span><span class="sxs-lookup"><span data-stu-id="4d5cd-113">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




