---
title: RWByteAddressBuffer：： InterlockedXor 函數
description: 在值上執行不可部分完成 XOR。
ms.assetid: 692f8b5e-a81e-4700-8a8d-3594aba85671
keywords:
- InterlockedXor 函式 HLSL
topic_type:
- apiref
api_name:
- InterlockedXor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 920ae912c599b66a03a25d7bc8ecc9b199036b26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933260"
---
# <a name="interlockedxor-function"></a><span data-ttu-id="fc6ed-104">InterlockedXor 函式</span><span class="sxs-lookup"><span data-stu-id="fc6ed-104">InterlockedXor function</span></span>

<span data-ttu-id="fc6ed-105">在值上執行不可部分完成 **XOR** 。</span><span class="sxs-lookup"><span data-stu-id="fc6ed-105">Performs an atomic **XOR** on the value.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc6ed-106">語法</span><span class="sxs-lookup"><span data-stu-id="fc6ed-106">Syntax</span></span>

``` syntax
void InterlockedXor(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="fc6ed-107">參數</span><span class="sxs-lookup"><span data-stu-id="fc6ed-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc6ed-108">*目的地* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fc6ed-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc6ed-109">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fc6ed-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fc6ed-110">目的地位址。</span><span class="sxs-lookup"><span data-stu-id="fc6ed-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="fc6ed-111">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fc6ed-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc6ed-112">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fc6ed-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fc6ed-113">輸入值。</span><span class="sxs-lookup"><span data-stu-id="fc6ed-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="fc6ed-114">*原始 \_ 值* \[ 輸出\]</span><span class="sxs-lookup"><span data-stu-id="fc6ed-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc6ed-115">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fc6ed-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fc6ed-116">原始的值。</span><span class="sxs-lookup"><span data-stu-id="fc6ed-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc6ed-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="fc6ed-117">Return value</span></span>

<span data-ttu-id="fc6ed-118">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="fc6ed-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc6ed-119">備註</span><span class="sxs-lookup"><span data-stu-id="fc6ed-119">Remarks</span></span>

<span data-ttu-id="fc6ed-120">此作業只能在 **INT** 或 **UINT** 型別資源和共用記憶體變數上執行。</span><span class="sxs-lookup"><span data-stu-id="fc6ed-120">This operation can be performed only on **INT** or **UINT** typed resources and shared memory variables.</span></span> <span data-ttu-id="fc6ed-121">此函數有三個可能的用途。</span><span class="sxs-lookup"><span data-stu-id="fc6ed-121">There are three possible uses for this function.</span></span> <span data-ttu-id="fc6ed-122">第一個是當 R 是共用記憶體變數型別時。</span><span class="sxs-lookup"><span data-stu-id="fc6ed-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="fc6ed-123">在此情況下，此函式會使用 *dest* 所參考的共用記憶體暫存器值來執行不可部分完成 **XOR** 。</span><span class="sxs-lookup"><span data-stu-id="fc6ed-123">In this case, the function performs an atomic **XOR** with the value of the shared memory register referenced by *dest*.</span></span> <span data-ttu-id="fc6ed-124">第二個案例是 R 是資源變數類型。</span><span class="sxs-lookup"><span data-stu-id="fc6ed-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="fc6ed-125">在此案例中，此函式會使用 *dest* 所參考資源位置的值來執行不可部分完成 **XOR** 。</span><span class="sxs-lookup"><span data-stu-id="fc6ed-125">In this scenario, the function performs an atomic **XOR** with the value of the resource location referenced by *dest*.</span></span> <span data-ttu-id="fc6ed-126">最後，第三個案例是 R 是本機變數類型。</span><span class="sxs-lookup"><span data-stu-id="fc6ed-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="fc6ed-127">在此案例中，此函式會縮減為 *dest* 值和 *值* 的 **XOR** 。</span><span class="sxs-lookup"><span data-stu-id="fc6ed-127">In this scenario, the function reduces to an **XOR** of the values of *dest* and *value*.</span></span> <span data-ttu-id="fc6ed-128">作業的結果會取代 *dest* 中的值。</span><span class="sxs-lookup"><span data-stu-id="fc6ed-128">The result of the operation replaces the value in *dest*.</span></span> <span data-ttu-id="fc6ed-129">多載函式有額外的輸出變數，其會設定為 *目的地* 的原始值。</span><span class="sxs-lookup"><span data-stu-id="fc6ed-129">The overloaded function has an additional output variable which will be set to the original value of *dest*.</span></span> <span data-ttu-id="fc6ed-130">只有當 R 是可讀取和可寫入時，才能使用此多載作業。</span><span class="sxs-lookup"><span data-stu-id="fc6ed-130">This overloaded operation is available only when R is readable and writable.</span></span>

<span data-ttu-id="fc6ed-131">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="fc6ed-131">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="fc6ed-132">VS</span><span class="sxs-lookup"><span data-stu-id="fc6ed-132">VS</span></span>  | <span data-ttu-id="fc6ed-133">房 協</span><span class="sxs-lookup"><span data-stu-id="fc6ed-133">HS</span></span>  | <span data-ttu-id="fc6ed-134">DS</span><span class="sxs-lookup"><span data-stu-id="fc6ed-134">DS</span></span>  | <span data-ttu-id="fc6ed-135">GS</span><span class="sxs-lookup"><span data-stu-id="fc6ed-135">GS</span></span>  | <span data-ttu-id="fc6ed-136">PS</span><span class="sxs-lookup"><span data-stu-id="fc6ed-136">PS</span></span>  | <span data-ttu-id="fc6ed-137">CS</span><span class="sxs-lookup"><span data-stu-id="fc6ed-137">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="fc6ed-138">x</span><span class="sxs-lookup"><span data-stu-id="fc6ed-138">x</span></span>   |  <span data-ttu-id="fc6ed-139">x</span><span class="sxs-lookup"><span data-stu-id="fc6ed-139">x</span></span>  | <span data-ttu-id="fc6ed-140">x</span><span class="sxs-lookup"><span data-stu-id="fc6ed-140">x</span></span>   | <span data-ttu-id="fc6ed-141">x</span><span class="sxs-lookup"><span data-stu-id="fc6ed-141">x</span></span>   | <span data-ttu-id="fc6ed-142">x</span><span class="sxs-lookup"><span data-stu-id="fc6ed-142">x</span></span>   | <span data-ttu-id="fc6ed-143">x</span><span class="sxs-lookup"><span data-stu-id="fc6ed-143">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="fc6ed-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fc6ed-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc6ed-145">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="fc6ed-145">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="fc6ed-146">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="fc6ed-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 