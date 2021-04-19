---
description: 這些旗標會提供有關效果參數的其他資訊。
ms.assetid: 7e1e4c64-56b8-4fdb-8178-50f7d61b917b
title: 'D3DX_PARAMETER (D3dx9effect) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX_PARAMETER_ANNOTATION
- D3DX_PARAMETER_LITERAL
- D3DX_PARAMETER_SHARED
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 49df84c49fd1f7a0c1b4de9157a36e27d29d5e29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107001790"
---
# <a name="d3dx_parameter"></a><span data-ttu-id="47caa-103">D3DX \_ 參數</span><span class="sxs-lookup"><span data-stu-id="47caa-103">D3DX\_PARAMETER</span></span>

<span data-ttu-id="47caa-104">這些旗標會提供有關效果參數的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="47caa-104">These flags provide additional information about effect parameters.</span></span>

<span data-ttu-id="47caa-105">[**D3DXPARAMETER \_ DESC**](d3dxparameter-desc.md)會使用效果參數常數。</span><span class="sxs-lookup"><span data-stu-id="47caa-105">Effect parameter constants are used by [**D3DXPARAMETER\_DESC**](d3dxparameter-desc.md).</span></span>



| <span data-ttu-id="47caa-106">常數</span><span class="sxs-lookup"><span data-stu-id="47caa-106">Constant</span></span>                                                                                                                                                                                           | <span data-ttu-id="47caa-107">描述</span><span class="sxs-lookup"><span data-stu-id="47caa-107">Description</span></span>                                                                                                                                                                                                                                                                                                                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DX_PARAMETER_ANNOTATION"></span><span id="d3dx_parameter_annotation"></span><dl> <span data-ttu-id="47caa-108"><dt>**D3DX \_ 參數 \_ 注釋**</dt></span><span class="sxs-lookup"><span data-stu-id="47caa-108"><dt>**D3DX\_PARAMETER\_ANNOTATION**</dt></span></span> </dl> | <span data-ttu-id="47caa-109">此參數會標示為批註。</span><span class="sxs-lookup"><span data-stu-id="47caa-109">This parameter is marked as an annotation.</span></span> <span data-ttu-id="47caa-110">請參閱 [使用批註將資訊新增至效果參數](using-an-effect.md)。</span><span class="sxs-lookup"><span data-stu-id="47caa-110">See [Add Information to Effect Parameters with Annotations](using-an-effect.md).</span></span><br/>                                                                                                                                                                                                 |
| <span id="D3DX_PARAMETER_LITERAL"></span><span id="d3dx_parameter_literal"></span><dl> <span data-ttu-id="47caa-111"><dt>**D3DX \_ 參數 \_ 常值**</dt></span><span class="sxs-lookup"><span data-stu-id="47caa-111"><dt>**D3DX\_PARAMETER\_LITERAL**</dt></span></span> </dl>          | <span data-ttu-id="47caa-112">此參數會標示為常值。</span><span class="sxs-lookup"><span data-stu-id="47caa-112">This parameter is marked as a literal value.</span></span> <span data-ttu-id="47caa-113">在編譯之後，常值參數無法變更，讓編譯器可以優化其使用方式。</span><span class="sxs-lookup"><span data-stu-id="47caa-113">Literal parameters cannot change after compile, allowing the compiler to optimize their usage.</span></span> <span data-ttu-id="47caa-114">共用參數不可標記為常值。</span><span class="sxs-lookup"><span data-stu-id="47caa-114">Shared parameters cannot be marked as a literal.</span></span> <span data-ttu-id="47caa-115">請參閱 [ (Direct3D 9) 的使用方式和常 ](usages-and-literals.md)值。</span><span class="sxs-lookup"><span data-stu-id="47caa-115">See [Usages and Literals (Direct3D 9)](usages-and-literals.md).</span></span> <br/>                                                               |
| <span id="D3DX_PARAMETER_SHARED"></span><span id="d3dx_parameter_shared"></span><dl> <span data-ttu-id="47caa-116"><dt>**共用的 D3DX \_ 參數 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="47caa-116"><dt>**D3DX\_PARAMETER\_SHARED**</dt></span></span> </dl>             | <span data-ttu-id="47caa-117">參數的值將由相同命名空間中的所有效果所共用。</span><span class="sxs-lookup"><span data-stu-id="47caa-117">The value of a parameter will be shared by all effects in the same namespace.</span></span> <span data-ttu-id="47caa-118">變更其中一個效果的值，會在所有的共用效果中變更。</span><span class="sxs-lookup"><span data-stu-id="47caa-118">Changing the value in one effect will change it in all shared effects.</span></span> <span data-ttu-id="47caa-119">請參閱 [共用參數](cloning-and-sharing.md)。</span><span class="sxs-lookup"><span data-stu-id="47caa-119">See [Sharing Parameters](cloning-and-sharing.md).</span></span> <span data-ttu-id="47caa-120">**D3DX \_無法 \_** 使用 **D3DX \_ 參數 \_ 常** 值或 **D3DX \_ 參數 \_ 注釋** 來合併參數共用。</span><span class="sxs-lookup"><span data-stu-id="47caa-120">**D3DX\_PARAMETER\_SHARED** cannot be combined with **D3DX\_PARAMETER\_LITERAL** or **D3DX\_PARAMETER\_ANNOTATION**.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="47caa-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="47caa-121">Requirements</span></span>



| <span data-ttu-id="47caa-122">需求</span><span class="sxs-lookup"><span data-stu-id="47caa-122">Requirement</span></span> | <span data-ttu-id="47caa-123">值</span><span class="sxs-lookup"><span data-stu-id="47caa-123">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="47caa-124">標頭</span><span class="sxs-lookup"><span data-stu-id="47caa-124">Header</span></span><br/> | <dl> <span data-ttu-id="47caa-125"><dt>D3dx9effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="47caa-125"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47caa-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="47caa-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47caa-127">效果常數</span><span class="sxs-lookup"><span data-stu-id="47caa-127">Effect Constants</span></span>](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 




