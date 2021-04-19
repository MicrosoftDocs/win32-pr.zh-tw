---
title: '平面結構 (Windowsnumerics .h) '
description: 此結構代表使用3D 向量法線和距離值的平面。
ms.assetid: 3C5A5EA0-8A51-4F9B-A84A-0C8E726CE3FD
keywords:
- 平面結構
topic_type:
- apiref
api_name:
- plane structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d870e2769121b4aec542235081011406e439d579
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998679"
---
# <a name="plane-structure"></a><span data-ttu-id="d7069-104">平面結構</span><span class="sxs-lookup"><span data-stu-id="d7069-104">plane structure</span></span>

<span data-ttu-id="d7069-105">此結構代表使用3D 向量法線和距離值的平面。</span><span class="sxs-lookup"><span data-stu-id="d7069-105">This structure represents a plane using a 3D vector normal and a distance value.</span></span>

<span data-ttu-id="d7069-106">此類型僅適用于 c + +。</span><span class="sxs-lookup"><span data-stu-id="d7069-106">This type is available only in C++.</span></span> <span data-ttu-id="d7069-107">它的 .NET 對等專案是 [system.object](/dotnet/api/system.numerics.plane?view=netframework-4.8)。</span><span class="sxs-lookup"><span data-stu-id="d7069-107">Its .NET equivalent is [System.Numerics.Plane](/dotnet/api/system.numerics.plane?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="d7069-108">建構函式</span><span class="sxs-lookup"><span data-stu-id="d7069-108">Constructors</span></span>

| <span data-ttu-id="d7069-109">名稱</span><span class="sxs-lookup"><span data-stu-id="d7069-109">Name</span></span> | <span data-ttu-id="d7069-110">描述</span><span class="sxs-lookup"><span data-stu-id="d7069-110">Description</span></span> |
|-|-|
| `plane()` | <span data-ttu-id="d7069-111">建立未初始化的平面。</span><span class="sxs-lookup"><span data-stu-id="d7069-111">Creates an uninitialized plane.</span></span> |
| `plane(float x, float y, float z, float d)` | <span data-ttu-id="d7069-112">建立具有指定值的平面。</span><span class="sxs-lookup"><span data-stu-id="d7069-112">Creates a plane with the specified values.</span></span> |
| `plane(float3 normal, float d)` | <span data-ttu-id="d7069-113">從 float3 和距離建立平面。</span><span class="sxs-lookup"><span data-stu-id="d7069-113">Creates a plane from a float3 and a distance.</span></span> |
| `explicit plane(float4 value)` | <span data-ttu-id="d7069-114">從 float4 建立平面。</span><span class="sxs-lookup"><span data-stu-id="d7069-114">Creates a plane from a float4.</span></span> |
| `plane(Microsoft::?Graphics::?Canvas::?Numerics::?Plane const& value)` | <span data-ttu-id="d7069-115">Converts a **Microsoft.Graphics.Canvas.Numerics.Plane** to a plane.</span><span class="sxs-lookup"><span data-stu-id="d7069-115">Converts a **Microsoft.Graphics.Canvas.Numerics.Plane** to a plane.</span></span> |

## <a name="functions"></a><span data-ttu-id="d7069-116">函式</span><span class="sxs-lookup"><span data-stu-id="d7069-116">Functions</span></span>

| <span data-ttu-id="d7069-117">Name</span><span class="sxs-lookup"><span data-stu-id="d7069-117">Name</span></span> | <span data-ttu-id="d7069-118">描述</span><span class="sxs-lookup"><span data-stu-id="d7069-118">Description</span></span> |
|-|-|
| `plane make_plane_from_vertices(float3 const& point1, float3 const& point2, float3 const& point3)` | <span data-ttu-id="d7069-119">從三個頂點位置的集合建立平面，這些位置必須全都不同，而不是直線。</span><span class="sxs-lookup"><span data-stu-id="d7069-119">Creates a plane from a set of three vertex positions, which must all be different and not in a straight line.</span></span> |
| `plane normalize(plane const& value)` | <span data-ttu-id="d7069-120">變更平面標準向量的係數，使其成為單位長度。</span><span class="sxs-lookup"><span data-stu-id="d7069-120">Changes the coefficients of the normal vector of a plane to make it of unit length.</span></span> |
| `plane transform(plane const& plane, float4x4 const& matrix)` | <span data-ttu-id="d7069-121">依矩陣轉換正規化的平面。</span><span class="sxs-lookup"><span data-stu-id="d7069-121">Transforms a normalized plane by a matrix.</span></span> |
| `plane transform(plane const& plane, quaternion const& rotation)` | <span data-ttu-id="d7069-122">以四元數的旋轉來轉換正規化的平面。</span><span class="sxs-lookup"><span data-stu-id="d7069-122">Transforms a normalized plane by a quaternion rotation.</span></span> |
| `float dot(plane const& plane, float4 const& value)` | <span data-ttu-id="d7069-123">使用向量計算平面的點乘積。</span><span class="sxs-lookup"><span data-stu-id="d7069-123">Calculates the dot product of a plane with a vector.</span></span> |
| `float dot_coordinate(plane const& plane, float3 const& value)` | <span data-ttu-id="d7069-124">以 float3 座標計算平面的點乘積。</span><span class="sxs-lookup"><span data-stu-id="d7069-124">Calculates the dot product of a plane with a float3 coordinate.</span></span> <span data-ttu-id="d7069-125">與點 \_ 法線不同的是，此計算包含平面 d 值。</span><span class="sxs-lookup"><span data-stu-id="d7069-125">Unlike dot\_normal, this computation includes the plane d value.</span></span> |
| `float dot_normal(plane const& plane, float3 const& value)` | <span data-ttu-id="d7069-126">以 float3 標準計算平面的點乘積。</span><span class="sxs-lookup"><span data-stu-id="d7069-126">Calculates the dot product of a plane with a float3 normal.</span></span> <span data-ttu-id="d7069-127">與點 \_ 座標不同的是，此計算會忽略平面 d 值。</span><span class="sxs-lookup"><span data-stu-id="d7069-127">Unlike dot\_coordinate, this computation ignores the plane d value.</span></span> |

## <a name="operators"></a><span data-ttu-id="d7069-128">運算子</span><span class="sxs-lookup"><span data-stu-id="d7069-128">Operators</span></span>

| <span data-ttu-id="d7069-129">Name</span><span class="sxs-lookup"><span data-stu-id="d7069-129">Name</span></span> | <span data-ttu-id="d7069-130">描述</span><span class="sxs-lookup"><span data-stu-id="d7069-130">Description</span></span> |
|-|-|
| `bool operator== (plane const& value1, plane const& value2)` | <span data-ttu-id="d7069-131">判斷平面的兩個實例是否相等。</span><span class="sxs-lookup"><span data-stu-id="d7069-131">Determines whether two instances of plane are equal.</span></span> |
| `bool operator!= (plane const& value1, plane const& value2)` | <span data-ttu-id="d7069-132">判斷平面的兩個實例是否不相等。</span><span class="sxs-lookup"><span data-stu-id="d7069-132">Determines whether two instances of plane are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Plane() const` | <span data-ttu-id="d7069-133">將平面轉換成中 **的平面。**</span><span class="sxs-lookup"><span data-stu-id="d7069-133">Converts a plane to a **Microsoft.Graphics.Canvas.Numerics.Plane**.</span></span> |

## <a name="fields"></a><span data-ttu-id="d7069-134">欄位</span><span class="sxs-lookup"><span data-stu-id="d7069-134">Fields</span></span>

| <span data-ttu-id="d7069-135">名稱</span><span class="sxs-lookup"><span data-stu-id="d7069-135">Name</span></span> | <span data-ttu-id="d7069-136">描述</span><span class="sxs-lookup"><span data-stu-id="d7069-136">Description</span></span> |
|-|-|
| `float3 normal` | <span data-ttu-id="d7069-137">平面的一般向量。</span><span class="sxs-lookup"><span data-stu-id="d7069-137">Normal vector of the plane.</span></span> |
| `float d` | <span data-ttu-id="d7069-138">平面與原點之間的距離。</span><span class="sxs-lookup"><span data-stu-id="d7069-138">Distance of the plane along its normal from the origin.</span></span> |

## <a name="requirements"></a><span data-ttu-id="d7069-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7069-139">Requirements</span></span>

| <span data-ttu-id="d7069-140">需求</span><span class="sxs-lookup"><span data-stu-id="d7069-140">Requirement</span></span> | <span data-ttu-id="d7069-141">值</span><span class="sxs-lookup"><span data-stu-id="d7069-141">Value</span></span> |
|-|-|
| <span data-ttu-id="d7069-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="d7069-142">Namespace</span></span> | <span data-ttu-id="d7069-143">Windows：： Foundation：：數值</span><span class="sxs-lookup"><span data-stu-id="d7069-143">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="d7069-144">標頭</span><span class="sxs-lookup"><span data-stu-id="d7069-144">Header</span></span> | <dl> <span data-ttu-id="d7069-145"><dt>Windowsnumerics。h</dt></span><span class="sxs-lookup"><span data-stu-id="d7069-145"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="d7069-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7069-146">See also</span></span>

[<span data-ttu-id="d7069-147">windowsnumerics .h Api</span><span class="sxs-lookup"><span data-stu-id="d7069-147">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
