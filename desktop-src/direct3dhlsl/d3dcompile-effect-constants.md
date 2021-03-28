---
title: 'D3DCOMPILE_EFFECT 常數 (D3DCompiler) '
description: 這些常數會指示編譯器編譯效果檔案的方式，或執行時間處理效果檔案的方式。
ms.assetid: AA46E5ED-92DD-4327-B852-8DD23A878562
topic_type:
- apiref
api_name:
- D3DCOMPILE_EFFECT_CHILD_EFFECT
- D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS
api_location:
- D3DCompiler.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69f0597341a331af82ed279a6030126d222b70f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974457"
---
# <a name="d3dcompile_effect-constants"></a><span data-ttu-id="0505e-103">D3DCOMPILE \_ 效果常數</span><span class="sxs-lookup"><span data-stu-id="0505e-103">D3DCOMPILE\_EFFECT Constants</span></span>

<span data-ttu-id="0505e-104">這些常數會指示編譯器編譯效果檔案的方式，或執行時間處理效果檔案的方式。</span><span class="sxs-lookup"><span data-stu-id="0505e-104">These constants direct how the compiler compiles an effect file or how the runtime processes the effect file.</span></span>

<dl> <dt>

<span data-ttu-id="0505e-105"><span id="D3DCOMPILE_EFFECT_CHILD_EFFECT"></span><span id="d3dcompile_effect_child_effect"></span>**D3DCOMPILE \_ 效果 \_ 子 \_ 效果**</span><span class="sxs-lookup"><span data-stu-id="0505e-105"><span id="D3DCOMPILE_EFFECT_CHILD_EFFECT"></span><span id="d3dcompile_effect_child_effect"></span>**D3DCOMPILE\_EFFECT\_CHILD\_EFFECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0505e-106"> (1 << 0) </span><span class="sxs-lookup"><span data-stu-id="0505e-106">(1 << 0)</span></span>
</dt> <dt>



<span data-ttu-id="0505e-107">將 ( 的效果編譯) 的子效果。</span><span class="sxs-lookup"><span data-stu-id="0505e-107">Compile the effects (.fx) file to a child effect.</span></span> <span data-ttu-id="0505e-108">子效果沒有任何共用值的初始化運算式，因為這些子效果會在效果集區)  (的主要效果中初始化。</span><span class="sxs-lookup"><span data-stu-id="0505e-108">Child effects have no initializers for any shared values because these child effects are initialized in the master effect (the effect pool).</span></span>

> [!Note]  
> <span data-ttu-id="0505e-109">效果集區受到效果 10 (FX10) 的支援，但不受效果 11 (FX11) 。</span><span class="sxs-lookup"><span data-stu-id="0505e-109">Effect pools are supported by Effects 10 (FX10) but not by Effects 11 (FX11).</span></span> <span data-ttu-id="0505e-110">如需 Direct3D 10 中效果集區與 Direct3D 11 中效果群組之間差異的詳細資訊，請參閱效果集區 [和群組](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects-differences)。</span><span class="sxs-lookup"><span data-stu-id="0505e-110">For more info about differences between effect pools in Direct3D 10 and effect groups in Direct3D 11, see [Effect Pools and Groups](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects-differences).</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="0505e-111"><span id="D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS"></span><span id="d3dcompile_effect_allow_slow_ops"></span>**D3DCOMPILE \_ 效果 \_ 允許 \_ 緩慢的 \_ OPS**</span><span class="sxs-lookup"><span data-stu-id="0505e-111"><span id="D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS"></span><span id="d3dcompile_effect_allow_slow_ops"></span>**D3DCOMPILE\_EFFECT\_ALLOW\_SLOW\_OPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0505e-112"> (1 << 1) </span><span class="sxs-lookup"><span data-stu-id="0505e-112">(1 << 1)</span></span>
</dt> <dt>



<span data-ttu-id="0505e-113">停用效能模式，並允許可變狀態物件。</span><span class="sxs-lookup"><span data-stu-id="0505e-113">Disables performance mode and allows for mutable state objects.</span></span>

<span data-ttu-id="0505e-114">預設會啟用效能模式。</span><span class="sxs-lookup"><span data-stu-id="0505e-114">By default, performance mode is enabled.</span></span> <span data-ttu-id="0505e-115">效能模式防止非常值運算式出現在狀態物件定義中，因此不允許可變動狀態物件。</span><span class="sxs-lookup"><span data-stu-id="0505e-115">Performance mode disallows mutable state objects by preventing non-literal expressions from appearing in state object definitions.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0505e-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="0505e-116">Requirements</span></span>



| <span data-ttu-id="0505e-117">需求</span><span class="sxs-lookup"><span data-stu-id="0505e-117">Requirement</span></span> | <span data-ttu-id="0505e-118">值</span><span class="sxs-lookup"><span data-stu-id="0505e-118">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0505e-119">標頭</span><span class="sxs-lookup"><span data-stu-id="0505e-119">Header</span></span><br/> | <dl> <span data-ttu-id="0505e-120"><dt>D3DCompiler。h</dt></span><span class="sxs-lookup"><span data-stu-id="0505e-120"><dt>D3DCompiler.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0505e-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0505e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0505e-122">D3DCompiler 常數</span><span class="sxs-lookup"><span data-stu-id="0505e-122">D3DCompiler Constants</span></span>](dx-graphics-d3dcompiler-reference-constants.md)
</dt> </dl>

 

