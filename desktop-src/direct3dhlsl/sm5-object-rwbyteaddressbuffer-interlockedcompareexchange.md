---
title: RWByteAddressBuffer：： InterlockedCompareExchange 函數
description: 比較輸入與比較值，並以不可部分完成的方式交換結果。
ms.assetid: 9d6e8d95-5157-49a7-8a79-f3ca6ba87ebb
keywords:
- InterlockedCompareExchange 函式 HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 18c7e5d58fe926d09e7ec48ee12a2336627d5db2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682818"
---
# <a name="interlockedcompareexchange-function"></a><span data-ttu-id="6afdc-104">InterlockedCompareExchange 函式</span><span class="sxs-lookup"><span data-stu-id="6afdc-104">InterlockedCompareExchange function</span></span>

<span data-ttu-id="6afdc-105">比較輸入與比較值，並以不可部分完成的方式交換結果。</span><span class="sxs-lookup"><span data-stu-id="6afdc-105">Compares the input to the comparison value and exchanges the result, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="6afdc-106">語法</span><span class="sxs-lookup"><span data-stu-id="6afdc-106">Syntax</span></span>

``` syntax
void InterlockedCompareExchange(
  in  UINT dest,
  in  UINT compare_value,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="6afdc-107">參數</span><span class="sxs-lookup"><span data-stu-id="6afdc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6afdc-108">*目的地* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6afdc-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6afdc-109">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6afdc-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6afdc-110">目的地位址。</span><span class="sxs-lookup"><span data-stu-id="6afdc-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="6afdc-111">*比較 \_ 值* \[\]</span><span class="sxs-lookup"><span data-stu-id="6afdc-111">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6afdc-112">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6afdc-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6afdc-113">比較值。</span><span class="sxs-lookup"><span data-stu-id="6afdc-113">The comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="6afdc-114">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6afdc-114">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6afdc-115">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6afdc-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6afdc-116">輸入值。</span><span class="sxs-lookup"><span data-stu-id="6afdc-116">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="6afdc-117">*原始 \_ 值* \[ 輸出\]</span><span class="sxs-lookup"><span data-stu-id="6afdc-117">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6afdc-118">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6afdc-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6afdc-119">原始的值。</span><span class="sxs-lookup"><span data-stu-id="6afdc-119">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6afdc-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="6afdc-120">Return value</span></span>

<span data-ttu-id="6afdc-121">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6afdc-121">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6afdc-122">備註</span><span class="sxs-lookup"><span data-stu-id="6afdc-122">Remarks</span></span>

<span data-ttu-id="6afdc-123">以不可部分完成的方式比較 *dest* 中的值與 *\_ 值*，如果值相符，則會將值儲存在 *dest* 中，並以 *原始 \_ 值* 傳回 *dest* 的原始值。</span><span class="sxs-lookup"><span data-stu-id="6afdc-123">Atomically compares the value in *dest* to *compare\_value*, stores value in *dest* if the values match, returns the original value of *dest* in *original\_value*.</span></span> <span data-ttu-id="6afdc-124">此作業只能在 **int** 或 *uint* 型別資源和共用記憶體變數上執行。</span><span class="sxs-lookup"><span data-stu-id="6afdc-124">This operation can only be performed on **int** or *uint* typed resources and shared memory variables.</span></span> <span data-ttu-id="6afdc-125">此函數有三個可能的用途。</span><span class="sxs-lookup"><span data-stu-id="6afdc-125">There are three possible uses for this function.</span></span> <span data-ttu-id="6afdc-126">第一個是當 R 是共用記憶體變數型別時。</span><span class="sxs-lookup"><span data-stu-id="6afdc-126">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="6afdc-127">在此情況下，此函式會在 *dest* 所參考的共用記憶體暫存器上執行作業。</span><span class="sxs-lookup"><span data-stu-id="6afdc-127">In this case, the function performs the operation on the shared memory register referenced by *dest*.</span></span> <span data-ttu-id="6afdc-128">第二個案例是 R 是資源變數類型。</span><span class="sxs-lookup"><span data-stu-id="6afdc-128">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="6afdc-129">在此案例中，此函式會在 *dest* 所參考的資源位置上執行作業。</span><span class="sxs-lookup"><span data-stu-id="6afdc-129">In this scenario, the function performs the operation on the resource location referenced by *dest*.</span></span> <span data-ttu-id="6afdc-130">最後，第三個案例是 R 是本機變數類型。</span><span class="sxs-lookup"><span data-stu-id="6afdc-130">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="6afdc-131">在此案例中，此函式會縮減為使用本機作業所執行的作業。</span><span class="sxs-lookup"><span data-stu-id="6afdc-131">In this scenario, the function reduces to the operation performed using local operations.</span></span> <span data-ttu-id="6afdc-132">只有當 R 可讀取和寫入時，才能使用此作業。</span><span class="sxs-lookup"><span data-stu-id="6afdc-132">This operation is only available when R is readable and writable.</span></span>

> [!Note]  
> <span data-ttu-id="6afdc-133">如果您在 [**for**](dx-graphics-hlsl-for.md)或 [**while**](dx-graphics-hlsl-while.md)計算著色器迴圈中呼叫 **InterlockedCompareExchange** ，以便正確編譯，您必須在該迴圈中使用 [ **\[ 允許 \_ uav \_ 條件 \]** ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="6afdc-133">If you call **InterlockedCompareExchange** in a [**for**](dx-graphics-hlsl-for.md) or [**while**](dx-graphics-hlsl-while.md) compute shader loop, to properly compile, you must use the **\[allow\_uav\_condition\]** attribute on that loop.</span></span>

 

<span data-ttu-id="6afdc-134">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="6afdc-134">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="6afdc-135">VS</span><span class="sxs-lookup"><span data-stu-id="6afdc-135">VS</span></span>  | <span data-ttu-id="6afdc-136">房 協</span><span class="sxs-lookup"><span data-stu-id="6afdc-136">HS</span></span>  | <span data-ttu-id="6afdc-137">DS</span><span class="sxs-lookup"><span data-stu-id="6afdc-137">DS</span></span>  | <span data-ttu-id="6afdc-138">GS</span><span class="sxs-lookup"><span data-stu-id="6afdc-138">GS</span></span>  | <span data-ttu-id="6afdc-139">PS</span><span class="sxs-lookup"><span data-stu-id="6afdc-139">PS</span></span>  | <span data-ttu-id="6afdc-140">CS</span><span class="sxs-lookup"><span data-stu-id="6afdc-140">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="6afdc-141">x</span><span class="sxs-lookup"><span data-stu-id="6afdc-141">x</span></span>   | <span data-ttu-id="6afdc-142">x</span><span class="sxs-lookup"><span data-stu-id="6afdc-142">x</span></span>   | <span data-ttu-id="6afdc-143">x</span><span class="sxs-lookup"><span data-stu-id="6afdc-143">x</span></span>   | <span data-ttu-id="6afdc-144">x</span><span class="sxs-lookup"><span data-stu-id="6afdc-144">x</span></span>   | <span data-ttu-id="6afdc-145">x</span><span class="sxs-lookup"><span data-stu-id="6afdc-145">x</span></span>   | <span data-ttu-id="6afdc-146">x</span><span class="sxs-lookup"><span data-stu-id="6afdc-146">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="6afdc-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6afdc-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6afdc-148">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="6afdc-148">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="6afdc-149">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="6afdc-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 