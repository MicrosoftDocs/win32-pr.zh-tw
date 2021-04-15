---
title: Texture2DMSArray：： Load (int，int，int，uint) 函數
description: 讀取材質資料並傳回作業的狀態。 |Texture2DMSArray：： Load (int，int，int，uint) 函數
ms.assetid: F5EA2FFF-7E43-4A34-9358-EA54382641DC
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
ms.openlocfilehash: 0065ee5e420c67876b87c67be1f5e5c8ff10e65b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991898"
---
# <a name="texture2dmsarrayloadintintintuint-function"></a><span data-ttu-id="bc0c8-105">Texture2DMSArray：： Load (int，int，int，uint) 函數</span><span class="sxs-lookup"><span data-stu-id="bc0c8-105">Texture2DMSArray::Load(int,int,int,uint) function</span></span>

<span data-ttu-id="bc0c8-106">讀取材質資料並傳回作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="bc0c8-106">Reads texture data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc0c8-107">語法</span><span class="sxs-lookup"><span data-stu-id="bc0c8-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  in  int  sampleindex,
  in  int  Offset,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="bc0c8-108">參數</span><span class="sxs-lookup"><span data-stu-id="bc0c8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc0c8-109">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bc0c8-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc0c8-110">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="bc0c8-110">Type: **int**</span></span>

<span data-ttu-id="bc0c8-111">材質座標。</span><span class="sxs-lookup"><span data-stu-id="bc0c8-111">The texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="bc0c8-112">*sampleindex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bc0c8-112">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc0c8-113">類型： **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bc0c8-113">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bc0c8-114">範例索引。</span><span class="sxs-lookup"><span data-stu-id="bc0c8-114">The sample index.</span></span>

</dd> <dt>

<span data-ttu-id="bc0c8-115">*位移* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bc0c8-115">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc0c8-116">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="bc0c8-116">Type: **int**</span></span>

<span data-ttu-id="bc0c8-117">在取樣之前套用至材質座標的位移。</span><span class="sxs-lookup"><span data-stu-id="bc0c8-117">An offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="bc0c8-118">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bc0c8-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc0c8-119">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="bc0c8-119">Type: **uint**</span></span>

<span data-ttu-id="bc0c8-120">作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="bc0c8-120">The status of the operation.</span></span> <span data-ttu-id="bc0c8-121">您無法直接存取狀態;相反地，請將狀態傳遞給 [**CheckAccessFullyMapped**](checkaccessfullymapped.md) 內建函式。</span><span class="sxs-lookup"><span data-stu-id="bc0c8-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="bc0c8-122">如果對應的 **範例**、**收集** 或 **載入** 作業中的所有值都是在 [磚資源](/windows/desktop/direct3d11/direct3d-11-2-features)中存取對應的磚， **CheckAccessFullyMapped** 會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="bc0c8-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="bc0c8-123">如果有任何值取自未對應的磚， **CheckAccessFullyMapped** 會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="bc0c8-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc0c8-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="bc0c8-124">Return value</span></span>

<span data-ttu-id="bc0c8-125">輸入：</span><span class="sxs-lookup"><span data-stu-id="bc0c8-125">Type:</span></span>

<span data-ttu-id="bc0c8-126">傳回型別符合 [**Texture2DMSArray**](sm5-object-texture2dmsarray.md) 物件宣告中的型別。</span><span class="sxs-lookup"><span data-stu-id="bc0c8-126">The return type matches the type in the declaration for the [**Texture2DMSArray**](sm5-object-texture2dmsarray.md) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="bc0c8-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc0c8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc0c8-128">載入方法</span><span class="sxs-lookup"><span data-stu-id="bc0c8-128">Load methods</span></span>](texture2dmsarray-load.md)
</dt> <dt>

[<span data-ttu-id="bc0c8-129">**Texture2DMSArray**</span><span class="sxs-lookup"><span data-stu-id="bc0c8-129">**Texture2DMSArray**</span></span>](sm5-object-texture2dmsarray.md)
</dt> </dl>

 

 
