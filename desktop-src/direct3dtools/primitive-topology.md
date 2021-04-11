---
description: 用來表示網格拓撲的列舉。 請參閱 MeshDataVertCallback。
MS-HAID: vspixengine.PRIMITIVE\_TOPOLOGY
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PRIMITIVE_TOPOLOGY 列舉
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A845DD10-C735-4EA1-82D3-07F3B26508E7
api_name:
- PRIMITIVE_TOPOLOGY
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7e448fcaaeaa2b1b50bd77b18ac4b3ac3f5e122a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025784"
---
# <a name="span-idvspixengineprimitive_topologyspanprimitive_topology-enumeration"></a><span data-ttu-id="5b88b-104"><span id="vspixengine.primitive_topology"></span>基本 \_ 拓撲列舉</span><span class="sxs-lookup"><span data-stu-id="5b88b-104"><span id="vspixengine.primitive_topology"></span>PRIMITIVE\_TOPOLOGY enumeration</span></span>

<span data-ttu-id="5b88b-105">用來表示網格拓撲的列舉。</span><span class="sxs-lookup"><span data-stu-id="5b88b-105">An enum used to indicate the topology of a mesh.</span></span> <span data-ttu-id="5b88b-106">請參閱 MeshDataVertCallback。</span><span class="sxs-lookup"><span data-stu-id="5b88b-106">See MeshDataVertCallback.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b88b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b88b-107">Syntax</span></span>


```C++
} PRIMITIVE_TOPOLOGY;
```

## <a name="constants"></a><span data-ttu-id="5b88b-108">常數</span><span class="sxs-lookup"><span data-stu-id="5b88b-108">Constants</span></span>

<span data-ttu-id="5b88b-109"><span id="PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="primitive_topology_undefined"></span>**\_ \_ 未定義基本拓撲**</span><span class="sxs-lookup"><span data-stu-id="5b88b-109"><span id="PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="primitive_topology_undefined"></span>**PRIMITIVE\_TOPOLOGY\_UNDEFINED**</span></span>  
<span data-ttu-id="5b88b-110">網格的拓撲是未定義的。</span><span class="sxs-lookup"><span data-stu-id="5b88b-110">The topology of the mesh is undefined.</span></span>

<span data-ttu-id="5b88b-111"><span id="PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="primitive_topology_pointlist"></span>**基本 \_ 拓撲 \_ POINTLIST**</span><span class="sxs-lookup"><span data-stu-id="5b88b-111"><span id="PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="primitive_topology_pointlist"></span>**PRIMITIVE\_TOPOLOGY\_POINTLIST**</span></span>  
<span data-ttu-id="5b88b-112">網格的拓撲是點清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-112">The topology of the mesh is a point list.</span></span>

<span data-ttu-id="5b88b-113"><span id="PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="primitive_topology_linelist"></span>**基本 \_ 拓撲 \_ LINELIST**</span><span class="sxs-lookup"><span data-stu-id="5b88b-113"><span id="PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="primitive_topology_linelist"></span>**PRIMITIVE\_TOPOLOGY\_LINELIST**</span></span>  
<span data-ttu-id="5b88b-114">網格的拓撲是行清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-114">The topology of the mesh is a line list.</span></span>

<span data-ttu-id="5b88b-115"><span id="PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="primitive_topology_linestrip"></span>**基本 \_ 拓撲 \_ LINESTRIP**</span><span class="sxs-lookup"><span data-stu-id="5b88b-115"><span id="PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="primitive_topology_linestrip"></span>**PRIMITIVE\_TOPOLOGY\_LINESTRIP**</span></span>  
<span data-ttu-id="5b88b-116">網格的拓撲是行帶狀。</span><span class="sxs-lookup"><span data-stu-id="5b88b-116">The topology of the mesh is a line strip.</span></span>

