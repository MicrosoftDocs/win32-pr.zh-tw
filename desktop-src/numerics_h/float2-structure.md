---
title: 'float2 結構 (Windowsnumerics .h) '
description: 具有兩個元件的向量。
ms.assetid: 1A23C1E3-F34F-4249-80EA-92A13CD4B34F
keywords:
- float2 結構
topic_type:
- apiref
api_name:
- float2 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72398bdc087e0f7a0845703a2cefea40b5465b21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984858"
---
# <a name="float2-structure"></a><span data-ttu-id="5c3ad-104">float2 結構</span><span class="sxs-lookup"><span data-stu-id="5c3ad-104">float2 structure</span></span>

<span data-ttu-id="5c3ad-105">具有兩個元件的向量。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-105">A vector with two components.</span></span>

<span data-ttu-id="5c3ad-106">此類型僅適用于 c + +。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-106">This type is available only in C++.</span></span> <span data-ttu-id="5c3ad-107">它的 .NET 對等專案是 [Vector2](/dotnet/api/system.numerics.vector2?view=netframework-4.8)。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-107">Its .NET equivalent is [System.Numerics.Vector2](/dotnet/api/system.numerics.vector2?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="5c3ad-108">建構函式</span><span class="sxs-lookup"><span data-stu-id="5c3ad-108">Constructors</span></span>

| <span data-ttu-id="5c3ad-109">名稱</span><span class="sxs-lookup"><span data-stu-id="5c3ad-109">Name</span></span> | <span data-ttu-id="5c3ad-110">描述</span><span class="sxs-lookup"><span data-stu-id="5c3ad-110">Description</span></span> |
|-|-|
| `float2()` | <span data-ttu-id="5c3ad-111">建立未初始化的 float2。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-111">Creates an uninitialized float2.</span></span> |
| `float2(float x, float y)` | <span data-ttu-id="5c3ad-112">使用指定的值建立 float2。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-112">Creates a float2 with the specified values.</span></span> |
| `explicit float2(float value)` | <span data-ttu-id="5c3ad-113">建立 float2，並將所有元件設定為指定的值。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-113">Creates a float2 with all components set to the specified value.</span></span> |
| `float2(Microsoft::Graphics::Canvas::Numerics::Vector2 const& value)` | <span data-ttu-id="5c3ad-114">將 **Vector2** 轉換成 float2 的格式。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-114">Converts a **Microsoft.Graphics.Canvas.Numerics.Vector2** to a float2.</span></span> |
| `float2(Windows::Foundation::Point const& value)` | <span data-ttu-id="5c3ad-115">[**將 float2 轉換為**](/uwp/api/Windows.Foundation.Point)。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-115">Converts a [**Windows.Foundation.Point**](/uwp/api/Windows.Foundation.Point) to a float2.</span></span> |
| `float2(Windows::Foundation::Size const& value)` | <span data-ttu-id="5c3ad-116">將 float2 的 [**大小**](/uwp/api/Windows.Foundation.Size) 轉換成。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-116">Converts a [**Windows.Foundation.Size**](/uwp/api/Windows.Foundation.Size) to a float2.</span></span> |

## <a name="functions"></a><span data-ttu-id="5c3ad-117">函式</span><span class="sxs-lookup"><span data-stu-id="5c3ad-117">Functions</span></span>

| <span data-ttu-id="5c3ad-118">Name</span><span class="sxs-lookup"><span data-stu-id="5c3ad-118">Name</span></span> | <span data-ttu-id="5c3ad-119">描述</span><span class="sxs-lookup"><span data-stu-id="5c3ad-119">Description</span></span> |
|-|-|
| `float length(float2 const& value)` | <span data-ttu-id="5c3ad-120">計算向量的長度（或 Euclidean 距離）。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-120">Calculates the length, or Euclidean distance, of the vector.</span></span> |
| `float length_squared(float2 const& value)` | <span data-ttu-id="5c3ad-121">計算向量平方的長度（或 Euclidean 距離）。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-121">Calculates the length, or Euclidean distance, of the vector squared.</span></span> |
| `float distance(float2 const& value1, float2 const& value2)` | <span data-ttu-id="5c3ad-122">計算兩個向量之間的 Euclidean 距離。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-122">Calculates the Euclidean distance between two vectors.</span></span> |
| `float distance_squared(float2 const& value1, float2 const& value2)` | <span data-ttu-id="5c3ad-123">計算兩個向量平方之間的 Euclidean 距離。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-123">Calculates the Euclidean distance between two vectors squared.</span></span> |
| `float dot(float2 const& value1, float2 const& value2)` | <span data-ttu-id="5c3ad-124">計算兩個向量的點乘積。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-124">Calculates the dot product of two vectors.</span></span> |
| `float2 normalize(float2 const& value)` | <span data-ttu-id="5c3ad-125">從指定的向量建立單元向量。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-125">Creates a unit vector from the specified vector.</span></span> |
| `float2 reflect(float2 const& vector, float2 const& normal)` | <span data-ttu-id="5c3ad-126">決定給定向量和一般的反映向量。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-126">Determines the reflect vector of the given vector and normal.</span></span> |
| `float2 min(float2 const& value1, float2 const& value2)` | <span data-ttu-id="5c3ad-127">傳回向量，其中包含每個相符元件配對的最小值。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-127">Returns a vector that contains the lowest value from each matching pair of components.</span></span> |
| `float2 max(float2 const& value1, float2 const& value2)` | <span data-ttu-id="5c3ad-128">傳回向量，其中包含每個相符元件的最高值。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-128">Returns a vector that contains the highest value from each matching pair of components.</span></span> |
| `float2 clamp(float2 const& value1, float2 const& min, float2 const& max)` | <span data-ttu-id="5c3ad-129">將值限制在指定的範圍內。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-129">Restricts a value to be within a specified range.</span></span> |
| `float2 lerp(float2 const& value1, float2 const& value2, float amount)` | <span data-ttu-id="5c3ad-130">在兩個向量之間執行線性插補。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-130">Performs a linear interpolation between two vectors.</span></span> |
| `float2 transform(float2 const& position, float3x2 const& matrix)` | <span data-ttu-id="5c3ad-131">將向量 (x、y、0、1) 由指定的矩陣進行轉換。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-131">Transforms the vector (x, y, 0, 1) by the specified matrix.</span></span> |
| `float2 transform(float2 const& position, float4x4 const& matrix)` | <span data-ttu-id="5c3ad-132">將向量 (x、y、0、1) 由指定的矩陣進行轉換。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-132">Transforms the vector (x, y, 0, 1) by the specified matrix.</span></span> |
| `float2 transform_normal(float2 const& normal, float3x2 const& matrix)` | <span data-ttu-id="5c3ad-133">將一般向量 (x、y、0、0) 由指定的矩陣進行轉換。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-133">Transforms the normal vector (x, y, 0, 0) by the specified matrix.</span></span> |
| `float2 transform_normal(float2 const& normal, float4x4 const& matrix)` | <span data-ttu-id="5c3ad-134">將一般向量 (x、y、0、0) 由指定的矩陣進行轉換。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-134">Transforms the normal vector (x, y, 0, 0) by the specified matrix.</span></span> |
| `float2 transform(float2 const& value, quaternion const& rotation)` | <span data-ttu-id="5c3ad-135">依據指定的四元數來轉換 float2。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-135">Transforms a float2 by the given quaternion.</span></span> |

## <a name="methods"></a><span data-ttu-id="5c3ad-136">方法</span><span class="sxs-lookup"><span data-stu-id="5c3ad-136">Methods</span></span>

| <span data-ttu-id="5c3ad-137">名稱</span><span class="sxs-lookup"><span data-stu-id="5c3ad-137">Name</span></span> | <span data-ttu-id="5c3ad-138">描述</span><span class="sxs-lookup"><span data-stu-id="5c3ad-138">Description</span></span> |
|-|-|
| `static float2 zero()` | <span data-ttu-id="5c3ad-139">傳回 float2，其中所有的元件都設為零。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-139">Returns a float2 with all of its components set to zero.</span></span> |
| `static float2 one()` | <span data-ttu-id="5c3ad-140">傳回 float2，其中所有的元件都設為1。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-140">Returns a float2 with all of its components set to one.</span></span> |
| `static float2 unit_x()` | <span data-ttu-id="5c3ad-141">傳回 float2 (1，0) 。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-141">Returns the float2 (1, 0).</span></span> |
| `static float2 unit_y()` | <span data-ttu-id="5c3ad-142">傳回 float2 (0，1) 。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-142">Returns the float2 (0, 1).</span></span> |

## <a name="operators"></a><span data-ttu-id="5c3ad-143">運算子</span><span class="sxs-lookup"><span data-stu-id="5c3ad-143">Operators</span></span>

| <span data-ttu-id="5c3ad-144">Name</span><span class="sxs-lookup"><span data-stu-id="5c3ad-144">Name</span></span> | <span data-ttu-id="5c3ad-145">描述</span><span class="sxs-lookup"><span data-stu-id="5c3ad-145">Description</span></span> |
|-|-|
| `operator Windows::Foundation::Point() const` | <span data-ttu-id="5c3ad-146">將 float2 轉換為 [**Windows. Point**](/uwp/api/Windows.Foundation.Point)。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-146">Converts a float2 to a [**Windows.Foundation.Point**](/uwp/api/Windows.Foundation.Point).</span></span> |
| `operator Windows::Foundation::Size() const` | <span data-ttu-id="5c3ad-147">將 float2 轉換為 [**Windows. 大小**](/uwp/api/Windows.Foundation.Size)。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-147">Converts a float2 to a [**Windows.Foundation.Size**](/uwp/api/Windows.Foundation.Size).</span></span> |
| `float2 operator+ (float2 const& value1, float2 const& value2)` | <span data-ttu-id="5c3ad-148">新增兩個向量。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-148">Adds two vectors.</span></span> |
| `float2 operator- (float2 const& value1, float2 const& value2)` | <span data-ttu-id="5c3ad-149">從向量減去向量。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-149">Subtracts a vector from a vector.</span></span> |
| `float2 operator* (float2 const& value1, float2 const& value2)` | <span data-ttu-id="5c3ad-150">將兩個向量的元件相乘。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-150">Multiplies the components of two vectors by each other.</span></span> |
| `float2 operator* (float2 const& value1, float value2)` | <span data-ttu-id="5c3ad-151">將向量乘以純量。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-151">Multiplies a vector by a scalar.</span></span> |
| `float2 operator* (float value1, float2 const& value2)` | <span data-ttu-id="5c3ad-152">將向量乘以純量。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-152">Multiplies a vector by a scalar.</span></span> |
| `float2 operator/ (float2 const& value1, float2 const& value2)` | <span data-ttu-id="5c3ad-153">將向量的元件除以另一個向量的元件。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-153">Divides the components of a vector by the components of another vector.</span></span> |
| `float2 operator/ (float2 const& value1, float value2)` | <span data-ttu-id="5c3ad-154">將向量除以純量值。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-154">Divides a vector by a scalar value.</span></span> |
| `float2 operator- (float2 const& value)` | <span data-ttu-id="5c3ad-155">傳回指向相反方向的向量。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-155">Returns a vector pointing in the opposite direction.</span></span> |
| `float2& operator+= (float2& value1, float2 const& value2)` | <span data-ttu-id="5c3ad-156">就地新增兩個向量。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-156">In-place adds two vectors.</span></span> |
| `float2& operator-= (float2& value1, float2 const& value2)` | <span data-ttu-id="5c3ad-157">就地從向量減去向量。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-157">In-place subtracts a vector from a vector.</span></span> |
| `float2& operator*= (float2& value1, float2 const& value2)` | <span data-ttu-id="5c3ad-158">就地將兩個向量的元件相乘。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-158">In-place multiplies the components of two vectors by each other.</span></span> |
| `float2& operator*= (float2& value1, float value2)` | <span data-ttu-id="5c3ad-159">就地將向量乘以純量。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-159">In-place multiplies a vector by a scalar.</span></span> |
| `float2& operator/= (float2& value1, float2 const& value2)` | <span data-ttu-id="5c3ad-160">就地將向量的元件除以另一個向量的元件。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-160">In-place divides the components of a vector by the components of another vector.</span></span> |
| `float2& operator/= (float2& value1, float value2)` | <span data-ttu-id="5c3ad-161">就地將向量除以純量值。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-161">In-place divides a vector by a scalar value.</span></span> |
| `bool operator== (float2 const& value1, float2 const& value2)` | <span data-ttu-id="5c3ad-162">判斷兩個 float2 實例是否相等。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-162">Determines whether two instances of float2 are equal.</span></span> |
| `bool operator!= (float2 const& value1, float2 const& value2)` | <span data-ttu-id="5c3ad-163">判斷 float2 的兩個實例是否不相等。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-163">Determines whether two instances of float2 are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector2() const` | <span data-ttu-id="5c3ad-164">將 float2 轉換成 **Vector2** 的格式。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-164">Converts a float2 to a **Microsoft.Graphics.Canvas.Numerics.Vector2**.</span></span> |

## <a name="fields"></a><span data-ttu-id="5c3ad-165">欄位</span><span class="sxs-lookup"><span data-stu-id="5c3ad-165">Fields</span></span>

| <span data-ttu-id="5c3ad-166">名稱</span><span class="sxs-lookup"><span data-stu-id="5c3ad-166">Name</span></span> | <span data-ttu-id="5c3ad-167">描述</span><span class="sxs-lookup"><span data-stu-id="5c3ad-167">Description</span></span> |
|-|-|
| `float x` | <span data-ttu-id="5c3ad-168">向量的 X 元件。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-168">X component of the vector.</span></span> |
| `float y` | <span data-ttu-id="5c3ad-169">向量的 Y 元件。</span><span class="sxs-lookup"><span data-stu-id="5c3ad-169">Y component of the vector.</span></span> |

## <a name="requirements"></a><span data-ttu-id="5c3ad-170">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c3ad-170">Requirements</span></span>

| <span data-ttu-id="5c3ad-171">需求</span><span class="sxs-lookup"><span data-stu-id="5c3ad-171">Requirement</span></span> | <span data-ttu-id="5c3ad-172">值</span><span class="sxs-lookup"><span data-stu-id="5c3ad-172">Value</span></span> |
|-|-|
| <span data-ttu-id="5c3ad-173">命名空間</span><span class="sxs-lookup"><span data-stu-id="5c3ad-173">Namespace</span></span> | <span data-ttu-id="5c3ad-174">Windows：： Foundation：：數值</span><span class="sxs-lookup"><span data-stu-id="5c3ad-174">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="5c3ad-175">標頭</span><span class="sxs-lookup"><span data-stu-id="5c3ad-175">Header</span></span> | <dl> <span data-ttu-id="5c3ad-176"><dt>Windowsnumerics。h</dt></span><span class="sxs-lookup"><span data-stu-id="5c3ad-176"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="5c3ad-177">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c3ad-177">See also</span></span>

[<span data-ttu-id="5c3ad-178">windowsnumerics .h Api</span><span class="sxs-lookup"><span data-stu-id="5c3ad-178">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
