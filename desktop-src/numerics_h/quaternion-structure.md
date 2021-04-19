---
title: '四元數結構 (Windowsnumerics .h) '
description: 用來表示旋轉的四個維度向量。
ms.assetid: A6B25885-8ECB-4039-9DC6-41D5F3A02489
keywords:
- 四元數結構
topic_type:
- apiref
api_name:
- quaternion structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b56ae169232f83e6753505f9d5d07fffac09e67e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984854"
---
# <a name="quaternion-structure"></a><span data-ttu-id="133c4-104">四元數結構</span><span class="sxs-lookup"><span data-stu-id="133c4-104">quaternion Structure</span></span>

<span data-ttu-id="133c4-105">用來表示旋轉的四個維度向量。</span><span class="sxs-lookup"><span data-stu-id="133c4-105">A four dimensional vector, used to represent a rotation.</span></span>

<span data-ttu-id="133c4-106">四元數可以有效率地將有關 (x，y，z) 向量的物件旋轉為角度 theta，其中 w = cos (theta/2) 。</span><span class="sxs-lookup"><span data-stu-id="133c4-106">A quaternion can efficiently rotate an object about the (x, y, z) vector by the angle theta, where w = cos(theta/2).</span></span> <span data-ttu-id="133c4-107">四元數通常是用來在兩個角度之間平滑插補，以避免歐拉角度可能發生的 gimbal 鎖定問題。</span><span class="sxs-lookup"><span data-stu-id="133c4-107">Quaternions are typically used for smooth interpolation between two angles, and for avoiding the gimbal lock problem that can occur with Euler angles.</span></span>

