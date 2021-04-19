---
title: 'Windows 數值和 DirectXMath interop Api (Windowsnumerics .h) '
description: 這些函式會將 DirectXMath SIMD 型別 XMVECTOR 和 XMMATRIX 中的 SIMD 類型轉換成和。
ms.assetid: 05851054-196E-4955-B9C5-85C2E33EF488
keywords:
- Windows 數值和 DirectXMath interop Api
topic_type:
- apiref
api_name:
- WWindows numerics and DirectXMath interop APIs
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02e39057c92eeed87c3f429acb56f0afa2468ded
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996076"
---
# <a name="windows-numerics-and-directxmath-interop-apis"></a>Windows 數值和 DirectXMath interop Api

這些函式會將 DirectXMath SIMD 型別 [XMVECTOR](../dxmath/xmvector-data-type.md)和 [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)中的 SIMD [**類型轉換成和。**](/uwp/api/Windows.Foundation.Numerics)

## <a name="functions"></a>函式

| Name | 描述 |
|-|-|
| `XMVECTOR XMLoadFloat2(_In_ float2 const* pSource)` | 將 float2 載入 DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md)。 |
| `XMVECTOR XMLoadFloat3(_In_ float3 const* pSource)` | 將 float3 載入 DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md)。 |
| `XMVECTOR XMLoadFloat4(_In_ float4 const* pSource)` | 將 float4 載入 DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md)。 |
| `XMMATRIX XMLoadFloat3x2(_In_ float3x2 const* pSource)` | 將 float3x2 載入 DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)。 |
| `XMMATRIX XMLoadFloat4x4(_In_ float4x4 const* pSource)` | 將 float4x4 載入 DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)。 |
| `XMVECTOR XMLoadPlane(_In_ plane const* pSource)` | 將平面載入至 DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)。 |
| `XMVECTOR XMLoadQuaternion(_In_ quaternion const* pSource)` | 將四元數載入至 DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)。 |
| `void XMStoreFloat2(_Out_ float2* pDestination, _In_ FXMVECTOR value)` | 將 DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) 儲存在 float2 中。 |
| `void XMStoreFloat3(_Out_ float3* pDestination, _In_ FXMVECTOR value)` | 將 DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) 儲存在 float3 中。 |
| `void XMStoreFloat4(_Out_ float4* pDestination, _In_ FXMVECTOR value)` | 將 DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) 儲存在 float4 中。 |
| `void XMStoreFloat3x2(_Out_ float3x2* pDestination, _In_ FXMMATRIX value)` | 將 DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) 儲存在 float3x2 中。 |
| `void XMStoreFloat4x4(_Out_ float4x4* pDestination, _In_ FXMMATRIX value)` | 將 DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) 儲存在 float4x4 中。 |
| `void XMStorePlane(_Out_ plane* pDestination, _In_ FXMVECTOR value)` | 將 DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) 儲存在平面中。 |
| `void XMStoreQuaternion(_Out_ quaternion* pDestination, _In_ FXMVECTOR value)` | 將 DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) 儲存至四元數。 |

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-|-|
| 命名空間 | DirectX |
| 標頭 | <dl> <dt>Windowsnumerics。h</dt> </dl> |

## <a name="see-also"></a>另請參閱

[windowsnumerics .h Api](windowsnumerics-h-apis-portal.md)
