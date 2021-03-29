---
description: 管線如何解讀系結至輸入組合語言階段的頂點資料。 這些基本拓撲值會決定在螢幕上呈現頂點資料的方式。
ms.assetid: ca0547b2-d0f8-4edc-a62c-3c903e1b33ea
title: D3D11 \_ 基本 \_ 拓撲列舉
ms.date: 06/26/2019
ms.topic: reference
ms.openlocfilehash: 1d2beab107a3f3abe03e5a17f068e1b508422241
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104991858"
---
# <a name="d3d11_primitive_topology-enumeration"></a><span data-ttu-id="b60c8-104">D3D11 \_ 基本 \_ 拓撲列舉</span><span class="sxs-lookup"><span data-stu-id="b60c8-104">D3D11\_PRIMITIVE\_TOPOLOGY enumeration</span></span>

<span data-ttu-id="b60c8-105">管線如何解讀系結至輸入組合語言階段的頂點資料。</span><span class="sxs-lookup"><span data-stu-id="b60c8-105">How the pipeline interprets vertex data that is bound to the input-assembler stage.</span></span> <span data-ttu-id="b60c8-106">這些基本拓撲值會決定在螢幕上呈現頂點資料的方式。</span><span class="sxs-lookup"><span data-stu-id="b60c8-106">These primitive topology values determine how the vertex data is rendered on screen.</span></span>

## <a name="syntax"></a><span data-ttu-id="b60c8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b60c8-107">Syntax</span></span>


```C++
} D3D11_PRIMITIVE_TOPOLOGY;
```