<span data-ttu-id="5b88b-117"><span id="PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="primitive_topology_trianglelist"></span>**基本 \_ 拓撲 \_ TRIANGLELIST**</span><span class="sxs-lookup"><span data-stu-id="5b88b-117"><span id="PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="primitive_topology_trianglelist"></span>**PRIMITIVE\_TOPOLOGY\_TRIANGLELIST**</span></span>  
<span data-ttu-id="5b88b-118">網格的拓撲是一種三角形清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-118">The topology of the mesh is a triangle list.</span></span>

<span data-ttu-id="5b88b-119"><span id="PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="primitive_topology_trianglestrip"></span>**基本 \_ 拓撲 \_ TRIANGLESTRIP**</span><span class="sxs-lookup"><span data-stu-id="5b88b-119"><span id="PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="primitive_topology_trianglestrip"></span>**PRIMITIVE\_TOPOLOGY\_TRIANGLESTRIP**</span></span>  
<span data-ttu-id="5b88b-120">網格的拓撲是一個三角形的帶。</span><span class="sxs-lookup"><span data-stu-id="5b88b-120">The topology of the mesh is a triangle strip.</span></span>

<span data-ttu-id="5b88b-121"><span id="PRIMITIVE_TOPOLOGY_TRIANGLEFAN"></span><span id="primitive_topology_trianglefan"></span>**基本 \_ 拓撲 \_ TRIANGLEFAN**</span><span class="sxs-lookup"><span data-stu-id="5b88b-121"><span id="PRIMITIVE_TOPOLOGY_TRIANGLEFAN"></span><span id="primitive_topology_trianglefan"></span>**PRIMITIVE\_TOPOLOGY\_TRIANGLEFAN**</span></span>  
<span data-ttu-id="5b88b-122">網格的拓撲是三角形風扇。</span><span class="sxs-lookup"><span data-stu-id="5b88b-122">The topology of the mesh is a triangle fan.</span></span>

<span data-ttu-id="5b88b-123"><span id="PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="primitive_topology_linelist_adj"></span>**基本 \_ 拓撲 \_ LINELIST \_ 形容詞**</span><span class="sxs-lookup"><span data-stu-id="5b88b-123"><span id="PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="primitive_topology_linelist_adj"></span>**PRIMITIVE\_TOPOLOGY\_LINELIST\_ADJ**</span></span>  
<span data-ttu-id="5b88b-124">網格的拓撲是具有連續的線條清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-124">The topology of the mesh is a line list with adjacency.</span></span>

<span data-ttu-id="5b88b-125"><span id="PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="primitive_topology_linestrip_adj"></span>**基本 \_ 拓撲 \_ LINESTRIP \_ 形容詞**</span><span class="sxs-lookup"><span data-stu-id="5b88b-125"><span id="PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="primitive_topology_linestrip_adj"></span>**PRIMITIVE\_TOPOLOGY\_LINESTRIP\_ADJ**</span></span>  
<span data-ttu-id="5b88b-126">網格的拓撲是具有連續的行帶狀。</span><span class="sxs-lookup"><span data-stu-id="5b88b-126">The topology of the mesh is a line strip with adjacency.</span></span>

<span data-ttu-id="5b88b-127"><span id="PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="primitive_topology_trianglelist_adj"></span>**基本 \_ 拓撲 \_ TRIANGLELIST \_ 形容詞**</span><span class="sxs-lookup"><span data-stu-id="5b88b-127"><span id="PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="primitive_topology_trianglelist_adj"></span>**PRIMITIVE\_TOPOLOGY\_TRIANGLELIST\_ADJ**</span></span>  
<span data-ttu-id="5b88b-128">網格的拓撲是具有連續的三角形清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-128">The topology of the mesh is a triangle list with adjacency.</span></span>

<span data-ttu-id="5b88b-129"><span id="PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="primitive_topology_trianglestrip_adj"></span>**基本 \_ 拓撲 \_ TRIANGLESTRIP \_ 形容詞**</span><span class="sxs-lookup"><span data-stu-id="5b88b-129"><span id="PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="primitive_topology_trianglestrip_adj"></span>**PRIMITIVE\_TOPOLOGY\_TRIANGLESTRIP\_ADJ**</span></span>  
<span data-ttu-id="5b88b-130">網格的拓撲是具有連續的三角形帶。</span><span class="sxs-lookup"><span data-stu-id="5b88b-130">The topology of the mesh is a triangle strip with adjacency.</span></span>

