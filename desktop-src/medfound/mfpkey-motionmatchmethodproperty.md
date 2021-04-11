---
description: 指定要用於動作比對的方法。
ms.assetid: 75bbc189-3092-4813-9f45-54e8e48b05cd
title: 'MFPKEY_MOTIONMATCHMETHOD 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09496e714633dd394f55122b7461f29a2daa3656
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943912"
---
# <a name="mfpkey_motionmatchmethod-property"></a><span data-ttu-id="063af-103">MFPKEY \_ MOTIONMATCHMETHOD 屬性</span><span class="sxs-lookup"><span data-stu-id="063af-103">MFPKEY\_MOTIONMATCHMETHOD Property</span></span>

<span data-ttu-id="063af-104">指定要用於動作比對的方法。</span><span class="sxs-lookup"><span data-stu-id="063af-104">Specifies the method to use for motion matching.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="063af-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="063af-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="063af-106">g \_ wszWMVCMotionMatchMethod</span><span class="sxs-lookup"><span data-stu-id="063af-106">g\_wszWMVCMotionMatchMethod</span></span>

## <a name="data-type"></a><span data-ttu-id="063af-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="063af-107">Data Type</span></span>

<span data-ttu-id="063af-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="063af-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="063af-109">預設值</span><span class="sxs-lookup"><span data-stu-id="063af-109">Default Value</span></span>

<span data-ttu-id="063af-110">0</span><span class="sxs-lookup"><span data-stu-id="063af-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="063af-111">備註</span><span class="sxs-lookup"><span data-stu-id="063af-111">Remarks</span></span>

<span data-ttu-id="063af-112">這個屬性可以設定為下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="063af-112">This property may be set to one of the following values.</span></span>



| <span data-ttu-id="063af-113">值</span><span class="sxs-lookup"><span data-stu-id="063af-113">Value</span></span> | <span data-ttu-id="063af-114">使用的方法</span><span class="sxs-lookup"><span data-stu-id="063af-114">Method used</span></span>                       |
|-------|-----------------------------------|
| <span data-ttu-id="063af-115">0</span><span class="sxs-lookup"><span data-stu-id="063af-115">0</span></span>     | <span data-ttu-id="063af-116"> (悲傷) 的絕對差異總和</span><span class="sxs-lookup"><span data-stu-id="063af-116">sum of absolute differences (SAD)</span></span> |
| <span data-ttu-id="063af-117">1</span><span class="sxs-lookup"><span data-stu-id="063af-117">1</span></span>     | <span data-ttu-id="063af-118">Hadamard</span><span class="sxs-lookup"><span data-stu-id="063af-118">Hadamard</span></span>                          |
| <span data-ttu-id="063af-119">-1</span><span class="sxs-lookup"><span data-stu-id="063af-119">-1</span></span>    | <span data-ttu-id="063af-120">巨大區塊-適應性。</span><span class="sxs-lookup"><span data-stu-id="063af-120">Macroblock-adaptive.</span></span>              |



 

<span data-ttu-id="063af-121"> (悲傷) 的絕對差異總和，是比 Hadamard 轉換更快速但較不精確的方法。</span><span class="sxs-lookup"><span data-stu-id="063af-121">The sum of absolute differences (SAD) is a faster but less accurate method than the Hadamard transform.</span></span> <span data-ttu-id="063af-122">Hadamard 轉換更準確，但需要大量計算。</span><span class="sxs-lookup"><span data-stu-id="063af-122">The Hadamard transform is more accurate but computationally intensive.</span></span> <span data-ttu-id="063af-123">巨大區塊-調適型模式提供兩種方法之間合理的折衷方式，方法是在兩個轉換之間進行動態選擇，只在適當的情況下選取 Hadamard 轉換。</span><span class="sxs-lookup"><span data-stu-id="063af-123">The macroblock-adaptive mode provides a reasonable compromise between the two methods by dynamically choosing between the two transforms, selecting the Hadamard transform only when appropriate.</span></span>

## <a name="requirements"></a><span data-ttu-id="063af-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="063af-124">Requirements</span></span>



| <span data-ttu-id="063af-125">需求</span><span class="sxs-lookup"><span data-stu-id="063af-125">Requirement</span></span> | <span data-ttu-id="063af-126">值</span><span class="sxs-lookup"><span data-stu-id="063af-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="063af-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="063af-127">Minimum supported client</span></span><br/> | <span data-ttu-id="063af-128">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="063af-128">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="063af-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="063af-129">Minimum supported server</span></span><br/> | <span data-ttu-id="063af-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="063af-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="063af-131">標頭</span><span class="sxs-lookup"><span data-stu-id="063af-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="063af-132"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="063af-132"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="063af-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="063af-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="063af-134">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="063af-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