## <a name="constants"></a><span data-ttu-id="b60c8-108">常數</span><span class="sxs-lookup"><span data-stu-id="b60c8-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b60c8-109"><span id="D3D11_PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="d3d11_primitive_topology_undefined"></span>**\_ \_ 未定義 D3D11 基本拓撲 \_**</span><span class="sxs-lookup"><span data-stu-id="b60c8-109"><span id="D3D11_PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="d3d11_primitive_topology_undefined"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-110">IA 階段尚未以基本拓撲初始化。</span><span class="sxs-lookup"><span data-stu-id="b60c8-110">The IA stage has not been initialized with a primitive topology.</span></span> <span data-ttu-id="b60c8-111">除非已定義基本拓撲，否則 IA 階段將無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="b60c8-111">The IA stage will not function properly unless a primitive topology is defined.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-112"><span id="D3D11_PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="d3d11_primitive_topology_pointlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ POINTLIST**</span><span class="sxs-lookup"><span data-stu-id="b60c8-112"><span id="D3D11_PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="d3d11_primitive_topology_pointlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_POINTLIST**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-113">將頂點資料解讀為點清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-113">Interpret the vertex data as a list of points.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-114"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="d3d11_primitive_topology_linelist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ LINELIST**</span><span class="sxs-lookup"><span data-stu-id="b60c8-114"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="d3d11_primitive_topology_linelist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_LINELIST**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-115">將頂點資料解讀為線條清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-115">Interpret the vertex data as a list of lines.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-116"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="d3d11_primitive_topology_linestrip"></span>**D3D11 \_ 基本 \_ 拓撲 \_ LINESTRIP**</span><span class="sxs-lookup"><span data-stu-id="b60c8-116"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="d3d11_primitive_topology_linestrip"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_LINESTRIP**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-117">將頂點資料解讀為行帶。</span><span class="sxs-lookup"><span data-stu-id="b60c8-117">Interpret the vertex data as a line strip.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-118"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="d3d11_primitive_topology_trianglelist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ TRIANGLELIST**</span><span class="sxs-lookup"><span data-stu-id="b60c8-118"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="d3d11_primitive_topology_trianglelist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_TRIANGLELIST**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-119">將頂點資料解讀為三角形清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-119">Interpret the vertex data as a list of triangles.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-120"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="d3d11_primitive_topology_trianglestrip"></span>**D3D11 \_ 基本 \_ 拓撲 \_ TRIANGLESTRIP**</span><span class="sxs-lookup"><span data-stu-id="b60c8-120"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="d3d11_primitive_topology_trianglestrip"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_TRIANGLESTRIP**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-121">將頂點資料解讀為三角形帶。</span><span class="sxs-lookup"><span data-stu-id="b60c8-121">Interpret the vertex data as a triangle strip.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-122"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="d3d11_primitive_topology_linelist_adj"></span>**D3D11 \_ 基本 \_ 拓撲 \_ LINELIST \_ 形容詞**</span><span class="sxs-lookup"><span data-stu-id="b60c8-122"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="d3d11_primitive_topology_linelist_adj"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_LINELIST\_ADJ**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-123">將頂點資料解讀為具有相鄰資料的線條清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-123">Interpret the vertex data as list of lines with adjacency data.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-124"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="d3d11_primitive_topology_linestrip_adj"></span>**D3D11 \_ 基本 \_ 拓撲 \_ LINESTRIP \_ 形容詞**</span><span class="sxs-lookup"><span data-stu-id="b60c8-124"><span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="d3d11_primitive_topology_linestrip_adj"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_LINESTRIP\_ADJ**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-125">以相鄰資料的行帶來解讀頂點資料。</span><span class="sxs-lookup"><span data-stu-id="b60c8-125">Interpret the vertex data as line strip with adjacency data.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-126"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="d3d11_primitive_topology_trianglelist_adj"></span>**D3D11 \_ 基本 \_ 拓撲 \_ TRIANGLELIST \_ 形容詞**</span><span class="sxs-lookup"><span data-stu-id="b60c8-126"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="d3d11_primitive_topology_trianglelist_adj"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_TRIANGLELIST\_ADJ**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-127">將頂點資料解讀為具有相鄰資料的三角形清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-127">Interpret the vertex data as list of triangles with adjacency data.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-128"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="d3d11_primitive_topology_trianglestrip_adj"></span>**D3D11 \_ 基本 \_ 拓撲 \_ TRIANGLESTRIP \_ 形容詞**</span><span class="sxs-lookup"><span data-stu-id="b60c8-128"><span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="d3d11_primitive_topology_trianglestrip_adj"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_TRIANGLESTRIP\_ADJ**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-129">使用相鄰資料將頂點資料解讀為三角形帶。</span><span class="sxs-lookup"><span data-stu-id="b60c8-129">Interpret the vertex data as triangle strip with adjacency data.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-130"><span id="D3D11_PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_1_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 1 \_ 控制 \_ 點 \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="b60c8-130"><span id="D3D11_PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_1_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_1\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-131">將頂點資料解讀為修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-131">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-132"><span id="D3D11_PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_2_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 2 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="b60c8-132"><span id="D3D11_PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_2_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_2\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-133">將頂點資料解讀為修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-133">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-134"><span id="D3D11_PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_3_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 3 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="b60c8-134"><span id="D3D11_PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_3_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_3\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-135">將頂點資料解讀為修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-135">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-136"><span id="D3D11_PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_4_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 4 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="b60c8-136"><span id="D3D11_PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_4_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_4\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-137">將頂點資料解讀為修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-137">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-138"><span id="D3D11_PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_5_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 5 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="b60c8-138"><span id="D3D11_PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_5_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_5\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-139">將頂點資料解讀為修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-139">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-140"><span id="D3D11_PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_6_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 6 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="b60c8-140"><span id="D3D11_PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_6_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_6\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-141">將頂點資料解讀為修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-141">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-142"><span id="D3D11_PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_7_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 7 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="b60c8-142"><span id="D3D11_PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_7_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_7\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-143">將頂點資料解讀為修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-143">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-144"><span id="D3D11_PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_8_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 8 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="b60c8-144"><span id="D3D11_PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_8_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_8\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-145">將頂點資料解讀為修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-145">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-146"><span id="D3D11_PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_9_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 9 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="b60c8-146"><span id="D3D11_PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_9_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_9\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-147">將頂點資料解讀為修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-147">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-148"><span id="D3D11_PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_10_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 10 \_ 控制 \_ 點 \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="b60c8-148"><span id="D3D11_PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_10_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_10\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-149">將頂點資料解讀為修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-149">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-150"><span id="D3D11_PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_11_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 11 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="b60c8-150"><span id="D3D11_PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_11_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_11\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-151">將頂點資料解讀為修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-151">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-152"><span id="D3D11_PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_12_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 12 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="b60c8-152"><span id="D3D11_PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_12_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_12\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-153">將頂點資料解讀為修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-153">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-154"><span id="D3D11_PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_13_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 13 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="b60c8-154"><span id="D3D11_PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_13_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_13\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-155">將頂點資料解讀為修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-155">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-156"><span id="D3D11_PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_14_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 14 \_ 控制 \_ 點 \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="b60c8-156"><span id="D3D11_PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_14_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_14\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-157">將頂點資料解讀為修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-157">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-158"><span id="D3D11_PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_15_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 15 \_ 控制 \_ 點 \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="b60c8-158"><span id="D3D11_PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_15_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_15\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-159">將頂點資料解讀為修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-159">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-160"><span id="D3D11_PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_16_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 16 \_ 控制 \_ 點 \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="b60c8-160"><span id="D3D11_PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_16_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_16\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-161">將頂點資料解讀為修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-161">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-162"><span id="D3D11_PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_17_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 17 \_ 控制 \_ 點 \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="b60c8-162"><span id="D3D11_PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_17_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_17\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-163">將頂點資料解讀為修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-163">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-164"><span id="D3D11_PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_18_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 18 \_ 控制 \_ 點 \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="b60c8-164"><span id="D3D11_PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_18_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_18\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-165">將頂點資料解讀為修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-165">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-166"><span id="D3D11_PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_19_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 19 \_ 控制 \_ 點 \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="b60c8-166"><span id="D3D11_PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_19_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_19\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-167">將頂點資料解讀為修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-167">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-168"><span id="D3D11_PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_20_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 20 \_ 控制 \_ 點 \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="b60c8-168"><span id="D3D11_PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_20_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_20\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-169">將頂點資料解讀為修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-169">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-170"><span id="D3D11_PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_21_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 21 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="b60c8-170"><span id="D3D11_PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_21_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_21\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-171">將頂點資料解讀為修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-171">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-172"><span id="D3D11_PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_22_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 22 \_ 控制 \_ 點 \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="b60c8-172"><span id="D3D11_PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_22_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_22\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-173">將頂點資料解讀為修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-173">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-174"><span id="D3D11_PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_23_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 23 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="b60c8-174"><span id="D3D11_PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_23_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_23\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-175">將頂點資料解讀為修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-175">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-176"><span id="D3D11_PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_24_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 24 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="b60c8-176"><span id="D3D11_PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_24_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_24\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-177">將頂點資料解讀為修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-177">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-178"><span id="D3D11_PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_25_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 25 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="b60c8-178"><span id="D3D11_PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_25_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_25\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-179">將頂點資料解讀為修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-179">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-180"><span id="D3D11_PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_26_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 26 \_ 控制 \_ 點 \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="b60c8-180"><span id="D3D11_PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_26_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_26\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-181">將頂點資料解讀為修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-181">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-182"><span id="D3D11_PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_27_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 27 \_ 控制 \_ 點 \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="b60c8-182"><span id="D3D11_PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_27_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_27\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-183">將頂點資料解讀為修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-183">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-184"><span id="D3D11_PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_28_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 28 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="b60c8-184"><span id="D3D11_PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_28_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_28\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-185">將頂點資料解讀為修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-185">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-186"><span id="D3D11_PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_29_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 29 \_ 控制 \_ 點 \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="b60c8-186"><span id="D3D11_PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_29_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_29\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-187">將頂點資料解讀為修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-187">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-188"><span id="D3D11_PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_30_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 30 \_ 控制 \_ 點 \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="b60c8-188"><span id="D3D11_PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_30_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_30\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-189">將頂點資料解讀為修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-189">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-190"><span id="D3D11_PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_31_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 31 \_ 控制 \_ 點 \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="b60c8-190"><span id="D3D11_PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_31_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_31\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-191">將頂點資料解讀為修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-191">Interpret the vertex data as a patch list.</span></span>

