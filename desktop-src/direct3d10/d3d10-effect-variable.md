---
description: 這些常數適用于效果變數。
ms.assetid: ef996443-b558-4aa6-acc1-38f8a89c9855
title: D3D10_EFFECT_VARIABLE 常數
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58d6367fe89f66ff90991b8493a03a6d1b4244f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970103"
---
# <a name="d3d10_effect_variable-constants"></a><span data-ttu-id="601c6-103">D3D10 \_ 效果 \_ 變數常數</span><span class="sxs-lookup"><span data-stu-id="601c6-103">D3D10\_EFFECT\_VARIABLE Constants</span></span>

<span data-ttu-id="601c6-104">這些常數適用于效果變數。</span><span class="sxs-lookup"><span data-stu-id="601c6-104">These constants apply to effect variables.</span></span>



| <span data-ttu-id="601c6-105">\#定義</span><span class="sxs-lookup"><span data-stu-id="601c6-105">\#define</span></span>                                       | <span data-ttu-id="601c6-106">描述</span><span class="sxs-lookup"><span data-stu-id="601c6-106">Description</span></span>  | <span data-ttu-id="601c6-107">值</span><span class="sxs-lookup"><span data-stu-id="601c6-107">Value</span></span>                                                                                                                                                                                                                                                             |
|------------------------------------------------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="601c6-108">D3D10 \_ 效果 \_ 變數 \_ 注釋</span><span class="sxs-lookup"><span data-stu-id="601c6-108">D3D10\_EFFECT\_VARIABLE\_ANNOTATION</span></span>            | <span data-ttu-id="601c6-109">1 << 0</span><span class="sxs-lookup"><span data-stu-id="601c6-109">1 << 0</span></span> | <span data-ttu-id="601c6-110">表示這是批註或全域變數。</span><span class="sxs-lookup"><span data-stu-id="601c6-110">Indicates that this is an annotation or a global variable.</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="601c6-111">D3D10 \_ 效果 \_ 變數集區 \_</span><span class="sxs-lookup"><span data-stu-id="601c6-111">D3D10\_EFFECT\_VARIABLE\_POOLED</span></span>                | <span data-ttu-id="601c6-112">1 << 1</span><span class="sxs-lookup"><span data-stu-id="601c6-112">1 << 1</span></span> | <span data-ttu-id="601c6-113">指出這個變數或常數緩衝區位於效果集區中。</span><span class="sxs-lookup"><span data-stu-id="601c6-113">Indicates that this variable or constant buffer resides in an effect pool.</span></span> <span data-ttu-id="601c6-114">如果未設定此旗標，則變數會處於獨立效果或子效果 (獨立效果會從 [**ID3D10Effect：： IsPool**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-ispool)傳回 false。</span><span class="sxs-lookup"><span data-stu-id="601c6-114">If this flag is not set, then the variable resides in a standalone effect or a child effect (standalone effects return false from [**ID3D10Effect::IsPool**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-ispool).</span></span> |
| <span data-ttu-id="601c6-115">D3D10 \_ 效果 \_ 變數 \_ 明確 \_ 綁定 \_ 點</span><span class="sxs-lookup"><span data-stu-id="601c6-115">D3D10\_EFFECT\_VARIABLE\_EXPLICIT\_BIND\_POINT</span></span> | <span data-ttu-id="601c6-116">1 << 2</span><span class="sxs-lookup"><span data-stu-id="601c6-116">1 << 2</span></span> | <span data-ttu-id="601c6-117">表示已使用 register 關鍵字明確地系結變數。</span><span class="sxs-lookup"><span data-stu-id="601c6-117">Indicates that the variable has been explicitly bound using the register keyword.</span></span>                                                                                                                                                                                 |



 

<span data-ttu-id="601c6-118">這些旗標在 d3d10effect 中會定義為宏。</span><span class="sxs-lookup"><span data-stu-id="601c6-118">These flags are defined as macros in d3d10effect.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="601c6-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="601c6-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="601c6-120"> (Direct3D 10) 的效果常數 </span><span class="sxs-lookup"><span data-stu-id="601c6-120">Effect Constants (Direct3D 10)</span></span>](d3d10-graphics-reference-effect-constants.md)
</dt> </dl>

 

 