<span data-ttu-id="5b88b-131"><span id="PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_1_control_point_patchlist"></span>**基本 \_ 拓撲 \_ 1 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="5b88b-131"><span id="PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_1_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_1\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="5b88b-132">網格的拓撲是包含1個控制點的修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-132">The topology of the mesh is a patch list with 1 control point.</span></span>

<span data-ttu-id="5b88b-133"><span id="PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_2_control_point_patchlist"></span>**基本 \_ 拓撲 \_ 2 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="5b88b-133"><span id="PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_2_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_2\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="5b88b-134">網格的拓撲是具有2個控制點的修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-134">The topology of the mesh is a patch list with 2 control points.</span></span>

<span data-ttu-id="5b88b-135"><span id="PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_3_control_point_patchlist"></span>**基本 \_ 拓撲 \_ 3 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="5b88b-135"><span id="PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_3_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_3\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="5b88b-136">網格的拓撲是含有3個控制點的修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-136">The topology of the mesh is a patch list with 3 control points.</span></span>

<span data-ttu-id="5b88b-137"><span id="PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_4_control_point_patchlist"></span>**基本 \_ 拓撲 \_ 4 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="5b88b-137"><span id="PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_4_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_4\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="5b88b-138">網格的拓撲是具有4個控制點的修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-138">The topology of the mesh is a patch list with 4 control points.</span></span>

<span data-ttu-id="5b88b-139"><span id="PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_5_control_point_patchlist"></span>**基本 \_ 拓撲 \_ 5 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="5b88b-139"><span id="PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_5_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_5\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="5b88b-140">網格的拓撲是具有5個控制點的修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-140">The topology of the mesh is a patch list with 5 control points.</span></span>

<span data-ttu-id="5b88b-141"><span id="PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_6_control_point_patchlist"></span>**基本 \_ 拓撲 \_ 6 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="5b88b-141"><span id="PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_6_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_6\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="5b88b-142">網格的拓撲是具有6個控制點的修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-142">The topology of the mesh is a patch list with 6 control points.</span></span>

<span data-ttu-id="5b88b-143"><span id="PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_7_control_point_patchlist"></span>**基本 \_ 拓撲 \_ 7 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="5b88b-143"><span id="PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_7_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_7\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="5b88b-144">網格的拓撲是具有7個控制點的修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-144">The topology of the mesh is a patch list with 7 control points.</span></span>

<span data-ttu-id="5b88b-145"><span id="PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_8_control_point_patchlist"></span>**基本 \_ 拓撲 \_ 8 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="5b88b-145"><span id="PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_8_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_8\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="5b88b-146">網格的拓撲是具有8個控制點的修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-146">The topology of the mesh is a patch list with 8 control points.</span></span>

<span data-ttu-id="5b88b-147"><span id="PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_9_control_point_patchlist"></span>**基本 \_ 拓撲 \_ 9 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="5b88b-147"><span id="PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_9_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_9\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="5b88b-148">網格的拓撲是具有9個控制點的修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-148">The topology of the mesh is a patch list with 9 control points.</span></span>

<span data-ttu-id="5b88b-149"><span id="PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_10_control_point_patchlist"></span>**基本 \_ 拓撲 \_ 10 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="5b88b-149"><span id="PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_10_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_10\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="5b88b-150">網格的拓撲是包含10個控制點的修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-150">The topology of the mesh is a patch list with 10 control points.</span></span>

<span data-ttu-id="5b88b-151"><span id="PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_11_control_point_patchlist"></span>**基本 \_ 拓撲 \_ 11 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="5b88b-151"><span id="PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_11_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_11\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="5b88b-152">網格的拓撲是包含11個控制點的修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-152">The topology of the mesh is a patch list with 11 control points.</span></span>

