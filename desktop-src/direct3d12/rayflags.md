---
description: 不帶正負號的整數，其中包含目前的光線旗標。
ms.assetid: ''
title: RayFlags
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RayFlags
api_type:
- NA
ms.openlocfilehash: 3aedb39ebaaadfc5c3b17af31c9ac3d6670e0b89
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973176"
---
# <a name="rayflags"></a><span data-ttu-id="deeca-103">RayFlags</span><span class="sxs-lookup"><span data-stu-id="deeca-103">RayFlags</span></span>

<span data-ttu-id="deeca-104">包含目前 [**ray_flag**](ray_flag.md) 旗標的不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="deeca-104">An unsigned integer containing the current [**ray_flag**](ray_flag.md) flags.</span></span> 

## <a name="syntax"></a><span data-ttu-id="deeca-105">語法</span><span class="sxs-lookup"><span data-stu-id="deeca-105">Syntax</span></span>

```
uint RayFlags();

```

## <a name="remarks"></a><span data-ttu-id="deeca-106">備註</span><span class="sxs-lookup"><span data-stu-id="deeca-106">Remarks</span></span>

<span data-ttu-id="deeca-107">您可以從下列 raytracing 著色器類型呼叫這個函數：</span><span class="sxs-lookup"><span data-stu-id="deeca-107">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="deeca-108">**任何命中著色器**</span><span class="sxs-lookup"><span data-stu-id="deeca-108">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="deeca-109">**最接近的點擊著色器**</span><span class="sxs-lookup"><span data-stu-id="deeca-109">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="deeca-110">**交集著色器**</span><span class="sxs-lookup"><span data-stu-id="deeca-110">**Intersection Shader**</span></span>](intersection-shader.md)
* [<span data-ttu-id="deeca-111">**遺漏著色器**</span><span class="sxs-lookup"><span data-stu-id="deeca-111">**Miss Shader**</span></span>](miss-shader.md)





## <a name="see-also"></a><span data-ttu-id="deeca-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="deeca-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deeca-113">Direct3D 12 Raytracing HLSL 參考</span><span class="sxs-lookup"><span data-stu-id="deeca-113">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




