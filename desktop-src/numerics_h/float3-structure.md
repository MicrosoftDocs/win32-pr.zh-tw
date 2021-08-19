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
ms.openlocfilehash: 521c63f99c35e68f18d9a6c0a81118f647ff131effb0f6528e2ef3882c43e234
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939509"
---
# <a name="float3-structure"></a>float3 結構

具有三個元件的向量。

此類型僅適用于 c + +。 它的 .NET 對等專案是 [Vector3](/dotnet/api/system.numerics.vector3?view=netframework-4.8)。

## <a name="constructors"></a>建構函式

| 名稱 | 描述 |
|-|-|
| `float3()` | 建立未初始化的 float3。 |
| `float3(float x, float y, float z)` | 使用指定的值建立 float3。 |
| `float3(float2 value, float z)` | 建立 float3，其 x 和 y 是從 float2 加上指定的 z 值複製而來。 |
| `explicit float3(float value)` | 建立 float3，並將所有元件設定為指定的值。 |
| `float3(Microsoft::Graphics::Canvas::Numerics::Vector3 const& value)` | 將 **Vector3** 轉換成 float3 的格式。 |

## <a name="functions"></a>函式

| 名稱 | 描述 |
|-|-|
| `float length(float3 const& value)` | 計算向量的長度（或 Euclidean 距離）。 |
| `float length_squared(float3 const& value)` | 計算向量平方的長度（或 Euclidean 距離）。 |
| `float distance(float3 const& value1, float3 const& value2)` | 計算兩個向量之間的 Euclidean 距離。 |
| `float distance_squared(float3 const& value1, float3 const& value2)` | 計算兩個向量平方之間的 Euclidean 距離。 |
| `float dot(float3 const& vector1, float3 const& vector2)` | 計算兩個向量的點乘積。 |
| `float3 normalize(float3 const& value)` | 從指定的向量建立單元向量。 |
| `float3 cross(float3 const& vector1, float3 const& vector2)` | 計算兩個向量的叉積。 |
| `float3 reflect(float3 const& vector, float3 const& normal)` | 決定給定向量和一般的反映向量。 |
| `float3 min(float3 const& value1, float3 const& value2)` | 傳回向量，其中包含每個相符元件配對的最小值。 |
| `float3 max(float3 const& value1, float3 const& value2)` | 傳回向量，其中包含每個相符元件的最高值。 |
| `float3 clamp(float3 const& value1, float3 const& min, float3 const& max)` | 將值限制在指定的範圍內。 |
| `float3 lerp(float3 const& value1, float3 const& value2, float amount)` | 在兩個向量之間執行線性插補。 |
| `float3 transform(float3 const& position, float4x4 const& matrix)` | 將向量 (x、y、z、1) 由指定的矩陣進行轉換。 |
| `float3 transform_normal(float3 const& normal, float4x4 const& matrix)` | 將一般向量 (x、y、z、0) 由指定的矩陣進行轉換。 |
| `float3 transform(float3 const& value, quaternion const& rotation)` | 依據指定的四元數來轉換 float3。 |

## <a name="methods"></a>方法

| 名稱 | 描述 |
|-|-|
| `static float3 zero()` | 傳回 float3，其中所有的元件都設為零。 |
| `static float3 one()` | 傳回 float3，其中所有的元件都設為1。 |
| `static float3 unit_x()` | 傳回 float3 (1，0，0) 。 |
| `static float3 unit_y()` | 傳回 float3 (0，1，0) 。 |
| `static float3 unit_z()` | 傳回 float3 (0，0，1) 。 |

## <a name="operators"></a>運算子

| 名稱 | 描述 |
|-|-|
| `float3 operator+ (float3 const& value1, float3 const& value2)` | 新增兩個向量。 |
| `float3 operator- (float3 const& value1, float3 const& value2)` | 從向量減去向量。 |
| `float3 operator* (float3 const& value1, float3 const& value2)` | 將兩個向量的元件相乘。 |
| `float3 operator* (float3 const& value1, float value2)` | 將向量乘以純量。 |
| `float3 operator* (float value1, float3 const& value2)` | 將向量乘以純量。 |
| `float3 operator/ (float3 const& value1, float3 const& value2)` | 將向量的元件除以另一個向量的元件。 |
| `float3 operator/ (float3 const& value1, float value2)` | 將向量除以純量值。 |
| `float3 operator- (float3 const& value)` | 傳回指向相反方向的向量。 |
| `float3& operator+= (float3& value1, float3 const& value2)` | 就地新增兩個向量。 |
| `float3& operator-= (float3& value1, float3 const& value2)` | 就地從向量減去向量。 |
| `float3& operator*= (float3& value1, float3 const& value2)` | 就地將兩個向量的元件相乘。 |
| `float3& operator*= (float3& value1, float value2)` | 就地將向量乘以純量。 |
| `float3& operator/= (float3& value1, float3 const& value2)` | 就地將向量的元件除以另一個向量的元件。 |
| `float3& operator/= (float3& value1, float value2)` | 就地將向量除以純量值。 |
| `bool operator== (float3 const& value1, float3 const& value2)` | 判斷兩個 float3 實例是否相等。 |
| `bool operator!= (float3 const& value1, float3 const& value2)` | 判斷 float3 的兩個實例是否不相等。 |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector3() const` | 將 float3 轉換成 **Vector3** 的格式。 |

## <a name="fields"></a>欄位

| 名稱 | 描述 |
|-|-|
| `float x` | 向量的 X 元件。 |
| `float y` | 向量的 Y 元件。 |
| `float z` | 向量的 Z 元件。 |

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-|-|
| 命名空間 | Windows：： Foundation：：數值 |
| 標頭 | <dl> <dt>Windowsnumerics。h</dt> </dl> |

## <a name="see-also"></a>另請參閱

[windowsnumerics .h Api](windowsnumerics-h-apis-portal.md)
