---
description: WorldToObject4x3-從世界空間轉換成物件空間的矩陣。
ms.assetid: ''
title: WorldToObject4x3
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WorldToObject4x3
api_type:
- NA
ms.openlocfilehash: 334a79352345fb35fbbafe68248a221bdaab9f6d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105245"
---
# <a name="worldtoobject4x3"></a><span data-ttu-id="f7b46-103">WorldToObject4x3</span><span class="sxs-lookup"><span data-stu-id="f7b46-103">WorldToObject4x3</span></span>

<span data-ttu-id="f7b46-104">從世界空間轉換成物件空間的矩陣。</span><span class="sxs-lookup"><span data-stu-id="f7b46-104">A matrix for transforming from world-space to object-space.</span></span> <span data-ttu-id="f7b46-105">物件空間是指目前最下層加速結構的空間。</span><span class="sxs-lookup"><span data-stu-id="f7b46-105">Object-space refers to the space of the current bottom-level acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7b46-106">語法</span><span class="sxs-lookup"><span data-stu-id="f7b46-106">Syntax</span></span>

```
void WorldToObject4x3();

```




## <a name="remarks"></a><span data-ttu-id="f7b46-107">備註</span><span class="sxs-lookup"><span data-stu-id="f7b46-107">Remarks</span></span>

<span data-ttu-id="f7b46-108">矩陣是 **WorldToObject3x4** 矩陣的調換。</span><span class="sxs-lookup"><span data-stu-id="f7b46-108">The matrix is a transposition of **WorldToObject3x4** matrix.</span></span>

<span data-ttu-id="f7b46-109">您可以從下列 raytracing 著色器類型呼叫這個函數：</span><span class="sxs-lookup"><span data-stu-id="f7b46-109">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="f7b46-110">**任何命中著色器**</span><span class="sxs-lookup"><span data-stu-id="f7b46-110">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="f7b46-111">**最接近的點擊著色器**</span><span class="sxs-lookup"><span data-stu-id="f7b46-111">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="f7b46-112">**交集著色器**</span><span class="sxs-lookup"><span data-stu-id="f7b46-112">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="f7b46-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f7b46-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7b46-114">Direct3D 12 Raytracing HLSL 參考</span><span class="sxs-lookup"><span data-stu-id="f7b46-114">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




