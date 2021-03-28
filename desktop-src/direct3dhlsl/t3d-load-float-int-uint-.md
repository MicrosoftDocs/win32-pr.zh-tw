---
title: Texture3D：： Load (int，int，uint) 函數
description: 讀取材質資料並傳回作業的狀態。 |Texture3D：： Load (int，int，uint) 函數
ms.assetid: 3F562ADB-225F-462B-A7AC-40797BBB632A
keywords:
- Load function HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 19522fe60567e55565265ce0c8b5051c7bf7ccdd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991886"
---
# <a name="texture3dloadintintuint-function"></a><span data-ttu-id="0be32-105">Texture3D：： Load (int，int，uint) 函數</span><span class="sxs-lookup"><span data-stu-id="0be32-105">Texture3D::Load(int,int,uint) function</span></span>

<span data-ttu-id="0be32-106">讀取材質資料並傳回作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="0be32-106">Reads texture data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="0be32-107">語法</span><span class="sxs-lookup"><span data-stu-id="0be32-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  in  int  Offset,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="0be32-108">參數</span><span class="sxs-lookup"><span data-stu-id="0be32-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0be32-109">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0be32-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0be32-110">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="0be32-110">Type: **int**</span></span>

<span data-ttu-id="0be32-111">材質座標。</span><span class="sxs-lookup"><span data-stu-id="0be32-111">The texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="0be32-112">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0be32-112">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0be32-113">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="0be32-113">Type: **int**</span></span>

<span data-ttu-id="0be32-114">在取樣之前套用至材質座標的位移。</span><span class="sxs-lookup"><span data-stu-id="0be32-114">An offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="0be32-115">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0be32-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0be32-116">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="0be32-116">Type: **uint**</span></span>

<span data-ttu-id="0be32-117">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="0be32-117">The status of the operation.</span></span> <span data-ttu-id="0be32-118">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="0be32-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="0be32-119">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="0be32-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="0be32-120">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="0be32-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0be32-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="0be32-121">Return value</span></span>

<span data-ttu-id="0be32-122">輸入：</span><span class="sxs-lookup"><span data-stu-id="0be32-122">Type:</span></span>

<span data-ttu-id="0be32-123">傳回型別符合 [**Texture3D**](sm5-object-texture3d.md) 物件宣告中的型別。</span><span class="sxs-lookup"><span data-stu-id="0be32-123">The return type matches the type in the declaration for the [**Texture3D**](sm5-object-texture3d.md) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="0be32-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0be32-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0be32-125">載入方法</span><span class="sxs-lookup"><span data-stu-id="0be32-125">Load methods</span></span>](texture3d-load.md)
</dt> <dt>

[<span data-ttu-id="0be32-126">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="0be32-126">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
