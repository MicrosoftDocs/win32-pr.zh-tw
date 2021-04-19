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
# <a name="quaternion-structure"></a>四元數結構

用來表示旋轉的四個維度向量。

四元數可以有效率地將有關 (x，y，z) 向量的物件旋轉為角度 theta，其中 w = cos (theta/2) 。 四元數通常是用來在兩個角度之間平滑插補，以避免歐拉角度可能發生的 gimbal 鎖定問題。

此類型僅適用于 c + +。 它的 .NET 對等[專案是 system.string。](/dotnet/api/system.numerics.quaternion?view=netframework-4.8)

## <a name="constructors"></a>建構函式

| 名稱 | 描述 |
|-|-|
| `quaternion()` | 建立未初始化的四元數。 |
| `quaternion(float x, float y, float z, float w)` | 使用指定的值建立四元數。 |
| `quaternion(float3 vectorPart, float scalarPart)` | 從 float3 和純量建立四元數。 |
| `quaternion(Microsoft::?Graphics::?Canvas::?Numerics::?Quaternion const& value)` | 將 node.js 的格式 **轉換為四元數。** |

## <a name="functions"></a>函式

| Name | 描述 |
|-|-|
| `quaternion make_quaternion_from_axis_angle(float3 const& axis, float angle)` | 從向量和對此向量旋轉的角度建立四元數。 |
| `quaternion make_quaternion_from_yaw_pitch_roll(float yaw, float pitch, float roll)` | 從指定的偏擺、音調和滾動角度建立四元數。 |
| `quaternion make_quaternion_from_rotation_matrix(float4x4 const& matrix)` | 從旋轉矩陣建立四元數。 |
| `bool is_identity(quaternion const& value)` | 檢查這是否為身分識別 (沒有任何旋轉) 四元數。 |
| `float length(quaternion const& value)` | 計算四元數的長度。 |
| `float length_squared(quaternion const& value)` | 計算四元數的長度平方。 |
| `float dot(quaternion const& quaternion1, quaternion const& quaternion2)` | 計算兩個四元數的內積。 |
| `quaternion normalize(quaternion const& value)` | 將四元數的每個元件除以四元數的長度。 |
| `quaternion conjugate(quaternion const& value)` | 計算四元數的共軛。 |
| `quaternion inverse(quaternion const& value)` | 計算四元數的反向。 |
| `quaternion slerp(quaternion const& quaternion1, quaternion const& quaternion2, float amount)` | 使用球面線性插補，在兩個四元數間進行插補。 |
| `quaternion lerp(quaternion const& quaternion1, quaternion const& quaternion2, float amount)` | 在兩個四元數之間的線性插補。 |
| `quaternion concatenate(quaternion const& value1, quaternion const& value2)` | 串連兩個四元數;結果代表第一個旋轉，後面接著第二個旋轉。 |

## <a name="methods"></a>方法

| 名稱 | 描述 |
|-|-|
| `static quaternion identity()` | 傳回識別四元數的實例。 |

## <a name="operators"></a>運算子

| Name | 描述 |
|-|-|
| `quaternion operator+ (quaternion const& value1, quaternion const& value2)` | 加入兩個四元數。 |
| `quaternion operator- (quaternion const& value1, quaternion const& value2)` | 從另一個四元數減去四元數。 |
| `quaternion operator* (quaternion const& value1, quaternion const& value2)` | 將四元數乘以另一個四元數。 |
| `quaternion operator* (quaternion const& value1, float value2)` | 將四元數乘以純量值。 |
| `quaternion operator/ (quaternion const& value1, quaternion const& value2)` | 將四元數除以另一個四元數。 |
| `quaternion operator- (quaternion const& value)` | 翻轉四元數的每個元件的正負號。 |
| `quaternion& operator+= (quaternion& value1, quaternion const& value2)` | 就地新增兩個四元數。 |
| `quaternion& operator-= (quaternion& value1, quaternion const& value2)` | 就地減去另一個四元數的四元數。 |
| `quaternion& operator*= (quaternion& value1, quaternion const& value2)` | 就地將四元數乘以另一個四元數。 |
| `quaternion& operator*= (quaternion& value1, float value2)` | 就地 nultiplies 具有純量值的四元數。 |
| `quaternion& operator/= (quaternion& value1, quaternion const& value2)` | 就地將四元數除以另一個四元數。 |
| `bool operator== (quaternion const& value1, quaternion const& value2)` | 判斷四元數的兩個實例是否相等。 |
| `bool operator!= (quaternion const& value1, quaternion const& value2)` | 判斷四元數的兩個實例是否不相等。 |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Quaternion() const` | Converts a quaternion to a **Microsoft.Graphics.Canvas.Numerics.Quaternion**. |

## <a name="fields"></a>欄位

| 名稱 | 描述 |
|-|-|
| `float x` | 四元數之向量元件的 X 值。 |
| `float y` | 四元數之向量元件的 Y 值。 |
| `float z` | 四元數之向量元件的 Z 值。 |
| `float w` | 四元數的旋轉元件。 |

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-|-|
| 命名空間 | Windows：： Foundation：：數值 |
| 標頭 | <dl> <dt>Windowsnumerics。h</dt> </dl> |

## <a name="see-also"></a>另請參閱

[windowsnumerics .h Api](windowsnumerics-h-apis-portal.md)
