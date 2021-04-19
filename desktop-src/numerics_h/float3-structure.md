---
title: 'float3 結構 (Windowsnumerics .h) '
description: 具有三個元件的向量。
ms.assetid: CAA10ADA-C5A8-4B75-A0A9-5C5B3FDD9A07
keywords:
- float3 結構
topic_type:
- apiref
api_name:
- float3 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ae524205c900c63438a50094dcd551a4903632b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981662"
---
# <a name="float3-structure"></a><span data-ttu-id="f3d2d-104">float3 結構</span><span class="sxs-lookup"><span data-stu-id="f3d2d-104">float3 structure</span></span>

<span data-ttu-id="f3d2d-105">具有三個元件的向量。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-105">A vector with three components.</span></span>

<span data-ttu-id="f3d2d-106">此類型僅適用于 c + +。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-106">This type is available only in C++.</span></span> <span data-ttu-id="f3d2d-107">它的 .NET 對等專案是 [Vector3](/dotnet/api/system.numerics.vector3?view=netframework-4.8)。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-107">Its .NET equivalent is [System.Numerics.Vector3](/dotnet/api/system.numerics.vector3?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="f3d2d-108">建構函式</span><span class="sxs-lookup"><span data-stu-id="f3d2d-108">Constructors</span></span>

| <span data-ttu-id="f3d2d-109">名稱</span><span class="sxs-lookup"><span data-stu-id="f3d2d-109">Name</span></span> | <span data-ttu-id="f3d2d-110">描述</span><span class="sxs-lookup"><span data-stu-id="f3d2d-110">Description</span></span> |
|-|-|
| `float3()` | <span data-ttu-id="f3d2d-111">建立未初始化的 float3。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-111">Creates an uninitialized float3.</span></span> |
| `float3(float x, float y, float z)` | <span data-ttu-id="f3d2d-112">使用指定的值建立 float3。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-112">Creates a float3 with the specified values.</span></span> |
| `float3(float2 value, float z)` | <span data-ttu-id="f3d2d-113">建立 float3，其 x 和 y 是從 float2 加上指定的 z 值複製而來。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-113">Creates a float3 with x and y copied from a float2 plus the specified z value.</span></span> |
| `explicit float3(float value)` | <span data-ttu-id="f3d2d-114">建立 float3，並將所有元件設定為指定的值。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-114">Creates a float3 with all components set to the specified value.</span></span> |
| `float3(Microsoft::Graphics::Canvas::Numerics::Vector3 const& value)` | <span data-ttu-id="f3d2d-115">將 **Vector3** 轉換成 float3 的格式。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-115">Converts a **Microsoft.Graphics.Canvas.Numerics.Vector3** to a float3.</span></span> |

## <a name="functions"></a><span data-ttu-id="f3d2d-116">函式</span><span class="sxs-lookup"><span data-stu-id="f3d2d-116">Functions</span></span>

| <span data-ttu-id="f3d2d-117">Name</span><span class="sxs-lookup"><span data-stu-id="f3d2d-117">Name</span></span> | <span data-ttu-id="f3d2d-118">描述</span><span class="sxs-lookup"><span data-stu-id="f3d2d-118">Description</span></span> |
|-|-|
| `float length(float3 const& value)` | <span data-ttu-id="f3d2d-119">計算向量的長度（或 Euclidean 距離）。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-119">Calculates the length, or Euclidean distance, of the vector.</span></span> |
| `float length_squared(float3 const& value)` | <span data-ttu-id="f3d2d-120">計算向量平方的長度（或 Euclidean 距離）。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-120">Calculates the length, or Euclidean distance, of the vector squared.</span></span> |
| `float distance(float3 const& value1, float3 const& value2)` | <span data-ttu-id="f3d2d-121">計算兩個向量之間的 Euclidean 距離。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-121">Calculates the Euclidean distance between two vectors.</span></span> |
| `float distance_squared(float3 const& value1, float3 const& value2)` | <span data-ttu-id="f3d2d-122">計算兩個向量平方之間的 Euclidean 距離。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-122">Calculates the Euclidean distance between two vectors squared.</span></span> |
| `float dot(float3 const& vector1, float3 const& vector2)` | <span data-ttu-id="f3d2d-123">計算兩個向量的點乘積。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-123">Calculates the dot product of two vectors.</span></span> |
| `float3 normalize(float3 const& value)` | <span data-ttu-id="f3d2d-124">從指定的向量建立單元向量。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-124">Creates a unit vector from the specified vector.</span></span> |
| `float3 cross(float3 const& vector1, float3 const& vector2)` | <span data-ttu-id="f3d2d-125">計算兩個向量的叉積。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-125">Calculates the cross product of two vectors.</span></span> |
| `float3 reflect(float3 const& vector, float3 const& normal)` | <span data-ttu-id="f3d2d-126">決定給定向量和一般的反映向量。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-126">Determines the reflect vector of the given vector and normal.</span></span> |
| `float3 min(float3 const& value1, float3 const& value2)` | <span data-ttu-id="f3d2d-127">傳回向量，其中包含每個相符元件配對的最小值。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-127">Returns a vector that contains the lowest value from each matching pair of components.</span></span> |
| `float3 max(float3 const& value1, float3 const& value2)` | <span data-ttu-id="f3d2d-128">傳回向量，其中包含每個相符元件的最高值。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-128">Returns a vector that contains the highest value from each matching pair of components.</span></span> |
| `float3 clamp(float3 const& value1, float3 const& min, float3 const& max)` | <span data-ttu-id="f3d2d-129">將值限制在指定的範圍內。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-129">Restricts a value to be within a specified range.</span></span> |
| `float3 lerp(float3 const& value1, float3 const& value2, float amount)` | <span data-ttu-id="f3d2d-130">在兩個向量之間執行線性插補。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-130">Performs a linear interpolation between two vectors.</span></span> |
| `float3 transform(float3 const& position, float4x4 const& matrix)` | <span data-ttu-id="f3d2d-131">將向量 (x、y、z、1) 由指定的矩陣進行轉換。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-131">Transforms the vector (x, y, z, 1) by the specified matrix.</span></span> |
| `float3 transform_normal(float3 const& normal, float4x4 const& matrix)` | <span data-ttu-id="f3d2d-132">將一般向量 (x、y、z、0) 由指定的矩陣進行轉換。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-132">Transforms the normal vector (x, y, z, 0) by the specified matrix.</span></span> |
| `float3 transform(float3 const& value, quaternion const& rotation)` | <span data-ttu-id="f3d2d-133">依據指定的四元數來轉換 float3。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-133">Transforms a float3 by the given quaternion.</span></span> |

## <a name="methods"></a><span data-ttu-id="f3d2d-134">方法</span><span class="sxs-lookup"><span data-stu-id="f3d2d-134">Methods</span></span>

| <span data-ttu-id="f3d2d-135">名稱</span><span class="sxs-lookup"><span data-stu-id="f3d2d-135">Name</span></span> | <span data-ttu-id="f3d2d-136">描述</span><span class="sxs-lookup"><span data-stu-id="f3d2d-136">Description</span></span> |
|-|-|
| `static float3 zero()` | <span data-ttu-id="f3d2d-137">傳回 float3，其中所有的元件都設為零。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-137">Returns a float3 with all of its components set to zero.</span></span> |
| `static float3 one()` | <span data-ttu-id="f3d2d-138">傳回 float3，其中所有的元件都設為1。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-138">Returns a float3 with all of its components set to one.</span></span> |
| `static float3 unit_x()` | <span data-ttu-id="f3d2d-139">傳回 float3 (1，0，0) 。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-139">Returns the float3 (1, 0, 0).</span></span> |
| `static float3 unit_y()` | <span data-ttu-id="f3d2d-140">傳回 float3 (0，1，0) 。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-140">Returns the float3 (0, 1, 0).</span></span> |
| `static float3 unit_z()` | <span data-ttu-id="f3d2d-141">傳回 float3 (0，0，1) 。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-141">Returns the float3 (0, 0, 1).</span></span> |

## <a name="operators"></a><span data-ttu-id="f3d2d-142">運算子</span><span class="sxs-lookup"><span data-stu-id="f3d2d-142">Operators</span></span>

| <span data-ttu-id="f3d2d-143">Name</span><span class="sxs-lookup"><span data-stu-id="f3d2d-143">Name</span></span> | <span data-ttu-id="f3d2d-144">描述</span><span class="sxs-lookup"><span data-stu-id="f3d2d-144">Description</span></span> |
|-|-|
| `float3 operator+ (float3 const& value1, float3 const& value2)` | <span data-ttu-id="f3d2d-145">新增兩個向量。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-145">Adds two vectors.</span></span> |
| `float3 operator- (float3 const& value1, float3 const& value2)` | <span data-ttu-id="f3d2d-146">從向量減去向量。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-146">Subtracts a vector from a vector.</span></span> |
| `float3 operator* (float3 const& value1, float3 const& value2)` | <span data-ttu-id="f3d2d-147">將兩個向量的元件相乘。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-147">Multiplies the components of two vectors by each other.</span></span> |
| `float3 operator* (float3 const& value1, float value2)` | <span data-ttu-id="f3d2d-148">將向量乘以純量。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-148">Multiplies a vector by a scalar.</span></span> |
| `float3 operator* (float value1, float3 const& value2)` | <span data-ttu-id="f3d2d-149">將向量乘以純量。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-149">Multiplies a vector by a scalar.</span></span> |
| `float3 operator/ (float3 const& value1, float3 const& value2)` | <span data-ttu-id="f3d2d-150">將向量的元件除以另一個向量的元件。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-150">Divides the components of a vector by the components of another vector.</span></span> |
| `float3 operator/ (float3 const& value1, float value2)` | <span data-ttu-id="f3d2d-151">將向量除以純量值。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-151">Divides a vector by a scalar value.</span></span> |
| `float3 operator- (float3 const& value)` | <span data-ttu-id="f3d2d-152">傳回指向相反方向的向量。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-152">Returns a vector pointing in the opposite direction.</span></span> |
| `float3& operator+= (float3& value1, float3 const& value2)` | <span data-ttu-id="f3d2d-153">就地新增兩個向量。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-153">In-place adds two vectors.</span></span> |
| `float3& operator-= (float3& value1, float3 const& value2)` | <span data-ttu-id="f3d2d-154">就地從向量減去向量。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-154">In-place subtracts a vector from a vector.</span></span> |
| `float3& operator*= (float3& value1, float3 const& value2)` | <span data-ttu-id="f3d2d-155">就地將兩個向量的元件相乘。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-155">In-place multiplies the components of two vectors by each other.</span></span> |
| `float3& operator*= (float3& value1, float value2)` | <span data-ttu-id="f3d2d-156">就地將向量乘以純量。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-156">In-place multiplies a vector by a scalar.</span></span> |
| `float3& operator/= (float3& value1, float3 const& value2)` | <span data-ttu-id="f3d2d-157">就地將向量的元件除以另一個向量的元件。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-157">In-place divides the components of a vector by the components of another vector.</span></span> |
| `float3& operator/= (float3& value1, float value2)` | <span data-ttu-id="f3d2d-158">就地將向量除以純量值。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-158">In-place divides a vector by a scalar value.</span></span> |
| `bool operator== (float3 const& value1, float3 const& value2)` | <span data-ttu-id="f3d2d-159">判斷兩個 float3 實例是否相等。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-159">Determines whether two instances of float3 are equal.</span></span> |
| `bool operator!= (float3 const& value1, float3 const& value2)` | <span data-ttu-id="f3d2d-160">判斷 float3 的兩個實例是否不相等。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-160">Determines whether two instances of float3 are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector3() const` | <span data-ttu-id="f3d2d-161">將 float3 轉換成 **Vector3** 的格式。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-161">Converts a float3 to a **Microsoft.Graphics.Canvas.Numerics.Vector3**.</span></span> |

## <a name="fields"></a><span data-ttu-id="f3d2d-162">欄位</span><span class="sxs-lookup"><span data-stu-id="f3d2d-162">Fields</span></span>

| <span data-ttu-id="f3d2d-163">名稱</span><span class="sxs-lookup"><span data-stu-id="f3d2d-163">Name</span></span> | <span data-ttu-id="f3d2d-164">描述</span><span class="sxs-lookup"><span data-stu-id="f3d2d-164">Description</span></span> |
|-|-|
| `float x` | <span data-ttu-id="f3d2d-165">向量的 X 元件。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-165">X component of the vector.</span></span> |
| `float y` | <span data-ttu-id="f3d2d-166">向量的 Y 元件。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-166">Y component of the vector.</span></span> |
| `float z` | <span data-ttu-id="f3d2d-167">向量的 Z 元件。</span><span class="sxs-lookup"><span data-stu-id="f3d2d-167">Z component of the vector.</span></span> |

## <a name="requirements"></a><span data-ttu-id="f3d2d-168">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3d2d-168">Requirements</span></span>

| <span data-ttu-id="f3d2d-169">需求</span><span class="sxs-lookup"><span data-stu-id="f3d2d-169">Requirement</span></span> | <span data-ttu-id="f3d2d-170">值</span><span class="sxs-lookup"><span data-stu-id="f3d2d-170">Value</span></span> |
|-|-|
| <span data-ttu-id="f3d2d-171">命名空間</span><span class="sxs-lookup"><span data-stu-id="f3d2d-171">Namespace</span></span> | <span data-ttu-id="f3d2d-172">Windows：： Foundation：：數值</span><span class="sxs-lookup"><span data-stu-id="f3d2d-172">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="f3d2d-173">標頭</span><span class="sxs-lookup"><span data-stu-id="f3d2d-173">Header</span></span> | <dl> <span data-ttu-id="f3d2d-174"><dt>Windowsnumerics。h</dt></span><span class="sxs-lookup"><span data-stu-id="f3d2d-174"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="f3d2d-175">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3d2d-175">See also</span></span>

[<span data-ttu-id="f3d2d-176">windowsnumerics .h Api</span><span class="sxs-lookup"><span data-stu-id="f3d2d-176">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
