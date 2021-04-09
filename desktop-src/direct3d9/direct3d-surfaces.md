---
description: 介面代表顯示記憶體的線性區域，而且通常位於顯示配接器的顯示記憶體中，雖然表面可以存在於系統記憶體中。 介面是由 IDirect3DSurface9 介面所管理。
ms.assetid: 17add726-3d95-46bc-8e15-3be0e570c49c
title: 'Direct3d (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08729cc7252c39ddf71048991a796469f2e8b0b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687376"
---
# <a name="direct3d-surfaces-direct3d-9"></a>Direct3d (Direct3D 9) 

介面代表顯示記憶體的線性區域，而且通常位於顯示配接器的顯示記憶體中，雖然表面可以存在於系統記憶體中。 介面是由 [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) 介面所管理。

-   前端緩衝區。 由圖形介面卡轉譯並顯示在監視器上的記憶體矩形。 在 Direct3D 中，應用程式永遠不會直接寫入至前端緩衝區。
-   背景緩衝區。 應用程式可直接寫入的記憶體矩形。 背景緩衝區永遠不會直接顯示在監視器上。
-   翻轉表面。 將背景緩衝區移至前端緩衝區的進程。
-   交換鏈。 一或多個後置緩衝區的集合，可連續呈現給前端緩衝區。

## <a name="getting-a-surface"></a>取得介面

藉由呼叫下列其中一種方法來建立介面：

-   [**CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)
-   [**CreateOffscreenPlainSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)
-   [**CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)

介面格式決定如何解讀介面記憶體中每個圖元的資料。 Direct3D 會使用 [**D3DSURFACE \_ DESC**](d3dsurface-desc.md)結構的 [D3DFORMAT](d3dformat.md)成員來描述介面格式。 您可以藉由呼叫 [**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc) 方法來取出現有介面的格式。

建立介面之後，您可以藉由呼叫下列其中一種方法來取得其指標：

-   [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface)
-   [**GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
-   [**GetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdepthstencilsurface)
-   [**GetFrontBufferData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getfrontbufferdata)
-   [**GetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrendertarget)
-   [**GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
-   [**GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel)

[**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)介面可讓您透過 [**UpdateSurface**](/windows/desktop/api)方法間接存取記憶體。 這個方法可讓您從一個 **IDirect3DSurface9** 介面，將一個圖元的矩形區域複製到另一個 **IDirect3DSurface9** 介面。 介面介面也有可直接存取顯示記憶體的方法。 例如，您可以使用 [**LockRect**](/windows/desktop/api) 方法來鎖定顯示記憶體的矩形區域。 在表面上使用鎖定的矩形區域完成之後，請務必呼叫 [**UnlockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-unlockrect) 。

## <a name="additional-surface-topics"></a>其他表面主題

深入瞭解如何搭配下列任何主題使用介面：

-   [ (Direct3D 9) 的表面格式 ](surface-formats.md)
-   [什麼是交換鏈？ (Direct3D 9) ](what-is-a-swap-chain-.md)
-   [寬度與音調 (Direct3D 9) ](width-vs--pitch.md)
-   [ (Direct3D 9 中翻轉表面) ](flipping-surfaces.md)
-   [ (Direct3D 9 的頁面翻轉和後臺緩衝) ](page-flipping-and-back-buffering.md)
-   [複製到 (Direct3D 9) 的表面 ](copying-to-surfaces.md)
-   [ (Direct3D 9) 複製表面 ](copying-surfaces.md)
-   [直接存取 (Direct3D 9) 的介面記憶體 ](accessing-surface-memory-directly.md)
-   [私用介面資料 (Direct3D 9) ](private-surface-data.md)
-   [ (Direct3D 9) 的 Gamma 控制項 ](gamma-controls.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[快速入門](getting-started.md)
</dt> </dl>

 

 
