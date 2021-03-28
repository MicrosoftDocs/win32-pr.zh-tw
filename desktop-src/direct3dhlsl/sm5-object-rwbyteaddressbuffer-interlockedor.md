---
title: RWByteAddressBuffer：： InterlockedOr 函數
description: 執行原子或值的。
ms.assetid: 3a05619b-db97-4cf1-af3c-12c376e605a6
keywords:
- InterlockedOr 函式 HLSL
topic_type:
- apiref
api_name:
- InterlockedOr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 14b902f70919c79ed3e313671ede709f284a1490
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933261"
---
# <a name="interlockedor-function"></a><span data-ttu-id="bd979-104">InterlockedOr 函式</span><span class="sxs-lookup"><span data-stu-id="bd979-104">InterlockedOr function</span></span>

<span data-ttu-id="bd979-105">執行原子 **或** 值的。</span><span class="sxs-lookup"><span data-stu-id="bd979-105">Performs an atomic **OR** on the value.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd979-106">語法</span><span class="sxs-lookup"><span data-stu-id="bd979-106">Syntax</span></span>

``` syntax
void InterlockedOr(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="bd979-107">參數</span><span class="sxs-lookup"><span data-stu-id="bd979-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd979-108">*目的地* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bd979-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd979-109">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bd979-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bd979-110">目的地位址。</span><span class="sxs-lookup"><span data-stu-id="bd979-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="bd979-111">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bd979-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd979-112">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bd979-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bd979-113">輸入值。</span><span class="sxs-lookup"><span data-stu-id="bd979-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="bd979-114">*原始 \_ 值* \[ 輸出\]</span><span class="sxs-lookup"><span data-stu-id="bd979-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd979-115">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bd979-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bd979-116">原始的值。</span><span class="sxs-lookup"><span data-stu-id="bd979-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd979-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="bd979-117">Return value</span></span>

<span data-ttu-id="bd979-118">Nothing</span><span class="sxs-lookup"><span data-stu-id="bd979-118">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="bd979-119">備註</span><span class="sxs-lookup"><span data-stu-id="bd979-119">Remarks</span></span>

<span data-ttu-id="bd979-120">此作業只能在 **INT** 或 **UINT** 型別資源和共用記憶體變數上執行。</span><span class="sxs-lookup"><span data-stu-id="bd979-120">This operation can be performed only on **INT** or **UINT** typed resources and shared memory variables.</span></span> <span data-ttu-id="bd979-121">此函數有三個可能的用途。</span><span class="sxs-lookup"><span data-stu-id="bd979-121">There are three possible uses for this function.</span></span> <span data-ttu-id="bd979-122">第一個是當 R 是共用記憶體變數型別時。</span><span class="sxs-lookup"><span data-stu-id="bd979-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="bd979-123">在此情況下，此函式會執行不可部分完成的 **或** 具有 *dest* 所參考之共用記憶體暫存器的值。</span><span class="sxs-lookup"><span data-stu-id="bd979-123">In this case, the function performs an atomic **OR** with the value of the shared memory register referenced by *dest*.</span></span> <span data-ttu-id="bd979-124">第二個案例是 R 是資源變數類型。</span><span class="sxs-lookup"><span data-stu-id="bd979-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="bd979-125">在此案例中，此函式會執行不可部分完成 **或** 具有 *dest* 所參考資源位置的值。</span><span class="sxs-lookup"><span data-stu-id="bd979-125">In this scenario, the function performs an atomic **OR** with the value of the resource location referenced by *dest*.</span></span> <span data-ttu-id="bd979-126">最後，第三個案例是 R 是本機變數類型。</span><span class="sxs-lookup"><span data-stu-id="bd979-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="bd979-127">在此案例中，此函式會縮減為， **或** 具有 *dest* 值和 *值* 的值。</span><span class="sxs-lookup"><span data-stu-id="bd979-127">In this scenario, the function reduces to an **OR** with the values of *dest* and *value*.</span></span> <span data-ttu-id="bd979-128">作業的結果會取代 *dest* 的值。</span><span class="sxs-lookup"><span data-stu-id="bd979-128">The result of the operation replaces the value of *dest*.</span></span> <span data-ttu-id="bd979-129">多載函式有額外的輸出變數，其會設定為 *目的地* 的原始值。</span><span class="sxs-lookup"><span data-stu-id="bd979-129">The overloaded function has an additional output variable, which will be set to the original value of *dest*.</span></span> <span data-ttu-id="bd979-130">只有當 R 是可讀取和可寫入時，才能使用此多載作業。</span><span class="sxs-lookup"><span data-stu-id="bd979-130">This overloaded operation is available only when R is readable and writable.</span></span>

<span data-ttu-id="bd979-131">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="bd979-131">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="bd979-132">VS</span><span class="sxs-lookup"><span data-stu-id="bd979-132">VS</span></span>  | <span data-ttu-id="bd979-133">房 協</span><span class="sxs-lookup"><span data-stu-id="bd979-133">HS</span></span>  | <span data-ttu-id="bd979-134">DS</span><span class="sxs-lookup"><span data-stu-id="bd979-134">DS</span></span>  | <span data-ttu-id="bd979-135">GS</span><span class="sxs-lookup"><span data-stu-id="bd979-135">GS</span></span>  | <span data-ttu-id="bd979-136">PS</span><span class="sxs-lookup"><span data-stu-id="bd979-136">PS</span></span>  | <span data-ttu-id="bd979-137">CS</span><span class="sxs-lookup"><span data-stu-id="bd979-137">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="bd979-138">x</span><span class="sxs-lookup"><span data-stu-id="bd979-138">x</span></span>   |  <span data-ttu-id="bd979-139">x</span><span class="sxs-lookup"><span data-stu-id="bd979-139">x</span></span>  | <span data-ttu-id="bd979-140">x</span><span class="sxs-lookup"><span data-stu-id="bd979-140">x</span></span>   | <span data-ttu-id="bd979-141">x</span><span class="sxs-lookup"><span data-stu-id="bd979-141">x</span></span>   | <span data-ttu-id="bd979-142">x</span><span class="sxs-lookup"><span data-stu-id="bd979-142">x</span></span>   | <span data-ttu-id="bd979-143">x</span><span class="sxs-lookup"><span data-stu-id="bd979-143">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="bd979-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd979-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd979-145">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="bd979-145">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="bd979-146">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="bd979-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 