---
title: def pragma 指示詞
description: 手動設定浮點著色器暫存器的 Pragma 指示詞。
ms.assetid: 45db94c4-f6f6-4c88-9bf2-4eaa9abf7844
keywords:
- def pragma 指示詞 HLSL
topic_type:
- apiref
api_name:
- def pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a921e17f8ddee4aaabfe50e75f42ce44812863d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104990679"
---
# <a name="def-pragma-directive"></a><span data-ttu-id="32fe5-104">def pragma 指示詞</span><span class="sxs-lookup"><span data-stu-id="32fe5-104">def pragma Directive</span></span>

<span data-ttu-id="32fe5-105">手動設定浮點著色器暫存器的 Pragma 指示詞。</span><span class="sxs-lookup"><span data-stu-id="32fe5-105">Pragma directive that manually allocates a floating-point shader register.</span></span>



| <span data-ttu-id="32fe5-106">\#pragma def ( *target*、 *register*、 *val1*、 *val2*、*val3*、 *val4* ) </span><span class="sxs-lookup"><span data-stu-id="32fe5-106">\#pragma def( *target*, *register*, *val1*, *val2*,*val3*, *val4* )</span></span> |
|---------------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="32fe5-107">參數</span><span class="sxs-lookup"><span data-stu-id="32fe5-107">Parameters</span></span>



| <span data-ttu-id="32fe5-108">項目</span><span class="sxs-lookup"><span data-stu-id="32fe5-108">Item</span></span>                                                                        | <span data-ttu-id="32fe5-109">描述</span><span class="sxs-lookup"><span data-stu-id="32fe5-109">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="32fe5-110"><span id="target"></span><span id="TARGET"></span>*目標*</span><span class="sxs-lookup"><span data-stu-id="32fe5-110"><span id="target"></span><span id="TARGET"></span>*target*</span></span><br/>       | <span data-ttu-id="32fe5-111">包含要配置之註冊的目標。</span><span class="sxs-lookup"><span data-stu-id="32fe5-111">Target that contains the register to allocate.</span></span> <br/>                  |
| <span data-ttu-id="32fe5-112"><span id="register"></span><span id="REGISTER"></span>*註冊*</span><span class="sxs-lookup"><span data-stu-id="32fe5-112"><span id="register"></span><span id="REGISTER"></span>*register*</span></span><br/> | <span data-ttu-id="32fe5-113">要配置的浮點著色器暫存器。</span><span class="sxs-lookup"><span data-stu-id="32fe5-113">Floating-point shader register to allocate.</span></span> <br/>                     |
| <span data-ttu-id="32fe5-114"><span id="val0"></span><span id="VAL0"></span>*val0*</span><span class="sxs-lookup"><span data-stu-id="32fe5-114"><span id="val0"></span><span id="VAL0"></span>*val0*</span></span><br/>             | <span data-ttu-id="32fe5-115">要配置給指定之暫存器的值的第一個位元組。</span><span class="sxs-lookup"><span data-stu-id="32fe5-115">First byte of the value to allocate to the specified register.</span></span> <br/>  |
| <span data-ttu-id="32fe5-116"><span id="val1"></span><span id="VAL1"></span>*val1*</span><span class="sxs-lookup"><span data-stu-id="32fe5-116"><span id="val1"></span><span id="VAL1"></span>*val1*</span></span><br/>             | <span data-ttu-id="32fe5-117">要配置給指定之暫存器的值的第二個位元組。</span><span class="sxs-lookup"><span data-stu-id="32fe5-117">Second byte of the value to allocate to the specified register.</span></span> <br/> |
| <span data-ttu-id="32fe5-118"><span id="val2"></span><span id="VAL2"></span>*val2*</span><span class="sxs-lookup"><span data-stu-id="32fe5-118"><span id="val2"></span><span id="VAL2"></span>*val2*</span></span><br/>             | <span data-ttu-id="32fe5-119">要配置給指定之註冊的值的第三個位元組。</span><span class="sxs-lookup"><span data-stu-id="32fe5-119">Third byte of the value to allocate to the specified register.</span></span> <br/>  |
| <span data-ttu-id="32fe5-120"><span id="val3"></span><span id="VAL3"></span>*val3*</span><span class="sxs-lookup"><span data-stu-id="32fe5-120"><span id="val3"></span><span id="VAL3"></span>*val3*</span></span><br/>             | <span data-ttu-id="32fe5-121">要配置給指定之註冊的值的第四個位元組。</span><span class="sxs-lookup"><span data-stu-id="32fe5-121">Fourth byte of the value to allocate to the specified register.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="32fe5-122">備註</span><span class="sxs-lookup"><span data-stu-id="32fe5-122">Remarks</span></span>

<span data-ttu-id="32fe5-123">Def pragma 可讓開發人員 prefill 具有指定值的浮點著色器暫存器。</span><span class="sxs-lookup"><span data-stu-id="32fe5-123">The def pragma allows a developer to prefill a floating-point shader register with the specified value.</span></span> <span data-ttu-id="32fe5-124">不常使用這個 pragma。</span><span class="sxs-lookup"><span data-stu-id="32fe5-124">This pragma is infrequently used.</span></span>

## <a name="see-also"></a><span data-ttu-id="32fe5-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32fe5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32fe5-126"> (DirectX HLSL) 的預處理器指示詞 </span><span class="sxs-lookup"><span data-stu-id="32fe5-126">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="32fe5-127">\# (DirectX HLSL) 的 pragma 指示詞 </span><span class="sxs-lookup"><span data-stu-id="32fe5-127">\#pragma Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





