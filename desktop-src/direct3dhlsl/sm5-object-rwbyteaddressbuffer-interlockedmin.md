---
title: RWByteAddressBuffer：： InterlockedMin 函數
description: 以不可部分完成的方式尋找最小值。
ms.assetid: bf650b2e-9c6c-4458-9565-1e9ec76a1472
keywords:
- InterlockedMin 函式 HLSL
topic_type:
- apiref
api_name:
- InterlockedMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b818a1fa0897d103e7d609a676212c6db428935f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023498"
---
# <a name="interlockedmin-function"></a><span data-ttu-id="76ab7-104">InterlockedMin 函式</span><span class="sxs-lookup"><span data-stu-id="76ab7-104">InterlockedMin function</span></span>

<span data-ttu-id="76ab7-105">以不可部分完成的方式尋找最小值。</span><span class="sxs-lookup"><span data-stu-id="76ab7-105">Finds the minimum value, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="76ab7-106">語法</span><span class="sxs-lookup"><span data-stu-id="76ab7-106">Syntax</span></span>

``` syntax
void InterlockedMin(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="76ab7-107">參數</span><span class="sxs-lookup"><span data-stu-id="76ab7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76ab7-108">*目的地* \[在\]</span><span class="sxs-lookup"><span data-stu-id="76ab7-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76ab7-109">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="76ab7-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="76ab7-110">目的地位址。</span><span class="sxs-lookup"><span data-stu-id="76ab7-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="76ab7-111">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="76ab7-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76ab7-112">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="76ab7-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="76ab7-113">輸入值。</span><span class="sxs-lookup"><span data-stu-id="76ab7-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="76ab7-114">*原始 \_ 值* \[ 輸出\]</span><span class="sxs-lookup"><span data-stu-id="76ab7-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76ab7-115">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="76ab7-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="76ab7-116">原始的值。</span><span class="sxs-lookup"><span data-stu-id="76ab7-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76ab7-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="76ab7-117">Return value</span></span>

<span data-ttu-id="76ab7-118">Nothing</span><span class="sxs-lookup"><span data-stu-id="76ab7-118">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="76ab7-119">備註</span><span class="sxs-lookup"><span data-stu-id="76ab7-119">Remarks</span></span>

<span data-ttu-id="76ab7-120">此作業只能在 int 和 uint 具類型的資源和共用記憶體變數上執行。</span><span class="sxs-lookup"><span data-stu-id="76ab7-120">This operation can only be performed on int and uint typed resources and shared memory variables.</span></span> <span data-ttu-id="76ab7-121">此函數有三個可能的用途。</span><span class="sxs-lookup"><span data-stu-id="76ab7-121">There are three possible uses for this function.</span></span> <span data-ttu-id="76ab7-122">第一個是當 R 是共用記憶體變數型別時。</span><span class="sxs-lookup"><span data-stu-id="76ab7-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="76ab7-123">在此情況下，此函式會針對 dest 所參考的共用記憶體暫存器，執行最小值的最小值。</span><span class="sxs-lookup"><span data-stu-id="76ab7-123">In this case, the function performs an atomic minimum of the value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="76ab7-124">第二個案例是 R 是資源變數類型。</span><span class="sxs-lookup"><span data-stu-id="76ab7-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="76ab7-125">在此案例中，此函式會對 dest 所參考的資源位置執行最小值的最小值。</span><span class="sxs-lookup"><span data-stu-id="76ab7-125">In this scenario, the function performs an atomic minimum of the value to the resource location referenced by dest.</span></span> <span data-ttu-id="76ab7-126">最後，第三個案例是 R 是本機變數類型。</span><span class="sxs-lookup"><span data-stu-id="76ab7-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="76ab7-127">在此案例中，此函式會減少為儲存在目的地中的 dest 和值的最小值。</span><span class="sxs-lookup"><span data-stu-id="76ab7-127">In this scenario, the function reduces to a minimum of the value of dest and value, stored in dest.</span></span> <span data-ttu-id="76ab7-128">多載函式有額外的輸出變數，其會設定為目的地的原始值。</span><span class="sxs-lookup"><span data-stu-id="76ab7-128">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="76ab7-129">只有在 R 可讀取和可寫入時，才能使用此多載作業。</span><span class="sxs-lookup"><span data-stu-id="76ab7-129">This overloaded operation is only available when R is readable and writable.</span></span>

<span data-ttu-id="76ab7-130">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="76ab7-130">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="76ab7-131">VS</span><span class="sxs-lookup"><span data-stu-id="76ab7-131">VS</span></span>  | <span data-ttu-id="76ab7-132">房 協</span><span class="sxs-lookup"><span data-stu-id="76ab7-132">HS</span></span>  | <span data-ttu-id="76ab7-133">DS</span><span class="sxs-lookup"><span data-stu-id="76ab7-133">DS</span></span>  | <span data-ttu-id="76ab7-134">GS</span><span class="sxs-lookup"><span data-stu-id="76ab7-134">GS</span></span>  | <span data-ttu-id="76ab7-135">PS</span><span class="sxs-lookup"><span data-stu-id="76ab7-135">PS</span></span>  | <span data-ttu-id="76ab7-136">CS</span><span class="sxs-lookup"><span data-stu-id="76ab7-136">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="76ab7-137">x</span><span class="sxs-lookup"><span data-stu-id="76ab7-137">x</span></span>   |  <span data-ttu-id="76ab7-138">x</span><span class="sxs-lookup"><span data-stu-id="76ab7-138">x</span></span>  | <span data-ttu-id="76ab7-139">x</span><span class="sxs-lookup"><span data-stu-id="76ab7-139">x</span></span>   | <span data-ttu-id="76ab7-140">x</span><span class="sxs-lookup"><span data-stu-id="76ab7-140">x</span></span>   | <span data-ttu-id="76ab7-141">x</span><span class="sxs-lookup"><span data-stu-id="76ab7-141">x</span></span>   | <span data-ttu-id="76ab7-142">x</span><span class="sxs-lookup"><span data-stu-id="76ab7-142">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="76ab7-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="76ab7-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76ab7-144">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="76ab7-144">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="76ab7-145">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="76ab7-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 