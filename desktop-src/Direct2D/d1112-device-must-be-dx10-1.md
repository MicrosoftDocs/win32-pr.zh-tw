---
title: D1112 裝置必須是 DX11 相互作用
ms.assetid: 39dcccaf-db56-402d-b62f-704ad4daf151
description: 與 DXGI 介面相關聯的裝置必須是 D3D11 裝置。
keywords:
- D1112 裝置必須是 DX11 相互作用 Direct2D
topic_type:
- apiref
api_name:
- D1112 Device Must Be DX11
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: b4204e04332876db9145baba9888dbb2d339eff9
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2020
ms.locfileid: "104023186"
---
# <a name="d1112-device-must-be-dx11"></a><span data-ttu-id="9897f-104">D1112：裝置必須是 DX11 相互作用</span><span class="sxs-lookup"><span data-stu-id="9897f-104">D1112: Device Must Be DX11</span></span>

<span data-ttu-id="9897f-105">與 DXGI 介面相關聯的裝置必須是 D3D11 裝置。</span><span class="sxs-lookup"><span data-stu-id="9897f-105">The device associated with the DXGI surface must be a D3D11 device.</span></span>



|             |         |
|-------------|---------|
| <span data-ttu-id="9897f-106">錯誤層級</span><span class="sxs-lookup"><span data-stu-id="9897f-106">Error Level</span></span> | <span data-ttu-id="9897f-107">警告</span><span class="sxs-lookup"><span data-stu-id="9897f-107">Warning</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="9897f-108">可能的原因</span><span class="sxs-lookup"><span data-stu-id="9897f-108">Possible Causes</span></span>

<span data-ttu-id="9897f-109">嘗試使用 [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) 搭配非 Direct3D11 裝置所建立的 DXGI 介面。</span><span class="sxs-lookup"><span data-stu-id="9897f-109">There was an attempt to use the [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) with a DXGI surface created by a non-Direct3D11 device.</span></span>

 

 




