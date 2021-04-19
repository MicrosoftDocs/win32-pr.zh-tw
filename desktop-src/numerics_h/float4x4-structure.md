---
title: 'float4x4 結構 (Windowsnumerics .h) '
description: 4x4 矩陣，用於3D 轉換。
ms.assetid: C0D2198A-B547-4153-AD02-9A47835FD272
keywords:
- float4x4 結構
topic_type:
- apiref
api_name:
- float4x4 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71c91de5eef404db33eff118568540be912d551d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999707"
---
# <a name="float4x4-structure"></a><span data-ttu-id="08fa0-104">float4x4 結構</span><span class="sxs-lookup"><span data-stu-id="08fa0-104">float4x4 structure</span></span>

<span data-ttu-id="08fa0-105">4x4 矩陣，用於3D 轉換。</span><span class="sxs-lookup"><span data-stu-id="08fa0-105">A 4x4 matrix, used for 3D transforms.</span></span>

<span data-ttu-id="08fa0-106">此矩陣類型使用資料列向量版面配置。</span><span class="sxs-lookup"><span data-stu-id="08fa0-106">This matrix type uses a row vector layout.</span></span> <span data-ttu-id="08fa0-107">這個矩陣轉譯向量的 x、y 和 z 對應到欄位 m41、m42、m43。</span><span class="sxs-lookup"><span data-stu-id="08fa0-107">The x, y, and z of this matrix's translation vector correspond to the fields m41, m42, m43.</span></span>

