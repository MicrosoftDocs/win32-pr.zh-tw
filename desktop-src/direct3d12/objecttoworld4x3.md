---
description: ObjectToWorld4x3-從物件空間轉換成世界空間的矩陣。
ms.assetid: ''
title: ObjectToWorld4x3
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObjectToWorld4x3
api_type:
- NA
ms.openlocfilehash: bc91c6e98aceb13af3f589f873a4b96c2b1843c4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098296"
---
# <a name="objecttoworld4x3"></a><span data-ttu-id="e2c47-103">ObjectToWorld4x3</span><span class="sxs-lookup"><span data-stu-id="e2c47-103">ObjectToWorld4x3</span></span>

<span data-ttu-id="e2c47-104">從物件空間轉換成世界空間的矩陣。</span><span class="sxs-lookup"><span data-stu-id="e2c47-104">A matrix for transforming from object-space to world-space.</span></span> <span data-ttu-id="e2c47-105">物件空間是指目前最下層加速結構的空間。</span><span class="sxs-lookup"><span data-stu-id="e2c47-105">Object-space refers to the space of the current bottom-level acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2c47-106">語法</span><span class="sxs-lookup"><span data-stu-id="e2c47-106">Syntax</span></span>

```
void ObjectToWorld4x3();

```




## <a name="remarks"></a><span data-ttu-id="e2c47-107">備註</span><span class="sxs-lookup"><span data-stu-id="e2c47-107">Remarks</span></span>

<span data-ttu-id="e2c47-108">矩陣是 **ObjectToWorld3x4** 矩陣的調換。</span><span class="sxs-lookup"><span data-stu-id="e2c47-108">The matrix is a transposition of **ObjectToWorld3x4** matrix.</span></span>

<span data-ttu-id="e2c47-109">您可以從下列 raytracing 著色器類型呼叫這個函數：</span><span class="sxs-lookup"><span data-stu-id="e2c47-109">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="e2c47-110">**任何命中著色器**</span><span class="sxs-lookup"><span data-stu-id="e2c47-110">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="e2c47-111">**最接近的點擊著色器**</span><span class="sxs-lookup"><span data-stu-id="e2c47-111">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="e2c47-112">**交集著色器**</span><span class="sxs-lookup"><span data-stu-id="e2c47-112">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="e2c47-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2c47-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2c47-114">Direct3D 12 Raytracing HLSL 參考</span><span class="sxs-lookup"><span data-stu-id="e2c47-114">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




