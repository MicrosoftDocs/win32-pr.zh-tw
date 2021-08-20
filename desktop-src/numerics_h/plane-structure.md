---
title: '平面結構 (Windowsnumerics .h) '
description: 此結構代表使用3D 向量法線和距離值的平面。
ms.assetid: 3C5A5EA0-8A51-4F9B-A84A-0C8E726CE3FD
keywords:
- 平面結構
topic_type:
- apiref
api_name:
- plane structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1479841c5e82c47e98b255d718bf1c74f50feafdec8b2bb951c43fa46cab71b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869570"
---
# <a name="plane-structure"></a>平面結構

此結構代表使用3D 向量法線和距離值的平面。

此類型僅適用于 c + +。 它的 .NET 對等專案是 [system.object](/dotnet/api/system.numerics.plane?view=netframework-4.8)。

## <a name="constructors"></a>建構函式

| 名稱 | 描述 |
|-|-|
| `plane()` | 建立未初始化的平面。 |
| `plane(float x, float y, float z, float d)` | 建立具有指定值的平面。 |
| `plane(float3 normal, float d)` | 從 float3 和距離建立平面。 |
| `explicit plane(float4 value)` | 從 float4 建立平面。 |
| `plane(Microsoft::?Graphics::?Canvas::?Numerics::?Plane const& value)` | Converts a **Microsoft.Graphics.Canvas.Numerics.Plane** to a plane. |

## <a name="functions"></a>函式

| 名稱 | 描述 |
|-|-|
| `plane make_plane_from_vertices(float3 const& point1, float3 const& point2, float3 const& point3)` | 從三個頂點位置的集合建立平面，這些位置必須全都不同，而不是直線。 |
| `plane normalize(plane const& value)` | 變更平面標準向量的係數，使其成為單位長度。 |
| `plane transform(plane const& plane, float4x4 const& matrix)` | 依矩陣轉換正規化的平面。 |
| `plane transform(plane const& plane, quaternion const& rotation)` | 以四元數的旋轉來轉換正規化的平面。 |
| `float dot(plane const& plane, float4 const& value)` | 使用向量計算平面的點乘積。 |
| `float dot_coordinate(plane const& plane, float3 const& value)` | 以 float3 座標計算平面的點乘積。 與點 \_ 法線不同的是，此計算包含平面 d 值。 |
| `float dot_normal(plane const& plane, float3 const& value)` | 以 float3 標準計算平面的點乘積。 與點 \_ 座標不同的是，此計算會忽略平面 d 值。 |

## <a name="operators"></a>運算子

| 名稱 | 描述 |
|-|-|
| `bool operator== (plane const& value1, plane const& value2)` | 判斷平面的兩個實例是否相等。 |
| `bool operator!= (plane const& value1, plane const& value2)` | 判斷平面的兩個實例是否不相等。 |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Plane() const` | 將平面轉換成中 **的平面。** |

## <a name="fields"></a>欄位

| 名稱 | 描述 |
|-|-|
| `float3 normal` | 平面的一般向量。 |
| `float d` | 平面與原點之間的距離。 |

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-|-|
| 命名空間 | Windows：： Foundation：：數值 |
| 標頭 | <dl> <dt>Windowsnumerics。h</dt> </dl> |

## <a name="see-also"></a>另請參閱

[windowsnumerics .h Api](windowsnumerics-h-apis-portal.md)