<span data-ttu-id="5b88b-153"><span id="PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_12_control_point_patchlist"></span>**基本 \_ 拓撲 \_ 12 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="5b88b-153"><span id="PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_12_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_12\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="5b88b-154">網格的拓撲是具有12個控制點的修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-154">The topology of the mesh is a patch list with 12 control points.</span></span>

<span data-ttu-id="5b88b-155"><span id="PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_13_control_point_patchlist"></span>**基本 \_ 拓撲 \_ 13 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="5b88b-155"><span id="PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_13_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_13\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="5b88b-156">網格的拓撲是含13個控制點的修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-156">The topology of the mesh is a patch list with 13 control points.</span></span>

<span data-ttu-id="5b88b-157"><span id="PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_14_control_point_patchlist"></span>**基本 \_ 拓撲 \_ 14 \_ 控制 \_ 點 \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="5b88b-157"><span id="PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_14_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_14\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="5b88b-158">網格的拓撲是具有14個控制點的修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-158">The topology of the mesh is a patch list with 14 control points.</span></span>

<span data-ttu-id="5b88b-159"><span id="PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_15_control_point_patchlist"></span>**基本 \_ 拓撲 \_ 15 \_ 控制 \_ 點 \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="5b88b-159"><span id="PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_15_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_15\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="5b88b-160">網格的拓撲是具有15個控制點的修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-160">The topology of the mesh is a patch list with 15 control points.</span></span>

<span data-ttu-id="5b88b-161"><span id="PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_16_control_point_patchlist"></span>**基本 \_ 拓撲 \_ 16 \_ 控制 \_ 點 \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="5b88b-161"><span id="PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_16_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_16\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="5b88b-162">網格的拓撲是包含16個控制點的修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-162">The topology of the mesh is a patch list with 16 control points.</span></span>

<span data-ttu-id="5b88b-163"><span id="PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_17_control_point_patchlist"></span>**基本 \_ 拓撲 \_ 17 \_ 控制 \_ 點 \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="5b88b-163"><span id="PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_17_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_17\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="5b88b-164">網格的拓撲是包含17個控制點的修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-164">The topology of the mesh is a patch list with 17 control points.</span></span>

<span data-ttu-id="5b88b-165"><span id="PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_18_control_point_patchlist"></span>**基本 \_ 拓撲 \_ 18 \_ 控制 \_ 點 \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="5b88b-165"><span id="PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_18_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_18\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="5b88b-166">網格的拓撲是包含18個控制點的修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-166">The topology of the mesh is a patch list with 18 control points.</span></span>

<span data-ttu-id="5b88b-167"><span id="PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_19_control_point_patchlist"></span>**基本 \_ 拓撲 \_ 19 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="5b88b-167"><span id="PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_19_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_19\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="5b88b-168">網格的拓撲是具有19個控制點的修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-168">The topology of the mesh is a patch list with 19 control points.</span></span>

<span data-ttu-id="5b88b-169"><span id="PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_20_control_point_patchlist"></span>**基本 \_ 拓撲 \_ 20 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="5b88b-169"><span id="PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_20_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_20\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="5b88b-170">網格的拓撲是具有20個控制點的修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-170">The topology of the mesh is a patch list with 20 control points.</span></span>

<span data-ttu-id="5b88b-171"><span id="PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_21_control_point_patchlist"></span>**基本 \_ 拓撲 \_ 21 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="5b88b-171"><span id="PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_21_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_21\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="5b88b-172">網格的拓撲是包含21個控制點的修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-172">The topology of the mesh is a patch list with 21 control points.</span></span>

<span data-ttu-id="5b88b-173"><span id="PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_22_control_point_patchlist"></span>**基本 \_ 拓撲 \_ 22 \_ 控制 \_ 點 \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="5b88b-173"><span id="PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_22_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_22\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="5b88b-174">網格的拓撲是包含22個控制點的修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-174">The topology of the mesh is a patch list with 22 control points.</span></span>

