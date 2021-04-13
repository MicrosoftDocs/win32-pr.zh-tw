---
description: 您的應用程式會操控資源以轉譯場景。
ms.assetid: 4f0eea7d-b1e4-4d53-a136-f40df7a0fbb1
title: " (Direct3D 9) 操作資源"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 886dfee3af024d103dab8666687f1b053a5fb46a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385493"
---
# <a name="manipulating-resources-direct3d-9"></a> (Direct3D 9) 操作資源

您的應用程式會操控資源以轉譯場景。 首先，應用程式必須使用下列其中一種方法來建立材質資源：

-   [**IDirect3DDevice9::CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
-   [**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
-   [**IDirect3DDevice9::CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)

您可以使用其中一個 D3DXCreatexxx 紋理函式來建立材質資源。

材質建立方法所傳回的材質物件是表面或磁片區的容器;這些容器一般稱為緩衝區。 資源所擁有的緩衝區會繼承資源的使用方式、格式和集區，但會有自己的類型。 如需詳細資訊，請參閱 [ (Direct3D 9) 的資源屬性 ](resource-properties.md)。

應用程式會藉由呼叫下列方法，取得所包含表面的存取權，以載入插圖。 如需詳細資訊，請參閱 [ (Direct3D 9) 的鎖定資源 ](locking-resources.md)。

-   [**IDirect3DCubeTexture9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
-   [**IDirect3DTexture9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-lockrect)
-   [**IDirect3DVolumeTexture9：：加密箱**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox)

鎖定方法會使用引數來表示內含的介面（例如，mipmap 的子層級或立方體的材質面），並將指標傳回至圖元。 一般的應用程式永遠不會直接使用介面物件。

藉由呼叫 [**IDirect3DDevice9：： CreateIndexBuffer**](/windows/desktop/api) 或 [**IDirect3DDevice9：： CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer)來建立幾何導向的資源。

藉由呼叫 [**IDirect3DIndexBuffer9：： lock**](/windows/desktop/api) 或 [**IDirect3DVertexBuffer9：： lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock)來鎖定和填滿緩衝區資源，視資源而定。

針對 managed 材質資源，資源建立程式會在此結束。 針對非受控材質資源，應用程式會藉由呼叫 [**IDirect3DDevice9：： UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture)，將系統記憶體資源升級為可存取裝置的資源 (硬體加速) 。

若要呈現從資源轉譯的影像，應用程式也需要色彩和深度樣板的緩衝區。 針對一般的應用程式，顏色緩衝區是由裝置的交換鏈所擁有，也就是後置緩衝區介面的集合，且會使用裝置隱含建立。 您可以使用 [**IDirect3DDevice9：： CreateDepthStencilSurface**](/windows/desktop/api) 方法，以隱含方式建立或明確建立深度樣板表面。 應用程式會透過呼叫 [**IDirect3DDevice9：： SetRenderTarget**](/windows/desktop/api) 或 [**IDirect3DDevice9：： SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface)，將裝置及其深度和色彩緩衝區相關聯。

如需呈現最終影像的詳細資訊，請參閱 [ (Direct3D 9 呈現場景) ](presenting-a-scene.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 資源](direct3d-resources.md)
</dt> </dl>

 

 
