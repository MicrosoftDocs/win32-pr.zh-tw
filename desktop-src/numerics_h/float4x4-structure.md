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
ms.openlocfilehash: c918ee81ddac31d697ff3885e04e8cb530cd31a98f842c109f9d281786ee2539
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825268"
---
# <a name="float4x4-structure"></a>float4x4 結構

4x4 矩陣，用於3D 轉換。

此矩陣類型使用資料列向量版面配置。 這個矩陣轉譯向量的 x、y 和 z 對應到欄位 m41、m42、m43。

此類型僅適用于 c + +。 它的 .NET 對等專案是 [Matrix4x4](/dotnet/api/system.numerics.matrix4x4?view=netframework-4.8)。

## <a name="constructors"></a>建構函式

| 名稱 | 描述 |
|-|-|
| `float4x4()` | 建立未初始化的 float4x4。 |
| `float4x4(float m11, float m12, float m13, float m14, float m21, float m22, float m23, float m24, float m31, float m32, float m33, float m34, float m41, float m42, float m43, float m44)` | 使用指定的值建立 float4x4。 |
| `explicit float4x4(float3x2 value)` | 從 float3x2 建立 float4x4。 |
| `float4x4(Microsoft::?Graphics::?Canvas::?Numerics::?Matrix4x4 const& value)` | 將 **Matrix4x4** 轉換成 float4x4 的格式。 |

## <a name="functions"></a>函式

| 名稱 | 描述 |
|-|-|
| `float4x4 make_float4x4_billboard(float3 const& objectPosition, float3 const& cameraPosition, float3 const& cameraUpVector, float3 const& cameraForwardVector)` | 使用右手旋轉的座標系統，建立在指定物件位置周圍旋轉的球形佈告欄。 |
| `float4x4 make_float4x4_?constrained_billboard(float3 const& objectPosition, float3 const& cameraPosition, float3 const& rotateAxis, float3 const& cameraForwardVector, float3 const& objectForwardVector)` | 使用右手座標系統，建立以指定軸旋轉的圓柱佈告欄。 |
| `float4x4 make_float4x4_translation(float3 const& position)` | 建立轉移矩陣。 |
| `float4x4 make_float4x4_translation(float xPosition, float yPosition, float zPosition)` | 建立轉移矩陣。 |
| `float4x4 make_float4x4_scale(float xScale, float yScale, float zScale)` | 建立以原點為中心的縮放矩陣。 |
| `float4x4 make_float4x4_scale(float xScale, float yScale, float zScale, float3 const& centerPoint)` | 建立以指定點為中心的縮放矩陣。 |
| `float4x4 make_float4x4_scale(float3 const& scales)` | 建立以原點為中心的縮放矩陣。 |
| `float4x4 make_float4x4_scale(float3 const& scales, float3 const& centerPoint)` | 建立以指定點為中心的縮放矩陣。 |
| `float4x4 make_float4x4_scale(float scale)` | 建立以原點為中心的縮放矩陣。 |
| `float4x4 make_float4x4_scale(float scale, float3 const& centerPoint)` | 建立以指定點為中心的縮放矩陣。 |
| `float4x4 make_float4x4_rotation_x(float radians)` | 建立以原點為中心的 X 軸旋轉矩陣。 |
| `float4x4 make_float4x4_rotation_x(float radians, float3 const& centerPoint)` | 建立 X 軸旋轉矩陣，並以指定的點為中心。 |
| `float4x4 make_float4x4_rotation_y(float radians)` | 建立以原點為中心的 y 軸旋轉矩陣。 |
| `float4x4 make_float4x4_rotation_y(float radians, float3 const& centerPoint)` | 建立 y 軸旋轉矩陣，並以指定的點為中心。 |
| `float4x4 make_float4x4_rotation_z(float radians)` | 建立以原點為中心的 Z 軸旋轉矩陣。 |
| `float4x4 make_float4x4_rotation_z(float radians, float3 const& centerPoint)` | 建立以指定點為中心的 Z 軸旋轉矩陣。 |
| `float4x4 make_float4x4_from_axis_angle(float3 const& axis, float angle)` | 建立繞著任意向量旋轉的矩陣。 |
| `float4x4 make_float4x4_?perspective_field_of_view(float fieldOfView, float aspectRatio, float nearPlaneDistance, float farPlaneDistance)` | 使用右手座標系統，根據視圖的欄位建立透視圖投影矩陣。 |
| `float4x4 make_float4x4_perspective(float width, float height, float nearPlaneDistance, float farPlaneDistance)` | 使用右手座標系統建立透視圖投影矩陣。 |
| `float4x4 make_float4x4_?perspective_off_center(float left, float right, float bottom, float top, float nearPlaneDistance, float farPlaneDistance)` | 使用右手座標系統建立自訂的透視圖投影矩陣。 |
| `float4x4 make_float4x4_orthographic(float width, float height, float zNearPlane, float zFarPlane)` | 使用右手座標系統建立正向投射矩陣。 |
| `float4x4 make_float4x4_?orthographic_off_center(float left, float right, float bottom, float top, float zNearPlane, float zFarPlane)` | 使用右手座標系統，建立自訂的正交投射矩陣。 |
| `float4x4 make_float4x4_look_at(float3 const& cameraPosition, float3 const& cameraTarget, float3 const& cameraUpVector)` | 使用右手座標系統建立視圖矩陣。 |
| `float4x4 make_float4x4_world(float3 const& position, float3 const& forward, float3 const& up)` | 使用右手座標系統建立世界矩陣。 這可以用來定位3D 空間中的物件。 |
| `float4x4 make_float4x4_?from_quaternion(quaternion const& quaternion)` | 從四元數建立旋轉矩陣。 |
| `float4x4 make_float4x4_?from_yaw_pitch_roll(float yaw, float pitch, float roll)` | 從指定的偏擺、音調和變換建立旋轉矩陣。 |
| `float4x4 make_float4x4_shadow(float3 const& lightDirection, plane const& plane)` | 建立會將幾何簡維成指定平面的矩陣，就像從指定光源投射的陰影一樣。 |
| `float4x4 make_float4x4_reflection(plane const& value)` | 建立反映指定平面之座標系統的矩陣。 |
| `bool is_identity(float4x4 const& value)` | 檢查這是否為識別矩陣。 |
| `float determinant(float4x4 const& value)` | 計算矩陣的行列式。 |
| `float3 translation(float4x4 const& value)` | 取得矩陣的平移向量。 |
| `bool invert(float4x4 const& matrix, _Out_ float4x4* result)` | 計算矩陣的反向。 如果矩陣可以反轉，則傳回 true;否則為 false。 |
| `bool decompose(float4x4 const& matrix, _Out_ float3* scale, _Out_ quaternion* rotation, _Out_ float3* translation)` | 從3D 縮放/旋轉/轉譯 (SRT) 矩陣中解壓縮純量、轉譯和旋轉元件。 如果可以分解矩陣，則傳回 true;否則為 false。 |
| `float4x4 transform(float4x4 const& value, quaternion const& rotation)` | 套用四元數旋轉來轉換矩陣。 |
| `float4x4 transpose(float4x4 const& matrix)` | 沿著矩陣的對角線來調換矩陣的元件。 |
| `float4x4 lerp(float4x4 const& matrix1, float4x4 const& matrix2, float amount)` | 以線性方式在兩個矩陣的對應值之間進行插補。 |