<span data-ttu-id="08fa0-108">此類型僅適用于 c + +。</span><span class="sxs-lookup"><span data-stu-id="08fa0-108">This type is available only in C++.</span></span> <span data-ttu-id="08fa0-109">它的 .NET 對等專案是 [Matrix4x4](/dotnet/api/system.numerics.matrix4x4?view=netframework-4.8)。</span><span class="sxs-lookup"><span data-stu-id="08fa0-109">Its .NET equivalent is [System.Numerics.Matrix4x4](/dotnet/api/system.numerics.matrix4x4?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="08fa0-110">建構函式</span><span class="sxs-lookup"><span data-stu-id="08fa0-110">Constructors</span></span>

| <span data-ttu-id="08fa0-111">名稱</span><span class="sxs-lookup"><span data-stu-id="08fa0-111">Name</span></span> | <span data-ttu-id="08fa0-112">描述</span><span class="sxs-lookup"><span data-stu-id="08fa0-112">Description</span></span> |
|-|-|
| `float4x4()` | <span data-ttu-id="08fa0-113">建立未初始化的 float4x4。</span><span class="sxs-lookup"><span data-stu-id="08fa0-113">Creates an uninitialized float4x4.</span></span> |
| `float4x4(float m11, float m12, float m13, float m14, float m21, float m22, float m23, float m24, float m31, float m32, float m33, float m34, float m41, float m42, float m43, float m44)` | <span data-ttu-id="08fa0-114">使用指定的值建立 float4x4。</span><span class="sxs-lookup"><span data-stu-id="08fa0-114">Creates a float4x4 with the specified values.</span></span> |
| `explicit float4x4(float3x2 value)` | <span data-ttu-id="08fa0-115">從 float3x2 建立 float4x4。</span><span class="sxs-lookup"><span data-stu-id="08fa0-115">Creates a float4x4 from a float3x2.</span></span> |
| `float4x4(Microsoft::?Graphics::?Canvas::?Numerics::?Matrix4x4 const& value)` | <span data-ttu-id="08fa0-116">將 **Matrix4x4** 轉換成 float4x4 的格式。</span><span class="sxs-lookup"><span data-stu-id="08fa0-116">Converts a **Microsoft.Graphics.Canvas.Numerics.Matrix4x4** to a float4x4.</span></span> |

## <a name="functions"></a><span data-ttu-id="08fa0-117">函式</span><span class="sxs-lookup"><span data-stu-id="08fa0-117">Functions</span></span>

| <span data-ttu-id="08fa0-118">Name</span><span class="sxs-lookup"><span data-stu-id="08fa0-118">Name</span></span> | <span data-ttu-id="08fa0-119">描述</span><span class="sxs-lookup"><span data-stu-id="08fa0-119">Description</span></span> |
|-|-|
| `float4x4 make_float4x4_billboard(float3 const& objectPosition, float3 const& cameraPosition, float3 const& cameraUpVector, float3 const& cameraForwardVector)` | <span data-ttu-id="08fa0-120">使用右手旋轉的座標系統，建立在指定物件位置周圍旋轉的球形佈告欄。</span><span class="sxs-lookup"><span data-stu-id="08fa0-120">Creates a spherical billboard that rotates around a specified object position, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_?constrained_billboard(float3 const& objectPosition, float3 const& cameraPosition, float3 const& rotateAxis, float3 const& cameraForwardVector, float3 const& objectForwardVector)` | <span data-ttu-id="08fa0-121">使用右手座標系統，建立以指定軸旋轉的圓柱佈告欄。</span><span class="sxs-lookup"><span data-stu-id="08fa0-121">Creates a cylindrical billboard that rotates around a specified axis, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_translation(float3 const& position)` | <span data-ttu-id="08fa0-122">建立轉移矩陣。</span><span class="sxs-lookup"><span data-stu-id="08fa0-122">Creates a translation matrix.</span></span> |
| `float4x4 make_float4x4_translation(float xPosition, float yPosition, float zPosition)` | <span data-ttu-id="08fa0-123">建立轉移矩陣。</span><span class="sxs-lookup"><span data-stu-id="08fa0-123">Creates a translation matrix.</span></span> |
| `float4x4 make_float4x4_scale(float xScale, float yScale, float zScale)` | <span data-ttu-id="08fa0-124">建立以原點為中心的縮放矩陣。</span><span class="sxs-lookup"><span data-stu-id="08fa0-124">Creates a scaling matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_scale(float xScale, float yScale, float zScale, float3 const& centerPoint)` | <span data-ttu-id="08fa0-125">建立以指定點為中心的縮放矩陣。</span><span class="sxs-lookup"><span data-stu-id="08fa0-125">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_scale(float3 const& scales)` | <span data-ttu-id="08fa0-126">建立以原點為中心的縮放矩陣。</span><span class="sxs-lookup"><span data-stu-id="08fa0-126">Creates a scaling matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_scale(float3 const& scales, float3 const& centerPoint)` | <span data-ttu-id="08fa0-127">建立以指定點為中心的縮放矩陣。</span><span class="sxs-lookup"><span data-stu-id="08fa0-127">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_scale(float scale)` | <span data-ttu-id="08fa0-128">建立以原點為中心的縮放矩陣。</span><span class="sxs-lookup"><span data-stu-id="08fa0-128">Creates a scaling matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_scale(float scale, float3 const& centerPoint)` | <span data-ttu-id="08fa0-129">建立以指定點為中心的縮放矩陣。</span><span class="sxs-lookup"><span data-stu-id="08fa0-129">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_rotation_x(float radians)` | <span data-ttu-id="08fa0-130">建立以原點為中心的 X 軸旋轉矩陣。</span><span class="sxs-lookup"><span data-stu-id="08fa0-130">Creates an x-axis rotation matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_rotation_x(float radians, float3 const& centerPoint)` | <span data-ttu-id="08fa0-131">建立 X 軸旋轉矩陣，並以指定的點為中心。</span><span class="sxs-lookup"><span data-stu-id="08fa0-131">Creates an x-axis rotation matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_rotation_y(float radians)` | <span data-ttu-id="08fa0-132">建立以原點為中心的 y 軸旋轉矩陣。</span><span class="sxs-lookup"><span data-stu-id="08fa0-132">Creates a y-axis rotation matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_rotation_y(float radians, float3 const& centerPoint)` | <span data-ttu-id="08fa0-133">建立 y 軸旋轉矩陣，並以指定的點為中心。</span><span class="sxs-lookup"><span data-stu-id="08fa0-133">Creates a y-axis rotation matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_rotation_z(float radians)` | <span data-ttu-id="08fa0-134">建立以原點為中心的 Z 軸旋轉矩陣。</span><span class="sxs-lookup"><span data-stu-id="08fa0-134">Creates a z-axis rotation matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_rotation_z(float radians, float3 const& centerPoint)` | <span data-ttu-id="08fa0-135">建立以指定點為中心的 Z 軸旋轉矩陣。</span><span class="sxs-lookup"><span data-stu-id="08fa0-135">Creates a z-axis rotation matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_from_axis_angle(float3 const& axis, float angle)` | <span data-ttu-id="08fa0-136">建立繞著任意向量旋轉的矩陣。</span><span class="sxs-lookup"><span data-stu-id="08fa0-136">Creates a matrix that rotates around an arbitrary vector.</span></span> |
| `float4x4 make_float4x4_?perspective_field_of_view(float fieldOfView, float aspectRatio, float nearPlaneDistance, float farPlaneDistance)` | <span data-ttu-id="08fa0-137">使用右手座標系統，根據視圖的欄位建立透視圖投影矩陣。</span><span class="sxs-lookup"><span data-stu-id="08fa0-137">Creates a perspective projection matrix based on a field of view, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_perspective(float width, float height, float nearPlaneDistance, float farPlaneDistance)` | <span data-ttu-id="08fa0-138">使用右手座標系統建立透視圖投影矩陣。</span><span class="sxs-lookup"><span data-stu-id="08fa0-138">Creates a perspective projection matrix, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_?perspective_off_center(float left, float right, float bottom, float top, float nearPlaneDistance, float farPlaneDistance)` | <span data-ttu-id="08fa0-139">使用右手座標系統建立自訂的透視圖投影矩陣。</span><span class="sxs-lookup"><span data-stu-id="08fa0-139">Creates a customized perspective projection matrix, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_orthographic(float width, float height, float zNearPlane, float zFarPlane)` | <span data-ttu-id="08fa0-140">使用右手座標系統建立正向投射矩陣。</span><span class="sxs-lookup"><span data-stu-id="08fa0-140">Creates an orthographic projection matrix, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_?orthographic_off_center(float left, float right, float bottom, float top, float zNearPlane, float zFarPlane)` | <span data-ttu-id="08fa0-141">使用右手座標系統，建立自訂的正交投射矩陣。</span><span class="sxs-lookup"><span data-stu-id="08fa0-141">Creates a customized orthographic projection matrix, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_look_at(float3 const& cameraPosition, float3 const& cameraTarget, float3 const& cameraUpVector)` | <span data-ttu-id="08fa0-142">使用右手座標系統建立視圖矩陣。</span><span class="sxs-lookup"><span data-stu-id="08fa0-142">Creates a view matrix, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_world(float3 const& position, float3 const& forward, float3 const& up)` | <span data-ttu-id="08fa0-143">使用右手座標系統建立世界矩陣。</span><span class="sxs-lookup"><span data-stu-id="08fa0-143">Creates a world matrix, using a right handed coordinate system.</span></span> <span data-ttu-id="08fa0-144">這可以用來定位3D 空間中的物件。</span><span class="sxs-lookup"><span data-stu-id="08fa0-144">This can be used to position objects in 3D space.</span></span> |
| `float4x4 make_float4x4_?from_quaternion(quaternion const& quaternion)` | <span data-ttu-id="08fa0-145">從四元數建立旋轉矩陣。</span><span class="sxs-lookup"><span data-stu-id="08fa0-145">Creates a rotation matrix from a quaternion.</span></span> |
| `float4x4 make_float4x4_?from_yaw_pitch_roll(float yaw, float pitch, float roll)` | <span data-ttu-id="08fa0-146">從指定的偏擺、音調和變換建立旋轉矩陣。</span><span class="sxs-lookup"><span data-stu-id="08fa0-146">Creates a rotation matrix from a specified yaw, pitch, and roll.</span></span> |
| `float4x4 make_float4x4_shadow(float3 const& lightDirection, plane const& plane)` | <span data-ttu-id="08fa0-147">建立會將幾何簡維成指定平面的矩陣，就像從指定光源投射的陰影一樣。</span><span class="sxs-lookup"><span data-stu-id="08fa0-147">Creates a matrix that flattens geometry into a specified plane as if casting a shadow from a specified light source.</span></span> |
| `float4x4 make_float4x4_reflection(plane const& value)` | <span data-ttu-id="08fa0-148">建立反映指定平面之座標系統的矩陣。</span><span class="sxs-lookup"><span data-stu-id="08fa0-148">Creates a matrix that reflects the coordinate system about a specified plane.</span></span> |
| `bool is_identity(float4x4 const& value)` | <span data-ttu-id="08fa0-149">檢查這是否為識別矩陣。</span><span class="sxs-lookup"><span data-stu-id="08fa0-149">Checks whether this is an identity matrix.</span></span> |
| `float determinant(float4x4 const& value)` | <span data-ttu-id="08fa0-150">計算矩陣的行列式。</span><span class="sxs-lookup"><span data-stu-id="08fa0-150">Calculates the determinant of the matrix.</span></span> |
| `float3 translation(float4x4 const& value)` | <span data-ttu-id="08fa0-151">取得矩陣的平移向量。</span><span class="sxs-lookup"><span data-stu-id="08fa0-151">Gets the translation vector of the matrix.</span></span> |
| `bool invert(float4x4 const& matrix, _Out_ float4x4* result)` | <span data-ttu-id="08fa0-152">計算矩陣的反向。</span><span class="sxs-lookup"><span data-stu-id="08fa0-152">Calculates the inverse of a matrix.</span></span> <span data-ttu-id="08fa0-153">如果矩陣可以反轉，則傳回 true;否則為 false。</span><span class="sxs-lookup"><span data-stu-id="08fa0-153">Returns true if the matrix can be inverted; false otherwise.</span></span> |
| `bool decompose(float4x4 const& matrix, _Out_ float3* scale, _Out_ quaternion* rotation, _Out_ float3* translation)` | <span data-ttu-id="08fa0-154">從3D 縮放/旋轉/轉譯 (SRT) 矩陣中解壓縮純量、轉譯和旋轉元件。</span><span class="sxs-lookup"><span data-stu-id="08fa0-154">Extracts the scalar, translation, and rotation components from a 3D scale/rotate/translate (SRT) matrix.</span></span> <span data-ttu-id="08fa0-155">如果可以分解矩陣，則傳回 true;否則為 false。</span><span class="sxs-lookup"><span data-stu-id="08fa0-155">Returns true if the matrix can be decomposed; false otherwise.</span></span> |
| `float4x4 transform(float4x4 const& value, quaternion const& rotation)` | <span data-ttu-id="08fa0-156">套用四元數旋轉來轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="08fa0-156">Transforms a matrix by applying a quaternion rotation.</span></span> |
| `float4x4 transpose(float4x4 const& matrix)` | <span data-ttu-id="08fa0-157">沿著矩陣的對角線來調換矩陣的元件。</span><span class="sxs-lookup"><span data-stu-id="08fa0-157">Transposes the components of a matrix along its diagonal.</span></span> |
| `float4x4 lerp(float4x4 const& matrix1, float4x4 const& matrix2, float amount)` | <span data-ttu-id="08fa0-158">以線性方式在兩個矩陣的對應值之間進行插補。</span><span class="sxs-lookup"><span data-stu-id="08fa0-158">Linearly interpolates between the corresponding values of two matrices.</span></span> |

## <a name="methods"></a><span data-ttu-id="08fa0-159">方法</span><span class="sxs-lookup"><span data-stu-id="08fa0-159">Methods</span></span>

| <span data-ttu-id="08fa0-160">名稱</span><span class="sxs-lookup"><span data-stu-id="08fa0-160">Name</span></span> | <span data-ttu-id="08fa0-161">描述</span><span class="sxs-lookup"><span data-stu-id="08fa0-161">Description</span></span> |
|-|-|
| `static float4x4 identity()` | <span data-ttu-id="08fa0-162">傳回識別矩陣的實例。</span><span class="sxs-lookup"><span data-stu-id="08fa0-162">Returns an instance of the identity matrix.</span></span> |

## <a name="operators"></a><span data-ttu-id="08fa0-163">運算子</span><span class="sxs-lookup"><span data-stu-id="08fa0-163">Operators</span></span>

| <span data-ttu-id="08fa0-164">Name</span><span class="sxs-lookup"><span data-stu-id="08fa0-164">Name</span></span> | <span data-ttu-id="08fa0-165">描述</span><span class="sxs-lookup"><span data-stu-id="08fa0-165">Description</span></span> |
|-|-|
| `float4x4 operator+ (float4x4 const& value1, float4x4 const& value2)` | <span data-ttu-id="08fa0-166">將矩陣的每個元件加入至另一個矩陣。</span><span class="sxs-lookup"><span data-stu-id="08fa0-166">Adds each component of a matrix to another matrix.</span></span> |
| `float4x4 operator- (float4x4 const& value1, float4x4 const& value2)` | <span data-ttu-id="08fa0-167">從另一個矩陣減去矩陣的每個元件。</span><span class="sxs-lookup"><span data-stu-id="08fa0-167">Subtracts each component of a matrix from another matrix.</span></span> |
| `float4x4 operator* (float4x4 const& value1, float4x4 const& value2)` | <span data-ttu-id="08fa0-168">將矩陣乘以另一個矩陣。</span><span class="sxs-lookup"><span data-stu-id="08fa0-168">Multiplies a matrix by another matrix.</span></span> <span data-ttu-id="08fa0-169">這有串連兩個轉換的效果。</span><span class="sxs-lookup"><span data-stu-id="08fa0-169">This has the effect of concatenating two transforms.</span></span> |
| `float4x4 operator* (float4x4 const& value1, float value2)` | <span data-ttu-id="08fa0-170">將矩陣的每個元件乘以純量值。</span><span class="sxs-lookup"><span data-stu-id="08fa0-170">Multiplies each component of a matrix by a scalar value.</span></span> |
| `float4x4 operator- (float4x4 const& value)` | <span data-ttu-id="08fa0-171">對矩陣的每個元件進行否定運算。</span><span class="sxs-lookup"><span data-stu-id="08fa0-171">Negates each component of a matrix.</span></span> |
| `float4x4& operator+= (float4x4& value1, float4x4 const& value2)` | <span data-ttu-id="08fa0-172">就地將矩陣的每個元件加入至另一個矩陣。</span><span class="sxs-lookup"><span data-stu-id="08fa0-172">In-place adds each component of a matrix to another matrix.</span></span> |
| `float4x4& operator-= (float4x4& value1, float4x4 const& value2)` | <span data-ttu-id="08fa0-173">就地減去另一個矩陣中矩陣的每個元件。</span><span class="sxs-lookup"><span data-stu-id="08fa0-173">In-place subtracts each component of a matrix from another matrix.</span></span> |
| `float4x4& operator*= (float4x4& value1, float4x4 const& value2)` | <span data-ttu-id="08fa0-174">就地將矩陣乘以另一個矩陣。</span><span class="sxs-lookup"><span data-stu-id="08fa0-174">In-place multiplies a matrix by another matrix.</span></span> <span data-ttu-id="08fa0-175">這有串連兩個轉換的效果。</span><span class="sxs-lookup"><span data-stu-id="08fa0-175">This has the effect of concatenating two transforms.</span></span> |
| `float4x4& operator*= (float4x4& value1, float value2)` | <span data-ttu-id="08fa0-176">就地將矩陣的每個元件乘以純量值。</span><span class="sxs-lookup"><span data-stu-id="08fa0-176">In-place multiplies each component of a matrix by a scalar value.</span></span> |
| `bool operator== (float4x4 const& value1, float4x4 const& value2)` | <span data-ttu-id="08fa0-177">判斷兩個 float4x4 實例是否相等。</span><span class="sxs-lookup"><span data-stu-id="08fa0-177">Determines whether two instances of float4x4 are equal.</span></span> |
| `bool operator!= (float4x4 const& value1, float4x4 const& value2)` | <span data-ttu-id="08fa0-178">判斷 float4x4 的兩個實例是否不相等。</span><span class="sxs-lookup"><span data-stu-id="08fa0-178">Determines whether two instances of float4x4 are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Matrix4x4() const` | <span data-ttu-id="08fa0-179">將 float4x4 轉換成 **Matrix4x4** 的格式。</span><span class="sxs-lookup"><span data-stu-id="08fa0-179">Converts a float4x4 to a **Microsoft.Graphics.Canvas.Numerics.Matrix4x4**.</span></span> |

## <a name="fields"></a><span data-ttu-id="08fa0-180">欄位</span><span class="sxs-lookup"><span data-stu-id="08fa0-180">Fields</span></span>

| <span data-ttu-id="08fa0-181">名稱</span><span class="sxs-lookup"><span data-stu-id="08fa0-181">Name</span></span> | <span data-ttu-id="08fa0-182">描述</span><span class="sxs-lookup"><span data-stu-id="08fa0-182">Description</span></span> |
|-|-|
| `float m11` | <span data-ttu-id="08fa0-183">矩陣的資料列1資料行1的值。</span><span class="sxs-lookup"><span data-stu-id="08fa0-183">Value at row 1 column 1 of the matrix.</span></span> |
| `float m12` | <span data-ttu-id="08fa0-184">矩陣的資料列1資料行2上的值。</span><span class="sxs-lookup"><span data-stu-id="08fa0-184">Value at row 1 column 2 of the matrix.</span></span> |
| `float m13` | <span data-ttu-id="08fa0-185">矩陣的第1欄第3欄的值。</span><span class="sxs-lookup"><span data-stu-id="08fa0-185">Value at row 1 column 3 of the matrix.</span></span> |
| `float m14` | <span data-ttu-id="08fa0-186">矩陣的資料列1資料行4的值。</span><span class="sxs-lookup"><span data-stu-id="08fa0-186">Value at row 1 column 4 of the matrix.</span></span> |
| `float m21` | <span data-ttu-id="08fa0-187">矩陣的資料列2資料行1的值。</span><span class="sxs-lookup"><span data-stu-id="08fa0-187">Value at row 2 column 1 of the matrix.</span></span> |
| `float m22` | <span data-ttu-id="08fa0-188">矩陣的資料列2資料行2上的值。</span><span class="sxs-lookup"><span data-stu-id="08fa0-188">Value at row 2 column 2 of the matrix.</span></span> |
| `float m23` | <span data-ttu-id="08fa0-189">矩陣的資料列2資料行3的值。</span><span class="sxs-lookup"><span data-stu-id="08fa0-189">Value at row 2 column 3 of the matrix.</span></span> |
| `float m24` | <span data-ttu-id="08fa0-190">矩陣的資料列2資料行4的值。</span><span class="sxs-lookup"><span data-stu-id="08fa0-190">Value at row 2 column 4 of the matrix.</span></span> |
| `float m31` | <span data-ttu-id="08fa0-191">矩陣的第3欄資料行1的值。</span><span class="sxs-lookup"><span data-stu-id="08fa0-191">Value at row 3 column 1 of the matrix.</span></span> |
| `float m32` | <span data-ttu-id="08fa0-192">矩陣的第3欄第2欄的值。</span><span class="sxs-lookup"><span data-stu-id="08fa0-192">Value at row 3 column 2 of the matrix.</span></span> |
| `float m33` | <span data-ttu-id="08fa0-193">矩陣中第3欄第3欄的值。</span><span class="sxs-lookup"><span data-stu-id="08fa0-193">Value at row 3 column 3 of the matrix.</span></span> |
| `float m34` | <span data-ttu-id="08fa0-194">矩陣的第3欄第4欄的值。</span><span class="sxs-lookup"><span data-stu-id="08fa0-194">Value at row 3 column 4 of the matrix.</span></span> |
| `float m41` | <span data-ttu-id="08fa0-195">矩陣的資料列4資料行1的值。</span><span class="sxs-lookup"><span data-stu-id="08fa0-195">Value at row 4 column 1 of the matrix.</span></span> |
| `float m42` | <span data-ttu-id="08fa0-196">矩陣中第4列第2欄的值。</span><span class="sxs-lookup"><span data-stu-id="08fa0-196">Value at row 4 column 2 of the matrix.</span></span> |
| `float m43` | <span data-ttu-id="08fa0-197">矩陣中第4列第3欄的值。</span><span class="sxs-lookup"><span data-stu-id="08fa0-197">Value at row 4 column 3 of the matrix.</span></span> |
| `float m44` | <span data-ttu-id="08fa0-198">矩陣的資料列4資料行4的值。</span><span class="sxs-lookup"><span data-stu-id="08fa0-198">Value at row 4 column 4 of the matrix.</span></span> |

## <a name="requirements"></a><span data-ttu-id="08fa0-199">規格需求</span><span class="sxs-lookup"><span data-stu-id="08fa0-199">Requirements</span></span>

| <span data-ttu-id="08fa0-200">需求</span><span class="sxs-lookup"><span data-stu-id="08fa0-200">Requirement</span></span> | <span data-ttu-id="08fa0-201">值</span><span class="sxs-lookup"><span data-stu-id="08fa0-201">Value</span></span> |
|-|-|
| <span data-ttu-id="08fa0-202">命名空間</span><span class="sxs-lookup"><span data-stu-id="08fa0-202">Namespace</span></span> | <span data-ttu-id="08fa0-203">Windows：： Foundation：：數值</span><span class="sxs-lookup"><span data-stu-id="08fa0-203">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="08fa0-204">標頭</span><span class="sxs-lookup"><span data-stu-id="08fa0-204">Header</span></span> | <dl> <span data-ttu-id="08fa0-205"><dt>Windowsnumerics。h</dt></span><span class="sxs-lookup"><span data-stu-id="08fa0-205"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="08fa0-206">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08fa0-206">See also</span></span>

[<span data-ttu-id="08fa0-207">windowsnumerics .h Api</span><span class="sxs-lookup"><span data-stu-id="08fa0-207">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