<span data-ttu-id="5b88b-175"><span id="PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_23_control_point_patchlist"></span>**基本 \_ 拓撲 \_ 23 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="5b88b-175"><span id="PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_23_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_23\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="5b88b-176">網格的拓撲是包含23個控制點的 patch 清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-176">The topology of the mesh is a patch list with 23 control points.</span></span>

<span data-ttu-id="5b88b-177"><span id="PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_24_control_point_patchlist"></span>**基本 \_ 拓撲 \_ 24 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="5b88b-177"><span id="PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_24_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_24\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="5b88b-178">網格的拓撲是包含24個控制點的修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-178">The topology of the mesh is a patch list with 24 control points.</span></span>

<span data-ttu-id="5b88b-179"><span id="PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_25_control_point_patchlist"></span>**基本 \_ 拓撲 \_ 25 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="5b88b-179"><span id="PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_25_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_25\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="5b88b-180">網格的拓撲是包含25個控制點的修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-180">The topology of the mesh is a patch list with 25 control points.</span></span>

<span data-ttu-id="5b88b-181"><span id="PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_26_control_point_patchlist"></span>**基本 \_ 拓撲 \_ 26 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="5b88b-181"><span id="PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_26_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_26\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="5b88b-182">網格的拓撲是具有26個控制點的修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-182">The topology of the mesh is a patch list with 26 control points.</span></span>

<span data-ttu-id="5b88b-183"><span id="PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_27_control_point_patchlist"></span>**基本 \_ 拓撲 \_ 27 \_ 控制 \_ 點 \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="5b88b-183"><span id="PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_27_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_27\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="5b88b-184">網格的拓撲是包含27個控制點的 patch 清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-184">The topology of the mesh is a patch list with 27 control points.</span></span>

<span data-ttu-id="5b88b-185"><span id="PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_28_control_point_patchlist"></span>**基本 \_ 拓撲 \_ 28 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="5b88b-185"><span id="PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_28_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_28\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="5b88b-186">網格的拓撲是包含28個控制點的修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-186">The topology of the mesh is a patch list with 28 control points.</span></span>

<span data-ttu-id="5b88b-187"><span id="PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_29_control_point_patchlist"></span>**基本 \_ 拓撲 \_ 29 \_ 控制 \_ 點 \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="5b88b-187"><span id="PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_29_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_29\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="5b88b-188">網格的拓撲是包含29個控制點的修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-188">The topology of the mesh is a patch list with 29 control points.</span></span>

<span data-ttu-id="5b88b-189"><span id="PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_30_control_point_patchlist"></span>**基本 \_ 拓撲 \_ 30 \_ 控制 \_ 點 \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="5b88b-189"><span id="PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_30_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_30\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="5b88b-190">網格的拓撲是具有30個控制點的修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-190">The topology of the mesh is a patch list with 30 control points.</span></span>

<span data-ttu-id="5b88b-191"><span id="PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_31_control_point_patchlist"></span>**基本 \_ 拓撲 \_ 31 \_ 控制 \_ 點 \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="5b88b-191"><span id="PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_31_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_31\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="5b88b-192">網格的拓撲是包含31個控制點的 patch 清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-192">The topology of the mesh is a patch list with 31 control points.</span></span>

<span data-ttu-id="5b88b-193"><span id="PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_32_control_point_patchlist"></span>**基本 \_ 拓撲 \_ 32 \_ 控制點 \_ \_ PATCHLIST**</span><span class="sxs-lookup"><span data-stu-id="5b88b-193"><span id="PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="primitive_topology_32_control_point_patchlist"></span>**PRIMITIVE\_TOPOLOGY\_32\_CONTROL\_POINT\_PATCHLIST**</span></span>  
<span data-ttu-id="5b88b-194">網格的拓撲是包含32控制點的修補程式清單。</span><span class="sxs-lookup"><span data-stu-id="5b88b-194">The topology of the mesh is a patch list with 32 control points.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b88b-195">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b88b-195">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="5b88b-196">標頭</span><span class="sxs-lookup"><span data-stu-id="5b88b-196">Header</span></span></p></td><td><span data-ttu-id="5b88b-197">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="5b88b-197">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



