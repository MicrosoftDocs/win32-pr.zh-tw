---
title: 一般資源屬性
description: 在16位 Windows 上支援的資源定義語句包含載入記憶體選項，可指定資源的載入和記憶體特性。
ms.assetid: 53740997-854b-447c-9ab1-de8e17c0de1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa15ae7207c80737e284151f0dfd3d7981935943
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968043"
---
# <a name="common-resource-attributes"></a><span data-ttu-id="017fb-103">一般資源屬性</span><span class="sxs-lookup"><span data-stu-id="017fb-103">Common Resource Attributes</span></span>

<span data-ttu-id="017fb-104">在16位 Windows 上支援的資源定義語句包含 *載入記憶體* 選項，可指定資源的載入和記憶體特性。</span><span class="sxs-lookup"><span data-stu-id="017fb-104">The resource-definition statements supported on 16-bit Windows include a *load-mem* option that specifies the loading and memory characteristics of the resource.</span></span> <span data-ttu-id="017fb-105">資源腳本中允許這些屬性以提供回溯相容性，但會忽略這些屬性。</span><span class="sxs-lookup"><span data-stu-id="017fb-105">These attributes are permitted in resource scripts for backward compatibility, but they are ignored.</span></span> <span data-ttu-id="017fb-106">載入對應的模組時，系統會載入 Windows 資源，並在卸載模組時將其釋出。</span><span class="sxs-lookup"><span data-stu-id="017fb-106">Windows resources are loaded when the corresponding module is loaded, and are freed when the module is unloaded.</span></span>

## <a name="load-attributes"></a><span data-ttu-id="017fb-107">載入屬性</span><span class="sxs-lookup"><span data-stu-id="017fb-107">Load Attributes</span></span>

<span data-ttu-id="017fb-108">Load 屬性會指定資源的載入時間。</span><span class="sxs-lookup"><span data-stu-id="017fb-108">The load attributes specify when the resource is to be loaded.</span></span> <span data-ttu-id="017fb-109">Load 參數必須是下列其中一個屬性。</span><span class="sxs-lookup"><span data-stu-id="017fb-109">The load parameter must be one of the following attributes.</span></span>



| <span data-ttu-id="017fb-110">屬性</span><span class="sxs-lookup"><span data-stu-id="017fb-110">Attribute</span></span>      | <span data-ttu-id="017fb-111">描述</span><span class="sxs-lookup"><span data-stu-id="017fb-111">Description</span></span>                                                                  |
|----------------|------------------------------------------------------------------------------|
| <span data-ttu-id="017fb-112">**預 緊**</span><span class="sxs-lookup"><span data-stu-id="017fb-112">**PRELOAD**</span></span>    | <span data-ttu-id="017fb-113">忽略。</span><span class="sxs-lookup"><span data-stu-id="017fb-113">Ignored.</span></span> <span data-ttu-id="017fb-114">在16位的 Windows 中，資源會與可執行檔一起載入。</span><span class="sxs-lookup"><span data-stu-id="017fb-114">In 16-bit Windows, the resource is loaded with the executable file.</span></span> |
| <span data-ttu-id="017fb-115">**LOADONCALL**</span><span class="sxs-lookup"><span data-stu-id="017fb-115">**LOADONCALL**</span></span> | <span data-ttu-id="017fb-116">忽略。</span><span class="sxs-lookup"><span data-stu-id="017fb-116">Ignored.</span></span> <span data-ttu-id="017fb-117">在16位的 Windows 中，會在呼叫時載入資源。</span><span class="sxs-lookup"><span data-stu-id="017fb-117">In 16-bit Windows, the resource is loaded when called.</span></span>              |



 

## <a name="memory-attributes"></a><span data-ttu-id="017fb-118">記憶體屬性</span><span class="sxs-lookup"><span data-stu-id="017fb-118">Memory Attributes</span></span>

<span data-ttu-id="017fb-119">Memory 屬性會指定資源為固定或可移動、是否為 discardable，以及是否為純虛擬。</span><span class="sxs-lookup"><span data-stu-id="017fb-119">The memory attributes specify whether the resource is fixed or movable, whether it is discardable, and whether it is pure.</span></span> <span data-ttu-id="017fb-120">Memory 參數可以是下列一或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="017fb-120">The memory parameter can be one or more of the following attributes.</span></span>



