---
title: Texture2DMS：： Load (int，int，int，uint) 函數
description: 讀取材質資料並傳回作業的狀態。 |Texture2DMS：： Load (int，int，int，uint) 函數
ms.assetid: 4230962C-2968-4030-9770-8318F1760AEB
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
ms.openlocfilehash: e967d69929c0b20317ffb74fc97c4e60e36c2854
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104321804"
---
# <a name="texture2dmsloadintintintuint-function"></a><span data-ttu-id="bca1a-105">Texture2DMS：： Load (int，int，int，uint) 函數</span><span class="sxs-lookup"><span data-stu-id="bca1a-105">Texture2DMS::Load(int,int,int,uint) function</span></span>

<span data-ttu-id="bca1a-106">讀取材質資料並傳回作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="bca1a-106">Reads texture data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="bca1a-107">語法</span><span class="sxs-lookup"><span data-stu-id="bca1a-107">Syntax</span></span>


``` syntax
 Load(
  in  int2 Location,
  in  int  sampleindex,
  in  int2 Offset,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="bca1a-108">參數</span><span class="sxs-lookup"><span data-stu-id="bca1a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bca1a-109">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bca1a-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bca1a-110">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="bca1a-110">Type: **int2**</span></span>

<span data-ttu-id="bca1a-111">材質座標。</span><span class="sxs-lookup"><span data-stu-id="bca1a-111">The texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="bca1a-112">*sampleindex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bca1a-112">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bca1a-113">類型： **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bca1a-113">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bca1a-114">範例索引。</span><span class="sxs-lookup"><span data-stu-id="bca1a-114">The sample index.</span></span>

</dd> <dt>

<span data-ttu-id="bca1a-115">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bca1a-115">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bca1a-116">類型： **int2**</span><span class="sxs-lookup"><span data-stu-id="bca1a-116">Type: **int2**</span></span>

<span data-ttu-id="bca1a-117">在載入之前套用至材質座標的位移。</span><span class="sxs-lookup"><span data-stu-id="bca1a-117">An offset applied to the texture coordinates before loading.</span></span>

</dd> <dt>

<span data-ttu-id="bca1a-118">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bca1a-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bca1a-119">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="bca1a-119">Type: **uint**</span></span>

<span data-ttu-id="bca1a-120">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="bca1a-120">The status of the operation.</span></span> <span data-ttu-id="bca1a-121">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="bca1a-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="bca1a-122">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="bca1a-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="bca1a-123">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="bca1a-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bca1a-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="bca1a-124">Return value</span></span>

<span data-ttu-id="bca1a-125">輸入：</span><span class="sxs-lookup"><span data-stu-id="bca1a-125">Type:</span></span>

<span data-ttu-id="bca1a-126">傳回型別符合 [**Texture2DMS**](sm5-object-texture2dms.md) 物件宣告中的型別。</span><span class="sxs-lookup"><span data-stu-id="bca1a-126">The return type matches the type in the declaration for the [**Texture2DMS**](sm5-object-texture2dms.md) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="bca1a-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bca1a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bca1a-128">載入方法</span><span class="sxs-lookup"><span data-stu-id="bca1a-128">Load methods</span></span>](texture2dms-load.md)
</dt> <dt>

[<span data-ttu-id="bca1a-129">**Texture2DMS**</span><span class="sxs-lookup"><span data-stu-id="bca1a-129">**Texture2DMS**</span></span>](sm5-object-texture2dms.md)
</dt> </dl>

 

 
