---
title: 屬性群組
description: 屬性群組
ms.assetid: 9fd7dc6e-6749-4e32-b795-21b63b64c291
keywords:
- OpenGL、attribute 群組
- OpenGL 參考，屬性群組
- OpenGL、attribute 群組的參考
- attribute 群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d93582c8996438ad99d7bf896cf83bdf6fbf72d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106979653"
---
# <a name="attribute-groups"></a><span data-ttu-id="9b8ee-107">屬性群組</span><span class="sxs-lookup"><span data-stu-id="9b8ee-107">Attribute Groups</span></span>



| <span data-ttu-id="9b8ee-108">遮罩位</span><span class="sxs-lookup"><span data-stu-id="9b8ee-108">Mask bit</span></span>                  | <span data-ttu-id="9b8ee-109">屬性群組</span><span class="sxs-lookup"><span data-stu-id="9b8ee-109">Attribute group</span></span> |
|---------------------------|-----------------|
| <span data-ttu-id="9b8ee-110">GL \_ ACCUM \_ 緩衝區 \_ 位</span><span class="sxs-lookup"><span data-stu-id="9b8ee-110">GL\_ACCUM\_BUFFER\_BIT</span></span>    | <span data-ttu-id="9b8ee-111">accum-緩衝區</span><span class="sxs-lookup"><span data-stu-id="9b8ee-111">accum-buffer</span></span>    |
| <span data-ttu-id="9b8ee-112">GL \_ 所有 \_ ATTRIB \_ 位</span><span class="sxs-lookup"><span data-stu-id="9b8ee-112">GL\_ALL\_ATTRIB\_BITS</span></span>     |                 |
| <span data-ttu-id="9b8ee-113">GL \_ 色彩 \_ 緩衝區 \_ 位</span><span class="sxs-lookup"><span data-stu-id="9b8ee-113">GL\_COLOR\_BUFFER\_BIT</span></span>    | <span data-ttu-id="9b8ee-114">色彩緩衝區</span><span class="sxs-lookup"><span data-stu-id="9b8ee-114">color-buffer</span></span>    |
| <span data-ttu-id="9b8ee-115">GL \_ 目前 \_ 位</span><span class="sxs-lookup"><span data-stu-id="9b8ee-115">GL\_CURRENT\_BIT</span></span>          | <span data-ttu-id="9b8ee-116">目前的</span><span class="sxs-lookup"><span data-stu-id="9b8ee-116">current</span></span>         |
| <span data-ttu-id="9b8ee-117">GL \_ 深度 \_ 緩衝區 \_ 位</span><span class="sxs-lookup"><span data-stu-id="9b8ee-117">GL\_DEPTH\_BUFFER\_BIT</span></span>    | <span data-ttu-id="9b8ee-118">深度-緩衝區</span><span class="sxs-lookup"><span data-stu-id="9b8ee-118">depth-buffer</span></span>    |
| <span data-ttu-id="9b8ee-119">GL \_ 啟用 \_ 位</span><span class="sxs-lookup"><span data-stu-id="9b8ee-119">GL\_ENABLE\_BIT</span></span>           | <span data-ttu-id="9b8ee-120">enable</span><span class="sxs-lookup"><span data-stu-id="9b8ee-120">enable</span></span>          |
| <span data-ttu-id="9b8ee-121">GL \_ EVAL \_ BIT</span><span class="sxs-lookup"><span data-stu-id="9b8ee-121">GL\_EVAL\_BIT</span></span>             | <span data-ttu-id="9b8ee-122">eval</span><span class="sxs-lookup"><span data-stu-id="9b8ee-122">eval</span></span>            |
| <span data-ttu-id="9b8ee-123">GL \_ 霧化 \_ 位</span><span class="sxs-lookup"><span data-stu-id="9b8ee-123">GL\_FOG\_BIT</span></span>              | <span data-ttu-id="9b8ee-124">霧</span><span class="sxs-lookup"><span data-stu-id="9b8ee-124">fog</span></span>             |
| <span data-ttu-id="9b8ee-125">GL \_ 提示 \_ 位</span><span class="sxs-lookup"><span data-stu-id="9b8ee-125">GL\_HINT\_BIT</span></span>             | <span data-ttu-id="9b8ee-126">提示</span><span class="sxs-lookup"><span data-stu-id="9b8ee-126">hint</span></span>            |
| <span data-ttu-id="9b8ee-127">GL \_ 照明 \_ 位</span><span class="sxs-lookup"><span data-stu-id="9b8ee-127">GL\_LIGHTING\_BIT</span></span>         | <span data-ttu-id="9b8ee-128">光源</span><span class="sxs-lookup"><span data-stu-id="9b8ee-128">lighting</span></span>        |
| <span data-ttu-id="9b8ee-129">GL \_ 行 \_ 位</span><span class="sxs-lookup"><span data-stu-id="9b8ee-129">GL\_LINE\_BIT</span></span>             | <span data-ttu-id="9b8ee-130">line</span><span class="sxs-lookup"><span data-stu-id="9b8ee-130">line</span></span>            |
| <span data-ttu-id="9b8ee-131">GL \_ 清單 \_ 位</span><span class="sxs-lookup"><span data-stu-id="9b8ee-131">GL\_LIST\_BIT</span></span>             | <span data-ttu-id="9b8ee-132">list</span><span class="sxs-lookup"><span data-stu-id="9b8ee-132">list</span></span>            |
| <span data-ttu-id="9b8ee-133">GL \_ 圖元 \_ 模式 \_ 位</span><span class="sxs-lookup"><span data-stu-id="9b8ee-133">GL\_PIXEL\_MODE\_BIT</span></span>      | <span data-ttu-id="9b8ee-134">像素</span><span class="sxs-lookup"><span data-stu-id="9b8ee-134">pixel</span></span>           |
| <span data-ttu-id="9b8ee-135">GL \_ 點 \_ 位</span><span class="sxs-lookup"><span data-stu-id="9b8ee-135">GL\_POINT\_BIT</span></span>            | <span data-ttu-id="9b8ee-136">點</span><span class="sxs-lookup"><span data-stu-id="9b8ee-136">point</span></span>           |
| <span data-ttu-id="9b8ee-137">GL \_ 多邊形 \_ 位</span><span class="sxs-lookup"><span data-stu-id="9b8ee-137">GL\_POLYGON\_BIT</span></span>          | <span data-ttu-id="9b8ee-138">多邊形</span><span class="sxs-lookup"><span data-stu-id="9b8ee-138">polygon</span></span>         |
| <span data-ttu-id="9b8ee-139">GL \_ 多邊形 \_ STIPPLE \_ 位</span><span class="sxs-lookup"><span data-stu-id="9b8ee-139">GL\_POLYGON\_STIPPLE\_BIT</span></span> | <span data-ttu-id="9b8ee-140">多邊形-stipple</span><span class="sxs-lookup"><span data-stu-id="9b8ee-140">polygon-stipple</span></span> |
| <span data-ttu-id="9b8ee-141">GL \_ 剪式 \_ 位</span><span class="sxs-lookup"><span data-stu-id="9b8ee-141">GL\_SCISSOR\_BIT</span></span>          | <span data-ttu-id="9b8ee-142">剪刀</span><span class="sxs-lookup"><span data-stu-id="9b8ee-142">scissor</span></span>         |
| <span data-ttu-id="9b8ee-143">GL \_ 樣板 \_ 緩衝區 \_ 位</span><span class="sxs-lookup"><span data-stu-id="9b8ee-143">GL\_STENCIL\_BUFFER\_BIT</span></span>  | <span data-ttu-id="9b8ee-144">樣板-緩衝區</span><span class="sxs-lookup"><span data-stu-id="9b8ee-144">stencil-buffer</span></span>  |
| <span data-ttu-id="9b8ee-145">GL \_ 材質 \_ 位</span><span class="sxs-lookup"><span data-stu-id="9b8ee-145">GL\_TEXTURE\_BIT</span></span>          | <span data-ttu-id="9b8ee-146">紋理</span><span class="sxs-lookup"><span data-stu-id="9b8ee-146">texture</span></span>         |
| <span data-ttu-id="9b8ee-147">GL \_ 轉換 \_ 位</span><span class="sxs-lookup"><span data-stu-id="9b8ee-147">GL\_TRANSFORM\_BIT</span></span>        | <span data-ttu-id="9b8ee-148">Transform - 轉換</span><span class="sxs-lookup"><span data-stu-id="9b8ee-148">transform</span></span>       |
| <span data-ttu-id="9b8ee-149">GL \_ 區 \_ 位</span><span class="sxs-lookup"><span data-stu-id="9b8ee-149">GL\_VIEWPORT\_BIT</span></span>         | <span data-ttu-id="9b8ee-150">Viewport - 檢視區</span><span class="sxs-lookup"><span data-stu-id="9b8ee-150">viewport</span></span>        |



 

 

 




