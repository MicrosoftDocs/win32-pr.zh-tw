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
# <a name="float2-structure"></a>float2 結構

具有兩個元件的向量。

此類型僅適用于 c + +。 它的 .NET 對等專案是 [Vector2](/dotnet/api/system.numerics.vector2?view=netframework-4.8)。

## <a name="constructors"></a>建構函式

| 名稱 | 描述 |
|-|-|
| `float2()` | 建立未初始化的 float2。 |
| `float2(float x, float y)` | 使用指定的值建立 float2。 |
| `explicit float2(float value)` | 建立 float2，並將所有元件設定為指定的值。 |
| `float2(Microsoft::Graphics::Canvas::Numerics::Vector2 const& value)` | 將 **Vector2** 轉換成 float2 的格式。 |
| `float2(Windows::Foundation::Point const& value)` | [**將 float2 轉換為**](/uwp/api/Windows.Foundation.Point)。 |
| `float2(Windows::Foundation::Size const& value)` | 將 float2 的 [**大小**](/uwp/api/Windows.Foundation.Size) 轉換成。 |

## <a name="functions"></a>函式

| Name | 描述 |
|-|-|
| `float length(float2 const& value)` | 計算向量的長度（或 Euclidean 距離）。 |
| `float length_squared(float2 const& value)` | 計算向量平方的長度（或 Euclidean 距離）。 |
| `float distance(float2 const& value1, float2 const& value2)` | 計算兩個向量之間的 Euclidean 距離。 |
| `float distance_squared(float2 const& value1, float2 const& value2)` | 計算兩個向量平方之間的 Euclidean 距離。 |
| `float dot(float2 const& value1, float2 const& value2)` | 計算兩個向量的點乘積。 |
| `float2 normalize(float2 const& value)` | 從指定的向量建立單元向量。 |
| `float2 reflect(float2 const& vector, float2 const& normal)` | 決定給定向量和一般的反映向量。 |
| `float2 min(float2 const& value1, float2 const& value2)` | 傳回向量，其中包含每個相符元件配對的最小值。 |
| `float2 max(float2 const& value1, float2 const& value2)` | 傳回向量，其中包含每個相符元件的最高值。 |
| `float2 clamp(float2 const& value1, float2 const& min, float2 const& max)` | 將值限制在指定的範圍內。 |
| `float2 lerp(float2 const& value1, float2 const& value2, float amount)` | 在兩個向量之間執行線性插補。 |
| `float2 transform(float2 const& position, float3x2 const& matrix)` | 將向量 (x、y、0、1) 由指定的矩陣進行轉換。 |
| `float2 transform(float2 const& position, float4x4 const& matrix)` | 將向量 (x、y、0、1) 由指定的矩陣進行轉換。 |
| `float2 transform_normal(float2 const& normal, float3x2 const& matrix)` | 將一般向量 (x、y、0、0) 由指定的矩陣進行轉換。 |
| `float2 transform_normal(float2 const& normal, float4x4 const& matrix)` | 將一般向量 (x、y、0、0) 由指定的矩陣進行轉換。 |
| `float2 transform(float2 const& value, quaternion const& rotation)` | 依據指定的四元數來轉換 float2。 |

## <a name="methods"></a>方法

| 名稱 | 描述 |
|-|-|
| `static float2 zero()` | 傳回 float2，其中所有的元件都設為零。 |
| `static float2 one()` | 傳回 float2，其中所有的元件都設為1。 |
| `static float2 unit_x()` | 傳回 float2 (1，0) 。 |
| `static float2 unit_y()` | 傳回 float2 (0，1) 。 |

## <a name="operators"></a>運算子

| Name | 描述 |
|-|-|
| `operator Windows::Foundation::Point() const` | 將 float2 轉換為 [**Windows. Point**](/uwp/api/Windows.Foundation.Point)。 |
| `operator Windows::Foundation::Size() const` | 將 float2 轉換為 [**Windows. 大小**](/uwp/api/Windows.Foundation.Size)。 |
| `float2 operator+ (float2 const& value1, float2 const& value2)` | 新增兩個向量。 |
| `float2 operator- (float2 const& value1, float2 const& value2)` | 從向量減去向量。 |
| `float2 operator* (float2 const& value1, float2 const& value2)` | 將兩個向量的元件相乘。 |
| `float2 operator* (float2 const& value1, float value2)` | 將向量乘以純量。 |
| `float2 operator* (float value1, float2 const& value2)` | 將向量乘以純量。 |
| `float2 operator/ (float2 const& value1, float2 const& value2)` | 將向量的元件除以另一個向量的元件。 |
| `float2 operator/ (float2 const& value1, float value2)` | 將向量除以純量值。 |
| `float2 operator- (float2 const& value)` | 傳回指向相反方向的向量。 |
| `float2& operator+= (float2& value1, float2 const& value2)` | 就地新增兩個向量。 |
| `float2& operator-= (float2& value1, float2 const& value2)` | 就地從向量減去向量。 |
| `float2& operator*= (float2& value1, float2 const& value2)` | 就地將兩個向量的元件相乘。 |
| `float2& operator*= (float2& value1, float value2)` | 就地將向量乘以純量。 |
| `float2& operator/= (float2& value1, float2 const& value2)` | 就地將向量的元件除以另一個向量的元件。 |
| `float2& operator/= (float2& value1, float value2)` | 就地將向量除以純量值。 |
| `bool operator== (float2 const& value1, float2 const& value2)` | 判斷兩個 float2 實例是否相等。 |
| `bool operator!= (float2 const& value1, float2 const& value2)` | 判斷 float2 的兩個實例是否不相等。 |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector2() const` | 將 float2 轉換成 **Vector2** 的格式。 |

## <a name="fields"></a>欄位

| 名稱 | 描述 |
|-|-|
| `float x` | 向量的 X 元件。 |
| `float y` | 向量的 Y 元件。 |

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-|-|
| 命名空間 | Windows：： Foundation：：數值 |
| 標頭 | <dl> <dt>Windowsnumerics。h</dt> </dl> |

## <a name="see-also"></a>另請參閱

[windowsnumerics .h Api](windowsnumerics-h-apis-portal.md)
