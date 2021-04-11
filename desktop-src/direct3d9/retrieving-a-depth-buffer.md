---
description: 下列程式碼範例示範如何使用 IDirect3DDevice9：： GetDepthStencilSurface 方法，來取得裝置所擁有之深度緩衝區介面的指標。
ms.assetid: cd5c158a-d2c4-4ced-aa6f-cd8c0e426a74
title: 抓取 (Direct3D 9) 的深度緩衝區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae914b8506fd0c4169f0cfec0d78d7c3bd9b9d61
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109600"
---
# <a name="retrieving-a-depth-buffer-direct3d-9"></a><span data-ttu-id="9c6e7-103">抓取 (Direct3D 9) 的深度緩衝區</span><span class="sxs-lookup"><span data-stu-id="9c6e7-103">Retrieving a Depth Buffer (Direct3D 9)</span></span>

<span data-ttu-id="9c6e7-104">下列程式碼範例示範如何使用 [**IDirect3DDevice9：： GetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdepthstencilsurface) 方法，來取得裝置所擁有之深度緩衝區介面的指標。</span><span class="sxs-lookup"><span data-stu-id="9c6e7-104">The following code example shows how to use the [**IDirect3DDevice9::GetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdepthstencilsurface) method to retrieve a pointer to the depth-buffer surface owned by the device.</span></span>


```
LPDIRECT3DSURFACE9 pZBuffer;

m_d3dDevice->GetDepthStencilSurface( &pZBuffer );
```



## <a name="related-topics"></a><span data-ttu-id="9c6e7-105">相關主題</span><span class="sxs-lookup"><span data-stu-id="9c6e7-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c6e7-106">深度緩衝區</span><span class="sxs-lookup"><span data-stu-id="9c6e7-106">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
