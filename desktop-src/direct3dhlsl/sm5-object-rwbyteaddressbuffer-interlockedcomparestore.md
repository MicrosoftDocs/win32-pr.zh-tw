---
title: RWByteAddressBuffer：： InterlockedCompareStore 函數
description: 以不可部分完成的方式 Ccompares 比較值的輸入。
ms.assetid: d82a73b6-24a5-4eb3-9f20-15ba263c93d0
keywords:
- InterlockedCompareStore 函式 HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareStore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: abaa390ba74657e42b54a5147a7bc4006564a5fb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842559"
---
# <a name="interlockedcomparestore-function"></a><span data-ttu-id="92fd5-104">InterlockedCompareStore 函式</span><span class="sxs-lookup"><span data-stu-id="92fd5-104">InterlockedCompareStore function</span></span>

<span data-ttu-id="92fd5-105">以不可部分完成的方式 Ccompares 比較值的輸入。</span><span class="sxs-lookup"><span data-stu-id="92fd5-105">Ccompares the input to the comparison value, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="92fd5-106">語法</span><span class="sxs-lookup"><span data-stu-id="92fd5-106">Syntax</span></span>

``` syntax
void InterlockedCompareStore(
  in UINT dest,
  in UINT compare_value,
  in UINT value
);
```

## <a name="parameters"></a><span data-ttu-id="92fd5-107">參數</span><span class="sxs-lookup"><span data-stu-id="92fd5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92fd5-108">*目的地* \[在\]</span><span class="sxs-lookup"><span data-stu-id="92fd5-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92fd5-109">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="92fd5-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="92fd5-110">目的地位址。</span><span class="sxs-lookup"><span data-stu-id="92fd5-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="92fd5-111">*比較 \_ 值* \[\]</span><span class="sxs-lookup"><span data-stu-id="92fd5-111">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92fd5-112">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="92fd5-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="92fd5-113">比較值。</span><span class="sxs-lookup"><span data-stu-id="92fd5-113">The comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="92fd5-114">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="92fd5-114">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92fd5-115">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="92fd5-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="92fd5-116">輸入值。</span><span class="sxs-lookup"><span data-stu-id="92fd5-116">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92fd5-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="92fd5-117">Return value</span></span>

<span data-ttu-id="92fd5-118">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="92fd5-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="92fd5-119">備註</span><span class="sxs-lookup"><span data-stu-id="92fd5-119">Remarks</span></span>

<span data-ttu-id="92fd5-120">此作業只能在 int 或 uint 型別資源和共用記憶體變數上執行。</span><span class="sxs-lookup"><span data-stu-id="92fd5-120">This operation can only be performed on int or uint typed resources and shared memory variables.</span></span> <span data-ttu-id="92fd5-121">此函數有三個可能的用途。</span><span class="sxs-lookup"><span data-stu-id="92fd5-121">There are three possible uses for this function.</span></span> <span data-ttu-id="92fd5-122">第一個是當 R 是共用記憶體變數型別時。</span><span class="sxs-lookup"><span data-stu-id="92fd5-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="92fd5-123">在此情況下，此函式會在 dest 所參考的共用記憶體暫存器上執行作業。</span><span class="sxs-lookup"><span data-stu-id="92fd5-123">In this case, the function performs the operation on the shared memory register referenced by dest.</span></span> <span data-ttu-id="92fd5-124">第二個案例是 R 是資源變數類型。</span><span class="sxs-lookup"><span data-stu-id="92fd5-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="92fd5-125">在此案例中，此函式會在 dest 所參考的資源位置上執行作業。</span><span class="sxs-lookup"><span data-stu-id="92fd5-125">In this scenario, the function performs the operation on the resource location referenced by dest.</span></span> <span data-ttu-id="92fd5-126">最後，第三個案例是 R 是本機變數類型。</span><span class="sxs-lookup"><span data-stu-id="92fd5-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="92fd5-127">在此案例中，此函式會縮減為使用本機作業所執行的作業。</span><span class="sxs-lookup"><span data-stu-id="92fd5-127">In this scenario, the function reduces to the operation performed using local operations.</span></span>

<span data-ttu-id="92fd5-128">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="92fd5-128">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="92fd5-129">VS</span><span class="sxs-lookup"><span data-stu-id="92fd5-129">VS</span></span>  | <span data-ttu-id="92fd5-130">房 協</span><span class="sxs-lookup"><span data-stu-id="92fd5-130">HS</span></span>  | <span data-ttu-id="92fd5-131">DS</span><span class="sxs-lookup"><span data-stu-id="92fd5-131">DS</span></span>  | <span data-ttu-id="92fd5-132">GS</span><span class="sxs-lookup"><span data-stu-id="92fd5-132">GS</span></span>  | <span data-ttu-id="92fd5-133">PS</span><span class="sxs-lookup"><span data-stu-id="92fd5-133">PS</span></span>  | <span data-ttu-id="92fd5-134">CS</span><span class="sxs-lookup"><span data-stu-id="92fd5-134">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="92fd5-135">x</span><span class="sxs-lookup"><span data-stu-id="92fd5-135">x</span></span>   | <span data-ttu-id="92fd5-136">x</span><span class="sxs-lookup"><span data-stu-id="92fd5-136">x</span></span>   | <span data-ttu-id="92fd5-137">x</span><span class="sxs-lookup"><span data-stu-id="92fd5-137">x</span></span>   | <span data-ttu-id="92fd5-138">x</span><span class="sxs-lookup"><span data-stu-id="92fd5-138">x</span></span>   | <span data-ttu-id="92fd5-139">x</span><span class="sxs-lookup"><span data-stu-id="92fd5-139">x</span></span>   | <span data-ttu-id="92fd5-140">x</span><span class="sxs-lookup"><span data-stu-id="92fd5-140">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="92fd5-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="92fd5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92fd5-142">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="92fd5-142">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="92fd5-143">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="92fd5-143">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 