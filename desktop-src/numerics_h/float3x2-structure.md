---
title: 'float3x2 結構 (Windowsnumerics .h) '
description: 用於2D 轉換的3x2 矩陣。
ms.assetid: 5C2A4C30-3EC4-4DE9-A42A-6A19F96F8D69
keywords:
- float3x2 結構
topic_type:
- apiref
api_name:
- float3x2 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9351fae9636ca2512825c7df5383eddf1558583e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991009"
---
# <a name="float3x2-structure"></a><span data-ttu-id="05d5d-104">float3x2 結構</span><span class="sxs-lookup"><span data-stu-id="05d5d-104">float3x2 structure</span></span>

<span data-ttu-id="05d5d-105">用於2D 轉換的3x2 矩陣。</span><span class="sxs-lookup"><span data-stu-id="05d5d-105">A 3x2 matrix, used for 2D transforms.</span></span>

<span data-ttu-id="05d5d-106">此矩陣類型使用資料列向量版面配置。</span><span class="sxs-lookup"><span data-stu-id="05d5d-106">This matrix type uses a row vector layout.</span></span> <span data-ttu-id="05d5d-107">這個矩陣轉譯向量的 x 和 y 對應到欄位 m31，m32。</span><span class="sxs-lookup"><span data-stu-id="05d5d-107">The x and y of this matrix's translation vector correspond to the fields m31, m32.</span></span>

