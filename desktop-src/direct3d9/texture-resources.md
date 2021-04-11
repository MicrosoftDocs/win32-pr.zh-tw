---
description: 材質資源會在 IDirect3DTexture9 介面中執行。 若要取得紋理介面的指標，請呼叫 IDirect3DDevice9：： CreateTexture 方法或下列任何 D3DX 函數。
ms.assetid: vs|directx_sdk|~\texture_resources.htm
title: " (Direct3D 9) 的材質資源"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14134ca53b7735426e3f01340308282858da5516
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187544"
---
# <a name="texture-resources-direct3d-9"></a> (Direct3D 9) 的材質資源

材質資源會在 [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) 介面中執行。 若要取得紋理介面的指標，請呼叫 [**IDirect3DDevice9：： CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) 方法或下列任何 D3DX 函數。

-   [**D3DXCreateTexture**](d3dxcreatetexture.md)
-   [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md)
-   [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md)
-   [**D3DXCreateTextureFromFileInMemory**](d3dxcreatetexturefromfileinmemory.md)
-   [**D3DXCreateTextureFromFileInMemoryEx**](d3dxcreatetexturefromfileinmemoryex.md)
-   [**D3DXCreateTextureFromResource**](d3dxcreatetexturefromresource.md)
-   [**D3DXCreateTextureFromResourceEx**](d3dxcreatetexturefromresourceex.md)

下列程式碼範例會使用 [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) 從 Tiger.bmp 載入材質。


```
// The following code example assumes that D3dDevice
// is a valid pointer to an IDirect3DDevice9 interface.

LPDIRECT3DTEXTURE9 pTexture;

D3DXCreateTextureFromFile( d3dDevice, "tiger.bmp", &pTexture);
```



[**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md)所接受的第一個參數是 [**IDirect3DDevice9**](/windows/desktop/api)介面的指標。 第二個參數會告訴 Direct3D 要從中載入材質的檔案名。 第三個參數會接受 [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) 介面指標的位址，表示所建立的材質物件。

## <a name="rendering-with-texture-resources"></a>以材質資源呈現

Direct3D 透過紋理階段的概念支援多重紋理混合。 每個紋理階段都包含了一個紋理及可以執行於該紋理之上的運算。 紋理階段中的紋理構成了現有紋理的組合。 如需詳細資訊，請參閱 [ (Direct3D 9) 的材質混色 ](texture-blending.md)。 每個紋理的狀態都封裝於其紋理階段中。

在 c + + 應用程式中，每個材質的狀態都必須使用 [**IDirect3DDevice9：： SetTextureStageState**](/windows/desktop/api) 方法來設定。 將階段號碼 (0-7) 傳遞為第一個參數的值。 將第二個參數的值設定為 [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) 列舉型別的成員。 最後一個參數是特定材質狀態的狀態值。

使用紋理介面指標時，您的應用程式可以轉譯最多8個材質的 blend。 藉由叫用 [**IDirect3DDevice9：： SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 方法來設定目前的材質。 Direct3D 會將所有目前的材質混合到它所呈現的基本專案。

> [!Note]  
> [**IDirect3DDevice9：： SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)方法會遞增所指派之材質介面的參考計數。 當不再需要材質時，您應該將適當階段的材質設定為 **Null**。 如果您無法這樣做，將不會釋放介面，導致記憶體流失。

 

您的應用程式可以藉由呼叫 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法，來設定目前材質的材質換行狀態。 從 D3DRS \_ WRAP0 到 D3DRS WRAP7 傳遞值 \_ 做為第一個參數的值，並使用 D3DWRAPCOORD \_ 0、D3DWRAPCOORD \_ 1、D3DWRAPCOORD \_ 2 和 D3DWRAPCOORD 3 旗標的組合， \_ 以啟用 u、v 或 w 方向的換行。

您的應用程式也可以設定紋理透視及紋理篩選狀態。 請參閱 [ (Direct3D 9) 的材質篩選 ](texture-filtering.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 紋理](direct3d-textures.md)
</dt> </dl>

 

 
