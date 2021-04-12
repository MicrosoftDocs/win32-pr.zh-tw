---
description: 資源是用來呈現場景的材質和緩衝區。
ms.assetid: 815a330c-9fd2-45ff-b7df-192fc197074f
title: 'Direct3d 資源 (direct3d 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7745318db3d880711ee962edb086996764455ec8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109165"
---
# <a name="direct3d-resources-direct3d-9"></a><span data-ttu-id="c4ad2-103">Direct3d 資源 (direct3d 9) </span><span class="sxs-lookup"><span data-stu-id="c4ad2-103">Direct3D Resources (Direct3D 9)</span></span>

<span data-ttu-id="c4ad2-104">資源是用來呈現場景的材質和緩衝區。</span><span class="sxs-lookup"><span data-stu-id="c4ad2-104">Resources are the textures and buffers that are used to render a scene.</span></span> <span data-ttu-id="c4ad2-105">應用程式需要建立、載入、複製及使用資源。</span><span class="sxs-lookup"><span data-stu-id="c4ad2-105">Applications need to create, load, copy, and use resources.</span></span> <span data-ttu-id="c4ad2-106">本節提供資源的簡介，以及應用程式在處理資源時所使用的步驟和方法。</span><span class="sxs-lookup"><span data-stu-id="c4ad2-106">This section gives a brief introduction to resources and the steps and methods used by applications when working with resources.</span></span>

<span data-ttu-id="c4ad2-107">所有資源（包括幾何資源 [**IDirect3DIndexBuffer9**](/windows/desktop/api) 和 [**IDirect3DVertexBuffer9**](/windows/desktop/api)）都會繼承自 [**IDirect3DResource9**](/windows/desktop/api) 介面。</span><span class="sxs-lookup"><span data-stu-id="c4ad2-107">All resources, including the geometry resources [**IDirect3DIndexBuffer9**](/windows/desktop/api) and [**IDirect3DVertexBuffer9**](/windows/desktop/api), inherit from the [**IDirect3DResource9**](/windows/desktop/api) interface.</span></span> <span data-ttu-id="c4ad2-108">材質資源（ [**IDirect3DCubeTexture9**](/windows/desktop/api)、 [**IDirect3DTexture9**](/windows/desktop/api)和 [**IDirect3DVolumeTexture9**](/windows/desktop/api)）也會繼承自 [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) 介面。</span><span class="sxs-lookup"><span data-stu-id="c4ad2-108">The texture resources, [**IDirect3DCubeTexture9**](/windows/desktop/api), [**IDirect3DTexture9**](/windows/desktop/api), and [**IDirect3DVolumeTexture9**](/windows/desktop/api), also inherit from the [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) interface.</span></span>

-   [<span data-ttu-id="c4ad2-109"> (Direct3D 9) 的資源屬性 </span><span class="sxs-lookup"><span data-stu-id="c4ad2-109">Resource Properties (Direct3D 9)</span></span>](resource-properties.md)
-   [<span data-ttu-id="c4ad2-110"> (Direct3D 9) 操作資源 </span><span class="sxs-lookup"><span data-stu-id="c4ad2-110">Manipulating Resources (Direct3D 9)</span></span>](manipulating-resources.md)
-   [<span data-ttu-id="c4ad2-111"> (Direct3D 9) 的鎖定資源 </span><span class="sxs-lookup"><span data-stu-id="c4ad2-111">Locking Resources (Direct3D 9)</span></span>](locking-resources.md)
-   [<span data-ttu-id="c4ad2-112"> (Direct3D 9) 的資源關聯性 </span><span class="sxs-lookup"><span data-stu-id="c4ad2-112">Resource Relationships (Direct3D 9)</span></span>](resource-relationships.md)
-   [<span data-ttu-id="c4ad2-113">管理 (Direct3D 9) 的資源 </span><span class="sxs-lookup"><span data-stu-id="c4ad2-113">Managing Resources (Direct3D 9)</span></span>](managing-resources.md)
-   [<span data-ttu-id="c4ad2-114"> (Direct3D 9) 的應用程式管理資源和配置策略 </span><span class="sxs-lookup"><span data-stu-id="c4ad2-114">Application-Managed Resources and Allocation Strategies (Direct3D 9)</span></span>](application-managed-resources-and-allocation-strategies.md)

<!-- -->

-   [<span data-ttu-id="c4ad2-115"> (Direct3D 9) 的索引緩衝區 </span><span class="sxs-lookup"><span data-stu-id="c4ad2-115">Index Buffers (Direct3D 9)</span></span>](index-buffers.md)
-   [<span data-ttu-id="c4ad2-116"> (Direct3D 9) 的頂點緩衝區 </span><span class="sxs-lookup"><span data-stu-id="c4ad2-116">Vertex Buffers (Direct3D 9)</span></span>](vertex-buffers.md)

## <a name="related-topics"></a><span data-ttu-id="c4ad2-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="c4ad2-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4ad2-118">快速入門</span><span class="sxs-lookup"><span data-stu-id="c4ad2-118">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 
