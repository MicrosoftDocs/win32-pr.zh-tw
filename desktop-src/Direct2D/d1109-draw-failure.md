---
title: D1109 繪圖失敗
ms.assetid: 76154839-719e-4c73-a80e-f9216f3468e3
description: 呈現目標的繪製呼叫失敗
keywords:
- D1109 Draw 失敗 Direct2D
topic_type:
- apiref
api_name:
- D1109 Draw Failure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 4b08dfb99d49dcb447443685e1fbfa01a2cbad1c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103683052"
---
# <a name="d1109-draw-failure"></a><span data-ttu-id="ae70a-104">D1109：繪製失敗</span><span class="sxs-lookup"><span data-stu-id="ae70a-104">D1109: Draw Failure</span></span>

<span data-ttu-id="ae70a-105">轉譯目標失敗資源的繪製呼叫 \[  \] 。</span><span class="sxs-lookup"><span data-stu-id="ae70a-105">A Draw call by a render target failed \[*resource*\].</span></span> <span data-ttu-id="ae70a-106">標記 \[ *tag1*、 *tag2* \] 。</span><span class="sxs-lookup"><span data-stu-id="ae70a-106">Tags \[*tag1*, *tag2*\].</span></span>

## <a name="placeholders"></a><span data-ttu-id="ae70a-107">預留位置</span><span class="sxs-lookup"><span data-stu-id="ae70a-107">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="ae70a-108"><span id="resource"></span><span id="RESOURCE"></span>*資源*</span><span class="sxs-lookup"><span data-stu-id="ae70a-108"><span id="resource"></span><span id="RESOURCE"></span>*resource*</span></span>
</dt> <dd>

<span data-ttu-id="ae70a-109">呈現目標的位址。</span><span class="sxs-lookup"><span data-stu-id="ae70a-109">The address of the render target.</span></span>

</dd> <dt>

<span data-ttu-id="ae70a-110"><span id="tag1"></span><span id="TAG1"></span>*tag1*</span><span class="sxs-lookup"><span data-stu-id="ae70a-110"><span id="tag1"></span><span id="TAG1"></span>*tag1*</span></span>
</dt> <dd>

<span data-ttu-id="ae70a-111">第一個標記值 (如需詳細資訊) ，請參閱 [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) 。</span><span class="sxs-lookup"><span data-stu-id="ae70a-111">The first tag value (see [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) more for information).</span></span>

</dd> <dt>

<span data-ttu-id="ae70a-112"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span><span class="sxs-lookup"><span data-stu-id="ae70a-112"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span></span>
</dt> <dd>

<span data-ttu-id="ae70a-113">第二個標籤值 (如需詳細資訊) ，請參閱 [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) 。</span><span class="sxs-lookup"><span data-stu-id="ae70a-113">The second tag value (see [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) more for information).</span></span>

</dd> </dl> 

|             |         |
|-------------|---------|
| <span data-ttu-id="ae70a-114">錯誤層級</span><span class="sxs-lookup"><span data-stu-id="ae70a-114">Error Level</span></span> | <span data-ttu-id="ae70a-115">警告</span><span class="sxs-lookup"><span data-stu-id="ae70a-115">Warning</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="ae70a-116">可能的原因</span><span class="sxs-lookup"><span data-stu-id="ae70a-116">Possible Causes</span></span>

<span data-ttu-id="ae70a-117">繪製呼叫可能會失敗的原因有很多。</span><span class="sxs-lookup"><span data-stu-id="ae70a-117">There are many reasons that a Draw call might fail.</span></span> <span data-ttu-id="ae70a-118">如需詳細資訊，請參閱 Direct2D SDK 檔集，以瞭解失敗的方法。</span><span class="sxs-lookup"><span data-stu-id="ae70a-118">For more information, see the Direct2D SDK documentation for the method that failed.</span></span>

 

 