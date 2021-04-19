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
# <a name="windows-numerics-and-directxmath-interop-apis"></a><span data-ttu-id="3a1f7-104">Windows 數值和 DirectXMath interop Api</span><span class="sxs-lookup"><span data-stu-id="3a1f7-104">Windows numerics and DirectXMath interop APIs</span></span>

<span data-ttu-id="3a1f7-105">這些函式會將 DirectXMath SIMD 型別 [XMVECTOR](../dxmath/xmvector-data-type.md)和 [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)中的 SIMD [**類型轉換成和。**](/uwp/api/Windows.Foundation.Numerics)</span><span class="sxs-lookup"><span data-stu-id="3a1f7-105">These functions convert [**Windows.Foundation.Numerics**](/uwp/api/Windows.Foundation.Numerics) types to and from the DirectXMath SIMD types [XMVECTOR](../dxmath/xmvector-data-type.md) and [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span>

## <a name="functions"></a><span data-ttu-id="3a1f7-106">函式</span><span class="sxs-lookup"><span data-stu-id="3a1f7-106">Functions</span></span>

| <span data-ttu-id="3a1f7-107">Name</span><span class="sxs-lookup"><span data-stu-id="3a1f7-107">Name</span></span> | <span data-ttu-id="3a1f7-108">描述</span><span class="sxs-lookup"><span data-stu-id="3a1f7-108">Description</span></span> |
|-|-|
| `XMVECTOR XMLoadFloat2(_In_ float2 const* pSource)` | <span data-ttu-id="3a1f7-109">將 float2 載入 DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-109">Loads a float2 into a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md).</span></span> |
| `XMVECTOR XMLoadFloat3(_In_ float3 const* pSource)` | <span data-ttu-id="3a1f7-110">將 float3 載入 DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-110">Loads a float3 into a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md).</span></span> |
| `XMVECTOR XMLoadFloat4(_In_ float4 const* pSource)` | <span data-ttu-id="3a1f7-111">將 float4 載入 DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-111">Loads a float4 into a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md).</span></span> |
| `XMMATRIX XMLoadFloat3x2(_In_ float3x2 const* pSource)` | <span data-ttu-id="3a1f7-112">將 float3x2 載入 DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-112">Loads a float3x2 into a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span> |
| `XMMATRIX XMLoadFloat4x4(_In_ float4x4 const* pSource)` | <span data-ttu-id="3a1f7-113">將 float4x4 載入 DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-113">Loads a float4x4 into a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span> |
| `XMVECTOR XMLoadPlane(_In_ plane const* pSource)` | <span data-ttu-id="3a1f7-114">將平面載入至 DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-114">Loads a plane into a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span> |
| `XMVECTOR XMLoadQuaternion(_In_ quaternion const* pSource)` | <span data-ttu-id="3a1f7-115">將四元數載入至 DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-115">Loads a quaternion into a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix).</span></span> |
| `void XMStoreFloat2(_Out_ float2* pDestination, _In_ FXMVECTOR value)` | <span data-ttu-id="3a1f7-116">將 DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) 儲存在 float2 中。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-116">Stores a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) into a float2.</span></span> |
| `void XMStoreFloat3(_Out_ float3* pDestination, _In_ FXMVECTOR value)` | <span data-ttu-id="3a1f7-117">將 DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) 儲存在 float3 中。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-117">Stores a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) into a float3.</span></span> |
| `void XMStoreFloat4(_Out_ float4* pDestination, _In_ FXMVECTOR value)` | <span data-ttu-id="3a1f7-118">將 DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) 儲存在 float4 中。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-118">Stores a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) into a float4.</span></span> |
| `void XMStoreFloat3x2(_Out_ float3x2* pDestination, _In_ FXMMATRIX value)` | <span data-ttu-id="3a1f7-119">將 DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) 儲存在 float3x2 中。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-119">Stores a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) into a float3x2.</span></span> |
| `void XMStoreFloat4x4(_Out_ float4x4* pDestination, _In_ FXMMATRIX value)` | <span data-ttu-id="3a1f7-120">將 DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) 儲存在 float4x4 中。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-120">Stores a DirectXMath [XMMATRIX](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) into a float4x4.</span></span> |
| `void XMStorePlane(_Out_ plane* pDestination, _In_ FXMVECTOR value)` | <span data-ttu-id="3a1f7-121">將 DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) 儲存在平面中。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-121">Stores a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) into a plane.</span></span> |
| `void XMStoreQuaternion(_Out_ quaternion* pDestination, _In_ FXMVECTOR value)` | <span data-ttu-id="3a1f7-122">將 DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) 儲存至四元數。</span><span class="sxs-lookup"><span data-stu-id="3a1f7-122">Stores a DirectXMath [XMVECTOR](../dxmath/xmvector-data-type.md) into a quaternion.</span></span> |

## <a name="requirements"></a><span data-ttu-id="3a1f7-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a1f7-123">Requirements</span></span>

| <span data-ttu-id="3a1f7-124">需求</span><span class="sxs-lookup"><span data-stu-id="3a1f7-124">Requirement</span></span> | <span data-ttu-id="3a1f7-125">值</span><span class="sxs-lookup"><span data-stu-id="3a1f7-125">Value</span></span> |
|-|-|
| <span data-ttu-id="3a1f7-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="3a1f7-126">Namespace</span></span> | <span data-ttu-id="3a1f7-127">DirectX</span><span class="sxs-lookup"><span data-stu-id="3a1f7-127">DirectX</span></span> |
| <span data-ttu-id="3a1f7-128">標頭</span><span class="sxs-lookup"><span data-stu-id="3a1f7-128">Header</span></span> | <dl> <span data-ttu-id="3a1f7-129"><dt>Windowsnumerics。h</dt></span><span class="sxs-lookup"><span data-stu-id="3a1f7-129"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="3a1f7-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a1f7-130">See also</span></span>

[<span data-ttu-id="3a1f7-131">windowsnumerics .h Api</span><span class="sxs-lookup"><span data-stu-id="3a1f7-131">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
