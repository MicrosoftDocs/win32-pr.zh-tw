---
title: 註冊
description: 註冊
ms.assetid: 45149f8c-8b76-4247-98d7-d141d7268da3
keywords:
- 註冊 HLSL
topic_type:
- apiref
api_name:
- register
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b378cd97bc9779951d62873d393009c98d32823
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375376"
---
# <a name="register"></a><span data-ttu-id="a9730-104">註冊</span><span class="sxs-lookup"><span data-stu-id="a9730-104">register</span></span>

<span data-ttu-id="a9730-105">選擇性的關鍵字，可將著色器變數指派給特定的暫存器，它會使用下列語法：</span><span class="sxs-lookup"><span data-stu-id="a9730-105">Optional keyword for assigning a shader variable to a particular register, which uses the following syntax:</span></span>



| <span data-ttu-id="a9730-106">：註冊 ( *\[ 著色 \_ 器 \] 設定檔*， *輸入 \# \[ 子元件 \]* ) </span><span class="sxs-lookup"><span data-stu-id="a9730-106">: register ( *\[shader\_profile\]*, *Type\#\[subcomponent\]* )</span></span> |
|----------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="a9730-107">參數</span><span class="sxs-lookup"><span data-stu-id="a9730-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9730-108"><span id="register"></span><span id="REGISTER"></span>註冊</span><span class="sxs-lookup"><span data-stu-id="a9730-108"><span id="register"></span><span id="REGISTER"></span>register</span></span>
</dt> <dd>

<span data-ttu-id="a9730-109">必要關鍵字。</span><span class="sxs-lookup"><span data-stu-id="a9730-109">Required keyword.</span></span>

</dd> <dt>

<span data-ttu-id="a9730-110"><span id="_shader_profile_"></span><span id="_SHADER_PROFILE_"></span>*\[著色器 \_ 設定檔\]*</span><span class="sxs-lookup"><span data-stu-id="a9730-110"><span id="_shader_profile_"></span><span id="_SHADER_PROFILE_"></span>*\[shader\_profile\]*</span></span>
</dt> <dd>

<span data-ttu-id="a9730-111">選擇性 [著色器設定檔](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax)，可以是著色器的目標，或只是 **ps** 或 **vs**。</span><span class="sxs-lookup"><span data-stu-id="a9730-111">Optional [shader profile](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax), which can be a shader target or simply **ps** or **vs**.</span></span>

</dd> <dt>

<span data-ttu-id="a9730-112"><span id="Type__subcomponent_"></span><span id="type__subcomponent_"></span><span id="TYPE__SUBCOMPONENT_"></span>*類型 \# \[ 子元件\]*</span><span class="sxs-lookup"><span data-stu-id="a9730-112"><span id="Type__subcomponent_"></span><span id="type__subcomponent_"></span><span id="TYPE__SUBCOMPONENT_"></span>*Type\#\[subcomponent\]*</span></span>
</dt> <dd>

<span data-ttu-id="a9730-113">註冊類型、數位和子元件宣告。</span><span class="sxs-lookup"><span data-stu-id="a9730-113">Register type, number, and subcomponent declaration.</span></span>

-   <span data-ttu-id="a9730-114">類型是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="a9730-114">Type is one of the following:</span></span>

    

    | <span data-ttu-id="a9730-115">類型</span><span class="sxs-lookup"><span data-stu-id="a9730-115">Type</span></span> | <span data-ttu-id="a9730-116">註冊描述</span><span class="sxs-lookup"><span data-stu-id="a9730-116">Register Description</span></span>       |
    |------|----------------------------|
    | <span data-ttu-id="a9730-117">b</span><span class="sxs-lookup"><span data-stu-id="a9730-117">b</span></span>    | <span data-ttu-id="a9730-118">常數緩衝區</span><span class="sxs-lookup"><span data-stu-id="a9730-118">Constant buffer</span></span>            |
    | <span data-ttu-id="a9730-119">t</span><span class="sxs-lookup"><span data-stu-id="a9730-119">t</span></span>    | <span data-ttu-id="a9730-120">材質和材質緩衝區</span><span class="sxs-lookup"><span data-stu-id="a9730-120">Texture and texture buffer</span></span> |
    | <span data-ttu-id="a9730-121">c</span><span class="sxs-lookup"><span data-stu-id="a9730-121">c</span></span>    | <span data-ttu-id="a9730-122">緩衝區位移</span><span class="sxs-lookup"><span data-stu-id="a9730-122">Buffer offset</span></span>              |
    | <span data-ttu-id="a9730-123">s</span><span class="sxs-lookup"><span data-stu-id="a9730-123">s</span></span>    | <span data-ttu-id="a9730-124">取樣器</span><span class="sxs-lookup"><span data-stu-id="a9730-124">Sampler</span></span>                    |
    | <span data-ttu-id="a9730-125">u</span><span class="sxs-lookup"><span data-stu-id="a9730-125">u</span></span>    | <span data-ttu-id="a9730-126">未排序的存取權視圖</span><span class="sxs-lookup"><span data-stu-id="a9730-126">Unordered Access View</span></span>      |

    

     

-   <span data-ttu-id="a9730-127">*\#* 這是暫存器編號，也就是整數。</span><span class="sxs-lookup"><span data-stu-id="a9730-127">*\#* is the register number, which is an integer number.</span></span>
-   <span data-ttu-id="a9730-128">*子元件* 是選擇性的整數數位。</span><span class="sxs-lookup"><span data-stu-id="a9730-128">The *subcomponent* is an optional integer number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9730-129">備註</span><span class="sxs-lookup"><span data-stu-id="a9730-129">Remarks</span></span>

<span data-ttu-id="a9730-130">您可以將一或多個註冊指派新增至相同的變數宣告，並以空格分隔。</span><span class="sxs-lookup"><span data-stu-id="a9730-130">You may add one or more register assignments to the same variable declaration, separated by spaces.</span></span>

<span data-ttu-id="a9730-131">針對全域範圍中的 Direct3D 10 變數， **register** 關鍵字的作用與 [PACKOFFSET (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) 關鍵字相同。</span><span class="sxs-lookup"><span data-stu-id="a9730-131">For Direct3D 10 variables in global scope, the **register** keyword acts the same as the [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) keyword.</span></span>

## <a name="examples"></a><span data-ttu-id="a9730-132">範例</span><span class="sxs-lookup"><span data-stu-id="a9730-132">Examples</span></span>

<span data-ttu-id="a9730-133">以下是一些範例：</span><span class="sxs-lookup"><span data-stu-id="a9730-133">Here are some examples:</span></span>


```
sampler myVar : register( ps_5_0, s ); 
```




```
sampler myVar : register( vs, s[8] );
```




```
sampler myVar : register( ps, s[2] ) 
              : register( ps_5_0, s[0] ) 
              : register( vs, s[8] );
```



## <a name="see-also"></a><span data-ttu-id="a9730-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a9730-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9730-135">語法變數</span><span class="sxs-lookup"><span data-stu-id="a9730-135">Variable Syntax</span></span>](dx-graphics-hlsl-variable-syntax.md)
</dt> <dt>

[<span data-ttu-id="a9730-136"> (DirectX HLSL) 的變數 </span><span class="sxs-lookup"><span data-stu-id="a9730-136">Variables (DirectX HLSL)</span></span>](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 