| <span data-ttu-id="017fb-121">屬性</span><span class="sxs-lookup"><span data-stu-id="017fb-121">Attribute</span></span>       | <span data-ttu-id="017fb-122">描述</span><span class="sxs-lookup"><span data-stu-id="017fb-122">Description</span></span>                                                                                                                               |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="017fb-123">**FIXED**</span><span class="sxs-lookup"><span data-stu-id="017fb-123">**FIXED**</span></span>       | <span data-ttu-id="017fb-124">忽略。</span><span class="sxs-lookup"><span data-stu-id="017fb-124">Ignored.</span></span> <span data-ttu-id="017fb-125">在16位的 Windows 中，資源會保留在固定的記憶體位置。</span><span class="sxs-lookup"><span data-stu-id="017fb-125">In 16-bit Windows, the resource remains at a fixed memory location.</span></span>                                                              |
| <span data-ttu-id="017fb-126">**移動**</span><span class="sxs-lookup"><span data-stu-id="017fb-126">**MOVEABLE**</span></span>    | <span data-ttu-id="017fb-127">忽略。</span><span class="sxs-lookup"><span data-stu-id="017fb-127">Ignored.</span></span> <span data-ttu-id="017fb-128">在16位的 Windows 中，可在需要時移動資源以壓縮記憶體。</span><span class="sxs-lookup"><span data-stu-id="017fb-128">In 16-bit Windows, the resource can be moved if necessary to compact memory.</span></span>                                                     |
| <span data-ttu-id="017fb-129">**DISCARDABLE**</span><span class="sxs-lookup"><span data-stu-id="017fb-129">**DISCARDABLE**</span></span> | <span data-ttu-id="017fb-130">忽略。</span><span class="sxs-lookup"><span data-stu-id="017fb-130">Ignored.</span></span> <span data-ttu-id="017fb-131">在16位的 Windows 中，如果不再需要資源，則可以將它捨棄。</span><span class="sxs-lookup"><span data-stu-id="017fb-131">In 16-bit Windows, the resource can be discarded if no longer needed.</span></span>                                                            |
| <span data-ttu-id="017fb-132">**純**</span><span class="sxs-lookup"><span data-stu-id="017fb-132">**PURE**</span></span>        | <span data-ttu-id="017fb-133">忽略。</span><span class="sxs-lookup"><span data-stu-id="017fb-133">Ignored.</span></span> <span data-ttu-id="017fb-134">已接受，可與現有的資源腳本相容。</span><span class="sxs-lookup"><span data-stu-id="017fb-134">Accepted for compatibility with existing resource scripts.</span></span>                                                                       |
| <span data-ttu-id="017fb-135">**IMPURE**</span><span class="sxs-lookup"><span data-stu-id="017fb-135">**IMPURE**</span></span>      | <span data-ttu-id="017fb-136">忽略。</span><span class="sxs-lookup"><span data-stu-id="017fb-136">Ignored.</span></span> <span data-ttu-id="017fb-137">已接受，可與現有的資源腳本相容。</span><span class="sxs-lookup"><span data-stu-id="017fb-137">Accepted for compatibility with existing resource scripts.</span></span>                                                                       |
| <span data-ttu-id="017fb-138">**共用**</span><span class="sxs-lookup"><span data-stu-id="017fb-138">**SHARED**</span></span>      | <span data-ttu-id="017fb-139">忽略。</span><span class="sxs-lookup"><span data-stu-id="017fb-139">Ignored.</span></span> <span data-ttu-id="017fb-140">在16位的 Windows 中，一般模組會忽略 SHARED。</span><span class="sxs-lookup"><span data-stu-id="017fb-140">In 16-bit Windows, SHARED is ignored for regular modules.</span></span> <span data-ttu-id="017fb-141">對於來自 ROM Windows 模組的資源，則會共用記憶體。</span><span class="sxs-lookup"><span data-stu-id="017fb-141">For a resource from a ROM Windows module, the memory is shared.</span></span>        |
| <span data-ttu-id="017fb-142">**非共用**</span><span class="sxs-lookup"><span data-stu-id="017fb-142">**NONSHARED**</span></span>   | <span data-ttu-id="017fb-143">忽略。</span><span class="sxs-lookup"><span data-stu-id="017fb-143">Ignored.</span></span> <span data-ttu-id="017fb-144">在16位的 Windows 中，一般模組會忽略非共用。</span><span class="sxs-lookup"><span data-stu-id="017fb-144">In 16-bit Windows, NONSHARED is ignored for regular modules.</span></span> <span data-ttu-id="017fb-145">對於來自 ROM Windows 模組的資源，則不會共用記憶體。</span><span class="sxs-lookup"><span data-stu-id="017fb-145">For a resource from a ROM Windows module, the memory is not shared.</span></span> |



 

 

 




