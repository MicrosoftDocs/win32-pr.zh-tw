---
title: 輸出色彩暫存器
description: 圖元著色器色彩輸出會註冊 (的 oC \ ) 是僅限寫入的暫存器，可將結果輸出至多個呈現目標。
ms.assetid: 88e69189-3956-47de-a336-921f1e62c025
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 316160e39ce172d56e4ecac17dfbd1d53077005b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382454"
---
# <a name="output-color-register"></a><span data-ttu-id="c182c-103">輸出色彩暫存器</span><span class="sxs-lookup"><span data-stu-id="c182c-103">Output Color Register</span></span>

<span data-ttu-id="c182c-104">圖元著色器色彩輸出會註冊 (的 oC # ) 是僅限寫入的暫存器，可將結果輸出至多個呈現目標。</span><span class="sxs-lookup"><span data-stu-id="c182c-104">The pixel shader color output registers (oC#) are write-only registers that output results to multiple render targets.</span></span>

<span data-ttu-id="c182c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c182c-105">Syntax</span></span>



| <span data-ttu-id="c182c-106">Oc#</span><span class="sxs-lookup"><span data-stu-id="c182c-106">oC#</span></span> |
|------|



 

<span data-ttu-id="c182c-107">其中：</span><span class="sxs-lookup"><span data-stu-id="c182c-107">Where:</span></span>



| <span data-ttu-id="c182c-108">Name</span><span class="sxs-lookup"><span data-stu-id="c182c-108">Name</span></span> | <span data-ttu-id="c182c-109">描述</span><span class="sxs-lookup"><span data-stu-id="c182c-109">Description</span></span>       |
|------|-------------------|
| <span data-ttu-id="c182c-110">oC0</span><span class="sxs-lookup"><span data-stu-id="c182c-110">oC0</span></span>  | <span data-ttu-id="c182c-111">轉譯目標 \# 0</span><span class="sxs-lookup"><span data-stu-id="c182c-111">render target \#0</span></span> |
| <span data-ttu-id="c182c-112">oC1</span><span class="sxs-lookup"><span data-stu-id="c182c-112">oC1</span></span>  | <span data-ttu-id="c182c-113">轉譯目標 \# 1</span><span class="sxs-lookup"><span data-stu-id="c182c-113">render target \#1</span></span> |
| <span data-ttu-id="c182c-114">oC2</span><span class="sxs-lookup"><span data-stu-id="c182c-114">oC2</span></span>  | <span data-ttu-id="c182c-115">轉譯目標 \# 2</span><span class="sxs-lookup"><span data-stu-id="c182c-115">render target \#2</span></span> |
| <span data-ttu-id="c182c-116">oC3</span><span class="sxs-lookup"><span data-stu-id="c182c-116">oC3</span></span>  | <span data-ttu-id="c182c-117">轉譯目標 \# 3</span><span class="sxs-lookup"><span data-stu-id="c182c-117">render target \#3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c182c-118">備註</span><span class="sxs-lookup"><span data-stu-id="c182c-118">Remarks</span></span>

-   <span data-ttu-id="c182c-119">如果寫入 oCn 但沒有對應的轉譯目標，則會忽略此寫入 oCn。</span><span class="sxs-lookup"><span data-stu-id="c182c-119">If oCn is written but there is no corresponding render target, then this write to oCn is ignored.</span></span>
-   <span data-ttu-id="c182c-120">轉譯狀態 D3DRS \_ COLORWRITEENABLE、D3DRS \_ COLORWRITEENABLE1、D3DRS \_ COLORWRITEENABLE2 和 D3DRS \_ COLORWRITEENABLE3 決定在 blend 之後 (oCn 的哪些元件會寫入轉譯目標（如果適用) ）。</span><span class="sxs-lookup"><span data-stu-id="c182c-120">The render states D3DRS\_COLORWRITEENABLE, D3DRS\_COLORWRITEENABLE1, D3DRS\_COLORWRITEENABLE2 and D3DRS\_COLORWRITEENABLE3 determine which components of oCn ultimately get written to the render target (after blend, if applicable).</span></span> <span data-ttu-id="c182c-121">如果著色器針對指定的 oCn 暫存器，寫入 D3DRS COLORWRITEENABLE 轉譯狀態所定義的部分（而非全部 \_ \* ）元件，則不成文通道會在對應的呈現目標中產生未定義的值。</span><span class="sxs-lookup"><span data-stu-id="c182c-121">If the shader writes some but not all of the components defined by the D3DRS\_COLORWRITEENABLE\* render states for a given oCn register, then the unwritten channels produce undefined values in the corresponding render target.</span></span> <span data-ttu-id="c182c-122">如果未寫入 oCn 的元件，則不一定要在上述) 的所有 (更新對應的轉譯目標，因此 D3DRS \_ COLORWRITEENABLE 轉譯 \* 狀態不適用。</span><span class="sxs-lookup"><span data-stu-id="c182c-122">If none of the components of an oCn are written, the corresponding render target must not be updated at all (as stated above), so the D3DRS\_COLORWRITEENABLE\* render states do not apply.</span></span>

### <a name="shader-model-2-restrictions"></a><span data-ttu-id="c182c-123">著色器模型2限制</span><span class="sxs-lookup"><span data-stu-id="c182c-123">Shader Model 2 Restrictions</span></span>

-   <span data-ttu-id="c182c-124">oCn 只能使用 [mov-ps](mov---ps.md) 指令來撰寫。</span><span class="sxs-lookup"><span data-stu-id="c182c-124">oCn can only be written with the [mov - ps](mov---ps.md) instruction.</span></span>
-   <span data-ttu-id="c182c-125">oC0 必須一律寫入著色器中。</span><span class="sxs-lookup"><span data-stu-id="c182c-125">oC0 must be always written in the shader.</span></span>
-   <span data-ttu-id="c182c-126">在寫入任何 oCn 時，不允許來源 swizzle (除了 xyzw = default swizzle) 或 source 修飾詞。</span><span class="sxs-lookup"><span data-stu-id="c182c-126">No source swizzle (except .xyzw = default swizzle) or source modifier is allowed when writing to any oCn.</span></span>
-   <span data-ttu-id="c182c-127">除了 xyzw = 預設遮罩) 或指令修飾詞寫入任何 oCn 時，不允許目的地寫入遮罩 (。</span><span class="sxs-lookup"><span data-stu-id="c182c-127">No destination write mask (except .xyzw = default mask) or instruction modifier is allowed when writing to any oCn.</span></span>
-   <span data-ttu-id="c182c-128">如果寫入 oCn，則也必須寫入 oC0-oCn-1。</span><span class="sxs-lookup"><span data-stu-id="c182c-128">If oCn is written, then oC0 - oCn-1 must also be written.</span></span> <span data-ttu-id="c182c-129">例如，若要寫入 oC2，您也必須寫入 oC0 和 oC1。</span><span class="sxs-lookup"><span data-stu-id="c182c-129">For example, to write to oC2, you must also write to oC0 and oC1.</span></span>
-   <span data-ttu-id="c182c-130">每個著色器最多隻能寫入一個 oC #。</span><span class="sxs-lookup"><span data-stu-id="c182c-130">At most one write to any oC# per shader is allowed.</span></span>
-   <span data-ttu-id="c182c-131">針對 ps \_ 2 \_ x 和 ps \_ 3 \_ 0，您無法寫入至動態流程式控制制或 predication 中的 oc # 和 oD 暫存器 \# (寫入靜態流程式控制制內的 oc #) 。</span><span class="sxs-lookup"><span data-stu-id="c182c-131">For ps\_2\_x and ps\_3\_0, you cannot write to oC# and oD\# registers within dynamic flow control or predication (writes to oC# inside static flow control is fine).</span></span>

### <a name="shader-model-3-restrictions"></a><span data-ttu-id="c182c-132">著色器模型3限制</span><span class="sxs-lookup"><span data-stu-id="c182c-132">Shader Model 3 Restrictions</span></span>

-   <span data-ttu-id="c182c-133">針對 ps \_ 3 \_ 0，輸出會將 oC # 和 oD \# 寫入任意次數。</span><span class="sxs-lookup"><span data-stu-id="c182c-133">For ps\_3\_0, output registers oC# and oD\# can be written any number of times.</span></span> <span data-ttu-id="c182c-134">圖元著色器的輸出來自于著色器執行結束時的輸出暫存器內容。</span><span class="sxs-lookup"><span data-stu-id="c182c-134">The output of the pixel shader comes from the contents of the output registers at the end of shader execution.</span></span> <span data-ttu-id="c182c-135">如果未進行寫入至輸出暫存器（可能是因為流量控制），或著色器剛剛未寫入，則對應的 rendertarget 也不會更新。</span><span class="sxs-lookup"><span data-stu-id="c182c-135">If a write to an output register does not happen, perhaps due to flow control or if the shader just did not write it, the corresponding rendertarget is also not updated.</span></span> <span data-ttu-id="c182c-136">如果寫入輸出暫存器中的通道子集，則會將未定義的值寫入其餘的通道。</span><span class="sxs-lookup"><span data-stu-id="c182c-136">If a subset of the channels in an output register are written, then undefined values will be written to the remaining channels.</span></span>
-   <span data-ttu-id="c182c-137">若是 ps \_ 3 \_ 0，可以使用任何 Writemasks 寫入 oC # 暫存器。</span><span class="sxs-lookup"><span data-stu-id="c182c-137">For ps\_3\_0, the oC# registers can be written with any writemasks.</span></span>
-   <span data-ttu-id="c182c-138">針對 ps \_ 2 \_ x 和 ps \_ 3 \_ 0，您無法寫入至動態流程式控制制或 predication 中的 oc # 和 oD 暫存器 \# (寫入靜態流程式控制制內的 oc #) 。</span><span class="sxs-lookup"><span data-stu-id="c182c-138">For ps\_2\_x and ps\_3\_0, you cannot write to oC# and oD\# registers within dynamic flow control or predication (writes to oC# inside static flow control is fine).</span></span>
-   <span data-ttu-id="c182c-139">您可能不會執行任何漸層計算 (或隱含叫用漸層計算的作業（例如 [texld-ps \_ 2 \_ 0 和 up](texld---ps-2-0.md)、 [texldb-ps](texldb---ps.md)、 [texldp-ps](texldp---ps.md)) 在流程式控制制語句內，其分支條件會因每個基準而異 (例如：動態流程式控制制指示) 。</span><span class="sxs-lookup"><span data-stu-id="c182c-139">You may not perform any gradient calculations (or operations that implicitly invoke gradient calculations such as [texld - ps\_2\_0 and up](texld---ps-2-0.md), [texldb - ps](texldb---ps.md), [texldp - ps](texldp---ps.md)) inside of flow control statements whose branching conditions vary on a per-primitive basis (ie: dynamic flow control instructions).</span></span> <span data-ttu-id="c182c-140">指令 predication 不會被視為動態流量控制。</span><span class="sxs-lookup"><span data-stu-id="c182c-140">Instruction predication is not considered dynamic flow control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c182c-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="c182c-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c182c-142">寄存 器</span><span class="sxs-lookup"><span data-stu-id="c182c-142">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> <dt>

[<span data-ttu-id="c182c-143"> (Direct3D 9) 的多個呈現目標 </span><span class="sxs-lookup"><span data-stu-id="c182c-143">Multiple Render Targets (Direct3D 9)</span></span>](/windows/desktop/direct3d9/multiple-render-targets)
</dt> </dl>

 

 