<span data-ttu-id="05d5d-108">此類型僅適用于 c + +。</span><span class="sxs-lookup"><span data-stu-id="05d5d-108">This type is available only in C++.</span></span> <span data-ttu-id="05d5d-109">它的 .NET 對等專案是 [Matrix3x2](/dotnet/api/system.numerics.matrix3x2?view=netframework-4.8)。</span><span class="sxs-lookup"><span data-stu-id="05d5d-109">Its .NET equivalent is [System.Numerics.Matrix3x2](/dotnet/api/system.numerics.matrix3x2?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="05d5d-110">建構函式</span><span class="sxs-lookup"><span data-stu-id="05d5d-110">Constructors</span></span>

| <span data-ttu-id="05d5d-111">名稱</span><span class="sxs-lookup"><span data-stu-id="05d5d-111">Name</span></span> | <span data-ttu-id="05d5d-112">描述</span><span class="sxs-lookup"><span data-stu-id="05d5d-112">Description</span></span> |
|-|-|
| `float3x2()` | <span data-ttu-id="05d5d-113">建立未初始化的 float3x2。</span><span class="sxs-lookup"><span data-stu-id="05d5d-113">Creates an uninitialized float3x2.</span></span> |
| `float3x2(float m11, float m12, float m21, float m22, float m31, float m32)` | <span data-ttu-id="05d5d-114">使用指定的值建立 float3x2。</span><span class="sxs-lookup"><span data-stu-id="05d5d-114">Creates a float3x2 with the specified values.</span></span> |
| `float3x2(Microsoft::?Graphics::?Canvas::?Numerics::?Matrix3x2 const& value)` | <span data-ttu-id="05d5d-115">將 **Matrix3x2** 轉換成 float3x2 的格式。</span><span class="sxs-lookup"><span data-stu-id="05d5d-115">Converts a **Microsoft.Graphics.Canvas.Numerics.Matrix3x2** to a float3x2.</span></span> |

## <a name="functions"></a><span data-ttu-id="05d5d-116">函式</span><span class="sxs-lookup"><span data-stu-id="05d5d-116">Functions</span></span>

| <span data-ttu-id="05d5d-117">Name</span><span class="sxs-lookup"><span data-stu-id="05d5d-117">Name</span></span> | <span data-ttu-id="05d5d-118">描述</span><span class="sxs-lookup"><span data-stu-id="05d5d-118">Description</span></span> |
|-|-|
| `float3x2 make_float3x2_translation(float2 const& position)` | <span data-ttu-id="05d5d-119">建立轉移矩陣。</span><span class="sxs-lookup"><span data-stu-id="05d5d-119">Creates a translation matrix.</span></span> |
| `float3x2 make_float3x2_translation(float xPosition, float yPosition)` | <span data-ttu-id="05d5d-120">建立轉移矩陣。</span><span class="sxs-lookup"><span data-stu-id="05d5d-120">Creates a translation matrix.</span></span> |
| `float3x2 make_float3x2_scale(float xScale, float yScale)` | <span data-ttu-id="05d5d-121">建立以原點為中心的縮放矩陣。</span><span class="sxs-lookup"><span data-stu-id="05d5d-121">Creates a scaling matrix, centered on the origin.</span></span> |
| `float3x2 make_float3x2_scale(float xScale, float yScale, float2 const& centerPoint)` | <span data-ttu-id="05d5d-122">建立以指定點為中心的縮放矩陣。</span><span class="sxs-lookup"><span data-stu-id="05d5d-122">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float3x2 make_float3x2_scale(float2 const& scales)` | <span data-ttu-id="05d5d-123">建立以原點為中心的縮放矩陣。</span><span class="sxs-lookup"><span data-stu-id="05d5d-123">Creates a scaling matrix, centered on the origin.</span></span> |
| `float3x2 make_float3x2_scale(float2 const& scales, float2 const& centerPoint)` | <span data-ttu-id="05d5d-124">建立以指定點為中心的縮放矩陣。</span><span class="sxs-lookup"><span data-stu-id="05d5d-124">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float3x2 make_float3x2_scale(float scale)` | <span data-ttu-id="05d5d-125">建立以原點為中心的縮放矩陣。</span><span class="sxs-lookup"><span data-stu-id="05d5d-125">Creates a scaling matrix, centered on the origin.</span></span> |
| `float3x2 make_float3x2_scale(float scale, float2 const& centerPoint)` | <span data-ttu-id="05d5d-126">建立以指定點為中心的縮放矩陣。</span><span class="sxs-lookup"><span data-stu-id="05d5d-126">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float3x2 make_float3x2_skew(float radiansX, float radiansY)` | <span data-ttu-id="05d5d-127">建立以原點為中心的扭曲矩陣。</span><span class="sxs-lookup"><span data-stu-id="05d5d-127">Creates a skew matrix, centered on the origin.</span></span> |
| `float3x2 make_float3x2_skew(float radiansX, float radiansY, float2 const& centerPoint)` | <span data-ttu-id="05d5d-128">建立以指定點為中心的扭曲矩陣。</span><span class="sxs-lookup"><span data-stu-id="05d5d-128">Creates a skew matrix, centered on the specified point.</span></span> |
| `float3x2 make_float3x2_rotation(float radians)` | <span data-ttu-id="05d5d-129">建立以原點為中心的旋轉矩陣。</span><span class="sxs-lookup"><span data-stu-id="05d5d-129">Creates a rotation matrix, centered on the origin.</span></span> |
| `float3x2 make_float3x2_rotation(float radians, float2 const& centerPoint)` | <span data-ttu-id="05d5d-130">建立以指定點為中心的旋轉矩陣。</span><span class="sxs-lookup"><span data-stu-id="05d5d-130">Creates a rotation matrix, centered on the specified point.</span></span> |
| `bool is_identity(float3x2 const& value)` | <span data-ttu-id="05d5d-131">檢查這是否為識別矩陣。</span><span class="sxs-lookup"><span data-stu-id="05d5d-131">Checks whether this is an identity matrix.</span></span> |
| `float determinant(float3x2 const& value)` | <span data-ttu-id="05d5d-132">計算矩陣的行列式。</span><span class="sxs-lookup"><span data-stu-id="05d5d-132">Calculates the determinant of the matrix.</span></span> |
| `float2 translation(float3x2 const& value)` | <span data-ttu-id="05d5d-133">取得矩陣的平移向量。</span><span class="sxs-lookup"><span data-stu-id="05d5d-133">Gets the translation vector of the matrix.</span></span> |
| `bool invert(float3x2 const& matrix, _Out_ float3x2* result)` | <span data-ttu-id="05d5d-134">計算矩陣的反向。</span><span class="sxs-lookup"><span data-stu-id="05d5d-134">Calculates the inverse of a matrix.</span></span> <span data-ttu-id="05d5d-135">如果矩陣可以反轉，則傳回 true;否則為 false。</span><span class="sxs-lookup"><span data-stu-id="05d5d-135">Returns true if the matrix can be inverted; false otherwise.</span></span> |
| `float3x2 lerp(float3x2 const& matrix1, float3x2 const& matrix2, float amount)` | <span data-ttu-id="05d5d-136">以線性方式在兩個矩陣的對應值之間進行插補。</span><span class="sxs-lookup"><span data-stu-id="05d5d-136">Linearly interpolates between the corresponding values of two matrices.</span></span> |

## <a name="methods"></a><span data-ttu-id="05d5d-137">方法</span><span class="sxs-lookup"><span data-stu-id="05d5d-137">Methods</span></span>

| <span data-ttu-id="05d5d-138">名稱</span><span class="sxs-lookup"><span data-stu-id="05d5d-138">Name</span></span> | <span data-ttu-id="05d5d-139">描述</span><span class="sxs-lookup"><span data-stu-id="05d5d-139">Description</span></span> |
|-|-|
| `static float3x2 identity()` | <span data-ttu-id="05d5d-140">傳回識別矩陣的實例。</span><span class="sxs-lookup"><span data-stu-id="05d5d-140">Returns an instance of the identity matrix.</span></span> |

## <a name="operators"></a><span data-ttu-id="05d5d-141">運算子</span><span class="sxs-lookup"><span data-stu-id="05d5d-141">Operators</span></span>

| <span data-ttu-id="05d5d-142">Name</span><span class="sxs-lookup"><span data-stu-id="05d5d-142">Name</span></span> | <span data-ttu-id="05d5d-143">描述</span><span class="sxs-lookup"><span data-stu-id="05d5d-143">Description</span></span> |
|-|-|
| `float3x2 operator+ (float3x2 const& value1, float3x2 const& value2)` | <span data-ttu-id="05d5d-144">將矩陣的每個元件加入至另一個矩陣。</span><span class="sxs-lookup"><span data-stu-id="05d5d-144">Adds each component of a matrix to another matrix.</span></span> |
| `float3x2 operator- (float3x2 const& value1, float3x2 const& value2)` | <span data-ttu-id="05d5d-145">從另一個矩陣減去矩陣的每個元件。</span><span class="sxs-lookup"><span data-stu-id="05d5d-145">Subtracts each component of a matrix from another matrix.</span></span> |
| `float3x2 operator* (float3x2 const& value1, float3x2 const& value2)` | <span data-ttu-id="05d5d-146">將矩陣乘以另一個矩陣。</span><span class="sxs-lookup"><span data-stu-id="05d5d-146">Multiplies a matrix by another matrix.</span></span> <span data-ttu-id="05d5d-147">這有串連兩個轉換的效果。</span><span class="sxs-lookup"><span data-stu-id="05d5d-147">This has the effect of concatenating two transforms.</span></span> |
| `float3x2 operator* (float3x2 const& value1, float value2)` | <span data-ttu-id="05d5d-148">將矩陣的每個元件乘以純量值。</span><span class="sxs-lookup"><span data-stu-id="05d5d-148">Multiplies each component of a matrix by a scalar value.</span></span> |
| `float3x2 operator- (float3x2 const& value)` | <span data-ttu-id="05d5d-149">對矩陣的每個元件進行否定運算。</span><span class="sxs-lookup"><span data-stu-id="05d5d-149">Negates each component of a matrix.</span></span> |
| `float3x2& operator+= (float3x2& value1, float3x2 const& value2)` | <span data-ttu-id="05d5d-150">就地將矩陣的每個元件加入至另一個矩陣。</span><span class="sxs-lookup"><span data-stu-id="05d5d-150">In-place adds each component of a matrix to another matrix.</span></span> |
| `float3x2& operator-= (float3x2& value1, float3x2 const& value2)` | <span data-ttu-id="05d5d-151">就地減去另一個矩陣中矩陣的每個元件。</span><span class="sxs-lookup"><span data-stu-id="05d5d-151">In-place subtracts each component of a matrix from another matrix.</span></span> |
| `float3x2& operator*= (float3x2& value1, float3x2 const& value2)` | <span data-ttu-id="05d5d-152">就地將矩陣乘以另一個矩陣。</span><span class="sxs-lookup"><span data-stu-id="05d5d-152">In-place multiplies a matrix by another matrix.</span></span> <span data-ttu-id="05d5d-153">這有串連兩個轉換的效果。</span><span class="sxs-lookup"><span data-stu-id="05d5d-153">This has the effect of concatenating two transforms.</span></span> |
| `float3x2& operator*= (float3x2& value1, float value2)` | <span data-ttu-id="05d5d-154">就地將矩陣的每個元件乘以純量值。</span><span class="sxs-lookup"><span data-stu-id="05d5d-154">In-place multiplies each component of a matrix by a scalar value.</span></span> |
| `bool operator== (float3x2 const& value1, float3x2 const& value2)` | <span data-ttu-id="05d5d-155">判斷兩個 float3x2 實例是否相等。</span><span class="sxs-lookup"><span data-stu-id="05d5d-155">Determines whether two instances of float3x2 are equal.</span></span> |
| `bool operator!= (float3x2 const& value1, float3x2 const& value2)` | <span data-ttu-id="05d5d-156">判斷 float3x2 的兩個實例是否不相等。</span><span class="sxs-lookup"><span data-stu-id="05d5d-156">Determines whether two instances of float3x2 are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Matrix3x2() const` | <span data-ttu-id="05d5d-157">將 float3x2 轉換成 **Matrix3x2** 的格式。</span><span class="sxs-lookup"><span data-stu-id="05d5d-157">Converts a float3x2 to a **Microsoft.Graphics.Canvas.Numerics.Matrix3x2**.</span></span> |

## <a name="fields"></a><span data-ttu-id="05d5d-158">欄位</span><span class="sxs-lookup"><span data-stu-id="05d5d-158">Fields</span></span>

| <span data-ttu-id="05d5d-159">名稱</span><span class="sxs-lookup"><span data-stu-id="05d5d-159">Name</span></span> | <span data-ttu-id="05d5d-160">描述</span><span class="sxs-lookup"><span data-stu-id="05d5d-160">Description</span></span> |
|-|-|
| `float m11` | <span data-ttu-id="05d5d-161">矩陣的資料列1資料行1的值。</span><span class="sxs-lookup"><span data-stu-id="05d5d-161">Value at row 1 column 1 of the matrix.</span></span> |
| `float m12` | <span data-ttu-id="05d5d-162">矩陣的資料列1資料行2上的值。</span><span class="sxs-lookup"><span data-stu-id="05d5d-162">Value at row 1 column 2 of the matrix.</span></span> |
| `float m21` | <span data-ttu-id="05d5d-163">矩陣的資料列2資料行1的值。</span><span class="sxs-lookup"><span data-stu-id="05d5d-163">Value at row 2 column 1 of the matrix.</span></span> |
| `float m22` | <span data-ttu-id="05d5d-164">矩陣的資料列2資料行2上的值。</span><span class="sxs-lookup"><span data-stu-id="05d5d-164">Value at row 2 column 2 of the matrix.</span></span> |
| `float m31` | <span data-ttu-id="05d5d-165">矩陣的第3欄資料行1的值。</span><span class="sxs-lookup"><span data-stu-id="05d5d-165">Value at row 3 column 1 of the matrix.</span></span> |
| `float m32` | <span data-ttu-id="05d5d-166">矩陣的第3欄第2欄的值。</span><span class="sxs-lookup"><span data-stu-id="05d5d-166">Value at row 3 column 2 of the matrix.</span></span> |

## <a name="requirements"></a><span data-ttu-id="05d5d-167">規格需求</span><span class="sxs-lookup"><span data-stu-id="05d5d-167">Requirements</span></span>

| <span data-ttu-id="05d5d-168">需求</span><span class="sxs-lookup"><span data-stu-id="05d5d-168">Requirement</span></span> | <span data-ttu-id="05d5d-169">值</span><span class="sxs-lookup"><span data-stu-id="05d5d-169">Value</span></span> |
|-|-|
| <span data-ttu-id="05d5d-170">命名空間</span><span class="sxs-lookup"><span data-stu-id="05d5d-170">Namespace</span></span> | <span data-ttu-id="05d5d-171">Windows：： Foundation：：數值</span><span class="sxs-lookup"><span data-stu-id="05d5d-171">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="05d5d-172">標頭</span><span class="sxs-lookup"><span data-stu-id="05d5d-172">Header</span></span> | <dl> <span data-ttu-id="05d5d-173"><dt>Windowsnumerics。h</dt></span><span class="sxs-lookup"><span data-stu-id="05d5d-173"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="05d5d-174">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05d5d-174">See also</span></span>

[<span data-ttu-id="05d5d-175">windowsnumerics .h Api</span><span class="sxs-lookup"><span data-stu-id="05d5d-175">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
