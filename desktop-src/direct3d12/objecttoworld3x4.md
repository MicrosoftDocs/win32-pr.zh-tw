---
description: ObjectToWorld3x4-從物件空間轉換成世界空間的矩陣。
ms.assetid: ''
title: ObjectToWorld3x4
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObjectToWorld3x4
api_type:
- NA
ms.openlocfilehash: 947676c25bd5cac50749c737afd7e4ff75426c0a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107736"
---
# <a name="objecttoworld3x4"></a><span data-ttu-id="6d0ef-103">ObjectToWorld3x4</span><span class="sxs-lookup"><span data-stu-id="6d0ef-103">ObjectToWorld3x4</span></span>

<span data-ttu-id="6d0ef-104">從物件空間轉換成世界空間的矩陣。</span><span class="sxs-lookup"><span data-stu-id="6d0ef-104">A matrix for transforming from object-space to world-space.</span></span> <span data-ttu-id="6d0ef-105">物件空間是指目前最下層加速結構的空間。</span><span class="sxs-lookup"><span data-stu-id="6d0ef-105">Object-space refers to the space of the current bottom-level acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d0ef-106">語法</span><span class="sxs-lookup"><span data-stu-id="6d0ef-106">Syntax</span></span>

```
void ObjectToWorld3x4();

```




## <a name="remarks"></a><span data-ttu-id="6d0ef-107">備註</span><span class="sxs-lookup"><span data-stu-id="6d0ef-107">Remarks</span></span>

<span data-ttu-id="6d0ef-108">矩陣是 **ObjectToWorld4x3** 矩陣的調換。</span><span class="sxs-lookup"><span data-stu-id="6d0ef-108">The matrix is a transposition of **ObjectToWorld4x3** matrix.</span></span>

<span data-ttu-id="6d0ef-109">您可以從下列 raytracing 著色器類型呼叫這個函數：</span><span class="sxs-lookup"><span data-stu-id="6d0ef-109">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="6d0ef-110">**任何命中著色器**</span><span class="sxs-lookup"><span data-stu-id="6d0ef-110">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="6d0ef-111">**最接近的點擊著色器**</span><span class="sxs-lookup"><span data-stu-id="6d0ef-111">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="6d0ef-112">**交集著色器**</span><span class="sxs-lookup"><span data-stu-id="6d0ef-112">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="6d0ef-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6d0ef-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d0ef-114">Direct3D 12 Raytracing HLSL 參考</span><span class="sxs-lookup"><span data-stu-id="6d0ef-114">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




