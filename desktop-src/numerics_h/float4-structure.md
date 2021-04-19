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
# <a name="float4-structure"></a>float4 結構

具有四個元件的向量。

此類型僅適用于 c + +。 它的 .NET 對等專案是 [Vector4](/dotnet/api/system.numerics.vector4?view=netframework-4.8)。

## <a name="constructors"></a>建構函式

| 名稱 | 描述 |
|-|-|
| `float4()` | 建立未初始化的 float4。 |
| `float4(float x, float y, float z, float w)` | 使用指定的值建立 float4。 |
| `float4(float2 value, float z, float w)` | 建立 float4，其 x 和 y 是從 float2 加上指定的 z 和 w 值複製而來。 |
| `float4(float3 value, float w)` | 建立 float4，其 x、y 和 z 是從 float3 加上指定的 w 值所複製。 |
| `explicit float4(float value)` | 建立 float4，並將所有的 ents 設定為指定的值。 |
| `float4(Microsoft::?Graphics::?Canvas::?Numerics::?Vector4 const& value)` | 將 **Vector4** 轉換成 float4 的格式。 |

## <a name="functions"></a>函式

| Name | 描述 |
|-|-|
| `float length(float4 const& value)` | 計算向量的長度（或 Euclidean 距離）。 |
| `float length_squared(float4 const& value)` | 計算向量平方的長度（或 Euclidean 距離）。 |
| `float distance(float4 const& value1, float4 const& value2)` | 計算兩個向量之間的 Euclidean 距離。 |
| `float distance_squared(float4 const& value1, float4 const& value2)` | 計算兩個向量平方之間的 Euclidean 距離。 |
| `float dot(float4 const& vector1, float4 const& vector2)` | 計算兩個向量的點乘積。 |
| `float4 normalize(float4 const& vector)` | 從指定的向量建立單元向量。 |
| `float4 min(float4 const& value1, float4 const& value2)` | 傳回向量，其中包含每個相符元件配對的最小值。 |
| `float4 max(float4 const& value1, float4 const& value2)` | 傳回向量，其中包含每個相符元件的最高值。 |
| `float4 clamp(float4 const& value1, float4 const& min, float4 const& max)` | 將值限制在指定的範圍內。 |
| `float4 lerp(float4 const& value1, float4 const& value2, float amount)` | 在兩個向量之間執行線性插補。 |
| `float4 transform(float4 const& vector, float4x4 const& matrix)` | 依指定的矩陣轉換 float4。 |
| `float4 transform4(float3 const& position, float4x4 const& matrix)` | 依指定的矩陣轉換 float3，傳回 float4。 |
| `float4 transform4(float2 const& position, float4x4 const& matrix)` | 依指定的矩陣轉換 float2，傳回 float4。 |
| `float4 transform(float4 const& value, quaternion const& rotation)` | 依據指定的四元數來轉換 float4。 |
| `float4 transform4(float3 const& value, quaternion const& rotation)` | 依指定的四元數轉換 float3，傳回 float4。 |
| `float4 transform4(float2 const& value, quaternion const& rotation)` | 依指定的四元數轉換 float2，傳回 float4。 |

## <a name="methods"></a>方法

| 名稱 | 描述 |
|-|-|
| `static float4 zero()` | 傳回 float4，其中所有的元件都設為零。 |
| `static float4 one()` | 傳回 float4，其中所有的元件都設為1。 |
| `static float4 unit_x()` | 傳回 float4 (1，0，0，0) 。 |
| `static float4 unit_y()` | 傳回 float4 (0，1，0，0) 。 |
| `static float4 unit_z()` | 傳回 float4 (0，0，1，0) 。 |
| `static float4 unit_w()` | 傳回 float4 (0、0、0、1) 。 |

## <a name="operators"></a>運算子

| Name | 描述 |
|-|-|
| `float4 operator+ (float4 const& value1, float4 const& value2)` | 新增兩個向量。 |
| `float4 operator- (float4 const& value1, float4 const& value2)` | 從向量減去向量。 |
| `float4 operator* (float4 const& value1, float4 const& value2)` | 將兩個向量的元件相乘。 |
| `float4 operator* (float4 const& value1, float value2)` | 將向量乘以純量。 |
| `float4 operator* (float value1, float4 const& value2)` | 將向量乘以純量。 |
| `float4 operator/ (float4 const& value1, float4 const& value2)` | 將向量的元件除以另一個向量的元件。 |
| `float4 operator/ (float4 const& value1, float value2)` | 將向量除以純量值。 |
| `float4 operator- (float4 const& value)` | 傳回指向相反方向的向量。 |
| `float4& operator+= (float4& value1, float4 const& value2)` | 就地新增兩個向量。 |
| `float4& operator-= (float4& value1, float4 const& value2)` | 就地從向量減去向量。 |
| `float4& operator*= (float4& value1, float4 const& value2)` | 就地將兩個向量的元件相乘。 |
| `float4& operator*= (float4& value1, float value2)` | 就地將向量乘以純量。 |
| `float4& operator/= (float4& value1, float4 const& value2)` | 就地將向量的元件除以另一個向量的元件。 |
| `float4& operator/= (float4& value1, float value2)` | 就地將向量除以純量值。 |
| `bool operator== (float4 const& value1, float4 const& value2)` | 判斷兩個 float4 實例是否相等。 |
| `bool operator!= (float4 const& value1, float4 const& value2)` | 判斷 float4 的兩個實例是否不相等。 |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector4() const` | 將 float4 轉換成 **Vector4** 的格式。 |

## <a name="fields"></a>欄位

| 名稱 | 描述 |
|-|-|
| `float x` | 向量的 X 元件。 |
| `float y` | 向量的 Y 元件。 |
| `float z` | 向量的 Z 元件。 |
| `float w` | 向量的 W 元件。 |

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-|-|
| 命名空間 | Windows：： Foundation：：數值 |
| 標頭 | <dl> <dt>Windowsnumerics。h</dt> </dl> |

## <a name="see-also"></a>另請參閱

[windowsnumerics .h Api](windowsnumerics-h-apis-portal.md)