</dd> <dt>

<span data-ttu-id="b60c8-192"><span id="D3D11_PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_32_control_point_patchlist"></span>**D3D11 \_ 基本 \_ 拓撲 \_ 32 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="b60c8-192"><span id="D3D11_PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_32_control_point_patchlist"></span>**D3D11\_PRIMITIVE\_TOPOLOGY\_32\_CONTROL\_POINT\_PATCHLIST**</span></span>
</dt> <dd>

<span data-ttu-id="b60c8-193">將頂點資料解讀為修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="b60c8-193">Interpret the vertex data as a patch list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b60c8-194">備註</span><span class="sxs-lookup"><span data-stu-id="b60c8-194">Remarks</span></span>

<span data-ttu-id="b60c8-195">**D3D11 \_ 基本 \_ 拓撲** 列舉是 D3D11 .h 標頭檔中定義的類型，做為 [**D3D \_ 基本 \_ 拓撲**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology)列舉，在 D3DCommon .h 標頭檔中完整定義。</span><span class="sxs-lookup"><span data-stu-id="b60c8-195">The **D3D11\_PRIMITIVE\_TOPOLOGY** enumeration is type defined in the D3D11.h header file as a [**D3D\_PRIMITIVE\_TOPOLOGY**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology) enumeration, which is fully defined in the D3DCommon.h header file.</span></span>
