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
# <a name="float3x2-structure"></a>float3x2 結構

用於2D 轉換的3x2 矩陣。

此矩陣類型使用資料列向量版面配置。 這個矩陣轉譯向量的 x 和 y 對應到欄位 m31，m32。

此類型僅適用于 c + +。 它的 .NET 對等專案是 [Matrix3x2](/dotnet/api/system.numerics.matrix3x2?view=netframework-4.8)。

## <a name="constructors"></a>建構函式

| 名稱 | 描述 |
|-|-|
| `float3x2()` | 建立未初始化的 float3x2。 |
| `float3x2(float m11, float m12, float m21, float m22, float m31, float m32)` | 使用指定的值建立 float3x2。 |
| `float3x2(Microsoft::?Graphics::?Canvas::?Numerics::?Matrix3x2 const& value)` | 將 **Matrix3x2** 轉換成 float3x2 的格式。 |

## <a name="functions"></a>函式

| Name | 描述 |
|-|-|
| `float3x2 make_float3x2_translation(float2 const& position)` | 建立轉移矩陣。 |
| `float3x2 make_float3x2_translation(float xPosition, float yPosition)` | 建立轉移矩陣。 |
| `float3x2 make_float3x2_scale(float xScale, float yScale)` | 建立以原點為中心的縮放矩陣。 |
| `float3x2 make_float3x2_scale(float xScale, float yScale, float2 const& centerPoint)` | 建立以指定點為中心的縮放矩陣。 |
| `float3x2 make_float3x2_scale(float2 const& scales)` | 建立以原點為中心的縮放矩陣。 |
| `float3x2 make_float3x2_scale(float2 const& scales, float2 const& centerPoint)` | 建立以指定點為中心的縮放矩陣。 |
| `float3x2 make_float3x2_scale(float scale)` | 建立以原點為中心的縮放矩陣。 |
| `float3x2 make_float3x2_scale(float scale, float2 const& centerPoint)` | 建立以指定點為中心的縮放矩陣。 |
| `float3x2 make_float3x2_skew(float radiansX, float radiansY)` | 建立以原點為中心的扭曲矩陣。 |
| `float3x2 make_float3x2_skew(float radiansX, float radiansY, float2 const& centerPoint)` | 建立以指定點為中心的扭曲矩陣。 |
| `float3x2 make_float3x2_rotation(float radians)` | 建立以原點為中心的旋轉矩陣。 |
| `float3x2 make_float3x2_rotation(float radians, float2 const& centerPoint)` | 建立以指定點為中心的旋轉矩陣。 |
| `bool is_identity(float3x2 const& value)` | 檢查這是否為識別矩陣。 |
| `float determinant(float3x2 const& value)` | 計算矩陣的行列式。 |
| `float2 translation(float3x2 const& value)` | 取得矩陣的平移向量。 |
| `bool invert(float3x2 const& matrix, _Out_ float3x2* result)` | 計算矩陣的反向。 如果矩陣可以反轉，則傳回 true;否則為 false。 |
| `float3x2 lerp(float3x2 const& matrix1, float3x2 const& matrix2, float amount)` | 以線性方式在兩個矩陣的對應值之間進行插補。 |

## <a name="methods"></a>方法

| 名稱 | 描述 |
|-|-|
| `static float3x2 identity()` | 傳回識別矩陣的實例。 |

## <a name="operators"></a>運算子

| Name | 描述 |
|-|-|
| `float3x2 operator+ (float3x2 const& value1, float3x2 const& value2)` | 將矩陣的每個元件加入至另一個矩陣。 |
| `float3x2 operator- (float3x2 const& value1, float3x2 const& value2)` | 從另一個矩陣減去矩陣的每個元件。 |
| `float3x2 operator* (float3x2 const& value1, float3x2 const& value2)` | 將矩陣乘以另一個矩陣。 這有串連兩個轉換的效果。 |
| `float3x2 operator* (float3x2 const& value1, float value2)` | 將矩陣的每個元件乘以純量值。 |
| `float3x2 operator- (float3x2 const& value)` | 對矩陣的每個元件進行否定運算。 |
| `float3x2& operator+= (float3x2& value1, float3x2 const& value2)` | 就地將矩陣的每個元件加入至另一個矩陣。 |
| `float3x2& operator-= (float3x2& value1, float3x2 const& value2)` | 就地減去另一個矩陣中矩陣的每個元件。 |
| `float3x2& operator*= (float3x2& value1, float3x2 const& value2)` | 就地將矩陣乘以另一個矩陣。 這有串連兩個轉換的效果。 |
| `float3x2& operator*= (float3x2& value1, float value2)` | 就地將矩陣的每個元件乘以純量值。 |
| `bool operator== (float3x2 const& value1, float3x2 const& value2)` | 判斷兩個 float3x2 實例是否相等。 |
| `bool operator!= (float3x2 const& value1, float3x2 const& value2)` | 判斷 float3x2 的兩個實例是否不相等。 |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Matrix3x2() const` | 將 float3x2 轉換成 **Matrix3x2** 的格式。 |

## <a name="fields"></a>欄位

| 名稱 | 描述 |
|-|-|
| `float m11` | 矩陣的資料列1資料行1的值。 |
| `float m12` | 矩陣的資料列1資料行2上的值。 |
| `float m21` | 矩陣的資料列2資料行1的值。 |
| `float m22` | 矩陣的資料列2資料行2上的值。 |
| `float m31` | 矩陣的第3欄資料行1的值。 |
| `float m32` | 矩陣的第3欄第2欄的值。 |

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-|-|
| 命名空間 | Windows：： Foundation：：數值 |
| 標頭 | <dl> <dt>Windowsnumerics。h</dt> </dl> |

## <a name="see-also"></a>另請參閱

[windowsnumerics .h Api](windowsnumerics-h-apis-portal.md)
