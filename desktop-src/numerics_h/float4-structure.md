---
title: 'float4 結構 (Windowsnumerics .h) '
description: 具有四個元件的向量。
ms.assetid: AC07C6D0-E7FD-4582-B40D-4838F49FB8B4
keywords:
- float4 結構
topic_type:
- apiref
api_name:
- float4 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c4a2a4721e3ab7e5520545b42367d2432ba967f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984756"
---
# <a name="float4-structure"></a><span data-ttu-id="d998b-104">float4 結構</span><span class="sxs-lookup"><span data-stu-id="d998b-104">float4 structure</span></span>

<span data-ttu-id="d998b-105">具有四個元件的向量。</span><span class="sxs-lookup"><span data-stu-id="d998b-105">A vector with four components.</span></span>

<span data-ttu-id="d998b-106">此類型僅適用于 c + +。</span><span class="sxs-lookup"><span data-stu-id="d998b-106">This type is available only in C++.</span></span> <span data-ttu-id="d998b-107">它的 .NET 對等專案是 [Vector4](/dotnet/api/system.numerics.vector4?view=netframework-4.8)。</span><span class="sxs-lookup"><span data-stu-id="d998b-107">Its .NET equivalent is [System.Numerics.Vector4](/dotnet/api/system.numerics.vector4?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="d998b-108">建構函式</span><span class="sxs-lookup"><span data-stu-id="d998b-108">Constructors</span></span>

| <span data-ttu-id="d998b-109">名稱</span><span class="sxs-lookup"><span data-stu-id="d998b-109">Name</span></span> | <span data-ttu-id="d998b-110">描述</span><span class="sxs-lookup"><span data-stu-id="d998b-110">Description</span></span> |
|-|-|
| `float4()` | <span data-ttu-id="d998b-111">建立未初始化的 float4。</span><span class="sxs-lookup"><span data-stu-id="d998b-111">Creates an uninitialized float4.</span></span> |
| `float4(float x, float y, float z, float w)` | <span data-ttu-id="d998b-112">使用指定的值建立 float4。</span><span class="sxs-lookup"><span data-stu-id="d998b-112">Creates a float4 with the specified values.</span></span> |
| `float4(float2 value, float z, float w)` | <span data-ttu-id="d998b-113">建立 float4，其 x 和 y 是從 float2 加上指定的 z 和 w 值複製而來。</span><span class="sxs-lookup"><span data-stu-id="d998b-113">Creates a float4 with x and y copied from a float2 plus the specified z and w values.</span></span> |
| `float4(float3 value, float w)` | <span data-ttu-id="d998b-114">建立 float4，其 x、y 和 z 是從 float3 加上指定的 w 值所複製。</span><span class="sxs-lookup"><span data-stu-id="d998b-114">Creates a float4 with x, y and z copied from a float3 plus the specified w value.</span></span> |
| `explicit float4(float value)` | <span data-ttu-id="d998b-115">建立 float4，並將所有的 ents 設定為指定的值。</span><span class="sxs-lookup"><span data-stu-id="d998b-115">Creates a float4 with all com.ents set to the specified value.</span></span> |
| `float4(Microsoft::?Graphics::?Canvas::?Numerics::?Vector4 const& value)` | <span data-ttu-id="d998b-116">將 **Vector4** 轉換成 float4 的格式。</span><span class="sxs-lookup"><span data-stu-id="d998b-116">Converts a **Microsoft.Graphics.Canvas.Numerics.Vector4** to a float4.</span></span> |

## <a name="functions"></a><span data-ttu-id="d998b-117">函式</span><span class="sxs-lookup"><span data-stu-id="d998b-117">Functions</span></span>

| <span data-ttu-id="d998b-118">Name</span><span class="sxs-lookup"><span data-stu-id="d998b-118">Name</span></span> | <span data-ttu-id="d998b-119">描述</span><span class="sxs-lookup"><span data-stu-id="d998b-119">Description</span></span> |
|-|-|
| `float length(float4 const& value)` | <span data-ttu-id="d998b-120">計算向量的長度（或 Euclidean 距離）。</span><span class="sxs-lookup"><span data-stu-id="d998b-120">Calculates the length, or Euclidean distance, of the vector.</span></span> |
| `float length_squared(float4 const& value)` | <span data-ttu-id="d998b-121">計算向量平方的長度（或 Euclidean 距離）。</span><span class="sxs-lookup"><span data-stu-id="d998b-121">Calculates the length, or Euclidean distance, of the vector squared.</span></span> |
| `float distance(float4 const& value1, float4 const& value2)` | <span data-ttu-id="d998b-122">計算兩個向量之間的 Euclidean 距離。</span><span class="sxs-lookup"><span data-stu-id="d998b-122">Calculates the Euclidean distance between two vectors.</span></span> |
| `float distance_squared(float4 const& value1, float4 const& value2)` | <span data-ttu-id="d998b-123">計算兩個向量平方之間的 Euclidean 距離。</span><span class="sxs-lookup"><span data-stu-id="d998b-123">Calculates the Euclidean distance between two vectors squared.</span></span> |
| `float dot(float4 const& vector1, float4 const& vector2)` | <span data-ttu-id="d998b-124">計算兩個向量的點乘積。</span><span class="sxs-lookup"><span data-stu-id="d998b-124">Calculates the dot product of two vectors.</span></span> |
| `float4 normalize(float4 const& vector)` | <span data-ttu-id="d998b-125">從指定的向量建立單元向量。</span><span class="sxs-lookup"><span data-stu-id="d998b-125">Creates a unit vector from the specified vector.</span></span> |
| `float4 min(float4 const& value1, float4 const& value2)` | <span data-ttu-id="d998b-126">傳回向量，其中包含每個相符元件配對的最小值。</span><span class="sxs-lookup"><span data-stu-id="d998b-126">Returns a vector that contains the lowest value from each matching pair of components.</span></span> |
| `float4 max(float4 const& value1, float4 const& value2)` | <span data-ttu-id="d998b-127">傳回向量，其中包含每個相符元件的最高值。</span><span class="sxs-lookup"><span data-stu-id="d998b-127">Returns a vector that contains the highest value from each matching pair of components.</span></span> |
| `float4 clamp(float4 const& value1, float4 const& min, float4 const& max)` | <span data-ttu-id="d998b-128">將值限制在指定的範圍內。</span><span class="sxs-lookup"><span data-stu-id="d998b-128">Restricts a value to be within a specified range.</span></span> |
| `float4 lerp(float4 const& value1, float4 const& value2, float amount)` | <span data-ttu-id="d998b-129">在兩個向量之間執行線性插補。</span><span class="sxs-lookup"><span data-stu-id="d998b-129">Performs a linear interpolation between two vectors.</span></span> |
| `float4 transform(float4 const& vector, float4x4 const& matrix)` | <span data-ttu-id="d998b-130">依指定的矩陣轉換 float4。</span><span class="sxs-lookup"><span data-stu-id="d998b-130">Transforms a float4 by the given matrix.</span></span> |
| `float4 transform4(float3 const& position, float4x4 const& matrix)` | <span data-ttu-id="d998b-131">依指定的矩陣轉換 float3，傳回 float4。</span><span class="sxs-lookup"><span data-stu-id="d998b-131">Transforms a float3 by the given matrix, returning a float4.</span></span> |
| `float4 transform4(float2 const& position, float4x4 const& matrix)` | <span data-ttu-id="d998b-132">依指定的矩陣轉換 float2，傳回 float4。</span><span class="sxs-lookup"><span data-stu-id="d998b-132">Transforms a float2 by the given matrix, returning a float4.</span></span> |
| `float4 transform(float4 const& value, quaternion const& rotation)` | <span data-ttu-id="d998b-133">依據指定的四元數來轉換 float4。</span><span class="sxs-lookup"><span data-stu-id="d998b-133">Transforms a float4 by the given quaternion.</span></span> |
| `float4 transform4(float3 const& value, quaternion const& rotation)` | <span data-ttu-id="d998b-134">依指定的四元數轉換 float3，傳回 float4。</span><span class="sxs-lookup"><span data-stu-id="d998b-134">Transforms a float3 by the given quaternion, returning a float4.</span></span> |
| `float4 transform4(float2 const& value, quaternion const& rotation)` | <span data-ttu-id="d998b-135">依指定的四元數轉換 float2，傳回 float4。</span><span class="sxs-lookup"><span data-stu-id="d998b-135">Transforms a float2 by the given quaternion, returning a float4.</span></span> |

## <a name="methods"></a><span data-ttu-id="d998b-136">方法</span><span class="sxs-lookup"><span data-stu-id="d998b-136">Methods</span></span>

| <span data-ttu-id="d998b-137">名稱</span><span class="sxs-lookup"><span data-stu-id="d998b-137">Name</span></span> | <span data-ttu-id="d998b-138">描述</span><span class="sxs-lookup"><span data-stu-id="d998b-138">Description</span></span> |
|-|-|
| `static float4 zero()` | <span data-ttu-id="d998b-139">傳回 float4，其中所有的元件都設為零。</span><span class="sxs-lookup"><span data-stu-id="d998b-139">Returns a float4 with all of its components set to zero.</span></span> |
| `static float4 one()` | <span data-ttu-id="d998b-140">傳回 float4，其中所有的元件都設為1。</span><span class="sxs-lookup"><span data-stu-id="d998b-140">Returns a float4 with all of its components set to one.</span></span> |
| `static float4 unit_x()` | <span data-ttu-id="d998b-141">傳回 float4 (1，0，0，0) 。</span><span class="sxs-lookup"><span data-stu-id="d998b-141">Returns the float4 (1, 0, 0, 0).</span></span> |
| `static float4 unit_y()` | <span data-ttu-id="d998b-142">傳回 float4 (0，1，0，0) 。</span><span class="sxs-lookup"><span data-stu-id="d998b-142">Returns the float4 (0, 1, 0, 0).</span></span> |
| `static float4 unit_z()` | <span data-ttu-id="d998b-143">傳回 float4 (0，0，1，0) 。</span><span class="sxs-lookup"><span data-stu-id="d998b-143">Returns the float4 (0, 0, 1, 0).</span></span> |
| `static float4 unit_w()` | <span data-ttu-id="d998b-144">傳回 float4 (0、0、0、1) 。</span><span class="sxs-lookup"><span data-stu-id="d998b-144">Returns the float4 (0, 0, 0, 1).</span></span> |

## <a name="operators"></a><span data-ttu-id="d998b-145">運算子</span><span class="sxs-lookup"><span data-stu-id="d998b-145">Operators</span></span>

| <span data-ttu-id="d998b-146">Name</span><span class="sxs-lookup"><span data-stu-id="d998b-146">Name</span></span> | <span data-ttu-id="d998b-147">描述</span><span class="sxs-lookup"><span data-stu-id="d998b-147">Description</span></span> |
|-|-|
| `float4 operator+ (float4 const& value1, float4 const& value2)` | <span data-ttu-id="d998b-148">新增兩個向量。</span><span class="sxs-lookup"><span data-stu-id="d998b-148">Adds two vectors.</span></span> |
| `float4 operator- (float4 const& value1, float4 const& value2)` | <span data-ttu-id="d998b-149">從向量減去向量。</span><span class="sxs-lookup"><span data-stu-id="d998b-149">Subtracts a vector from a vector.</span></span> |
| `float4 operator* (float4 const& value1, float4 const& value2)` | <span data-ttu-id="d998b-150">將兩個向量的元件相乘。</span><span class="sxs-lookup"><span data-stu-id="d998b-150">Multiplies the components of two vectors by each other.</span></span> |
| `float4 operator* (float4 const& value1, float value2)` | <span data-ttu-id="d998b-151">將向量乘以純量。</span><span class="sxs-lookup"><span data-stu-id="d998b-151">Multiplies a vector by a scalar.</span></span> |
| `float4 operator* (float value1, float4 const& value2)` | <span data-ttu-id="d998b-152">將向量乘以純量。</span><span class="sxs-lookup"><span data-stu-id="d998b-152">Multiplies a vector by a scalar.</span></span> |
| `float4 operator/ (float4 const& value1, float4 const& value2)` | <span data-ttu-id="d998b-153">將向量的元件除以另一個向量的元件。</span><span class="sxs-lookup"><span data-stu-id="d998b-153">Divides the components of a vector by the components of another vector.</span></span> |
| `float4 operator/ (float4 const& value1, float value2)` | <span data-ttu-id="d998b-154">將向量除以純量值。</span><span class="sxs-lookup"><span data-stu-id="d998b-154">Divides a vector by a scalar value.</span></span> |
| `float4 operator- (float4 const& value)` | <span data-ttu-id="d998b-155">傳回指向相反方向的向量。</span><span class="sxs-lookup"><span data-stu-id="d998b-155">Returns a vector pointing in the opposite direction.</span></span> |
| `float4& operator+= (float4& value1, float4 const& value2)` | <span data-ttu-id="d998b-156">就地新增兩個向量。</span><span class="sxs-lookup"><span data-stu-id="d998b-156">In-place adds two vectors.</span></span> |
| `float4& operator-= (float4& value1, float4 const& value2)` | <span data-ttu-id="d998b-157">就地從向量減去向量。</span><span class="sxs-lookup"><span data-stu-id="d998b-157">In-place subtracts a vector from a vector.</span></span> |
| `float4& operator*= (float4& value1, float4 const& value2)` | <span data-ttu-id="d998b-158">就地將兩個向量的元件相乘。</span><span class="sxs-lookup"><span data-stu-id="d998b-158">In-place multiplies the components of two vectors by each other.</span></span> |
| `float4& operator*= (float4& value1, float value2)` | <span data-ttu-id="d998b-159">就地將向量乘以純量。</span><span class="sxs-lookup"><span data-stu-id="d998b-159">In-place multiplies a vector by a scalar.</span></span> |
| `float4& operator/= (float4& value1, float4 const& value2)` | <span data-ttu-id="d998b-160">就地將向量的元件除以另一個向量的元件。</span><span class="sxs-lookup"><span data-stu-id="d998b-160">In-place divides the components of a vector by the components of another vector.</span></span> |
| `float4& operator/= (float4& value1, float value2)` | <span data-ttu-id="d998b-161">就地將向量除以純量值。</span><span class="sxs-lookup"><span data-stu-id="d998b-161">In-place divides a vector by a scalar value.</span></span> |
| `bool operator== (float4 const& value1, float4 const& value2)` | <span data-ttu-id="d998b-162">判斷兩個 float4 實例是否相等。</span><span class="sxs-lookup"><span data-stu-id="d998b-162">Determines whether two instances of float4 are equal.</span></span> |
| `bool operator!= (float4 const& value1, float4 const& value2)` | <span data-ttu-id="d998b-163">判斷 float4 的兩個實例是否不相等。</span><span class="sxs-lookup"><span data-stu-id="d998b-163">Determines whether two instances of float4 are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector4() const` | <span data-ttu-id="d998b-164">將 float4 轉換成 **Vector4** 的格式。</span><span class="sxs-lookup"><span data-stu-id="d998b-164">Converts a float4 to a **Microsoft.Graphics.Canvas.Numerics.Vector4**.</span></span> |

## <a name="fields"></a><span data-ttu-id="d998b-165">欄位</span><span class="sxs-lookup"><span data-stu-id="d998b-165">Fields</span></span>

| <span data-ttu-id="d998b-166">名稱</span><span class="sxs-lookup"><span data-stu-id="d998b-166">Name</span></span> | <span data-ttu-id="d998b-167">描述</span><span class="sxs-lookup"><span data-stu-id="d998b-167">Description</span></span> |
|-|-|
| `float x` | <span data-ttu-id="d998b-168">向量的 X 元件。</span><span class="sxs-lookup"><span data-stu-id="d998b-168">X component of the vector.</span></span> |
| `float y` | <span data-ttu-id="d998b-169">向量的 Y 元件。</span><span class="sxs-lookup"><span data-stu-id="d998b-169">Y component of the vector.</span></span> |
| `float z` | <span data-ttu-id="d998b-170">向量的 Z 元件。</span><span class="sxs-lookup"><span data-stu-id="d998b-170">Z component of the vector.</span></span> |
| `float w` | <span data-ttu-id="d998b-171">向量的 W 元件。</span><span class="sxs-lookup"><span data-stu-id="d998b-171">W component of the vector.</span></span> |

## <a name="requirements"></a><span data-ttu-id="d998b-172">規格需求</span><span class="sxs-lookup"><span data-stu-id="d998b-172">Requirements</span></span>

| <span data-ttu-id="d998b-173">需求</span><span class="sxs-lookup"><span data-stu-id="d998b-173">Requirement</span></span> | <span data-ttu-id="d998b-174">值</span><span class="sxs-lookup"><span data-stu-id="d998b-174">Value</span></span> |
|-|-|
| <span data-ttu-id="d998b-175">命名空間</span><span class="sxs-lookup"><span data-stu-id="d998b-175">Namespace</span></span> | <span data-ttu-id="d998b-176">Windows：： Foundation：：數值</span><span class="sxs-lookup"><span data-stu-id="d998b-176">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="d998b-177">標頭</span><span class="sxs-lookup"><span data-stu-id="d998b-177">Header</span></span> | <dl> <span data-ttu-id="d998b-178"><dt>Windowsnumerics。h</dt></span><span class="sxs-lookup"><span data-stu-id="d998b-178"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="d998b-179">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d998b-179">See also</span></span>

[<span data-ttu-id="d998b-180">windowsnumerics .h Api</span><span class="sxs-lookup"><span data-stu-id="d998b-180">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
