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
# <a name="direct3d-resources-direct3d-9"></a>Direct3d 資源 (direct3d 9) 

資源是用來呈現場景的材質和緩衝區。 應用程式需要建立、載入、複製及使用資源。 本節提供資源的簡介，以及應用程式在處理資源時所使用的步驟和方法。

所有資源（包括幾何資源 [**IDirect3DIndexBuffer9**](/windows/desktop/api) 和 [**IDirect3DVertexBuffer9**](/windows/desktop/api)）都會繼承自 [**IDirect3DResource9**](/windows/desktop/api) 介面。 材質資源（ [**IDirect3DCubeTexture9**](/windows/desktop/api)、 [**IDirect3DTexture9**](/windows/desktop/api)和 [**IDirect3DVolumeTexture9**](/windows/desktop/api)）也會繼承自 [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) 介面。

-   [ (Direct3D 9) 的資源屬性 ](resource-properties.md)
-   [ (Direct3D 9) 操作資源 ](manipulating-resources.md)
-   [ (Direct3D 9) 的鎖定資源 ](locking-resources.md)
-   [ (Direct3D 9) 的資源關聯性 ](resource-relationships.md)
-   [管理 (Direct3D 9) 的資源 ](managing-resources.md)
-   [ (Direct3D 9) 的應用程式管理資源和配置策略 ](application-managed-resources-and-allocation-strategies.md)

<!-- -->

-   [ (Direct3D 9) 的索引緩衝區 ](index-buffers.md)
-   [ (Direct3D 9) 的頂點緩衝區 ](vertex-buffers.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[快速入門](getting-started.md)
</dt> </dl>

 

 