## <a name="methods"></a>方法

| 名稱 | 描述 |
|-|-|
| `static float4x4 identity()` | 傳回識別矩陣的實例。 |

## <a name="operators"></a>運算子

| 名稱 | 描述 |
|-|-|
| `float4x4 operator+ (float4x4 const& value1, float4x4 const& value2)` | 將矩陣的每個元件加入至另一個矩陣。 |
| `float4x4 operator- (float4x4 const& value1, float4x4 const& value2)` | 從另一個矩陣減去矩陣的每個元件。 |
| `float4x4 operator* (float4x4 const& value1, float4x4 const& value2)` | 將矩陣乘以另一個矩陣。 這有串連兩個轉換的效果。 |
| `float4x4 operator* (float4x4 const& value1, float value2)` | 將矩陣的每個元件乘以純量值。 |
| `float4x4 operator- (float4x4 const& value)` | 對矩陣的每個元件進行否定運算。 |
| `float4x4& operator+= (float4x4& value1, float4x4 const& value2)` | 就地將矩陣的每個元件加入至另一個矩陣。 |
| `float4x4& operator-= (float4x4& value1, float4x4 const& value2)` | 就地減去另一個矩陣中矩陣的每個元件。 |
| `float4x4& operator*= (float4x4& value1, float4x4 const& value2)` | 就地將矩陣乘以另一個矩陣。 這有串連兩個轉換的效果。 |
| `float4x4& operator*= (float4x4& value1, float value2)` | 就地將矩陣的每個元件乘以純量值。 |
| `bool operator== (float4x4 const& value1, float4x4 const& value2)` | 判斷兩個 float4x4 實例是否相等。 |
| `bool operator!= (float4x4 const& value1, float4x4 const& value2)` | 判斷 float4x4 的兩個實例是否不相等。 |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Matrix4x4() const` | 將 float4x4 轉換成 **Matrix4x4** 的格式。 |

## <a name="fields"></a>欄位

| 名稱 | 描述 |
|-|-|
| `float m11` | 矩陣的資料列1資料行1的值。 |
| `float m12` | 矩陣的資料列1資料行2上的值。 |
| `float m13` | 矩陣的第1欄第3欄的值。 |
| `float m14` | 矩陣的資料列1資料行4的值。 |
| `float m21` | 矩陣的資料列2資料行1的值。 |
| `float m22` | 矩陣的資料列2資料行2上的值。 |
| `float m23` | 矩陣的資料列2資料行3的值。 |
| `float m24` | 矩陣的資料列2資料行4的值。 |
| `float m31` | 矩陣的第3欄資料行1的值。 |
| `float m32` | 矩陣的第3欄第2欄的值。 |
| `float m33` | 矩陣中第3欄第3欄的值。 |
| `float m34` | 矩陣的第3欄第4欄的值。 |
| `float m41` | 矩陣的資料列4資料行1的值。 |
| `float m42` | 矩陣中第4列第2欄的值。 |
| `float m43` | 矩陣中第4列第3欄的值。 |
| `float m44` | 矩陣的資料列4資料行4的值。 |

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-|-|
| 命名空間 | Windows：： Foundation：：數值 |
| 標頭 | <dl> <dt>Windowsnumerics。h</dt> </dl> |

## <a name="see-also"></a>另請參閱

[windowsnumerics .h Api](windowsnumerics-h-apis-portal.md)
