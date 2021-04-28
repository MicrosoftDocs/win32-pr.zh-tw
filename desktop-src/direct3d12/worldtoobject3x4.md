---
description: WorldToObject3x4-從世界空間轉換成物件空間的矩陣。
ms.assetid: ''
title: WorldToObject3x4
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WorldToObject3x4
api_type:
- NA
ms.openlocfilehash: cc7bf7dc2f06102b9b23eafd45655f12816c8359
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105236"
---
# <a name="worldtoobject3x4"></a><span data-ttu-id="47d06-103">WorldToObject3x4</span><span class="sxs-lookup"><span data-stu-id="47d06-103">WorldToObject3x4</span></span>

<span data-ttu-id="47d06-104">從世界空間轉換成物件空間的矩陣。</span><span class="sxs-lookup"><span data-stu-id="47d06-104">A matrix for transforming from world-space to object-space.</span></span> <span data-ttu-id="47d06-105">物件空間是指目前最下層加速結構的空間。</span><span class="sxs-lookup"><span data-stu-id="47d06-105">Object-space refers to the space of the current bottom-level acceleration structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="47d06-106">語法</span><span class="sxs-lookup"><span data-stu-id="47d06-106">Syntax</span></span>

```
void WorldToObject3x4();

```




## <a name="remarks"></a><span data-ttu-id="47d06-107">備註</span><span class="sxs-lookup"><span data-stu-id="47d06-107">Remarks</span></span>

<span data-ttu-id="47d06-108">矩陣是 **WorldToObject4x3** 矩陣的調換。</span><span class="sxs-lookup"><span data-stu-id="47d06-108">The matrix is a transposition of **WorldToObject4x3** matrix.</span></span>

<span data-ttu-id="47d06-109">您可以從下列 raytracing 著色器類型呼叫這個函數：</span><span class="sxs-lookup"><span data-stu-id="47d06-109">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="47d06-110">**任何命中著色器**</span><span class="sxs-lookup"><span data-stu-id="47d06-110">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="47d06-111">**最接近的點擊著色器**</span><span class="sxs-lookup"><span data-stu-id="47d06-111">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="47d06-112">**交集著色器**</span><span class="sxs-lookup"><span data-stu-id="47d06-112">**Intersection Shader**</span></span>](intersection-shader.md)





## <a name="see-also"></a><span data-ttu-id="47d06-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="47d06-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47d06-114">Direct3D 12 Raytracing HLSL 參考</span><span class="sxs-lookup"><span data-stu-id="47d06-114">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