<span data-ttu-id="133c4-108">此類型僅適用于 c + +。</span><span class="sxs-lookup"><span data-stu-id="133c4-108">This type is available only in C++.</span></span> <span data-ttu-id="133c4-109">它的 .NET 對等[專案是 system.string。](/dotnet/api/system.numerics.quaternion?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="133c4-109">Its .NET equivalent is [System.Numerics.Quaternion](/dotnet/api/system.numerics.quaternion?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="133c4-110">建構函式</span><span class="sxs-lookup"><span data-stu-id="133c4-110">Constructors</span></span>

| <span data-ttu-id="133c4-111">名稱</span><span class="sxs-lookup"><span data-stu-id="133c4-111">Name</span></span> | <span data-ttu-id="133c4-112">描述</span><span class="sxs-lookup"><span data-stu-id="133c4-112">Description</span></span> |
|-|-|
| `quaternion()` | <span data-ttu-id="133c4-113">建立未初始化的四元數。</span><span class="sxs-lookup"><span data-stu-id="133c4-113">Creates an uninitialized quaternion.</span></span> |
| `quaternion(float x, float y, float z, float w)` | <span data-ttu-id="133c4-114">使用指定的值建立四元數。</span><span class="sxs-lookup"><span data-stu-id="133c4-114">Creates a quaternion with the specified values.</span></span> |
| `quaternion(float3 vectorPart, float scalarPart)` | <span data-ttu-id="133c4-115">從 float3 和純量建立四元數。</span><span class="sxs-lookup"><span data-stu-id="133c4-115">Creates a quaternion from a float3 and scalar.</span></span> |
| `quaternion(Microsoft::?Graphics::?Canvas::?Numerics::?Quaternion const& value)` | <span data-ttu-id="133c4-116">將 node.js 的格式 **轉換為四元數。**</span><span class="sxs-lookup"><span data-stu-id="133c4-116">Converts a **Microsoft.Graphics.Canvas.Numerics.Quaternion** to a quaternion.</span></span> |

## <a name="functions"></a><span data-ttu-id="133c4-117">函式</span><span class="sxs-lookup"><span data-stu-id="133c4-117">Functions</span></span>

| <span data-ttu-id="133c4-118">Name</span><span class="sxs-lookup"><span data-stu-id="133c4-118">Name</span></span> | <span data-ttu-id="133c4-119">描述</span><span class="sxs-lookup"><span data-stu-id="133c4-119">Description</span></span> |
|-|-|
| `quaternion make_quaternion_from_axis_angle(float3 const& axis, float angle)` | <span data-ttu-id="133c4-120">從向量和對此向量旋轉的角度建立四元數。</span><span class="sxs-lookup"><span data-stu-id="133c4-120">Creates a quaternion from a vector and an angle to rotate about the vector.</span></span> |
| `quaternion make_quaternion_from_yaw_pitch_roll(float yaw, float pitch, float roll)` | <span data-ttu-id="133c4-121">從指定的偏擺、音調和滾動角度建立四元數。</span><span class="sxs-lookup"><span data-stu-id="133c4-121">Creates a quaternion from specified yaw, pitch, and roll angles.</span></span> |
| `quaternion make_quaternion_from_rotation_matrix(float4x4 const& matrix)` | <span data-ttu-id="133c4-122">從旋轉矩陣建立四元數。</span><span class="sxs-lookup"><span data-stu-id="133c4-122">Creates a quaternion from a rotation matrix.</span></span> |
| `bool is_identity(quaternion const& value)` | <span data-ttu-id="133c4-123">檢查這是否為身分識別 (沒有任何旋轉) 四元數。</span><span class="sxs-lookup"><span data-stu-id="133c4-123">Checks whether this is an identity (no rotation) quaternion.</span></span> |
| `float length(quaternion const& value)` | <span data-ttu-id="133c4-124">計算四元數的長度。</span><span class="sxs-lookup"><span data-stu-id="133c4-124">Calculates the length of a quaternion.</span></span> |
| `float length_squared(quaternion const& value)` | <span data-ttu-id="133c4-125">計算四元數的長度平方。</span><span class="sxs-lookup"><span data-stu-id="133c4-125">Calculates the length squared of a quaternion.</span></span> |
| `float dot(quaternion const& quaternion1, quaternion const& quaternion2)` | <span data-ttu-id="133c4-126">計算兩個四元數的內積。</span><span class="sxs-lookup"><span data-stu-id="133c4-126">Calculates the dot product of two quaternions.</span></span> |
| `quaternion normalize(quaternion const& value)` | <span data-ttu-id="133c4-127">將四元數的每個元件除以四元數的長度。</span><span class="sxs-lookup"><span data-stu-id="133c4-127">Divides each component of a quaternion by the length of the quaternion.</span></span> |
| `quaternion conjugate(quaternion const& value)` | <span data-ttu-id="133c4-128">計算四元數的共軛。</span><span class="sxs-lookup"><span data-stu-id="133c4-128">Calculates the conjugate of a quaternion.</span></span> |
| `quaternion inverse(quaternion const& value)` | <span data-ttu-id="133c4-129">計算四元數的反向。</span><span class="sxs-lookup"><span data-stu-id="133c4-129">Calculates the inverse of a quaternion.</span></span> |
| `quaternion slerp(quaternion const& quaternion1, quaternion const& quaternion2, float amount)` | <span data-ttu-id="133c4-130">使用球面線性插補，在兩個四元數間進行插補。</span><span class="sxs-lookup"><span data-stu-id="133c4-130">Interpolates between two quaternions, using spherical linear interpolation.</span></span> |
| `quaternion lerp(quaternion const& quaternion1, quaternion const& quaternion2, float amount)` | <span data-ttu-id="133c4-131">在兩個四元數之間的線性插補。</span><span class="sxs-lookup"><span data-stu-id="133c4-131">Linearly interpolates between two quaternions.</span></span> |
| `quaternion concatenate(quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="133c4-132">串連兩個四元數;結果代表第一個旋轉，後面接著第二個旋轉。</span><span class="sxs-lookup"><span data-stu-id="133c4-132">Concatenates two quaternions; the result represents the first rotation followed by the second rotation.</span></span> |

## <a name="methods"></a><span data-ttu-id="133c4-133">方法</span><span class="sxs-lookup"><span data-stu-id="133c4-133">Methods</span></span>

| <span data-ttu-id="133c4-134">名稱</span><span class="sxs-lookup"><span data-stu-id="133c4-134">Name</span></span> | <span data-ttu-id="133c4-135">描述</span><span class="sxs-lookup"><span data-stu-id="133c4-135">Description</span></span> |
|-|-|
| `static quaternion identity()` | <span data-ttu-id="133c4-136">傳回識別四元數的實例。</span><span class="sxs-lookup"><span data-stu-id="133c4-136">Returns an instance of the identity quaternion.</span></span> |

## <a name="operators"></a><span data-ttu-id="133c4-137">運算子</span><span class="sxs-lookup"><span data-stu-id="133c4-137">Operators</span></span>

| <span data-ttu-id="133c4-138">Name</span><span class="sxs-lookup"><span data-stu-id="133c4-138">Name</span></span> | <span data-ttu-id="133c4-139">描述</span><span class="sxs-lookup"><span data-stu-id="133c4-139">Description</span></span> |
|-|-|
| `quaternion operator+ (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="133c4-140">加入兩個四元數。</span><span class="sxs-lookup"><span data-stu-id="133c4-140">Adds two quaternions.</span></span> |
| `quaternion operator- (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="133c4-141">從另一個四元數減去四元數。</span><span class="sxs-lookup"><span data-stu-id="133c4-141">Subtracts a quaternion from another quaternion.</span></span> |
| `quaternion operator* (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="133c4-142">將四元數乘以另一個四元數。</span><span class="sxs-lookup"><span data-stu-id="133c4-142">Multiplies a quaternion by another quaternion.</span></span> |
| `quaternion operator* (quaternion const& value1, float value2)` | <span data-ttu-id="133c4-143">將四元數乘以純量值。</span><span class="sxs-lookup"><span data-stu-id="133c4-143">Multiplies a quaternion by a scalar value.</span></span> |
| `quaternion operator/ (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="133c4-144">將四元數除以另一個四元數。</span><span class="sxs-lookup"><span data-stu-id="133c4-144">Divides a quaternion by another quaternion.</span></span> |
| `quaternion operator- (quaternion const& value)` | <span data-ttu-id="133c4-145">翻轉四元數的每個元件的正負號。</span><span class="sxs-lookup"><span data-stu-id="133c4-145">Flips the sign of each component of the quaternion.</span></span> |
| `quaternion& operator+= (quaternion& value1, quaternion const& value2)` | <span data-ttu-id="133c4-146">就地新增兩個四元數。</span><span class="sxs-lookup"><span data-stu-id="133c4-146">In-place adds two quaternions.</span></span> |
| `quaternion& operator-= (quaternion& value1, quaternion const& value2)` | <span data-ttu-id="133c4-147">就地減去另一個四元數的四元數。</span><span class="sxs-lookup"><span data-stu-id="133c4-147">In-place subtracts a quaternion from another quaternion.</span></span> |
| `quaternion& operator*= (quaternion& value1, quaternion const& value2)` | <span data-ttu-id="133c4-148">就地將四元數乘以另一個四元數。</span><span class="sxs-lookup"><span data-stu-id="133c4-148">In-place multiplies a quaternion by another quaternion.</span></span> |
| `quaternion& operator*= (quaternion& value1, float value2)` | <span data-ttu-id="133c4-149">就地 nultiplies 具有純量值的四元數。</span><span class="sxs-lookup"><span data-stu-id="133c4-149">In-place nultiplies a quaternion by a scalar value.</span></span> |
| `quaternion& operator/= (quaternion& value1, quaternion const& value2)` | <span data-ttu-id="133c4-150">就地將四元數除以另一個四元數。</span><span class="sxs-lookup"><span data-stu-id="133c4-150">In-place divides a quaternion by another quaternion.</span></span> |
| `bool operator== (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="133c4-151">判斷四元數的兩個實例是否相等。</span><span class="sxs-lookup"><span data-stu-id="133c4-151">Determines whether two instances of quaternion are equal.</span></span> |
| `bool operator!= (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="133c4-152">判斷四元數的兩個實例是否不相等。</span><span class="sxs-lookup"><span data-stu-id="133c4-152">Determines whether two instances of quaternion are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Quaternion() const` | <span data-ttu-id="133c4-153">Converts a quaternion to a **Microsoft.Graphics.Canvas.Numerics.Quaternion**.</span><span class="sxs-lookup"><span data-stu-id="133c4-153">Converts a quaternion to a **Microsoft.Graphics.Canvas.Numerics.Quaternion**.</span></span> |

## <a name="fields"></a><span data-ttu-id="133c4-154">欄位</span><span class="sxs-lookup"><span data-stu-id="133c4-154">Fields</span></span>

| <span data-ttu-id="133c4-155">名稱</span><span class="sxs-lookup"><span data-stu-id="133c4-155">Name</span></span> | <span data-ttu-id="133c4-156">描述</span><span class="sxs-lookup"><span data-stu-id="133c4-156">Description</span></span> |
|-|-|
| `float x` | <span data-ttu-id="133c4-157">四元數之向量元件的 X 值。</span><span class="sxs-lookup"><span data-stu-id="133c4-157">X value of the vector component of the quaternion.</span></span> |
| `float y` | <span data-ttu-id="133c4-158">四元數之向量元件的 Y 值。</span><span class="sxs-lookup"><span data-stu-id="133c4-158">Y value of the vector component of the quaternion.</span></span> |
| `float z` | <span data-ttu-id="133c4-159">四元數之向量元件的 Z 值。</span><span class="sxs-lookup"><span data-stu-id="133c4-159">Z value of the vector component of the quaternion.</span></span> |
| `float w` | <span data-ttu-id="133c4-160">四元數的旋轉元件。</span><span class="sxs-lookup"><span data-stu-id="133c4-160">Rotation component of the quaternion.</span></span> |

## <a name="requirements"></a><span data-ttu-id="133c4-161">規格需求</span><span class="sxs-lookup"><span data-stu-id="133c4-161">Requirements</span></span>

| <span data-ttu-id="133c4-162">需求</span><span class="sxs-lookup"><span data-stu-id="133c4-162">Requirement</span></span> | <span data-ttu-id="133c4-163">值</span><span class="sxs-lookup"><span data-stu-id="133c4-163">Value</span></span> |
|-|-|
| <span data-ttu-id="133c4-164">命名空間</span><span class="sxs-lookup"><span data-stu-id="133c4-164">Namespace</span></span> | <span data-ttu-id="133c4-165">Windows：： Foundation：：數值</span><span class="sxs-lookup"><span data-stu-id="133c4-165">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="133c4-166">標頭</span><span class="sxs-lookup"><span data-stu-id="133c4-166">Header</span></span> | <dl> <span data-ttu-id="133c4-167"><dt>Windowsnumerics。h</dt></span><span class="sxs-lookup"><span data-stu-id="133c4-167"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="133c4-168">另請參閱</span><span class="sxs-lookup"><span data-stu-id="133c4-168">See also</span></span>

[<span data-ttu-id="133c4-169">windowsnumerics .h Api</span><span class="sxs-lookup"><span data-stu-id="133c4-169">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
