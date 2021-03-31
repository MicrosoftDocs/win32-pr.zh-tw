---
title: Texture2D：： Load (int，int，uint) 函數
description: 讀取材質資料並傳回作業的狀態。 |Texture2D：： Load (int，int，uint) 函數
ms.assetid: 05A12BE2-4604-470B-9EE8-F03F51E6D254
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
ms.openlocfilehash: 0c591b92b64641e169023f30663d8f5c6ef8a6c9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322280"
---
# <a name="texture2dloadintintuint-function"></a><span data-ttu-id="11a10-105">Texture2D：： Load (int，int，uint) 函數</span><span class="sxs-lookup"><span data-stu-id="11a10-105">Texture2D::Load(int,int,uint) function</span></span>

<span data-ttu-id="11a10-106">讀取材質資料並傳回作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="11a10-106">Reads texture data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="11a10-107">語法</span><span class="sxs-lookup"><span data-stu-id="11a10-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  in  int  Offset,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="11a10-108">參數</span><span class="sxs-lookup"><span data-stu-id="11a10-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11a10-109">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="11a10-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11a10-110">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="11a10-110">Type: **int**</span></span>

<span data-ttu-id="11a10-111">材質座標。</span><span class="sxs-lookup"><span data-stu-id="11a10-111">The texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="11a10-112">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="11a10-112">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11a10-113">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="11a10-113">Type: **int**</span></span>

<span data-ttu-id="11a10-114">在取樣之前套用至材質座標的位移。</span><span class="sxs-lookup"><span data-stu-id="11a10-114">An offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="11a10-115">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="11a10-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11a10-116">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="11a10-116">Type: **uint**</span></span>

<span data-ttu-id="11a10-117">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="11a10-117">The status of the operation.</span></span> <span data-ttu-id="11a10-118">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="11a10-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="11a10-119">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="11a10-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="11a10-120">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="11a10-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11a10-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="11a10-121">Return value</span></span>

<span data-ttu-id="11a10-122">輸入：</span><span class="sxs-lookup"><span data-stu-id="11a10-122">Type:</span></span>

<span data-ttu-id="11a10-123">傳回型別符合 [**Texture2D**](sm5-object-texture2d.md) 物件宣告中的型別。</span><span class="sxs-lookup"><span data-stu-id="11a10-123">The return type matches the type in the declaration for the [**Texture2D**](sm5-object-texture2d.md) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="11a10-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="11a10-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11a10-125">載入方法</span><span class="sxs-lookup"><span data-stu-id="11a10-125">Load methods</span></span>](texture2d-load.md)
</dt> </dl>

 

 
