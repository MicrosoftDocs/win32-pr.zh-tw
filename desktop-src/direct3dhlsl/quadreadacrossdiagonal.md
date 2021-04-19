---
title: QuadReadAcrossDiagonal 函式
description: 傳回指定的區域值，此值是從這個四個對角線中的相反通道讀取的。
ms.assetid: 2914F1F9-5CE2-437A-ADDB-4955D2C1490B
keywords:
- QuadReadAcrossDiagonal 函式 HLSL
topic_type:
- apiref
api_name:
- QuadReadAcrossDiagonal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0e208a022f339e69ea63120db1f67070fa4dfed7
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104991038"
---
# <a name="quadreadacrossdiagonal-function"></a><span data-ttu-id="cca7a-104">QuadReadAcrossDiagonal 函式</span><span class="sxs-lookup"><span data-stu-id="cca7a-104">QuadReadAcrossDiagonal function</span></span>

<span data-ttu-id="cca7a-105">傳回指定的區域值，此值是從這個四個對角線中的相反通道讀取的。</span><span class="sxs-lookup"><span data-stu-id="cca7a-105">Returns the specified local value which is read from the diagonally opposite lane in this quad.</span></span>

## <a name="syntax"></a><span data-ttu-id="cca7a-106">語法</span><span class="sxs-lookup"><span data-stu-id="cca7a-106">Syntax</span></span>


``` syntax
<type> QuadReadAcrossDiagonal(
   <type> localValue
);
```



## <a name="parameters"></a><span data-ttu-id="cca7a-107">參數</span><span class="sxs-lookup"><span data-stu-id="cca7a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cca7a-108">*localValue*</span><span class="sxs-lookup"><span data-stu-id="cca7a-108">*localValue*</span></span> 
</dt> <dd>

<span data-ttu-id="cca7a-109">要求的類型。</span><span class="sxs-lookup"><span data-stu-id="cca7a-109">The requested type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cca7a-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="cca7a-110">Return value</span></span>

<span data-ttu-id="cca7a-111">指定的區域值，此值會從這個四項的對角線方向進行讀取。</span><span class="sxs-lookup"><span data-stu-id="cca7a-111">The specified local value which is read from the diagonally opposite lane in this quad.</span></span>

## <a name="remarks"></a><span data-ttu-id="cca7a-112">備註</span><span class="sxs-lookup"><span data-stu-id="cca7a-112">Remarks</span></span>

<span data-ttu-id="cca7a-113">如需四邊形的詳細資訊，請參閱 [著色器模型6的總覽](hlsl-shader-model-6-0-features-for-direct3d-12.md)。</span><span class="sxs-lookup"><span data-stu-id="cca7a-113">For more information on quads, refer to [Overview of Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span></span>

<span data-ttu-id="cca7a-114">只有在圖元和計算著色器中才支援來自著色器模型6.0 的函式。</span><span class="sxs-lookup"><span data-stu-id="cca7a-114">This function is supported from shader model 6.0 only in pixel and compute shaders.</span></span>



 

## <a name="see-also"></a><span data-ttu-id="cca7a-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cca7a-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cca7a-116">著色器模型6</span><span class="sxs-lookup"><span data-stu-id="cca7a-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




