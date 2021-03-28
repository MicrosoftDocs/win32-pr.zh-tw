---
title: RWByteAddressBuffer：： InterlockedAdd 函數
description: 以不可部分完成的方式加入值。
ms.assetid: 27274aae-1e75-4626-9997-57c4e9393000
keywords:
- InterlockedAdd 函式 HLSL
topic_type:
- apiref
api_name:
- InterlockedAdd
api_location:
- winnt.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d352ed97df15ce076c10950c6da94aaeaff0f2d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990930"
---
# <a name="interlockedadd-function"></a><span data-ttu-id="e8540-104">InterlockedAdd 函式</span><span class="sxs-lookup"><span data-stu-id="e8540-104">InterlockedAdd function</span></span>

<span data-ttu-id="e8540-105">以不可部分完成的方式加入值。</span><span class="sxs-lookup"><span data-stu-id="e8540-105">Adds the value, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8540-106">語法</span><span class="sxs-lookup"><span data-stu-id="e8540-106">Syntax</span></span>

``` syntax
void InterlockedAdd(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="e8540-107">參數</span><span class="sxs-lookup"><span data-stu-id="e8540-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8540-108">*目的地* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e8540-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8540-109">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e8540-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e8540-110">目的地位址。</span><span class="sxs-lookup"><span data-stu-id="e8540-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="e8540-111">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e8540-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8540-112">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e8540-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e8540-113">輸入值。</span><span class="sxs-lookup"><span data-stu-id="e8540-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="e8540-114">*原始 \_ 值* \[ 輸出\]</span><span class="sxs-lookup"><span data-stu-id="e8540-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8540-115">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e8540-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e8540-116">原始的值。</span><span class="sxs-lookup"><span data-stu-id="e8540-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8540-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="e8540-117">Return value</span></span>

<span data-ttu-id="e8540-118">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="e8540-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8540-119">備註</span><span class="sxs-lookup"><span data-stu-id="e8540-119">Remarks</span></span>

<span data-ttu-id="e8540-120">此作業只能在 int 或 uint 型別資源和共用記憶體變數上執行。</span><span class="sxs-lookup"><span data-stu-id="e8540-120">This operation can be performed only on int or uint typed resources and shared memory variables.</span></span> <span data-ttu-id="e8540-121">此函數有三個可能的用途。</span><span class="sxs-lookup"><span data-stu-id="e8540-121">There are three possible uses for this function.</span></span> <span data-ttu-id="e8540-122">第一個是當 R 是共用記憶體變數型別時。</span><span class="sxs-lookup"><span data-stu-id="e8540-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="e8540-123">在此情況下，此函式會針對 dest 所參考的共用記憶體暫存器執行值的不可部分完成新增。</span><span class="sxs-lookup"><span data-stu-id="e8540-123">In this case, the function performs an atomic add of value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="e8540-124">第二個案例是 R 是資源變數類型。</span><span class="sxs-lookup"><span data-stu-id="e8540-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="e8540-125">在此案例中，此函式會對 dest 所參考的資源位置執行值的不可部分完成加入。</span><span class="sxs-lookup"><span data-stu-id="e8540-125">In this scenario, the function performs an atomic add of the value to the resource location referenced by dest.</span></span> <span data-ttu-id="e8540-126">最後，第三個案例是 R 是本機變數類型。</span><span class="sxs-lookup"><span data-stu-id="e8540-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="e8540-127">在此案例中，此函式會縮減為儲存在 dest 中的 dest 值和值的總和。</span><span class="sxs-lookup"><span data-stu-id="e8540-127">In this scenario, the function reduces to a sum of the value of dest and value, stored in dest.</span></span> <span data-ttu-id="e8540-128">多載函式有額外的輸出變數，其會設定為目的地的原始值。</span><span class="sxs-lookup"><span data-stu-id="e8540-128">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="e8540-129">只有在 R 可讀取和可寫入時，才能使用此多載作業。</span><span class="sxs-lookup"><span data-stu-id="e8540-129">This overloaded operation is only available when R is readable and writable.</span></span>

<span data-ttu-id="e8540-130">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="e8540-130">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="e8540-131">VS</span><span class="sxs-lookup"><span data-stu-id="e8540-131">VS</span></span>  | <span data-ttu-id="e8540-132">房 協</span><span class="sxs-lookup"><span data-stu-id="e8540-132">HS</span></span>  | <span data-ttu-id="e8540-133">DS</span><span class="sxs-lookup"><span data-stu-id="e8540-133">DS</span></span>  | <span data-ttu-id="e8540-134">GS</span><span class="sxs-lookup"><span data-stu-id="e8540-134">GS</span></span>  | <span data-ttu-id="e8540-135">PS</span><span class="sxs-lookup"><span data-stu-id="e8540-135">PS</span></span>  | <span data-ttu-id="e8540-136">CS</span><span class="sxs-lookup"><span data-stu-id="e8540-136">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="e8540-137">x</span><span class="sxs-lookup"><span data-stu-id="e8540-137">x</span></span>   | <span data-ttu-id="e8540-138">x</span><span class="sxs-lookup"><span data-stu-id="e8540-138">x</span></span>   | <span data-ttu-id="e8540-139">x</span><span class="sxs-lookup"><span data-stu-id="e8540-139">x</span></span>   | <span data-ttu-id="e8540-140">x</span><span class="sxs-lookup"><span data-stu-id="e8540-140">x</span></span>   | <span data-ttu-id="e8540-141">x</span><span class="sxs-lookup"><span data-stu-id="e8540-141">x</span></span>   | <span data-ttu-id="e8540-142">x</span><span class="sxs-lookup"><span data-stu-id="e8540-142">x</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="e8540-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8540-143">Requirements</span></span>




## <a name="see-also"></a><span data-ttu-id="e8540-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8540-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8540-145">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="e8540-145">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="e8540-146">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="e8540-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

