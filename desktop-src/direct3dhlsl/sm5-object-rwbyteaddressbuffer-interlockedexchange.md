---
title: RWByteAddressBuffer：： InterlockedExchange 函數
description: 以不可部分完成的方式交換值。
ms.assetid: a50f4cba-a7a2-44b0-9de7-003b4c7a947f
keywords:
- InterlockedExchange 函式 HLSL
topic_type:
- apiref
api_name:
- InterlockedExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 47c51374b7dcd62ac208e0aa8811a8d693ce0ac6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990899"
---
# <a name="interlockedexchange-function"></a><span data-ttu-id="ad4a1-104">InterlockedExchange 函式</span><span class="sxs-lookup"><span data-stu-id="ad4a1-104">InterlockedExchange function</span></span>

<span data-ttu-id="ad4a1-105">以不可部分完成的方式交換值。</span><span class="sxs-lookup"><span data-stu-id="ad4a1-105">Exchanges a value, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad4a1-106">語法</span><span class="sxs-lookup"><span data-stu-id="ad4a1-106">Syntax</span></span>

``` syntax
void InterlockedExchange(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="ad4a1-107">參數</span><span class="sxs-lookup"><span data-stu-id="ad4a1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad4a1-108">*目的地* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ad4a1-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad4a1-109">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ad4a1-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ad4a1-110">目的地位址。</span><span class="sxs-lookup"><span data-stu-id="ad4a1-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="ad4a1-111">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ad4a1-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad4a1-112">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ad4a1-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ad4a1-113">輸入值。</span><span class="sxs-lookup"><span data-stu-id="ad4a1-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="ad4a1-114">*原始 \_ 值* \[ 輸出\]</span><span class="sxs-lookup"><span data-stu-id="ad4a1-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad4a1-115">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ad4a1-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ad4a1-116">原始的值。</span><span class="sxs-lookup"><span data-stu-id="ad4a1-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad4a1-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="ad4a1-117">Return value</span></span>

<span data-ttu-id="ad4a1-118">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ad4a1-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad4a1-119">備註</span><span class="sxs-lookup"><span data-stu-id="ad4a1-119">Remarks</span></span>

<span data-ttu-id="ad4a1-120">這種作業只能對純量類型的資源和共用記憶體變數執行。</span><span class="sxs-lookup"><span data-stu-id="ad4a1-120">This operation can only be performed on scalar-typed resources and shared memory variables.</span></span> <span data-ttu-id="ad4a1-121">此函數有三個可能的用途。</span><span class="sxs-lookup"><span data-stu-id="ad4a1-121">There are three possible uses for this function.</span></span> <span data-ttu-id="ad4a1-122">第一個是當 R 是共用記憶體變數型別時。</span><span class="sxs-lookup"><span data-stu-id="ad4a1-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="ad4a1-123">在此情況下，此函式會在 dest 所參考的共用記憶體暫存器上執行作業。</span><span class="sxs-lookup"><span data-stu-id="ad4a1-123">In this case, the function performs the operation on the shared memory register referenced by dest.</span></span> <span data-ttu-id="ad4a1-124">第二個案例是 R 是資源變數類型。</span><span class="sxs-lookup"><span data-stu-id="ad4a1-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="ad4a1-125">在此案例中，此函式會在 dest 所參考的資源位置上執行作業。</span><span class="sxs-lookup"><span data-stu-id="ad4a1-125">In this scenario, the function performs the operation on the resource location referenced by dest.</span></span> <span data-ttu-id="ad4a1-126">最後，第三個案例是 R 是本機變數類型。</span><span class="sxs-lookup"><span data-stu-id="ad4a1-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="ad4a1-127">在此案例中，此函式會縮減為使用本機作業所執行的作業。</span><span class="sxs-lookup"><span data-stu-id="ad4a1-127">In this scenario, the function reduces to the operation performed using local operations.</span></span> <span data-ttu-id="ad4a1-128">只有當 R 可讀取和寫入時，才能使用此作業。</span><span class="sxs-lookup"><span data-stu-id="ad4a1-128">This operation is only available when R is readable and writable.</span></span>

<span data-ttu-id="ad4a1-129">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="ad4a1-129">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="ad4a1-130">VS</span><span class="sxs-lookup"><span data-stu-id="ad4a1-130">VS</span></span>  | <span data-ttu-id="ad4a1-131">房 協</span><span class="sxs-lookup"><span data-stu-id="ad4a1-131">HS</span></span>  | <span data-ttu-id="ad4a1-132">DS</span><span class="sxs-lookup"><span data-stu-id="ad4a1-132">DS</span></span>  | <span data-ttu-id="ad4a1-133">GS</span><span class="sxs-lookup"><span data-stu-id="ad4a1-133">GS</span></span>  | <span data-ttu-id="ad4a1-134">PS</span><span class="sxs-lookup"><span data-stu-id="ad4a1-134">PS</span></span>  | <span data-ttu-id="ad4a1-135">CS</span><span class="sxs-lookup"><span data-stu-id="ad4a1-135">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
|  <span data-ttu-id="ad4a1-136">x</span><span class="sxs-lookup"><span data-stu-id="ad4a1-136">x</span></span>  |  <span data-ttu-id="ad4a1-137">x</span><span class="sxs-lookup"><span data-stu-id="ad4a1-137">x</span></span>  |  <span data-ttu-id="ad4a1-138">x</span><span class="sxs-lookup"><span data-stu-id="ad4a1-138">x</span></span>  |  <span data-ttu-id="ad4a1-139">x</span><span class="sxs-lookup"><span data-stu-id="ad4a1-139">x</span></span>  | <span data-ttu-id="ad4a1-140">x</span><span class="sxs-lookup"><span data-stu-id="ad4a1-140">x</span></span>   | <span data-ttu-id="ad4a1-141">x</span><span class="sxs-lookup"><span data-stu-id="ad4a1-141">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="ad4a1-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ad4a1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad4a1-143">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="ad4a1-143">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="ad4a1-144">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="ad4a1-144">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 